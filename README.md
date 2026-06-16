<div align="center">

```
██████╗ ██╗     ██╗   ██╗███████╗███████╗ ██████╗ ██████╗  ██████╗ ███████╗
██╔══██╗██║     ██║   ██║██╔════╝██╔════╝██╔═══██╗██╔══██╗██╔════╝ ██╔════╝
██████╔╝██║     ██║   ██║█████╗  █████╗  ██║   ██║██████╔╝██║  ███╗█████╗  
██╔══██╗██║     ██║   ██║██╔══╝  ██╔══╝  ██║   ██║██╔══██╗██║   ██║██╔══╝  
██████╔╝███████╗╚██████╔╝███████╗██║     ╚██████╔╝██║  ██║╚██████╔╝███████╗
╚═════╝ ╚══════╝ ╚═════╝ ╚══════╝╚═╝      ╚═════╝ ╚═╝  ╚═╝ ╚═════╝ ╚══════╝
```

### Blue Team Forge — SOC Runbooks · KQL Detections · MITRE ATT&CK · Network Security

[![Made by SOC Analyst](https://img.shields.io/badge/Made%20by-SOC%20Analyst-blue?style=flat-square)](https://github.com/BALAbm7/BlueForge)
[![KQL Queries](https://img.shields.io/badge/KQL%20Queries-50-5c4ee5?style=flat-square)](./03-kql-queries/)
[![Runbook Alerts](https://img.shields.io/badge/Runbook%20Alerts-50-e03131?style=flat-square)](./02-soc-runbooks/)
[![MITRE Tactics](https://img.shields.io/badge/MITRE%20Tactics-11-f08c00?style=flat-square)](./04-mitre-attack/)
[![Network Chapters](https://img.shields.io/badge/Network%20Chapters-15-2f9e44?style=flat-square)](./01-network-security/)
[![License](https://img.shields.io/badge/License-MIT-gray?style=flat-square)](./LICENSE)
[![Status](https://img.shields.io/badge/Status-Actively%20Maintained-brightgreen?style=flat-square)](#)

</div>

---

## What is BlueForge?

**BlueForge** is a structured, production-grade blue team knowledge base built from real SOC operations. Everything here comes from hands-on work — not textbooks. It covers the full analyst workflow: from understanding a network packet at the wire level, to detecting a Golden Ticket attack in Microsoft Sentinel, to responding to an active ransomware incident.

This repo serves two purposes simultaneously: a **daily reference** for working SOC analysts and a **career portfolio** demonstrating detection engineering, threat hunting, and incident response capabilities.

> Built by **Balamurugan A** — SOC Analyst with 2+ years in blue team operations across Microsoft Sentinel, SentinelOne, Cortex XDR, Zscaler, and Armis.

---

## Table of Contents

- [Repo Structure](#repo-structure)
- [01 — Network Security](#01--network-security)
- [02 — SOC Runbooks](#02--soc-runbooks)
- [03 — KQL Queries](#03--kql-queries)
- [04 — MITRE ATT&CK](#04--mitre-attck)
- [05 — Tools & Resources](#05--tools--resources)
- [06 — Interview Prep](#06--interview-prep)
- [07 — Projects](#07--projects)
- [08 — Study Roadmap](#08--study-roadmap)
- [Tech Stack](#tech-stack)
- [Certifications](#certifications)
- [How to Use This Repo](#how-to-use-this-repo)
- [Contributing](#contributing)
- [Connect](#connect)

---

## Repo Structure

```
BlueForge/
│
├── 📄 README.md
├── 📄 LICENSE
├── 📄 .gitignore
│
├── 📁 01-network-security/
│   ├── 📕 Network_Security_Study_Material.pdf
│   ├── 📁 notes/                        ← 15 chapter markdown files
│   └── 📁 cheatsheets/                  ← ports, protocols, subnetting
│
├── 📁 02-soc-runbooks/
│   ├── 📕 SOC_Alert_Runbook_50_Alerts.pdf
│   ├── 📄 alert-index.md
│   ├── 📄 severity-sla-matrix.md
│   └── 📁 alerts/                       ← 11 tactic subfolders, one .md per alert
│       ├── credential-access/
│       ├── initial-access/
│       ├── execution/
│       ├── lateral-movement/
│       ├── persistence/
│       ├── defense-evasion/
│       ├── exfiltration/
│       ├── command-and-control/
│       ├── discovery/
│       ├── privilege-escalation/
│       └── collection/
│
├── 📁 03-kql-queries/
│   ├── 📄 master-query-library.kql      ← all 50 queries in one file
│   ├── 📄 credential-access.kql
│   ├── 📄 initial-access.kql
│   ├── 📄 execution.kql
│   ├── 📄 lateral-movement.kql
│   ├── 📄 persistence.kql
│   ├── 📄 defense-evasion.kql
│   ├── 📄 exfiltration.kql
│   ├── 📄 c2-detection.kql
│   ├── 📄 discovery.kql
│   ├── 📄 privilege-escalation.kql
│   └── 📄 collection.kql
│
├── 📁 04-mitre-attack/
│   ├── 📄 ttp-coverage-map.md
│   ├── 📄 tactics-reference.md
│   └── 📄 navigator-layer.json          ← import into ATT&CK Navigator
│
├── 📁 05-tools-and-resources/
│   ├── 📄 soc-tools-reference.md
│   ├── 📄 threat-intel-feeds.md
│   ├── 📄 windows-event-ids.md
│   └── 📄 ioc-enrichment-sources.md
│
├── 📁 06-interview-prep/
│   ├── 📕 SOC_Interview_91_Questions.pdf
│   ├── 📄 scenario-based-questions.md
│   └── 📄 kql-interview-questions.md
│
├── 📁 07-projects/
│   ├── 📁 phishprobe/                   ← Python CLI phishing email analyzer
│   └── 📁 sentinel-detections/          ← custom Sentinel analytics rules
│
└── 📁 08-study-roadmap/
    ├── 📄 cert-progression-path.md
    ├── 📄 detection-engineer-roadmap.md
    └── 📄 12-week-cysa-roadmap.md
```

---

## 01 — Network Security

> **15 chapters · Beginner to Advanced · Exam + Career Prep**

Complete network security study material covering everything a SOC analyst needs to understand what they're defending. Each chapter is available as a full PDF and as individual markdown notes for quick reference.

| Chapter | Topic | Key Concepts |
|---------|-------|--------------|
| 01 | Networking Fundamentals | LAN/WAN/MAN, topologies, network devices |
| 02 | OSI & TCP/IP Models | 7 layers, attack surfaces per layer, TCP vs UDP |
| 03 | IP Addressing & Subnetting | IPv4 classes, CIDR, private ranges, IPv6 |
| 04 | Core Protocols | HTTP/S, SSH, DNS, SMB, RDP — with security notes |
| 05 | Firewalls & Packet Filtering | Stateful, NGFW, WAF, DMZ architecture |
| 06 | VPNs & Tunneling | IPSec, WireGuard, OpenVPN, split tunneling risks |
| 07 | IDS / IPS Systems | Signature vs anomaly detection, NIDS vs HIDS |
| 08 | Network Attacks | DDoS, ARP poisoning, DNS spoofing, BGP hijacking |
| 09 | Wireless Security | WPA2/3, evil twin, KRACK, deauth attacks |
| 10 | Cryptography Basics | AES, RSA, ECC, hashing, symmetric vs asymmetric |
| 11 | PKI & Certificates | CA, X.509, TLS handshake, certificate revocation |
| 12 | DNS & Web Security | DNS record types, DNS tunneling, DNSSEC |
| 13 | Network Monitoring | Wireshark, tcpdump, Snort, Suricata, Zeek |
| 14 | Zero Trust Architecture | Never trust always verify, ZT pillars, ZTNA |
| 15 | Incident Response | NIST SP 800-61 lifecycle, IoC types, IR phases |

📁 [`01-network-security/`](./01-network-security/)

---

## 02 — SOC Runbooks

> **50 real-world alerts · MITRE ATT&CK mapped · Step-by-step response procedures**

Every runbook entry follows the same 4-part structure:

- **WHY TRIGGERED** — the attacker behavior or anomaly causing the alert to fire
- **HOW DETECTED** — the log source, rule logic, or ML model involved
- **RUNBOOK STEPS** — numbered, prioritized response procedure to follow in sequence
- **KQL DETECTION QUERY** — ready-to-use Microsoft Sentinel query

### Severity SLA Reference

| Severity | SLA | Required Action |
|----------|-----|-----------------|
| 🔴 CRITICAL | Immediate | Isolate, escalate, page IR team |
| 🟠 HIGH | < 1 hour | Investigate, contain, escalate if needed |
| 🟡 MEDIUM | < 4 hours | Investigate, document, tune if false positive |
| 🟢 LOW | < 24 hours | Review, close or escalate with evidence |

### Alerts by MITRE Tactic

<details>
<summary><strong>Credential Access (9 alerts)</strong></summary>

| # | Alert | Severity | MITRE |
|---|-------|----------|-------|
| 01 | Brute Force Login Attempt | 🟠 HIGH | T1110.001 |
| 02 | Password Spray Attack | 🔴 CRITICAL | T1110.003 |
| 03 | MFA Fatigue / Multiple Failed MFA | 🟠 HIGH | T1621 |
| 13 | Kerberoasting Attack | 🟠 HIGH | T1558.003 |
| 14 | DCSync Attack Detected | 🔴 CRITICAL | T1003.006 |
| 15 | Mimikatz / Credential Dumping Tool | 🔴 CRITICAL | T1003.001 |
| 32 | LSASS Memory Access | 🔴 CRITICAL | T1003.001 |
| 46 | Account Lockout Storm | 🟡 MEDIUM | T1110 |
| 50 | Golden Ticket / Kerberos Ticket Anomaly | 🔴 CRITICAL | T1558.001 |

</details>

<details>
<summary><strong>Initial Access (5 alerts)</strong></summary>

| # | Alert | Severity | MITRE |
|---|-------|----------|-------|
| 04 | Impossible Travel Alert | 🟠 HIGH | T1078 |
| 05 | Phishing Email Delivered to Mailbox | 🟠 HIGH | T1566.001 |
| 17 | Privileged Account Login Outside Business Hours | 🟡 MEDIUM | T1078.002 |
| 38 | Anomalous Azure AD / Entra ID Sign-in Risk | 🟠 HIGH | T1078.004 |
| 39 | SQL Injection Attack Detected | 🟠 HIGH | T1190 |

</details>

<details>
<summary><strong>Execution (4 alerts)</strong></summary>

| # | Alert | Severity | MITRE |
|---|-------|----------|-------|
| 06 | Malicious URL Clicked by User | 🔴 CRITICAL | T1566.002 |
| 07 | Malware Detected by EDR | 🔴 CRITICAL | T1204 |
| 09 | Suspicious PowerShell Execution | 🟠 HIGH | T1059.001 |
| 42 | Unusual Process Spawned from Office Application | 🟠 HIGH | T1566.001 |

</details>

<details>
<summary><strong>Lateral Movement (3 alerts)</strong></summary>

| # | Alert | Severity | MITRE |
|---|-------|----------|-------|
| 11 | Lateral Movement via SMB / PsExec | 🔴 CRITICAL | T1021.002 |
| 12 | Pass-the-Hash (PtH) Attack | 🔴 CRITICAL | T1550.002 |
| 18 | Suspicious RDP Connection from External IP | 🟠 HIGH | T1021.001 |

</details>

<details>
<summary><strong>Persistence (5 alerts)</strong></summary>

| # | Alert | Severity | MITRE |
|---|-------|----------|-------|
| 16 | New Local Administrator Account Created | 🟠 HIGH | T1136.001 |
| 25 | Suspicious Scheduled Task Created | 🟠 HIGH | T1053.005 |
| 26 | Registry Run Key Modified for Persistence | 🟠 HIGH | T1547.001 |
| 30 | Suspicious New Service Installed | 🟠 HIGH | T1543.003 |
| 40 | Web Shell Uploaded / Detected | 🔴 CRITICAL | T1505.003 |

</details>

<details>
<summary><strong>Defense Evasion (7 alerts)</strong></summary>

| # | Alert | Severity | MITRE |
|---|-------|----------|-------|
| 10 | Living off the Land (LOLBins) Abuse | 🟠 HIGH | T1218 |
| 28 | Windows Defender / AV Disabled | 🟠 HIGH | T1562.001 |
| 29 | Firewall Rules Modified | 🟡 MEDIUM | T1562.004 |
| 31 | Process Injection Detected | 🔴 CRITICAL | T1055 |
| 34 | Encoded / Obfuscated Command Execution | 🟠 HIGH | T1027 |
| 36 | Windows Event Log Cleared | 🔴 CRITICAL | T1070.001 |
| 49 | Mass Email Deletion by User | 🟠 HIGH | T1070.008 |

</details>

<details>
<summary><strong>Exfiltration (2 alerts)</strong></summary>

| # | Alert | Severity | MITRE |
|---|-------|----------|-------|
| 19 | Data Exfiltration via Cloud Storage | 🔴 CRITICAL | T1567.002 |
| 20 | Sensitive Data in Email Attachment (DLP) | 🟠 HIGH | T1048 |

</details>

<details>
<summary><strong>Command & Control (4 alerts)</strong></summary>

| # | Alert | Severity | MITRE |
|---|-------|----------|-------|
| 21 | DNS Tunneling Detected | 🟠 HIGH | T1071.004 |
| 22 | C2 Beaconing Activity Detected | 🔴 CRITICAL | T1071.001 |
| 23 | Tor Network Usage Detected | 🟠 HIGH | T1090.003 |
| 48 | Outbound Traffic to Known Malicious IP | 🟠 HIGH | T1071 |

</details>

<details>
<summary><strong>Discovery (2 alerts)</strong></summary>

| # | Alert | Severity | MITRE |
|---|-------|----------|-------|
| 24 | Internal Port Scan Detected | 🟡 MEDIUM | T1046 |
| 35 | Network Share Enumeration (SMB Recon) | 🟡 MEDIUM | T1135 |

</details>

<details>
<summary><strong>Privilege Escalation (2 alerts)</strong></summary>

| # | Alert | Severity | MITRE |
|---|-------|----------|-------|
| 33 | UAC Bypass Attempt | 🟠 HIGH | T1548.002 |
| 45 | Domain Admin Account Used from Non-PAW | 🟠 HIGH | T1078.002 |

</details>

<details>
<summary><strong>Collection / Others (7 alerts)</strong></summary>

| # | Alert | Severity | MITRE |
|---|-------|----------|-------|
| 37 | Suspicious Email Forwarding Rule Created | 🟠 HIGH | T1114.003 |
| 41 | Suspicious AWS API Calls (CloudTrail) | 🟠 HIGH | T1530 |
| 43 | Large Number of Files Accessed — Insider Threat | 🟠 HIGH | T1039 |
| 44 | USB Mass Storage Device Inserted | 🟡 MEDIUM | T1091 |
| 47 | Sensitive File Access by Unusual User | 🟠 HIGH | T1083 |
| 08 | Ransomware Behavioral Detection | 🔴 CRITICAL | T1486 |
| 27 | Volume Shadow Copy Deletion | 🔴 CRITICAL | T1490 |

</details>

📁 [`02-soc-runbooks/`](./02-soc-runbooks/)

---

## 03 — KQL Queries

> **50 production queries · Microsoft Sentinel · Organized by tactic**

All detection queries from the runbook, organized by MITRE tactic, commented for clarity, and ready to paste into Microsoft Sentinel Analytics or the Logs blade.

### Quick Start

1. Open **Microsoft Sentinel → Logs**
2. Copy any query from the relevant `.kql` file
3. Adjust thresholds to match your environment's baseline
4. For Analytics Rules: paste into **Sentinel → Analytics → Create → Scheduled query rule**

### Query Files

| File | Tactic | Queries |
|------|--------|---------|
| `master-query-library.kql` | All tactics | 50 |
| `credential-access.kql` | Credential Access | 9 |
| `initial-access.kql` | Initial Access | 5 |
| `execution.kql` | Execution | 4 |
| `lateral-movement.kql` | Lateral Movement | 3 |
| `persistence.kql` | Persistence | 5 |
| `defense-evasion.kql` | Defense Evasion | 7 |
| `exfiltration.kql` | Exfiltration | 2 |
| `c2-detection.kql` | Command & Control | 4 |
| `discovery.kql` | Discovery | 2 |
| `privilege-escalation.kql` | Privilege Escalation | 2 |
| `collection.kql` | Collection + Impact | 7 |

### Sample Query — Brute Force Detection

```kql
// #01 Brute Force Login Attempt | HIGH | T1110.001
// Fires when 5+ failed logins occur on the same account within 5 minutes from one IP
SecurityEvent
| where EventID == 4625
| summarize Failures = count() by Account, IpAddress, bin(TimeGenerated, 5m)
| where Failures > 5
| project TimeGenerated, Account, IpAddress, Failures
| order by Failures desc
```

### Sample Query — Ransomware Behavioral Detection

```kql
// #08 Ransomware Behavioral Detection | CRITICAL | T1486
// Fires when a process renames/encrypts 100+ files in under 30 seconds
DeviceFileEvents
| where ActionType == 'FileRenamed'
| summarize Count = count() by InitiatingProcessFileName, bin(Timestamp, 30s)
| where Count > 100
| project Timestamp, InitiatingProcessFileName, Count
| order by Count desc
```

📁 [`03-kql-queries/`](./03-kql-queries/)

---

## 04 — MITRE ATT&CK

> **11 tactics · 30+ techniques · ATT&CK Navigator JSON export**

Complete TTP coverage mapping for all 50 runbook alerts. Includes an ATT&CK Navigator layer JSON you can import directly at [mitre-attack.github.io/attack-navigator](https://mitre-attack.github.io/attack-navigator/) to visualize your detection coverage.

### Tactics Covered

| Tactic | ID | Alerts Covering It |
|--------|----|--------------------|
| Initial Access | TA0001 | 5 |
| Execution | TA0002 | 4 |
| Persistence | TA0003 | 5 |
| Privilege Escalation | TA0004 | 2 |
| Defense Evasion | TA0005 | 7 |
| Credential Access | TA0006 | 9 |
| Discovery | TA0007 | 2 |
| Lateral Movement | TA0008 | 3 |
| Collection | TA0009 | 5 |
| Command & Control | TA0011 | 4 |
| Exfiltration | TA0010 | 2 |
| Impact | TA0040 | 2 |

📁 [`04-mitre-attack/`](./04-mitre-attack/)

---

## 05 — Tools & Resources

> **Quick reference sheets for the tools used in every runbook**

### SOC Tools Reference

| Tool | Category | Used For |
|------|----------|---------|
| Microsoft Sentinel | SIEM | KQL queries, alert correlation, threat hunting |
| Microsoft Defender XDR | XDR | Device isolation, process tree, alerts |
| SentinelOne | EDR | Endpoint behavioral detection, memory protection |
| Cortex XDR | EDR/XDR | Causality analysis, threat intelligence |
| Awake Security | NDR | Network traffic analysis, encrypted traffic |
| Armis | OT/IoT | Asset discovery, passive device monitoring |
| Zscaler | Proxy/SSE | Web filtering, SSL inspection, CASB |
| VirusTotal | TI | Hash, IP, domain reputation lookup |
| AbuseIPDB | TI | IP reputation, abuse reports |
| AnyRun / Hybrid Analysis | Sandbox | Interactive malware analysis |
| Wireshark / Zeek | Network | Packet capture and traffic analysis |
| Volatility | DFIR | Memory forensics, malware unpacking |
| CyberChef | Analysis | Decoding, decryption, data manipulation |
| MITRE ATT&CK Navigator | Planning | TTP visualization, detection gap mapping |

### Key Windows Event IDs — Quick Reference

| Event ID | Description | Why It Matters |
|----------|-------------|----------------|
| 4624 | Successful logon | Baseline and anomaly detection |
| 4625 | Failed logon | Brute force, spray detection |
| 4648 | Logon with explicit credentials | Pass-the-hash indicator |
| 4662 | Object operation on AD object | DCSync detection |
| 4663 | File access attempt | Sensitive file access monitoring |
| 4698 | Scheduled task created | Persistence mechanism |
| 4720 | User account created | Backdoor account detection |
| 4732 | Member added to security group | Privilege escalation |
| 4740 | Account locked out | Spray/brute force result |
| 4769 | Kerberos ticket requested | Kerberoasting detection |
| 5001 | Defender real-time protection disabled | AV tamper detection |
| 5140 | Network share accessed | SMB enumeration |
| 7045 | New service installed | Persistence via service |
| 1102 | Audit log cleared | Log tampering indicator |

📁 [`05-tools-and-resources/`](./05-tools-and-resources/)

---

## 06 — Interview Prep

> **91 SOC interview questions · Scenario walkthroughs · KQL interview questions**

Covers all question types encountered in SOC analyst interviews at Tier 1 through Tier 3 levels — technical triage scenarios, detection logic questions, MITRE ATT&CK questions, KQL-specific questions, and behavioral/situational rounds.

### Topics Covered

- Alert triage decision trees
- Phishing investigation walkthroughs
- Malware analysis scenario questions
- Incident response process (PICERL)
- Log analysis and KQL query writing
- MITRE ATT&CK technique identification
- Tool-specific questions (Sentinel, Defender, SentinelOne)
- Behavioral round preparation (reason for leaving, salary, career goals)

📁 [`06-interview-prep/`](./06-interview-prep/)

---

## 07 — Projects

> **Functional tools built from real SOC needs**

### PhishProbe

A zero-dependency Python CLI tool for phishing email forensics. Drop an `.eml` file in, get a full analysis report out.

**Capabilities:**
- Email header forensics — SPF, DKIM, DMARC validation
- URL extraction and reputation inspection
- IOC extraction — IPs, domains, hashes
- Attachment analysis — file type, hash generation
- Threat scoring — LOW / MEDIUM / HIGH / CRITICAL output
- JSON report export for SIEM ingestion

```bash
# Usage
python phishprobe.py --file suspicious.eml
python phishprobe.py --file suspicious.eml --output report.json
```

📁 [`07-projects/phishprobe/`](./07-projects/phishprobe/)

---

### Sentinel Detections

Custom Microsoft Sentinel Analytics Rules beyond the default content hub — written for detection gaps identified during real incident investigations.

📁 [`07-projects/sentinel-detections/`](./07-projects/sentinel-detections/)

---

## 08 — Study Roadmap

> **Structured learning plans for the certifications that matter in blue team**

### Certification Progression Path

```
[Current]                    [Next 6 Months]              [Long-Term]
─────────────────────────────────────────────────────────────────────
SC-200 ✅                    CySA+ CS0-003 🎯             PNPT
AWS SAA-C03 ✅               CCSP                         OSCP
ISC2 CC ✅                   AZ-500                       GREM (GIAC)
```

### 12-Week CySA+ Self-Study Plan

Structured week-by-week study plan mapped to CySA+ CS0-003 exam domains, with labs, practice tests, and checkpoints.

📁 [`08-study-roadmap/`](./08-study-roadmap/)

---

## Tech Stack

```
SIEM          Microsoft Sentinel · Splunk (concepts)
EDR / XDR     SentinelOne · Microsoft Defender for Endpoint · Cortex XDR
Network       Awake Security (NDR) · Zscaler · Wireshark · Suricata
OT / IoT      Armis
Identity      Azure AD / Entra ID · Active Directory
Cloud         AWS (GuardDuty, CloudTrail) · Microsoft Azure
Query Lang    KQL (Kusto) · SPL (Splunk basics)
Scripting     Python · PowerShell · Bash
Frameworks    MITRE ATT&CK · NIST CSF · Cyber Kill Chain · PICERL
```

---

## Certifications

| Certification | Issuer | Status |
|---------------|--------|--------|
| SC-200 — Security Operations Analyst | Microsoft | ✅ Active |
| SAA-C03 — Solutions Architect Associate | AWS | ✅ Active |
| CC — Certified in Cybersecurity | ISC2 | ✅ Active |
| CySA+ CS0-003 | CompTIA | 🎯 In Progress |

---

## How to Use This Repo

### For SOC Analysts
Start at `02-soc-runbooks/` — find the alert type you're investigating and follow the numbered runbook steps. Use the corresponding KQL file in `03-kql-queries/` to run detections in Sentinel.

### For Interview Prep
Start at `06-interview-prep/` for question banks and `04-mitre-attack/` to memorize TTP mappings. Walk through `02-soc-runbooks/` to practice talking through real alert scenarios.

### For Detection Engineers
Go to `03-kql-queries/` — copy, adapt, and tune the 50 queries for your environment. Use `04-mitre-attack/navigator-layer.json` to visualize gaps in your detection coverage.

### For Students
Start at `01-network-security/` and work through the 15 chapters in order. Use the cheatsheets for quick revision before exams.

---

## Roadmap

- [ ] Add Sigma rule versions of all 50 KQL queries
- [ ] Add Python IOC enrichment script (VirusTotal + AbuseIPDB automation)
- [ ] Add cloud attack runbooks — AWS-specific (GuardDuty alerts)
- [ ] Add Active Directory attack detection deep-dives
- [ ] Add Defender XDR advanced hunting query library
- [ ] Add SOAR playbook templates (Logic Apps / Sentinel Automation)

---

## Contributing

This is a personal reference repo but corrections and additions are welcome.

**Good PRs:**
- Fixing incorrect information or outdated KQL syntax
- Adding new runbook entries with the standard 4-part format
- Improving markdown formatting or fixing typos
- Adding new KQL queries with proper comments and MITRE mapping

**Please do not:**
- Add content that is not directly applicable to blue team / SOC work
- Submit AI-generated content without verifying accuracy

To contribute: Fork → Branch → PR with a clear description of what changed and why.

---

## Connect

<div align="center">

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Balamurugan%20A-0077B5?style=flat-square&logo=linkedin)](www.linkedin.com/in/balamurugan-a-3581a120b)
[![GitHub](https://img.shields.io/badge/GitHub-balamurugan--a-181717?style=flat-square&logo=github)](https://github.com/BALAbm7/BlueForge)
[![Email](https://img.shields.io/badge/Email-your@email.com-EA4335?style=flat-square&logo=gmail)](mailto:balube2019@gmail.com)

</div>

---

<div align="center">

**BlueForge** · Built by a SOC analyst, for SOC analysts · 2025

*Alert → Triage → Contain → Investigate → Remediate → Document → Improve*

</div>
