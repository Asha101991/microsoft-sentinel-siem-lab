# Microsoft Sentinel Configuration

## Data Connectors

Recommended connectors:

- Windows Security Events via AMA
- Microsoft Defender for Endpoint
- Microsoft Entra ID
- Azure Activity
- Microsoft 365 Defender

## Analytics Rules

Create scheduled analytics rules for:

- Brute force authentication attempts
- Suspicious PowerShell activity
- Impossible travel
- Ransomware-like file activity
- Privilege escalation

## Incident Management

Each incident should include:

- Alert name
- Severity
- Entities involved
- MITRE ATT&CK technique
- Timeline
- Analyst notes
- Response actions
