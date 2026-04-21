# Advanced Nmap Recon and Service Enumeration Lab

## Overview
This project demonstrates advanced network reconnaissance using Nmap on Kali Linux.  
The goal was to identify live hosts, discover open ports, detect running services and versions, infer operating system details, and document the exposure in a professional security report format.

## Objectives
- Perform host discovery on authorized targets.
- Identify open TCP ports using multiple scan techniques.
- Enumerate services and versions.
- Attempt OS fingerprinting.
- Use NSE default scripts for deeper enumeration.
- Document findings and security implications clearly.

## Scope
This lab was performed only on systems I owned or had explicit authorization to scan.  
No intrusive exploitation or unauthorized activity was performed.

## Tools Used
- Kali Linux
- Nmap
- Terminal
- Screenshot tool
- Markdown documentation

## Lab Methodology
1. Performed host discovery to confirm the target was online.
2. Ran a SYN scan to identify exposed TCP ports.
3. Expanded the scan to the full port range for better coverage.
4. Used version detection to identify services and software versions.
5. Ran OS fingerprinting to estimate the target operating system.
6. Executed default NSE scripts to gather additional context.
7. Saved all output files and screenshots for reporting.

## Commands Used
```bash
nmap -sn <target>
sudo nmap -sS <target>
sudo nmap -p- <target>
sudo nmap -sS -sV <target>
sudo nmap -O <target>
sudo nmap -sC -sV <target>
sudo nmap -sS -sV -sC -O <target> -oA advanced_recon
```

## Findings Summary
- Host discovery confirmed the target was reachable.
- SYN scanning revealed open TCP services.
- Version detection identified service banners and probable software versions.
- OS fingerprinting suggested the target operating system.
- NSE scripts returned additional service information useful for assessment.

## Sample Risk Observations
- Exposed SSH services should be restricted and protected with key-based authentication.
- Web services should be reviewed for unnecessary public exposure.
- Database or file-sharing ports should only be accessible from trusted networks.
- Any unnecessary service should be disabled or firewalled.

## Evidence Collected
- Nmap output files in normal, XML, and grepable formats.
- Screenshots of host discovery, service detection, and OS fingerprinting.
- Written notes explaining scan results and findings.

## Repository Structure
```text
advanced-nmap-recon-lab/
│── README.md
│── scans/
│   ├── advanced_recon.nmap
│   ├── advanced_recon.xml
│   └── advanced_recon.gnmap
│── screenshots/
│   ├── host-discovery.png
│   ├── syn-scan.png
│   ├── service-versions.png
│   ├── os-detection.png
│   └── final-scan.png
│── report/
│   └── findings.md
│── notes/
│   ├── commands-used.md
│   └── scope-and-ethics.md
```

## Skills Demonstrated
- Network reconnaissance
- Host discovery
- Port scanning
- Service enumeration
- OS fingerprinting
- Security documentation
- Exposure analysis

## Conclusion
This project improved my ability to perform structured reconnaissance and interpret scan results like a junior cybersecurity analyst.  
It also helped me understand how exposed services, version data, and OS fingerprints contribute to attack surface analysis.

## Future Improvements
- Add targeted NSE scripts for deeper enumeration.
- Compare results across multiple hosts.
- Create a risk matrix for exposed services.
- Add remediation recommendations for each finding.
