# 🛡️ Phishing Alert Investigation - SOC Analyst Simulation

This repository showcases a simulated phishing alert investigation performed in a Security Operations Center (SOC) environment. The goal of this project is to demonstrate threat detection, analysis, and incident response skills.

## 📄 Overview

A suspicious URL was detected within network traffic logs and flagged for investigation. This project documents the steps taken to analyze, verify, and respond to the potential phishing threat.

---

## 📌 Alert Summary

- **Date of Event:** March 22, 2021, 09:23 PM  
- **Source IP:** `172.16.17.49`  
- **Destination IP:** `91.189.114.8`  
- **User:** Emily comp  
- **User-Agent:** Chrome/79.0.3945.88 (Windows 10 x64)  
- **URL Accessed:**  
  `http://mogagrocol.ru/wp-content/plugins/akismet/fv/index.php?email=ellie@letsdefend.io`  
- **EDR Action:** Containment initiated  
- **Device Action:** Allowed (initially)

---

## 🔍 Investigation Steps

1. **Log Review**
   - Extracted source and destination IPs, timestamp, and user identity.
   - Identified that the request was not blocked by firewall/EDR initially.

2. **Threat Intelligence Lookup**
   - Analyzed URL using:
     - [VirusTotal](https://www.virustotal.com/)
     - [Hybrid Analysis](https://www.hybrid-analysis.com/)
     - [AnyRun](https://any.run/)
     - [URLScan.io](https://urlscan.io/)
   - Confirmed domain was malicious (Threat Score: 100/100).

3. **Endpoint Containment**
   - EDR automatically isolated the affected endpoint.
   - Verified no further outbound connections to malicious IPs.

4. **User Awareness**
   - Notified the user and provided phishing awareness reinforcement.

5. **IOC Blocking**
   - Blocked malicious domain and associated IPs across the network.

---

## ✅ Resolution

- No lateral movement detected.
- Device contained and remediated.
- Threat identified as **malicious phishing URL**.
- Alert closed after confirmation and mitigation steps.

---

## 📁 Files Included

| File | Description |
|------|-------------|
| `analyst_note.md` | Detailed SOC analyst note |
| `close_alert_note.md` | Final summary used to close the alert |
| `ioc_list.txt` | Indicators of compromise (URLs, IPs) |
| `screenshots/` | Screenshots of threat intel lookups and EDR actions |

---

## 🧠 Skills Demonstrated

- SOC alert triage
- Threat intelligence analysis
- Incident response and documentation
- EDR containment and remediation
- Communication and reporting

---

## 📬 Contact

If you have questions or want to discuss cybersecurity topics, feel free to reach out via GitHub or connect on [LinkedIn](https://www.linkedin.com/tajaysamms/).

---

