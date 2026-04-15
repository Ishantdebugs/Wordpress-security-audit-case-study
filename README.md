# WordPress Security Audit Case Study

This repository documents a hands-on WordPress security audit performed in a local lab environment.

##  Objective

To identify, analyze, and remediate common WordPress vulnerabilities using practical tools and techniques.

##  Environment Setup

- Local server: XAMPP (Apache + MySQL + PHP)
- Target: WordPress installation
- Testing machine: Kali Linux
- Tool used: WPScan

## Audit Process

1. Initial vulnerability scan using WPScan
2. Identification of security issues
3. Understanding risk and impact
4. Applying remediation steps
5. Re-scanning to validate fixes

## Key Vulnerabilities Identified

- XML-RPC enabled
- User enumeration
- Directory listing
- Information disclosure
- WP-Cron exposure
- Plugin vulnerability (Akismet)

## Remediation Actions

- Disabled XML-RPC
- Changed default admin user
- Disabled directory listing
- Removed sensitive files
- Improved server configuration

## Validation

A follow-up scan was conducted to verify that critical vulnerabilities were successfully fixed.

## Outcome

Improved security posture of the WordPress application by reducing attack surface and eliminating high-risk vulnerabilities.

## Note

This project is part of my cybersecurity learning journey focused on practical WordPress security auditing.
