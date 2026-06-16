# Microsoft Sentinel SIEM Lab

A cloud-based Security Information and Event Management (SIEM) lab built with **Microsoft Sentinel**, **Azure Log Analytics**, **Microsoft Defender**, and **Kusto Query Language (KQL)**.

## Project Objectives

- Deploy Microsoft Sentinel in Azure
- Create a Log Analytics Workspace
- Connect Windows Security Events
- Ingest Microsoft Entra ID logs
- Write KQL threat hunting queries
- Build analytics rules
- Create incident response playbooks
- Map detections to MITRE ATT&CK
- Document SOC investigation workflows

## Tools & Technologies

- Microsoft Sentinel
- Microsoft Azure
- Log Analytics Workspace
- Azure Monitor
- Microsoft Defender for Endpoint
- Microsoft Entra ID
- Kusto Query Language (KQL)
- Logic Apps
- MITRE ATT&CK

## Repository Structure

```text
microsoft-sentinel-siem-lab/
├── README.md
├── LICENSE
├── .gitignore
├── docs/
├── kql-queries/
├── analytics-rules/
├── workbooks/
├── playbooks/
├── screenshots/
└── reports/
```

## Sample KQL Queries

### Failed Logons

```kql
SecurityEvent
| where EventID == 4625
| summarize FailedAttempts=count() by Account, Computer, IpAddress, bin(TimeGenerated, 15m)
| where FailedAttempts >= 5
```

### Successful Logons

```kql
SecurityEvent
| where EventID == 4624
| project TimeGenerated, Account, Computer, LogonType, IpAddress
```

### Suspicious PowerShell

```kql
DeviceProcessEvents
| where FileName =~ "powershell.exe"
| where ProcessCommandLine has_any ("-enc", "EncodedCommand", "DownloadString", "Invoke-WebRequest", "IEX")
| project TimeGenerated, DeviceName, AccountName, FileName, ProcessCommandLine
```

## MITRE ATT&CK Mapping

| Detection | Technique | ID |
|---|---|---|
| PowerShell Abuse | Command and Scripting Interpreter: PowerShell | T1059.001 |
| Brute Force Logons | Brute Force | T1110 |
| Valid Account Usage | Valid Accounts | T1078 |
| Credential Dumping | OS Credential Dumping | T1003 |
| Remote Services | Remote Services | T1021 |

## Skills Demonstrated

- SIEM Administration
- Cloud Security Monitoring
- KQL Query Writing
- Threat Hunting
- Incident Response
- Detection Engineering
- Microsoft Sentinel Analytics Rules
- SOC Documentation
- MITRE ATT&CK Mapping
- SOAR Playbook Planning

## Screenshots

Add screenshots of:

- Microsoft Sentinel overview
- Log Analytics Workspace
- Analytics rules
- Incidents page
- Hunting queries
- Workbooks/dashboard

## Author

Ashaar Leacock-Thomas  
Cybersecurity Graduate Student | SOC Analyst Portfolio Project
