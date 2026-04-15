# 🔐 SOC Alert Triage & Incident Response Lab

## 📌 Overview

This project simulates a Tier 1 Security Operations Center (SOC) workflow, focusing on alert triage, log analysis, and incident response using a SIEM platform.

The objective is to detect, investigate, and respond to suspicious authentication activity by correlating security events and identifying indicators of compromise (IOCs).

---

## 🎯 Objectives

* Perform alert triage in a SIEM environment (Splunk)
* Analyze Windows authentication logs
* Correlate security events across multiple data sources
* Identify potential brute-force attack behavior
* Document findings and response actions

---

## 🛠️ Tools & Technologies

* Splunk (SIEM & Log Analysis)
* Windows Event Logs
* Kali Linux
* Nmap (supporting reconnaissance context)

---

## 🚨 Scenario

A security alert was triggered after multiple failed login attempts were detected on a user account, followed by a successful authentication from an unfamiliar IP address.

---

## 🔎 Alert Details

* **Alert Type:** Suspicious Authentication Activity
* **Trigger Condition:** Excessive failed login attempts within a defined time window
* **Log Source:** Windows Security Event Logs
* **Relevant Event IDs:**

  * 4625 – Failed Logon
  * 4624 – Successful Logon

---

## 🧪 Investigation Workflow

### 1. Alert Triage

* Reviewed Splunk alert for authentication anomalies
* Identified a spike in failed login attempts from a single external IP

### 2. Log Analysis

* Queried Event IDs 4625 and 4624 in Splunk
* Correlated timestamps to identify a successful login following repeated failures

### 3. Event Correlation

* Mapped source IP activity across multiple login events
* Evaluated login frequency and timing patterns
* Compared activity against expected user behavior baseline

### 4. Threat Analysis

* Activity consistent with brute-force attack techniques
* Indicators suggest potential credential compromise

---

## 🔍 Findings

* High volume of failed login attempts originating from a single IP
* Successful authentication occurred after repeated failures
* Login behavior deviates from normal user activity

---

## 🛡️ Response Actions

* Initiated password reset for affected account
* Recommended account lockout policy enforcement
* Suggested blocking or investigating source IP
* Escalated incident for further analysis

---

## 📈 Outcome

The activity was identified as a probable brute-force attack. Early detection and analysis enabled rapid containment and reduced the risk of further compromise.

---

## 🧠 Lessons Learned

* Correlating failed and successful login events is critical for detecting account compromise
* SIEM tools are essential for identifying patterns across large datasets
* Rapid triage and response significantly reduce impact

---

## 🔗 SOC Analyst Skills Demonstrated

* Alert Triage
* Log Analysis (Splunk)
* Event Correlation
* Threat Detection
* Incident Response

---

## 📎 Future Improvements

* Implement automated detection rules for brute-force behavior
* Integrate additional log sources (firewall, endpoint telemetry)
* Expand detection coverage for lateral movement and persistence

---

## 👤 Author

Christopher Alan Sehnert
Cybersecurity Analyst (SOC Path)
GitHub: https://github.com/sehnert32-cmyk

---
