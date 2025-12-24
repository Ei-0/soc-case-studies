# Potential Insider Data Access Investigation

## Environment
A technology organization with an internal IT team and multiple
departmental file shares. Several systems contain sensitive financial
and human resources data. IT administrators have broad access across
systems as part of their operational responsibilities.

User activity is logged centrally, including file access events and
device-level actions. No active alerts were triggered at the start of
this investigation.

## Initial Signal
The investigation began following an internal notification that
sensitive financial documents had appeared outside of their expected
storage location. No security alerts or automated detections had been
triggered at the time.

Due to the nature of the report, the investigation was approached from
a post-incident (DFIR) perspective, focusing on determining how the
data was accessed, by whom, and through which mechanism.

## Reverse Timeline

The investigation began by identifying the last known point at which
the sensitive documents were confirmed to be stored within the internal
environment. From this point, access records were reviewed in reverse
chronological order to determine when and how the data may have been
copied or moved.

Analysis revealed repeated access to multiple sensitive files over a
period of several days by a single IT administrator account. The files
were accessed without modification, suggesting review or collection
rather than legitimate operational changes.

Subsequent activity showed that copies of the accessed data were staged
within an internal shared directory, a location not typically used for
official data processing or archival purposes.

## Analysis

The observed activity did not align with typical administrative tasks.
While IT administrators have broad access, the pattern of repeated
access across multiple sensitive financial and HR files lacked a clear
operational justification.

The access behavior was characterized by:
- Repeated file access without modification
- Targeting of multiple sensitive departments
- Gradual accumulation of data over several days
- Staging of files in a non-standard internal directory

This pattern suggested intentional data collection rather than
accidental access or routine troubleshooting. The absence of immediate
external data transfer indicated a cautious approach, potentially
aimed at avoiding detection before removal of the data.

At this stage, the activity was assessed as a high-risk insider threat
scenario requiring careful escalation rather than direct confrontation.

## Decision & Escalation

Given the absence of an immediate external data transfer but the clear
pattern of intentional data collection, the decision was made not to
confront the user directly or disrupt access prematurely.

The case was escalated through appropriate internal channels, including
incident response leadership and management, to ensure proper handling
with legal and human resources considerations in mind.

Preservation of evidence was prioritized, including access logs,
file activity records, and device usage data, to support further
investigation and potential formal proceedings.

## Outcome

The investigation established a consistent pattern of non-routine
access to sensitive data by a privileged internal account. While no
confirmed external exfiltration was observed during the review period,
the activity met the threshold for a confirmed insider risk case.

The findings were formally documented and transferred to the
appropriate internal stakeholders for further action.

## Recommendations

- Implement stricter monitoring of privileged user access to sensitive
data.
- Establish clearer documentation for approved administrative access
activities.
- Enable alerting for large-scale internal data staging behaviors.
- Conduct periodic reviews of privileged account usage patterns.
