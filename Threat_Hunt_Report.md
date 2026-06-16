# Threat Hunt Report

## Hunt Name

Brute Force Authentication Hunt

## Objective

Identify accounts with excessive failed logon attempts that may indicate password spraying or brute force attacks.

## Hypothesis

An attacker may attempt multiple failed logons against one or more accounts to gain unauthorized access.

## Data Sources

- Windows Security Events
- Microsoft Entra ID Sign-in Logs

## KQL Query

```kql
SecurityEvent
| where EventID == 4625
| summarize FailedAttempts=count() by Account, IpAddress, Computer, bin(TimeGenerated, 15m)
| where FailedAttempts >= 5
```

## Findings

Document findings here after running the query in Microsoft Sentinel.

## Recommendations

- Enable MFA
- Review risky sign-ins
- Block suspicious IP addresses
- Reset impacted user passwords
- Create analytics rule for repeated failed logons
