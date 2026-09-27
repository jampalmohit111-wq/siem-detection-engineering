# siem-detection-engineering
Hands-on SIEM detection engineering lab using Wazuh, Sysmon, Sigma and MITRE ATT&amp;CK.
# SIEM Detection Engineering Lab

## Overview

This project demonstrates a hands-on Security Operations Center (SOC)
detection engineering lab using Wazuh, Sysmon, Sigma and MITRE ATT&CK.

The lab focuses on collecting Windows endpoint telemetry, detecting
suspicious activity, generating security alerts, investigating incidents,
and mapping detections to MITRE ATT&CK techniques.

## Objectives

- Collect Windows security telemetry using Sysmon
- Forward endpoint logs to Wazuh
- Create and test detection rules
- Detect suspicious Windows activity
- Investigate generated security alerts
- Map detections to MITRE ATT&CK
- Document investigation findings
- Develop practical SOC and detection engineering skills

## Technologies

- Wazuh
- Sysmon
- Windows
- Linux
- Sigma
- MITRE ATT&CK
- VMware

## Lab Architecture

Windows Endpoint
→ Sysmon
→ Wazuh Agent
→ Wazuh Manager
→ Detection Rules
→ Security Alert
→ Investigation
→ MITRE ATT&CK Mapping

## Detection Scenarios

The lab includes multiple security detection scenarios involving
Windows endpoint activity.

Examples include:

- PowerShell activity
- Brute-force authentication attempts
- Suspicious process execution
- Persistence activity
- Suspicious administrative activity

## Investigation Process

For each detection, the investigation follows a structured process:

1. Generate or identify the security event
2. Collect endpoint telemetry
3. Review the Wazuh alert
4. Analyse the relevant event details
5. Identify the associated MITRE ATT&CK technique
6. Determine the security impact
7. Document the investigation
8. Record the detection and evidence

## MITRE ATT&CK

Detections are mapped to relevant MITRE ATT&CK techniques to provide
context for attacker behaviour and detection coverage.

## Evidence

Screenshots and investigation evidence are included in the project
documentation.

## Project Status

Completed lab with documented detection scenarios and investigations.
