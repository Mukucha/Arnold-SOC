# Hello, I'm Arnold Mukucha
[![LinkedIn](https://img.shields.io/badge/-LinkedIn-0072b1?&style=for-the-badge&logo=linkedin&logoColor=white)](https://pl.linkedin.com/in/arnold-mukucha-8475a9203)

I am a Computer Engineering graduate with a strong interest in **networking, cloud computing, and information security**. I hold the **Azure Administrator Associate**, **Cisco Certified Network Associate (CCNA)**, and **CompTIA Security+** certifications, reflecting a solid foundation in cloud administration, cybersecurity, and networking technologies.

I have hands-on experience with **Azure and AWS, Linux and Windows system administration, virtualization, and system monitoring**, and practical knowledge of **relational databases** including installation, configuration, performance tuning, backup, and optimization.

I am familiar with the **MITRE ATT&CK framework**, information security best practices, and application security testing concepts. I also have foundational knowledge of **Artificial Intelligence and Machine Learning**, including basic algorithms and practical applications.

I am committed to **continuous learning** and building **secure, scalable, and compliant IT and cloud environments**.

---

## 🎯 Objective

To leverage my skills in **networking, cloud administration, and information security** to contribute to building **secure and reliable IT infrastructures** while gaining hands-on experience in **cybersecurity monitoring and threat detection**.

---

## 🛠 Skills

| Skill | Associated Project |
|-------|------------------|
| SIEM Implementation and Log Analysis | [Malware Detection Lab](https://github.com/YOUR_USERNAME/malware-detection-lab-splunk) |
| Network Traffic Monitoring and Attack Detection | [Malware Detection Lab](https://github.com/YOUR_USERNAME/malware-detection-lab-splunk) |
| Endpoint Monitoring and Telemetry Analysis | [Malware Detection Lab](https://github.com/YOUR_USERNAME/malware-detection-lab-splunk) |
| Threat Detection using SIEM | [Malware Detection Lab](https://github.com/YOUR_USERNAME/malware-detection-lab-splunk) |
| Cyber Kill Chain Analysis | [Malware Detection Lab](https://github.com/YOUR_USERNAME/malware-detection-lab-splunk) |

---

## 🧰 Tools

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

## Project: Malware Detection Lab using Splunk, Sysmon, and Metasploit

### Overview
This lab demonstrates a **malware attack simulation and detection workflow** in a virtual environment. A malicious payload is created using `msfvenom` and executed on a Windows VM. System telemetry is captured using **Sysmon** and analyzed with **Splunk SIEM**.

**Goal:** Simulate real-world attack behavior and detect malicious activity using SIEM and log-based analysis.

---

### Lab Architecture

- **Attacker Machine:** Kali Linux  
- **Target Machine:** Windows 10  
- **Monitoring Tool:** Sysmon  
- **SIEM:** Splunk  

**Attack Flow:**
```text
Kali Linux (Attacker)
        ↓
   Malware Payload
        ↓
Windows 10 VM (Victim)
        ↓
    Sysmon Logs
        ↓
     Splunk SIEM
