Date:16/12/25

Alert Name:
Multiple Failed Login Attempts Detected

Severity:
Medium

Description:
The SIEM generated an alert after detecting multiple failed login attempts on a Windows system, indicating a potential brute-force attack.

Detection Source:
Splunk SIEM – Windows Security Event Logs

Event Details:
Event ID: 4625

Log Source: WinEventLog:Security

Affected Account: Chipat

Analysis: Multiple failed authentication attempts were observed within a short time window. The activity was manually generated for testing purposes to validate alert functionality.

Impact: No successful compromise detected.

Response Taken: Alert reviewed

Activity verified as test event

No further action required

Lessons Learned: Failed login detection alerts are effective for identifying brute-force attempts and validating SIEM monitoring.