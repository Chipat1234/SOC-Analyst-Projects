📌 Objective
* To monitor Windows Security Event Logs using Splunk SIEM and detect suspicious authentication activity through alerting.


🛠 Tools Used
* Splunk Enterprise
* Windows Security Event Logs


🔍 Data Source
* WinEventLog:Security
* Event IDs: 4624 (Successful Login), 4625 (Failed Login)


🚨 Detection Logic
* An alert was created to detect multiple failed login attempts that may indicate brute-force activity.


📊 Outcome
* Successfully ingested Windows event logs into Splunk
* Detected failed login attempts
* Triggered and validated a SOC alert
* Documented the incident using an incident report


📁 Files Included
* incident report.md
* screenshots (Splunk dashboard, alerts, log searches)
