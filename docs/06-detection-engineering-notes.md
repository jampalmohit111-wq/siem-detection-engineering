# 06: Detection Engineering Notes

## Overview

Detection engineering is the process of creating, testing and
improving security detections so that suspicious activity can be
identified reliably.

This project uses Wazuh, Sysmon, Sigma and MITRE ATT&CK to develop
and validate detections in a controlled lab environment.

## 1. Detection Development Process

The detection workflow used in this lab is:

1. Identify a security behaviour to detect.
2. Map the behaviour to MITRE ATT&CK.
3. Identify the telemetry required for detection.
4. Create or configure the detection rule.
5. Generate controlled test activity.
6. Review the resulting SIEM alert.
7. Investigate the alert and supporting evidence.
8. Tune the detection if necessary.
9. Document the final detection.

## 2. Telemetry Sources

The main telemetry sources include:

- Windows Event Logs
- Sysmon
- Wazuh agent telemetry
- Wazuh manager alerts

Sysmon provides additional visibility into process creation,
network activity, registry activity and other endpoint events.

## 3. Detection Technologies

### Wazuh

Wazuh is used as the SIEM and security monitoring platform for
collecting, processing and alerting on endpoint telemetry.

### Sysmon

Sysmon provides detailed Windows endpoint telemetry that can be
used to investigate process, network and system activity.

### Sigma

Sigma rules provide a structured and portable format for describing
security detections.

### MITRE ATT&CK

MITRE ATT&CK is used to map detected behaviours to adversary tactics
and techniques.

## 4. Detection Validation

Each detection should be tested using controlled activity.

Validation should confirm:

- The expected telemetry is generated.
- The detection rule matches the relevant event.
- The SIEM generates the expected alert.
- The alert contains useful investigation information.
- Unrelated activity does not unnecessarily trigger the detection.

## 5. False Positive Reduction

Detection rules should be reviewed for unnecessary alerts.

Possible improvements include:

- Filtering known legitimate processes.
- Restricting detections to relevant users or hosts.
- Adding appropriate event conditions.
- Increasing the required confidence before generating an alert.
- Documenting known legitimate activity.

## 6. Detection Documentation

For each detection, document:

- Detection name
- Description
- Data source
- Detection logic
- MITRE ATT&CK technique
- Test activity
- Expected result
- Observed result
- Investigation evidence
- False-positive considerations

## 7. Example Detection Workflow

Example:

```text
Windows activity
       ↓
     Sysmon
       ↓
   Wazuh Agent
       ↓
  Wazuh Manager
       ↓
 Detection Rule
       ↓
     Alert
       ↓
 Investigation
       ↓
MITRE ATT&CK Mapping
       ↓
 Response / Documentation
