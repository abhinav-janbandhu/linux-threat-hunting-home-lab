# Linux Threat Hunting Home Lab

> A hands-on Blue Team project focused on Linux threat hunting, incident response, and attacker behavior simulation using Kali Linux, Ubuntu Server, and Auditd.

---

## Project Overview

This repository documents a practical Linux Threat Hunting Home Lab built to simulate real-world attacker techniques and investigate them from a defender's perspective.

Across ten structured labs (Labs 21–30), I simulated activities such as persistence, credential discovery, data staging, and exfiltration, then analyzed the resulting evidence using Linux Auditd and mapped each activity to the MITRE ATT&CK framework.

The primary objective of this project was to strengthen practical Blue Team skills in:

- Threat Hunting
- Incident Response
- Linux Security Monitoring
- MITRE ATT&CK Mapping
- Attack Timeline Reconstruction
- Security Investigation

Rather than focusing only on offensive commands, each lab emphasizes how defenders can detect, investigate, and understand attacker behavior.

---

## Lab Environment

| Component | Technology |
|-----------|------------|
| Host OS | Windows 11 |
| Hypervisor | Oracle VirtualBox |
| Attacker VM | Kali Linux |
| Target VM | Ubuntu Server |
| Monitoring | Linux Auditd |
| Investigation | ausearch, aureport |
| Framework | MITRE ATT&CK |

---


## Lab Architecture

```text
                    Home Lab Environment

                    +-------------------+
                    |   Windows 11 Host |
                    |   Oracle VirtualBox|
                    +---------+---------+
                              |
             +----------------+----------------+
             |                                 |
     +-------+--------+               +--------+-------+
     |  Kali Linux    |               | Ubuntu Server  |
     | (Attacker VM)  |<------------->| (Target VM)    |
     +----------------+               +----------------+
                                              |
                                              |
                                      +-------+-------+
                                      |    Auditd     |
                                      | Linux Audit   |
                                      +-------+-------+
                                              |
                                              |
                                      +-------+-------+
                                      | Threat Hunting|
                                      | Investigation |
                                      +---------------+
```
---

## Tools Used

| Category | Tools |
|----------|-------|
| Operating Systems | Windows 11, Ubuntu Server, Kali Linux |
| Virtualization | Oracle VirtualBox |
| Monitoring | Linux Auditd |
| Investigation | ausearch, aureport |
| Networking | SSH, Nmap |
| Framework | MITRE ATT&CK |
---

## Labs Completed

| Lab    | Title                                      | Primary Skill               |
| ------ | ------------------------------------------ | --------------------------- |
| Lab 21 | Incident Investigation Workflow            | Incident Investigation      |
| Lab 22 | Hypothesis-Driven Threat Hunting           | Threat Hunting              |
| Lab 23 | Cron Persistence Hunting                   | Linux Persistence           |
| Lab 24 | SSH Persistence Hunting                    | SSH Security                |
| Lab 25 | Lateral Movement & Network Discovery       | Discovery & Enumeration     |
| Lab 26 | Credential Access & Sensitive Data Hunting | Credential Access Detection |
| Lab 27 | Data Staging & Collection Hunting          | Data Collection & Staging   |
| Lab 28 | Exfiltration Detection Concepts            | Exfiltration Detection      |
| Lab 29 | End-to-End Attack Chain Simulation         | Attack Chain Analysis       |
| Lab 30 | Blue Team Capstone Investigation           | Incident Response           |


---

## Technical Skills Demonstrated

### Threat Hunting

- Hypothesis-driven threat hunting
- Linux audit log analysis
- Attack timeline reconstruction
- Threat investigation

### Linux Security

- Auditd configuration
- Command execution monitoring
- Persistence detection
- SSH security analysis

### Incident Response

- Evidence collection
- Root cause analysis
- Indicators of Compromise (IOCs)
- MITRE ATT&CK mapping

### Blue Team Operations

- Credential access hunting
- Data collection detection
- Exfiltration investigation
- Attack chain reconstruction

---

## MITRE ATT&CK Coverage

| Tactic | Techniques Practiced |
|---------|----------------------|
| Discovery | System Discovery, Network Discovery |
| Persistence | Cron Jobs, SSH Authorized Keys |
| Credential Access | Unsecured Credentials |
| Collection | Local Data Collection, Archive Creation |
| Exfiltration | Data Movement & Exfiltration Concepts |

---

## Repository Structure

```text
linux-threat-hunting-home-lab/
│
├── Lab21-Incident-Investigation/
├── Lab22-Threat-Hunting/
├── Lab23-Cron-Persistence/
├── Lab24-SSH-Persistence/
├── Lab25-Lateral-Movement/
├── Lab26-Credential-Access/
├── Lab27-Data-Staging/
├── Lab28-Exfiltration/
├── Lab29-Attack-Chain/
├── Lab30-Capstone-Investigation/
└── screenshots/
```
---

## Key Outcomes

- Built and documented a Linux Threat Hunting home lab.
- Simulated attacker behavior across multiple MITRE ATT&CK tactics.
- Investigated persistence, credential access, collection, and exfiltration activities.
- Reconstructed attack timelines using Linux Auditd.
- Produced structured incident investigation documentation for every lab.


---

## About Me

I'm a cybersecurity professional focused on Blue Team operations, threat hunting, detection engineering, and security leadership.

This project is part of my continuous learning journey to strengthen hands-on defensive security skills through practical home lab simulations.
