# Network Traffic Analysis Using Wireshark

## Project Overview
This project documents my hands-on practice with Wireshark, a network protocol analyzer used to capture and examine network traffic.

The purpose is to develop practical skills relevant to entry-level Security Operations Center (SOC) analysis.

## Objectives
- Capture network traffic in a controlled environment.
- Identify common protocols including DNS, TCP, and HTTP/HTTPS.
- Examine source and destination IP addresses.
- Apply Wireshark display filters to investigate network activity.
- Document observations and distinguish normal from potentially suspicious traffic.

## Tools and Environment
- Wireshark
- Windows laptop
- Web browser (Google Chrome)
- Local network connection

## Investigation Methodology
1. Open Wireshark and select the active network interface.
2. Start a packet capture.
3. Generate test traffic by visiting a website.
4. Stop the capture and inspect the packets.
5. Apply relevant display filters.
6. Record findings with supporting screenshots.

## Analysis and Findings
### Investigation 1: DNS Query and Response Analysis

**Tool:** Wireshark  
**Capture:** baseline.pcapng  
**Filter:** `dns`

#### Findings
- Requested domain: `edge.microsoft.com`
- DNS server: `8.8.8.8`
- Request packet: 4
- Response packet: 5
- DNS answer records: 4 (2 CNAME and 2 A records)
- Resolved IP addresses: `150.171.28.11` and `150.171.27.11`
- Response time: 16.81 milliseconds

#### Security Assessment
The DNS traffic was consistent with normal domain resolution. No malicious activity was established from this transaction alone.
## Screenshots
![DNS Query and Response Analysis](dns%20analysis.png.jpg)
## Lessons Learned
- Learned how to capture and analyze network traffic using Wireshark.
- Used DNS filters to identify domain name queries and responses.
- Identified source and destination IP addresses.
- Examined DNS records, including CNAME and A records.
- Learned how DNS analysis supports SOC investigations and network monitoring.

## Disclaimer
This project is for educational purposes. Network analysis is performed only on traffic I am authorized to capture and inspect.
