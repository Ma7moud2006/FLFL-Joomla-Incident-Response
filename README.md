# FLFL — SOC Incident Response: Joomla Web Server Compromise

A hands-on incident response investigation based on the Splunk BOTS v1 simulated enterprise dataset.

## Overview

This project investigates the compromise and defacement of a simulated Joomla web server.

The investigation reconstructs the attack chain using multiple security telemetry sources and analyzes attacker infrastructure, execution activity, command-and-control communication, and indicators of compromise.

## Attack Chain

```text
Reconnaissance
      ↓
Brute Force
      ↓
Credential Reuse
      ↓
Web Shell Upload
      ↓
Command Execution
      ↓
C2 Communication
      ↓
Website Defacement
```

## Investigation Areas

- HTTP traffic analysis
- Suricata alert analysis
- Joomla brute-force investigation
- Credential reuse detection
- Web shell investigation
- Sysmon process analysis
- C2 identification
- IOC extraction
- MITRE ATT&CK mapping
- SOC detection opportunities
- Security recommendations

## Key Findings

- A simulated Joomla web server compromise was identified.
- Web shell activity was observed during the investigation.
- Suspicious process execution was analyzed using Sysmon telemetry.
- Command-and-control communication was identified through network telemetry.
- Indicators of compromise were extracted and correlated across multiple data sources.

## Tools & Technologies

- Splunk
- Suricata
- Sysmon
- FortiGate
- MITRE ATT&CK

## Data Sources

- `stream:http`
- `suricata`
- `fortigate_utm`
- `xmlwineventlog`

## Environment

**Scenario:** Splunk BOTS v1 simulated enterprise dataset  
**Affected Asset:** Joomla web server — `192.168.250.70`  
**IR Phase:** Detection and Analysis

> This is a simulated lab investigation based on the Splunk BOTS v1 dataset and is not a real-world incident.

## Evidence

Investigation screenshots and supporting evidence are available in the [`screenshots`](screenshots/) directory.

Selected evidence includes:

- Website defacement
- Suricata detection of Acunetix activity
- Web shell process activity
- Command-and-control traffic

## Report

📄 [View the Full Incident Response Report](./report/FLFL_Incident_Response_Report.pdf)

## Author

**Mahmoud Hassan Mahmoud**  
SOC Analyst / Cybersecurity

---

**FLFL | SOC Portfolio Project**
