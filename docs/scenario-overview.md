# Scenario Overview — TechPay Solutions SOC Lab

## Company Profile
- **Name**: TechPay Solutions S.L.
- **Sector**: Financial Technology (Fintech)
- **Employees**: 50
- **Location**: Barcelona, Spain
- **Services**: Digital payment processing, peer-to-peer 
  transfers, virtual card issuing

## SOC Context
TechPay operates a Security Operations Centre (SOC) using 
Microsoft Sentinel as its primary SIEM solution. The SOC 
monitors all Microsoft 365 and Azure activity for threats.

## Threat Landscape
As a fintech company, TechPay faces these primary threats:
- Account takeover via credential stuffing or brute force
- Insider threats from privileged users
- Data exfiltration of payment and customer data
- Unauthorized access outside business hours
- Login attempts from unusual geographic locations

## Detection Rules Implemented
| Rule | Tactic | Severity |
|---|---|---|
| Multiple Failed Logins | Credential Access | High |
| Unusual Country Login | Initial Access | Medium |
| After Hours Login | Initial Access | Medium |
| Privileged Role Assignment | Privilege Escalation | High |
