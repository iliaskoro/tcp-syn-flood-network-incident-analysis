# TCP SYN Flood Network Traffic Incident Analysis

This repository contains a **cybersecurity incident report** based on network traffic analysis involving a **TCP SYN flood attack**.  
The report documents the investigation of a denial-of-service condition affecting a fictional organization’s web server, using packet-level evidence captured with a network protocol analyzer.

The project focuses on identifying abnormal TCP connection patterns, analyzing the TCP three-way handshake abuse, and documenting the incident in a structured format aligned with real-world SOC and incident response practices.

## Scope

- Analysis of TCP-based network traffic
- Identification of denial-of-service attack patterns
- Interpretation of TCP handshake behavior
- Incident documentation and impact assessment

All IP addresses, systems, and network traffic analyzed in this project are **fictional** and used strictly for educational and portfolio purposes.

## Protocols & Technologies

- **Transmission Control Protocol (TCP)**
  - Three-way handshake analysis
  - SYN, SYN/ACK, ACK packet behavior
  - Half-open connection exhaustion

- **Hypertext Transfer Protocol (HTTP/HTTPS)**
  - Service availability impact
  - HTTP 504 Gateway Time-out errors

- **Tools**
  - Wireshark (network protocol analyzer)

## Incident Analysis Components

### Network Traffic Analysis
- Inspection of TCP SYN packets targeting the web server
- Identification of repeated, high-rate SYN requests from a single external source
- Correlation of abnormal TCP traffic with service degradation

### Findings
- A sustained flood of TCP SYN packets was observed targeting port 443 (HTTPS)
- The attacker failed to complete the TCP three-way handshake consistently
- The web server accumulated a large number of half-open connections
- Legitimate client connections experienced resets and timeouts
- HTTP 504 Gateway Time-out errors were generated as the server became overwhelmed

### Attack Classification
- **Attack Type:** TCP SYN Flood
- **Category:** Denial of Service (DoS)
- **Characteristics:**
  - Single-source origin
  - Resource exhaustion through TCP handshake abuse
  - Loss of service availability for legitimate users

## Project Structure

```
/
├── incident_report_tcp_syn_flood.pdf
├── wireshark_tcp_http_log.xlsx
└── README.md
```


## Project Status

**Complete**

Included deliverables:
- Formal cybersecurity incident report (PDF)
- Packet-level network traffic log captured with Wireshark
- Documented analysis, findings, and incident conclusions

This repository represents a finished incident response and analysis artifact, not a draft or partial investigation.

## Notes

- All domains, IP addresses, and network traffic are fictional.
- IP ranges used align with documentation and non-production standards.
- The report structure and terminology follow real-world SOC and incident response practices.
- The focus of this project is analysis and documentation, not remediation or system hardening.

## Author

Ilias Korompilis

## License

Academic and educational use only