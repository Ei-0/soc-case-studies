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

