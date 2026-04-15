# WordPress Security Audit Case Study

This repository documents a hands-on WordPress security audit performed in a local lab environment using WPScan.

---

## Objective

To identify, analyze, remediate, and validate common WordPress vulnerabilities in a controlled setup.

---

## Environment

- Local Server: XAMPP (Apache, MySQL, PHP)
- Target: WordPress installation
- Testing Machine: Kali Linux
- Tool Used: WPScan

---

## Methodology

1. Initial vulnerability scan
2. Identification of security issues
3. Risk analysis
4. Remediation and hardening
5. Re-scan to validate fixes

---

## Case Study Files

- initial-scan.txt → Raw scan before fixes
- rescan.txt → Scan after applying fixes
- findings.md → Identified vulnerabilities with severity and impact
- remediation.md → Steps taken to fix and harden the system

---

## Key Vulnerabilities Identified

- XML-RPC exposure
- User enumeration
- Directory listing
- Server information disclosure
- WP-Cron exposure
- Plugin vulnerability (Akismet)

---

## Results

- Critical vulnerabilities reduced
- Attack surface minimized
- Security posture improved

---

## Case Study Access

Full audit report:
- case-study/local-lab/report.pdf

## Note

This project is part of a practical cybersecurity learning journey focused on WordPress security auditing and remediation.
