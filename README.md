
# W2 Pentesting Report — Footprinting & Network Scanning

Week 2 practical report from the **Networkwalks Cybersecurity Internship Program**, covering the reconnaissance/footprinting phase against an authorized target domain and a network scanning exercise on a local LAN.

## Author
**Muhammad Moazam Tariq**
Cybersecurity Professional — Networkwalks Internship Program

## Project Info
- **Program:** Cybersecurity Program at Networkwalks
- **Week:** 02
- **Modules:** W2-PM1 (Multiple Kali Tools), W2-PM5 (Zenmap Scanning)
- **Date:** 21 August 2026

## Scope & Authorization
- **Target 1:** networkwalks.com — tested with written permission from Networkwalks
- **Target 2:** My own local LAN network

All activities were performed only on systems with explicit written permission or systems I own. This work is for educational purposes only, completed as part of an authorized internship lab.

## Phases Covered
- ✅ Phase 1: Reconnaissance & Footprinting
- ✅ Phase 2: Scanning & Network Discovery
- ⏳ Phase 3–5: In Progress

## Tools Used

| Tool | Purpose |
|---|---|
| Kali Linux | OS used for reconnaissance activities |
| WHOIS | Domain registration details (owner, dates, name servers) |
| WhatWeb | Fingerprint web technologies (server, CMS, plugins, IP) |
| nslookup | Resolve domain name to IP address via DNS |
| curl -I | Read HTTP response headers |
| wafw00f | Detect Web Application Firewall presence |
| dnsrecon | Enumerate DNS records (SOA, MX, TXT/SPF, SRV) |
| Zenmap (Nmap GUI) | Scan local host for open ports and services |

## Summary of Findings
- Domain registered via GoDaddy, hosted on HostGator name servers, DNSSEC not enabled
- Website runs WordPress 7.1 with WP Download Manager 3.3.58, Bootstrap 7.1, JQuery 3.7.1
- Server resolves to `192.232.216.135`
- Site protected by ModSecurity (SpiderLabs) WAF
- DNS enumeration revealed MX, SPF, and 8 Autodiscover SRV records
- Zenmap scan of local host `192.168.56.1` found 4 open ports (135, 139, 445, 5357) — indicating SMB/NetBIOS services typical of a Windows host

Full details, evidence, and risk analysis are in the report.

## Repository Structure
```
├── report/          # Full pentesting report (Word/PDF)
├── evidence/         # Screenshots (Zenmap scan)
├── raw-outputs/       # Raw tool output text files
└── README.md
```

## Disclaimer
All activities documented here were performed only on authorized systems. This repository is for educational and portfolio purposes only. Unauthorized access to systems you do not own or have permission to test is illegal.
