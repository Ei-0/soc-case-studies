## Incident Overview
The SOC team received multiple SIEM alerts indicating suspicious external activity targeting a corporate endpoint.

## Alert Source
- SIEM correlation rule
- Windows Security Logs
- Network traffic logs

## Suspicious Indicators
- Multiple failed login attempts
- Successful login from external IP
- Unusual PowerShell execution shortly after login

## Alert Details
- Alert Type: Brute Force / Suspicious Login
- Severity: High
- Source IP: External (Non-corporate)
- Target: Employee workstation

## Reason for Alert
Multiple failed authentication attempts followed by a successful login from the same external IP.

## Investigation Steps

1. Reviewed authentication logs for failed and successful logins
2. Analyzed source IP reputation
3. Checked login time vs normal user behavior
4. Investigated post-login activity
5. Reviewed PowerShell execution logs

| Time | Event |
|------|------|
| 02:11 | Multiple failed login attempts detected |
| 02:14 | Successful login from same IP |
| 02:16 | PowerShell executed |
| 02:18 | File system enumeration |
| 02:25 | SOC analyst escalated incident |

## Log Analysis

### Authentication
- Event ID 4625 (Failed Logon)
- Event ID 4624 (Successful Logon)
- Login occurred outside normal working hours

### PowerShell
- Encoded command detected
- Suspicious execution flags used

### Network
- Source IP flagged in threat intelligence feed

- T1110 – Brute Force
- T1078 – Valid Accounts
- T1059.001 – PowerShell
- T1083 – File and Directory Discovery

## Key Findings
- External attacker successfully authenticated
- Credentials likely compromised
- PowerShell used for initial reconnaissance
- No evidence of lateral movement

## Response Actions
- Disabled affected user account
- Forced password reset
- Blocked malicious IP at firewall
- Collected endpoint logs for DFIR

## Lessons Learned
- MFA was not enforced on the affected account
- Brute force detection threshold needs tuning
- PowerShell logging should be enhanced

## Conclusion
This incident was confirmed as a successful external attack using compromised credentials.
Early detection limited the attack to initial access with no further impact.
