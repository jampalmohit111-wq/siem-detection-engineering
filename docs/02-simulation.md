# 02: Security Event Simulation

## Purpose

The purpose of this stage was to generate controlled security events
on the Windows test environment and verify that Sysmon and Wazuh
captured the resulting activity.

The simulated activities were performed in an isolated lab environment
for detection and investigation purposes.

## Simulation Workflow

The general workflow was:

1. Perform a controlled activity on the Windows test machine.
2. Allow Sysmon to record the relevant endpoint telemetry.
3. Forward the telemetry through the Wazuh agent.
4. Review the resulting event in Wazuh.
5. Verify that the appropriate detection rule generated an alert.
6. Investigate the alert and collect supporting evidence.
7. Map the activity to MITRE ATT&CK.

## Simulation Scenarios

### 1. Suspicious PowerShell Activity

A controlled PowerShell activity was generated on the Windows test
machine to verify PowerShell-related telemetry and detection.

The investigation focused on:

- PowerShell process execution
- Command-line information
- Parent and child processes
- Sysmon event information
- Wazuh alert information
- MITRE ATT&CK mapping

**Evidence:** See the corresponding investigation and screenshots.

---

### 2. Local Administrator Account Activity

A controlled local account/administrator activity was performed to
test whether changes involving local accounts could be detected.

The investigation focused on:

- Account creation or modification
- Username involved
- Process responsible for the activity
- Windows/Sysmon event information
- Wazuh alert information
- MITRE ATT&CK mapping

**Evidence:** See the corresponding investigation and screenshots.

---

### 3. Credential Access Activity

A controlled credential-access scenario was used to test endpoint
visibility and detection of suspicious access to credential-related
processes.

The investigation focused on:

- Process involved
- Access activity
- Relevant Sysmon telemetry
- Wazuh alert information
- MITRE ATT&CK mapping
- Supporting evidence

**Evidence:** See the corresponding investigation and screenshots.

## Validation

After each simulation, the following checks were performed:

- Sysmon recorded the relevant activity.
- The Wazuh agent forwarded the telemetry.
- Wazuh processed the event.
- The appropriate detection generated an alert.
- The alert contained sufficient information for investigation.
- The activity could be mapped to a relevant MITRE ATT&CK technique.

## Evidence Collection

Evidence collected during the simulations included:

- Wazuh alerts
- Sysmon events
- Process information
- Command-line information
- Investigation screenshots
- MITRE ATT&CK mappings

Screenshots are stored in the `screenshots/` directory.

## Safety

All simulations were performed in a controlled test environment.
No production systems or third-party systems were targeted.

## Result

The simulations provided test events for validating the detection
rules and the subsequent investigation workflow.
