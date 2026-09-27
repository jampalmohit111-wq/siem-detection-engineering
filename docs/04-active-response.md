# 04: Active Response

## Purpose

This document describes the response process used after a security
alert is detected and investigated in the SIEM environment.

The response process focuses on validating the alert, containing
suspicious activity and documenting the actions taken.

## 1. Alert Validation

Before taking response action:

- Review the Wazuh alert.
- Verify the affected host.
- Identify the user and process involved.
- Review the available Sysmon and Windows event information.
- Determine whether the activity is expected or suspicious.

## 2. Investigation

The analyst reviews the available evidence to understand:

- What happened?
- When did it happen?
- Which account was involved?
- Which process generated the activity?
- What other events occurred around the same time?
- Which MITRE ATT&CK technique is relevant?

## 3. Containment

If suspicious activity is confirmed, appropriate containment actions
may include:

- Isolating the affected test machine.
- Disabling a compromised test account.
- Terminating a suspicious process.
- Blocking a malicious indicator in the lab environment.
- Preventing further communication with a suspicious destination.

Containment actions should be documented before and after execution.

## 4. Evidence Preservation

Relevant evidence should be preserved for further investigation.

Examples include:

- Wazuh alert details
- Sysmon events
- Windows event logs
- Process information
- Network information
- Screenshots
- Relevant timestamps

## 5. Recovery

After the investigation:

1. Remove the simulated malicious activity.
2. Restore the test environment if required.
3. Verify that the system is functioning normally.
4. Confirm that monitoring and detection remain operational.

## 6. Documentation

Record:

- Alert name
- Date and time
- Affected host
- User/account
- Detection rule
- Evidence collected
- Investigation findings
- Response actions
- Final outcome

## 7. Lessons Learned

Document improvements identified during the investigation.

Examples:

- Improve detection rules.
- Reduce false positives.
- Add additional telemetry.
- Improve alert enrichment.
- Improve investigation procedures.

## Result

The active-response workflow provides a structured approach for
moving from alert detection to investigation, containment, evidence
preservation and recovery in the controlled lab environment.
