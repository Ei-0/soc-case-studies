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
