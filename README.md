# Automated Log Analyzer & Alerting System

## 1. Introduction

In today’s digital environment, cyber attacks such as brute-force attempts, unauthorized access, and privilege escalation are increasing rapidly. Organizations rely on Security Operations Centers (SOC) to continuously monitor system logs and detect such threats. However, manual log monitoring is time-consuming and inefficient.

The **Automated Log Analyzer & Alerting System** is a Linux-based security monitoring project developed using **Python and Shell scripting**. The system automatically collects system logs, analyzes them for high-risk security threats, and generates alerts. This project simulates a **real-world SOC / SIEM-style log monitoring workflow**.

📸 *Screenshot 1: Project directory structure*
<img width="461" height="647" alt="Directory_structure" src="https://github.com/user-attachments/assets/dcc7a675-d4aa-4138-b199-d640e89b5d67" />

---

## 2. Objectives of the Project

The key objectives of this project are:

* To automate the collection of Linux system and authentication logs
* To analyze logs and detect suspicious or malicious activities
* To identify high-risk security threats using rule-based detection
* To generate real-time alerts for detected threats
* To understand SOC-level log monitoring concepts

📸 *Screenshot 2: Log collection script execution*
<img width="1920" height="1080" alt="logs_collection" src="https://github.com/user-attachments/assets/b6923ab8-ebc8-4c3e-85df-fc7a739d8bbf" />

---

## 3. Scope of the Project

This project focuses on local Linux system monitoring. It analyzes authentication and system logs to detect security incidents. The project is suitable for academic use and beginner-to-intermediate SOC analyst training.

**In Scope:**

* Authentication and system log analysis
* High-risk threat detection
* Automated alert generation

**Out of Scope:**

* Graphical dashboards
* Cloud-based SIEM integration
* Advanced machine learning models

---

## 4. System Architecture

The project follows a modular and layered architecture:

1. **Shell Script Module** – Collects and manages system logs
2. **Log Parser Module (Python)** – Reads and processes log files
3. **Threat Detection Module (Python)** – Identifies security threats
4. **Alerting Module (Python)** – Generates alerts and reports

**Architecture Flow:**
System Logs → Shell Script → Python Analyzer → Alerts

📸 *Screenshot 3: Architecture diagram*
<img width="529" height="410" alt="Architecture_diagram" src="https://github.com/user-attachments/assets/b08e1e71-713d-4a51-9a4d-4a762c408073" />

---

## 5. Technologies Used

* Operating System: Linux (Ubuntu / Kali)
* Programming Language: Python 3
* Scripting Language: Bash (Shell scripting)
* Logs: auth.log, syslog, journalctl
* Tools & Concepts: Cron jobs, Regular Expressions, Log Analysis

---

## 6. Project Modules Description

### 6.1 Log Collection Module

This module uses Shell scripting to collect system and authentication logs from `/var/log`. The collected logs are copied into the project directory for analysis. Old logs are compressed automatically to manage storage efficiently.

📸 *Screenshot 4: Collected log files in logs directory*
<img width="1920" height="1080" alt="collected_logs" src="https://github.com/user-attachments/assets/5013b39e-1263-4bc8-99dc-672e51ee0698" />

---

### 6.2 Log Parsing Module

The log parsing module is implemented in Python. It reads multiple log files, extracts individual log entries, and prepares them for threat analysis. The parser ensures compatibility across different Linux distributions.

📸 *Screenshot 5: Python log parser execution*
<img width="1920" height="1080" alt="LogParser" src="https://github.com/user-attachments/assets/c8ca4fd2-3612-44bd-9773-92e35a7c3d7a" />


---

### 6.3 Threat Detection Module

This module contains rule-based detection logic to identify high-risk security threats, including:

* SSH brute-force attacks
* Root SSH login attempts
* Privilege escalation (sudo abuse)
* Account enumeration
* Cron job abuse and persistence
* Log tampering attempts

Each threat is detected by analyzing specific patterns within the log entries.

📸 *Screenshot 6: Threat detection alerts on terminal*
<img width="1920" height="1080" alt="Screenshot From 2026-01-23 00-00-01" src="https://github.com/user-attachments/assets/b40b75d0-e82e-47aa-b44a-4ae524b7269f" />

---

### 6.4 Alerting Module

The alerting module generates real-time alerts with timestamps. Alerts are displayed on the terminal and stored in log files for future reference. This simulates SOC alert handling mechanisms.

📸 *Screenshot 7: alerts.log output file*
<img width="1920" height="1080" alt="ThreatAlert" src="https://github.com/user-attachments/assets/e09c54f9-7eb1-4201-9859-dce467518e74" />


---

## 7. High-Risk Threats Identified

The system can successfully detect the following high-risk threats:

* Brute-force login attacks
* Root account login attempts
* Privilege escalation attempts
* Account enumeration attacks
* Cron job abuse for persistence
* Log tampering activities

---

## 8. Automation and Scheduling

The project includes a scheduler shell script and supports **cron job automation**. This allows the system to run periodically and monitor logs continuously without manual intervention.

📸 *Screenshot 8: Cron job configuration*
<img width="1920" height="1080" alt="Screenshot From 2026-01-23 00-01-46" src="https://github.com/user-attachments/assets/79ebd1b9-d967-4512-af29-021dddd77f43" />

---

## 9. Results and Output

The system produces the following outputs:

* Real-time alerts displayed on the terminal
* Alert logs saved in `alerts.log`
* Security reports for analysis

The alerts help in identifying and responding to security incidents quickly.

📸 *Screenshot 9: Final report output*
<img width="1920" height="1080" alt="Screenshot From 2026-01-23 00-07-45" src="https://github.com/user-attachments/assets/5efea7ec-6770-48df-b4dd-91e9270adbea" />

---

## 10. Advantages of the System

* Automates log monitoring and threat detection
* Lightweight and easy to deploy
* Improves system security visibility
* Enhances understanding of SOC operations

---

## 11. Limitations

* Detection is rule-based
* No visualization dashboard
* Limited to local system logs

---

## 12. Future Enhancements

The project can be further enhanced by:

* Integrating email or messaging alerts
* Adding MITRE ATT&CK mapping
* Implementing machine learning-based anomaly detection
* Developing a web-based dashboard

---

## 13. Conclusion

The **Automated Log Analyzer & Alerting System** demonstrates how Python and Shell scripting can be effectively used to build a SOC-style security monitoring tool. The project successfully automates log analysis, detects high-risk threats, and generates alerts, making it suitable for academic submission and practical cybersecurity learning.

---

## 14. References

* Linux System Logging Documentation
* Python Official Documentation
* MITRE ATT&CK Framework
