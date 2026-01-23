# PCAP Traffic Analysis Report

## Overview
This project focuses on analyzing a packet capture (PCAP) file to understand network traffic behavior from a SOC analyst perspective. The traffic was captured in a controlled lab environment and analyzed using Wireshark.

## Data Collection
- PCAP captured using `tcpdump` on Kali Linux
- Traffic was intentionally generated using:
  - HTTP requests (`curl`)
  - ICMP echo requests (`ping`)

## Protocol Analysis
Using the Protocol Hierarchy feature in Wireshark, the following protocols were identified:
- Ethernet
- IPv4
- TCP
- HTTP
- ICMP
- DNS

This indicates standard client-server communication and basic network activity.

## HTTP Traffic Analysis
Filtered HTTP traffic showed:
- HTTP GET requests to `example.com` and `neverssl.com`
- Clear-text HTTP communication
- Standard User-Agent headers

This demonstrates how unencrypted HTTP traffic can be inspected and analyzed at the packet level.

## ICMP Traffic Analysis
ICMP echo request and reply packets were observed between the source and destination hosts. This confirms successful connectivity testing and normal ICMP behavior.

## Conclusion
This project demonstrates essential SOC analyst skills, including packet inspection, protocol identification, and traffic analysis using Wireshark. The ability to analyze PCAP files is critical for detecting suspicious activity and supporting incident investigations.

