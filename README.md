# Microsoft Sentinel SIEM Lab — TechPay Solutions

## Project Overview
This project simulates the setup and configuration of Microsoft 
Sentinel as a SIEM solution for a fictional fintech company — 
TechPay Solutions S.L. It covers data connector setup, KQL 
detection rule creation, and incident investigation workflow.

## What This Project Covers
- Microsoft Sentinel workspace deployment on Azure
- Data connector configuration (Entra ID, Azure Activity, 
  Microsoft Defender XDR)
- 4 custom KQL detection rules mapped to MITRE ATT&CK framework
- Incident creation and SOC investigation workflow
- Real-world fintech threat scenarios

## Detection Rules
| Rule | Tactic | Severity | File |
|---|---|---|---|
| Multiple Failed Logins | Credential Access | High | brute-force-detection.kql |
| Unusual Country Login | Initial Access | Medium | unusual-country-login.kql |
| After Hours Login | Initial Access | Medium | after-hours-login.kql |
| Privileged Role Assignment | Privilege Escalation | High | privilege-escalation.kql |

## MITRE ATT&CK Framework
All detection rules are mapped to the MITRE ATT&CK framework:
- **T1110** — Brute Force (Credential Access)
- **T1078** — Valid Accounts (Initial Access)
- **T1078.004** — Cloud Accounts (Privilege Escalation)

## Tools & Technologies
- Microsoft Sentinel (SIEM)
- Microsoft Defender Portal
- Azure Log Analytics Workspace
- KQL (Kusto Query Language)
- Microsoft Entra ID
- Azure Activity Logs

## Architecture
See [sentinel-architecture.md](docs/sentinel-architecture.md) 
for the full architecture diagram.

## Related Projects
- [TechPay GDPR ROPA](https://github.com/Andrea1864/gdpr-ropa-fintech)
- [MedCore GDPR ROPA](https://github.com/Andrea1864/gdpr-ropa-healthcare)

## Author
Andrea Castillo — Law Graduate | Cybersecurity & GRC Specialist  
