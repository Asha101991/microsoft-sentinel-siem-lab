# Lab Setup Guide

## Requirements

- Azure account
- Microsoft Sentinel access
- Log Analytics Workspace
- Windows VM or Windows endpoint
- Microsoft Defender for Endpoint trial or tenant access

## Steps

1. Create an Azure Resource Group.
2. Create a Log Analytics Workspace.
3. Enable Microsoft Sentinel on the workspace.
4. Connect data sources:
   - Windows Security Events
   - Microsoft Entra ID logs
   - Microsoft Defender incidents
5. Create hunting queries using KQL.
6. Create analytics rules from validated detections.
7. Document incidents and investigation findings.

## Notes

Use a lab subscription and avoid storing real credentials, secrets, or production data in this repository.
