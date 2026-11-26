# OWASP mapping

This page maps the scanner's built-in checks to **OWASP Top 10**-style
categories. These are **heuristic probes**, not a replacement for manual
testing with Burp Suite, OWASP ZAP, or a qualified pentester.

| Scanner check | OWASP area | What it looks for |
| :--- | :--- | :--- |
| SQLi Error Probe | A03 Injection | Database error patterns in responses |
| Reflection / XSS Probe | A03 Injection | Reflected input without encoding |
| LFI / Path Traversal | A01 Broken Access Control | Traversal payloads reaching files |
| SSRF Heuristic Probe | A10 Server-Side Request Forgery | Outbound-fetch style parameters |
| Sensitive File Exposure | A05 Security Misconfiguration | `.env`, `.git/HEAD`, backups, configs |
| Backup Discovery | A05 Security Misconfiguration | `backup.zip`, `db.sql`, `config.php.bak` |
| Git / VCS Exposure | A05 Security Misconfiguration | Public `.git` repository metadata |
| Directory Listing | A05 Security Misconfiguration | Index pages exposing file trees |
| CORS Misconfig Check | A05 Security Misconfiguration | Over-permissive `Access-Control-Allow-*` |
| HTTP Methods Check | A05 Security Misconfiguration | TRACE / TRACK / dangerous methods |
| Cookie Security Flags | A02 / A05 | Missing `Secure`, `HttpOnly`, `SameSite` |
| HSTS / HTTPS Redirect | A02 Cryptographic Failures | Missing HSTS or weak redirect handling |
| Mixed Content Scan | A02 Cryptographic Failures | HTTP resources on HTTPS pages |
| Open Redirect Probe | A01 Broken Access Control | Unvalidated redirect parameters |
| Host Header Injection | A05 Security Misconfiguration | Reflected or poisoned Host header |
| Admin Panel Finder | A05 Security Misconfiguration | Exposed `/admin`, `/panel`, `/dashboard` |
| Security Headers | A05 Security Misconfiguration | Missing CSP, X-Frame-Options, etc. |
| Technology Disclosure | A05 Security Misconfiguration | Version-banner leakage |

> **Important:** A finding from this scanner is a lead to investigate, not a
> confirmed vulnerability. Verify manually and follow your engagement's rules
> of scope. Authorized testing only.
