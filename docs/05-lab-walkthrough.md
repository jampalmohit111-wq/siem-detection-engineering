# 05: SIEM Lab Walkthrough

## Overview

This walkthrough documents the end-to-end SIEM detection engineering
lab using Wazuh, Windows, Sysmon, Sigma and MITRE ATT&CK.

The objective is to generate security telemetry, detect suspicious
activity, investigate the resulting alerts and document the findings.

## 1. Lab Environment

The lab consists of:

- Wazuh manager
- Windows test machine
- Sysmon
- Wazuh agent
- Windows event telemetry
- Sigma detection rules
- MITRE ATT&CK technique mapping

All testing is performed in a controlled virtual lab environment.

## 2. Configure the SIEM

The Wazuh manager is configured to receive security telemetry from
the Windows test machine.

The Wazuh dashboard is used to review alerts, search events and
investigate suspicious activity.

## 3. Configure Windows Telemetry

Sysmon is configured on the Windows test machine to provide detailed
process, network, registry and other system telemetry.

The Wazuh agent forwards relevant events to the Wazuh manager.

## 4. Generate Test Activity

Controlled security-related activities are performed on the test
machine to generate telemetry.

Examples include:

- PowerShell activity
- New process execution
- Account or privilege-related activity
- Suspicious command execution
- Network-related activity

The activities are performed only inside the isolated lab environment.

## 5. Detect the Activity

Wazuh processes the incoming telemetry and evaluates the configured
detection rules.

When matching activity is identified, an alert is generated.

The alert is reviewed for:

- Timestamp
- Host
- User
- Process
- Command line
- Source information
- Detection rule
- Severity

## 6. Investigate the Alert

The generated alert is investigated using Wazuh and the available
Windows/Sysmon telemetry.

The investigation follows the structure documented in
`03-investigation-template.md`.

Relevant evidence is collected and mapped to the appropriate
MITRE ATT&CK technique.

## 7. Response

If the activity is considered suspicious, the response process
documented in `04-active-response.md` is followed.

Possible actions include containment, evidence preservation and
recovery of the test environment.

## 8. Document the Findings

Investigation results are documented with:

- Alert information
- Evidence
- Investigation timeline
- MITRE ATT&CK mapping
- Response actions
- Final conclusion
- Lessons learned

Screenshots can be stored in the appropriate evidence directory.

## 9. Skills Demonstrated

This lab demonstrates practical experience with:

- SIEM monitoring
- Wazuh
- Windows security monitoring
- Sysmon
- Detection engineering
- Alert investigation
- Sigma
- MITRE ATT&CK
- Incident response
- Security documentation

## Conclusion

The lab demonstrates an end-to-end detection engineering workflow:
collecting telemetry, generating alerts, investigating security events,
mapping activity to MITRE ATT&CK and documenting the response.
