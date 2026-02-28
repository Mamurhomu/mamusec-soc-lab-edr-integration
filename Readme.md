\# Enterprise EDR Deployment \& Detection Validation – CrowdStrike Falcon



\## Overview



This project documents my hands-on deployment and validation of CrowdStrike Falcon EDR within a hybrid SOC lab environment.



The objective was to:



\- Deploy Falcon sensors on Windows endpoints

\- Apply custom security policies

\- Generate and validate execution-based detections

\- Review MITRE ATT\&CK mappings

\- Analyze detection telemetry from a SOC perspective



---



\## Lab Environment



\- Windows 11 Endpoint (WIN11-1)

\- Active Directory (Lab Domain)

\- Ubuntu Server (SOC tooling)

\- CrowdStrike Falcon Insight (Trial)

\- SIEM: Splunk / Wazuh (separate project)



---



\## What Was Validated



\- Sensor installation \& communication

\- Policy enforcement

\- Execution detection telemetry

\- Process lineage review

\- MITRE ATT\&CK tactic mapping



---



\## Sample Detection Observed



\- Process: powershell.exe

\- User: it.admin

\- Host: WIN11-1

\- Tactic: Execution

\- Severity: Informational

\- Source: Falcon Insight


### Detailed Detection Analysis
The EICAR test file triggered a mapped execution technique (T1204).
Detection telemetry included process path, hash, and file write activity.



This confirms endpoint telemetry visibility and EDR functionality.



---



\## Key SOC Learning



\- Execution events alone are not malicious

\- Context (command-line, parent process, frequency) determines severity

\- Proper triage workflow includes validating:

\- User legitimacy

\- Process lineage

\- Time of execution

\- Host history



