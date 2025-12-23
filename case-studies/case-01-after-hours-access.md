# After-Hours Access to Financial Data

## Environment
A medium-sized organization with approximately 300 employees.
The environment includes an internal file server hosting financial
documents. Business hours are from 8:00 AM to 5:00 PM.
Non-IT users do not normally use PowerShell as part of their daily work.

## Initial Signal
The investigation began after a successful login was observed outside
of normal business hours. The login involved a finance department user
accessing the system at approximately 2:17 AM from an internal workstation.

At this stage, the activity was treated as an event rather than a
confirmed incident, as no malicious behavior had yet been observed.

## Timeline

- **02:17 AM** — A successful login occurred for a finance department user
outside normal business hours. While unusual, no immediate malicious
activity was observed at this point.

- **02:19 AM** — PowerShell execution was detected on the user's workstation.
This represented a clear deviation from the established baseline, as
non-IT users do not typically use PowerShell in this environment.

- **02:20 AM** — Access to sensitive financial directories on the internal
file server was observed shortly after the PowerShell execution. The
sequence of events suggested a transition from access to potential
intent-driven activity.

## Analysis

The initial after-hours login alone was not sufficient to confirm
malicious intent, as legitimate explanations such as overtime work or
remote access could not be ruled out.

However, the subsequent execution of PowerShell by a non-IT user
represented a significant deviation from normal behavior. In this
environment, finance users do not typically require command-line tools
to perform their duties.

The rapid sequence from PowerShell execution to access of sensitive
financial directories further increased concern. This progression
suggested intentional activity rather than accidental or routine user
behavior.

At this stage, the situation was assessed as a high-risk anomaly
requiring close monitoring, but not yet immediate containment, in order
to better understand the user’s intent and avoid disrupting legitimate
business activity prematurely.

## Decision

Based on the available evidence at this stage, the decision was made to
continue monitoring the activity rather than immediately containing the
user or isolating the workstation.

This decision was driven by the absence of confirmed data exfiltration,
privilege escalation, or destructive behavior. Immediate containment
could have prematurely disrupted legitimate business activity or
alerted a potential threat actor before sufficient context was
gathered.

Additional logging and monitoring were prioritized to capture further
activity and enable a more confident response if the behavior
escalated.

## Outcome

Following continued monitoring, no evidence of data exfiltration,
privilege escalation, or malicious persistence was observed. The
activity was ultimately assessed as non-malicious but anomalous user
behavior.

The case was documented to improve future detection and reduce
uncertainty around similar events.

## Recommendations

- Improve baseline documentation for after-hours access by non-IT
users.
- Implement alerting for PowerShell usage by finance department users.
- Reinforce the principle of least privilege and review access needs
periodically.
