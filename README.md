# 🔵 Incident Intelligence Report — RDP Brute Force Campaign (IR-2026-001)

**Classification:** TLP:GREEN — For Security Operations Use  
**Date:** June 25, 2026  
**Author:** Roshanak Khodaparast, Security Engineer  
**Disposition:** ✅ True Positive — Contained, No Compromise  

---

## Summary

A sustained brute force campaign targeted internet-exposed RDP endpoints (port 3389) 
on Azure virtual machines. Detected via Microsoft Sentinel scheduled analytics rule 
querying DeviceLogonEvents. Six distinct source IPs generated 10+ failed logon attempts 
each against 2 production VMs over a 5-hour window. Zero successful authentications confirmed.

---

## Key Details

| Field | Value |
|---|---|
| Attack Type | Brute Force — Password Spraying (T1110.003) |
| Target | Azure VMs — Microsoft Defender for Endpoint |
| Detection Tool | Microsoft Sentinel — Scheduled Analytics Rule |
| Source IPs | 6 distinct IPs |
| Timeframe | 5-hour active campaign window |
| Outcome | No compromise — NSG hardened |

---

## MITRE ATT&CK Mapping

| Tactic | Technique | ID |
|---|---|---|
| Credential Access | Password Spraying | T1110.003 |
| Lateral Movement (if successful) | Remote Desktop Protocol | T1021.001 |
| Impact (if successful) | Data Encrypted for Impact | T1486 |

---

## Tools & Technologies
`Microsoft Sentinel` `Microsoft Defender for Endpoint` `KQL` `Azure NSG` `MITRE ATT&CK`

---

📄 Full report: [IR-2026-001 PDF](./IR-2026-001_Brute_Force_Intelligence_Report.pdf)
