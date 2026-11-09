# Security Incident Investigation Using Splunk and pfSense

## Project Overview

This project demonstrates a simulated cybersecurity incident investigation using Splunk, pfSense, Snort IDS, and Infection Monkey. The objective was to investigate suspicious network activity, identify potential security threats, and evaluate the effectiveness of security monitoring tools in a virtual lab environment.

## Tools and Technologies

- Splunk Enterprise: Security log analysis and investigation using SPL.
- pfSense:Firewall management, network segmentation, and logging.
- Snort IDS: Intrusion detection and security alerts.
- Infection Monkey: Cyberattack simulation and security assessment.
- Linux: Target systems in the simulated environment.

## Investigation Process

1. Verified that Splunk collected 8,084 syslog events from the pfSense environment.
2. Searched Splunk for Snort intrusion detection alerts and identified 338 events.
3. Identified suspicious traffic from 172.31.0.50 targeting multiple Linux machines.
4. Investigated Snort alerts associated with possible Shellshock exploitation attempts (CVE-2014-6271).
5. Correlated security alerts and timestamps to understand the sequence of suspicious activities.
6. Compared Splunk findings with the Infection Monkey security report.

## Key Findings

- Infection Monkey discovered seven open services across four machines.
- Snort detected possible Shellshock exploitation attempts targeting TCP port 80.
- The simulation report confirmed that TargetLinux02 (172.31.0.30) was compromised through a VSFTPD backdoor exploit.
- The available Snort alerts did not independently confirm the successful compromise.
- Additional endpoint monitoring and improved IDS/IPS visibility could strengthen security monitoring.

## Security Recommendations

- Remove or update vulnerable services and disable unnecessary network services.
- Review and update Snort detection rules.
- Improve monitoring visibility within the DMZ network.
- Collect additional Linux endpoint and authentication logs for incident investigation.

## Skills Demonstrated

- Security Information and Event Management (SIEM)
- Splunk Search Processing Language (SPL)
- Security log analysis
- Intrusion Detection Systems (IDS)
- Threat detection and incident investigation
- Event correlation and timeline analysis
- Incident reporting and documentation

## Full Investigation Report

[View Full Security Incident Investigation Report (PDF)](Security%20Incident%20Investigation%20Using%20Splunk.pdf)

## Project Environment

This investigation was conducted in an authorized virtual cybersecurity lab for educational and professional development purposes.
