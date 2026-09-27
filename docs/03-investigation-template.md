# 03: Investigation Template

## Purpose

This template provides a consistent structure for investigating
security alerts generated during the SIEM detection engineering lab.

## 1. Alert Information

- Alert name:
- Alert ID:
- Date and time:
- Severity:
- Detection rule:
- Affected host:

## 2. Event Details

- Source:
- User:
- Process:
- Parent process:
- Command line:
- Source IP:
- Destination IP:
- File or registry activity:

## 3. Detection

Describe what activity triggered the alert and why the detection
rule identified it as suspicious.

## 4. Evidence

Document the relevant Wazuh, Sysmon or Windows event information.

Screenshots and supporting evidence should be stored in the
`screenshots/` directory.

## 5. MITRE ATT&CK Mapping

- Tactic:
- Technique:
- Technique ID:

Explain why the observed activity maps to the selected MITRE ATT&CK
technique.

## 6. Investigation

Describe:

1. What happened?
2. Which account or process was involved?
3. What evidence supports the finding?
4. Was the activity expected or suspicious?
5. What additional investigation was performed?

## 7. Impact Assessment

Describe the potential security impact of the activity.

## 8. Response

Document the response or containment actions taken during the lab.

## 9. Conclusion

Summarize the investigation findings and whether the alert was
considered suspicious, benign or a false positive.

## 10. Lessons Learned

Document improvements that could be made to the detection,
investigation process or monitoring configuration.
