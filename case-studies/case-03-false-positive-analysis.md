# Suspicious Activity Determined as False Positive

## Environment
A corporate environment with centralized logging and security
monitoring. Multiple automated alerts are generated daily based on
behavioral thresholds and rule-based detections.

The organization includes technical and non-technical users, with some
legitimate activities occasionally triggering security alerts due to
their similarity to malicious behavior.

## Initial Signal

A security alert was generated indicating suspicious PowerShell
execution associated with a user workstation. The alert was categorized
as high severity due to the involvement of command-line activity and
potential scripting behavior.

At the time of detection, no additional indicators such as data
exfiltration, privilege escalation, or lateral movement were observed.
The alert required analyst review to determine whether the activity
represented malicious behavior or a false positive.

## Timeline & Context Gathering

- **09:12 AM** — PowerShell execution was detected on a user workstation
during standard business hours. The activity originated from the user's
assigned device within the corporate network.

- **09:13 AM** — The executed command was correlated with a legitimate
internal automation script used to perform system inventory checks.
The script was signed and had been previously observed within the
environment.

- **09:15 AM** — No additional suspicious behavior was detected following
the execution. There was no evidence of external network connections,
unauthorized file access, or privilege escalation.

Further context revealed that the user belonged to a technical support
team that routinely performed troubleshooting and system validation
tasks as part of their role.

