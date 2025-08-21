# 🔍 SOC Level 1 Incident Response Simulation

*Hands-on analysis of security alerts in a simulated SOC environment using TryHackMe's SOC Level 1 path.*

![TryHackMe](https://img.shields.io/badge/TryHackMe-SOC_Level_1-FF6D70?style=for-the-badge&logo=tryhackme&logoColor=white)
![Splunk](https://img.shields.io/badge/Splunk-Querying-000000?style=for-the-badge&logo=splunk&logoColor=white)
![MITRE ATT&CK](https://img.shields.io/badge/MITRE-ATT&CK-FF6D70?style=for-the-badge&logo=mitre&logoColor=white)

## 📋 Project Overview

This project involved completing **TryHackMe's SOC Level 1** simulator, a hands-on environment designed to mimic real-world Security Operations Center workflows. I analyzed various security alerts, investigated incidents, and documented findings following standard IR procedures.

**Key Skills Practiced:**
- Security alert triage and analysis
- Splunk querying for log investigation
- IOC extraction and threat intelligence correlation
- Incident documentation and reporting
- MITRE ATT&CK framework application

## 🛠️ Tools & Technologies Used

- **SIEM Platform:** Splunk
- **Threat Intelligence:** VirusTotal, URLScan.io
- **Analysis Tools:** Windows Event Viewer, CMD, PowerShell
- **Framework:** MITRE ATT&CK
- **Platform:** TryHackMe

## 🔬 Incident Analysis Examples

### Phishing Email Investigation
- **Alert:** Suspicious email reported by user
- **Analysis:** 
  - Examined email headers for spoofing indicators
  - Analyzed embedded URLs using URLScan.io
  - Extracted and examined attachments
- **Findings:** Identified malicious payload delivery attempt
- **MITRE Technique:** T1566 - Phishing

### Brute Force Attack Detection
- **Alert:** Multiple failed login attempts
- **Analysis:**
  ```sql
  index=windows EventCode=4625
  | stats count by src_ip, user
  | where count > 10
  | sort - count

- **Findings:** Identified brute force attempt from suspicious IP

- **MITRE Technique:** T1110 - Brute Force

**Malware Execution Analysis**
- **Alert:** Suspicious process execution

- **Analysis:**

  - Examined process tree relationships

  - Submitted file hashes to VirusTotal

  - Analyzed network connections

- **Findings:** Identified malware persistence mechanism

- **MITRE Technique:** T1204 - User Execution

## 📊 Key Results & Metrics
- **Incidents Handled:** 10+ security alerts

- **Detection Accuracy:** 90% correct classification rate

- **IOCs Extracted:** 15+ indicators (IPs, hashes, domains)

- **Techniques Mapped:** 8+ MITRE ATT&CK techniques

## 🎯 Lessons Learned
"This simulation reinforced that effective documentation is as crucial as detection - clear notes enable smoother handoffs to Tier 2 analysts and better incident resolution."

"I gained practical understanding of how apparent false positives often reveal deeper security issues when investigated thoroughly."
