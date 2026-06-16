# Azure Architecture

## Components

- Azure Resource Group
- Log Analytics Workspace
- Microsoft Sentinel
- Windows Virtual Machine
- Microsoft Defender for Endpoint
- Microsoft Entra ID
- Logic Apps

## Data Flow

1. Endpoint generates security telemetry.
2. Logs are sent to Log Analytics Workspace.
3. Microsoft Sentinel analyzes the logs.
4. Analytics rules generate incidents.
5. SOC analyst investigates alerts.
6. Playbooks automate response actions.
