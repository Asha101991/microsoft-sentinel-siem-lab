# Incident Report

## Incident Title

Suspicious PowerShell Execution

## Severity

High

## Summary

A PowerShell command containing suspicious indicators was detected on a monitored endpoint.

## Evidence

- Process: powershell.exe
- Suspicious arguments: EncodedCommand, DownloadString, bypass
- Data source: Microsoft Defender for Endpoint

## MITRE ATT&CK

- T1059.001 - PowerShell

## Response Actions

- Reviewed process command line
- Checked parent process
- Investigated user activity
- Recommended endpoint isolation if malicious behavior is confirmed

## Lessons Learned

Enable PowerShell logging and monitor suspicious command-line arguments.
