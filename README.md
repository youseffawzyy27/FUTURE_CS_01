# FUTURE_CS_01 — Vulnerability Assessment Report

**Internship:** Future Interns Cyber Security Internship
**Track:** Cyber Security (CS)
**Task:** Task 1 — Vulnerability Assessment Report for a Live Website
**Intern:** Yousef Ahmed Fawzy
**CIN ID:** FIT/JUN26/CS9482
**Date:** 30 June 2026

---

## Target Information

| Item | Details |
|---|---|
| **Website Tested** | OWASP Juice Shop (deliberately vulnerable demo web application) |
| **URL** | http://localhost:3000 |
| **Hosting** | Self-hosted via Docker on Kali Linux |
| **Type** | Demo/training web application (legal to test) |

---

## Scope

- Public-facing pages only
- Passive scanning only (no exploitation, no brute force, no DoS)
- Read-only analysis

---

## Tools Used

| Tool | Purpose |
|---|-----|
| Nmap 7.95 | Port scanning and service detection |
| Browser DevTools (Firefox) | HTTP response header analysis |
| OWASP ZAP 2.17.0 | Passive vulnerability scanning |
| Canva | Professional report design |

---

## Findings Summary

| # | Finding | Risk Level | Tool |
|---|---|---|---|
| 1 | Wildcard CORS (Access-Control-Allow-Origin: *) | Medium | Nmap, DevTools, ZAP |
| 2 | Missing Content-Security-Policy Header | Medium | DevTools |
| 3 | Missing Strict-Transport-Security Header | Medium | DevTools |
| 4 | No HTTPS Enforcement (HTTP only) | Medium | DevTools |
| 5 | X-Recruiting Header Information Disclosure | Low | Nmap, DevTools |
| 6 | Timestamp Disclosure in API Responses | Low | ZAP |

---

## Evidence

All screenshots are in the `/Evidence` folder:

- `01_juiceshop_homepage.png` — Target website loaded in browser
- `02_nmap_scan.png` — Nmap port scan output
- `03_devtools_network_tab.png` — DevTools Network tab
- `04_devtools_response_headers.png` — HTTP Response Headers
- `05_zap_history.png` — ZAP captured traffic
- `06_zap_cors_alert.png` — ZAP Cross-Domain Misconfiguration alert
- `07_zap_timestamp_alert.png` — ZAP Timestamp Disclosure alert

---

## Report

Full Vulnerability Assessment Report (PDF) is available in the `/Report` folder.
