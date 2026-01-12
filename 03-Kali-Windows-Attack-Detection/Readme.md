# Kali Linux Brute-Force Attack Detection on Windows using Splunk

## Project Overview

This project demonstrates a real-world SOC analyst scenario where a Linux-based attacker attempts unauthorized access against a Windows machine. Failed authentication attempts are detected and analyzed using Splunk SIEM.

## Lab Setup

* Attacker Machine: Kali Linux
* Victim Machine: Windows 10 (VM)
* SIEM: Splunk Enterprise (installed on host)
* Network: VirtualBox internal/host-only network

## Attack Simulation

* SMB authentication attempts were made from Kali Linux using invalid credentials.
* Tools used:

  * smbclient
  * xfreerdp

## Detection & Analysis

* Windows Security logs (Event ID 4625) were forwarded to Splunk.
* Splunk query used to detect brute-force attempts:

```
index=main EventCode=4625
| stats count by Account_Name, Source_Network_Address
| where count > 3
```

## Key Findings

* Multiple failed login attempts detected from Kali IP.
* Logon Type 3 confirmed network-based authentication attempts.
* Attacker IP successfully identified in Splunk.

## Skills Demonstrated

* Windows Event Log analysis
* Brute-force attack detection
* Splunk SPL queries
* SOC investigation workflow
* Attacker–defender lab setup

## Outcome

This project simulates real SOC monitoring and incident detection workflows used in enterprise environments.
