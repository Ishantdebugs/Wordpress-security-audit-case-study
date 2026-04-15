# WordPress Security Audit Findings

This document summarizes the vulnerabilities identified during the initial WPScan assessment of the local WordPress environment, along with their risk levels and current status after remediation.

---

## 1. XML-RPC Enabled

- **Severity:** Critical  
- **Risk:** Brute-force attacks, DDoS amplification  
- **Description:**  
  The XML-RPC endpoint (`xmlrpc.php`) was accessible, allowing attackers to send multiple authentication attempts in a single request.

- **Impact:**  
  Attackers can bypass login protections and perform large-scale password attacks.

- **Status:** Fixed  

---

##  2. User Enumeration

- **Severity:** Critical  
- **Risk:** Username disclosure  
- **Description:**  
  The WordPress site exposed usernames via API and other methods. Initially, the default `admin` user was detected.

- **Impact:**  
  Makes brute-force attacks easier by revealing valid usernames.

- **Action Taken:**  
  - Removed default `admin` user  
  - Created new admin user (`site_manager`)

- **Status:** Partially Fixed (username still detectable)

---

## 3. Directory Listing Enabled

- **Severity:** Medium  
- **Risk:** Sensitive file exposure  
- **Description:**  
  The `/wp-content/uploads/` directory allowed public listing of files.

- **Impact:**  
  Anyone could view uploaded files including images and documents.

- **Status:** Fixed  

---

## 4. Server Information Disclosure

- **Severity:** Medium  
- **Risk:** Exposure of server technologies  
- **Description:**  
  Server headers revealed Apache, PHP, and OpenSSL versions.

- **Impact:**  
  Helps attackers identify known vulnerabilities for targeted attacks.

- **Status:** Partially Fixed  

---

## 5. WP-Cron Exposure

- **Severity:** Low  
- **Risk:** Resource abuse / DDoS  
- **Description:**  
  The `wp-cron.php` file was publicly accessible and could be triggered externally.

- **Impact:**  
  Attackers can overload server resources.

- **Status:**  Not Fixed  

---

##  6. WordPress Readme File Exposure

- **Severity:** Low  
- **Risk:** Version disclosure  
- **Description:**  
  The `readme.html` file was accessible and revealed WordPress version details.

- **Impact:**  
  Assists attackers in identifying known vulnerabilities.

- **Status:** Fixed  

---

## 7. Plugin Vulnerability (Akismet)

- **Severity:** Critical  
- **Risk:** Stored Cross-Site Scripting (XSS)  
- **Description:**  
  The Akismet plugin was detected with a known vulnerability (CVE-2015-9357), affecting older versions.

- **Impact:**  
  Allows attackers to inject malicious scripts affecting all users.

- **Status:** Not Confirmed / Needs Update  

---

#  Summary

| Category            | Status              |
|--------------------|-------------------|
| Critical Issues     | Partially Resolved |
| Medium Issues       | Mostly Resolved    |
| Low Issues          | Some Pending       |

---

# Conclusion

The initial security assessment revealed multiple vulnerabilities affecting the confidentiality and integrity of the WordPress application.  

After applying remediation steps, several high-risk issues were successfully resolved, significantly improving the security posture. However, some issues such as user enumeration, WP-Cron exposure, and plugin risk still require further hardening.
