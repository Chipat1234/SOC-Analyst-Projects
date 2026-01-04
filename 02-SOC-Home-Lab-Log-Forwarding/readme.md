# Windows Log Forwarding & Alerting with Splunk

## 📌 Project Overview
This project demonstrates a basic SOC home lab where a Windows endpoint forwards critical security logs to an on-premises Splunk SIEM for centralized monitoring and analysis.  
The goal of this project is to understand how logs are generated at the endpoint level and ingested into a SIEM platform.

---

## 🏗️ Lab Architecture

→ Windows 10 (Victim VM)  
→ Splunk Universal Forwarder  
→ Splunk Enterprise (Host Machine)

---

## 🧰 Tools & Technologies Used
- Splunk Enterprise (SIEM)
- Splunk Universal Forwarder
- Windows 10 Virtual Machine
- VirtualBox / VMware
- Windows Event Viewer

---

## 🔍 Log Sources Configured
Only high-value logs were forwarded to reduce noise:

- **Security Logs**
  - Authentication events (Event ID 4624, 4625)
  - Account activity

- **System Logs**
  - System and service-related events

---

## ⚙️ Configuration Details

### Splunk Universal Forwarder Configuration
The following `inputs.conf` file was used on the Windows endpoint:

[WinEventLog://Security]
disabled = 0

[WinEventLog://System]
disabled = 0


This configuration ensures that Security and System event logs are forwarded to the Splunk Enterprise instance running on the host machine.

---

## ✅ Verification
Log ingestion was verified in Splunk using the following searches:

- Security logs:
index=* source="WinEventLog:Security"

- System logs:

Successful log ingestion confirms correct endpoint-to-SIEM communication.

---

## 📸 Screenshots
Screenshots showing Security and System logs successfully received in Splunk are included in the `screenshots/` directory.

---

## 🎯 Skills Demonstrated
- SOC home lab setup
- Windows Event Log analysis
- Splunk Universal Forwarder configuration
- Log forwarding and ingestion
- SIEM data verification
- Noise reduction through selective logging

---

## 📚 Key Learning Outcome
This project helped me understand how endpoint logs are generated, collected, and centralized in a SIEM environment — a core responsibility of SOC analysts.
