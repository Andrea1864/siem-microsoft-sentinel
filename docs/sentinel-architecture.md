# Microsoft Sentinel Architecture — TechPay Lab

## Architecture Overview

Microsoft Entra ID ──┐
Azure Activity ───────┼──→ Log Analytics Workspace ──→ Microsoft Sentinel
Microsoft Defender ──┘ (law-sentinel-techpay) │
│
┌─────────┴─────────┐
│ Detection Rules │
│ KQL Analytics │
└─────────┬─────────┘
│
┌─────────┴─────────┐
│ Incidents │
│ SOC Investigation │
└───────────────────┘


## Components

### Log Analytics Workspace
- **Name**: law-sentinel-techpay
- **Region**: France Central
- **Retention**: 30 days (trial)

### Data Connectors
| Connector | Data Type | Purpose |
|---|---|---|
| Microsoft Entra ID | SigninLogs, AuditLogs | Identity monitoring |
| Azure Activity | AzureActivity | Infrastructure monitoring |
| Microsoft Defender XDR | SecurityAlert | Threat detection |

### Detection Rules
| Rule | Query Frequency | Lookback | Severity |
|---|---|---|---|
| Brute Force Detection | 5 min | 10 min | High |
| Unusual Country Login | 1 hour | 1 hour | Medium |
| After Hours Login | 1 hour | 1 hour | Medium |
| Privilege Escalation | 30 min | 30 min | High |

## MITRE ATT&CK Coverage
| Tactic | Technique | Rule |
|---|---|---|
| Credential Access | T1110 Brute Force | brute-force-detection.kql |
| Initial Access | T1078 Valid Accounts | unusual-country-login.kql |
| Initial Access | T1078 Valid Accounts | after-hours-login.kql |
| Privilege Escalation | T1078.004 Cloud Accounts | privilege-escalation.kql |
