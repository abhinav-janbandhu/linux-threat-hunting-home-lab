# Linux Threat Hunting Home Lab

> A practical Blue Team home lab that simulates the complete Linux attack lifecycle—from reconnaissance and persistence to credential access, data staging, and exfiltration—while demonstrating how defenders detect, investigate, and map attacker behavior using Linux Auditd and the MITRE ATT&CK framework.

![Blue Team](https://img.shields.io/badge/Role-Blue%20Team-blue)
![Platform](https://img.shields.io/badge/Platform-VirtualBox-blue)
![OS](https://img.shields.io/badge/Linux-Ubuntu%20%7C%20Kali-green)
![Security](https://img.shields.io/badge/Focus-Threat%20Hunting-red)
![Framework](https://img.shields.io/badge/MITRE-ATT%26CK-orange)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen)
![License](https://img.shields.io/badge/License-MIT-yellow)

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

## Table of Contents

- [Linux Threat Hunting Home Lab](#linux-threat-hunting-home-lab)
  - [Project Overview](#project-overview)
  - [Table of Contents](#table-of-contents)
  - [Project Highlights](#project-highlights)
  - [Project Metrics](#project-metrics)
  - [Project Goals](#project-goals)
  - [Lab Environment](#lab-environment)
  - [Threat Hunting Lab Architecture](#threat-hunting-lab-architecture)
  - [Tools Used](#tools-used)
  - [| Framework | MITRE ATT\&CK |](#-framework--mitre-attck-)
  - [Labs Completed](#labs-completed)
  - [Skills Gained](#skills-gained)
  - [MITRE ATT\&CK Coverage](#mitre-attck-coverage)
  - [Repository Structure](#repository-structure)
  - [Key Outcomes](#key-outcomes)
  - [Learning Outcomes](#learning-outcomes)
  - [Future Enhancements](#future-enhancements)
  - [Portfolio](#portfolio)
  - [Final Thoughts](#final-thoughts)

---

## Project Highlights

- 🔍 Simulated a complete Linux attack lifecycle across 10 structured labs.
- 🛡️ Performed hypothesis-driven threat hunting using Linux Auditd.
- 🔐 Investigated persistence techniques including Cron Jobs and SSH Authorized Keys.
- 🔎 Simulated credential discovery, data staging, and exfiltration scenarios.
- 📊 Mapped attacker behavior to the MITRE ATT&CK framework.
- 📝 Produced investigation reports and documented findings for every lab.

---

## Project Metrics

| Metric | Value |
|--------|------:|
| Hands-on Labs Completed | 10 |
| Investigation Reports | 10 |
| Linux VMs | 2 (Kali Linux & Ubuntu Server) |
| MITRE ATT&CK Tactics Covered | 5 |
| MITRE ATT&CK Techniques Demonstrated | 8+ |
| Investigation Screenshots | 20+ |
| Attack Lifecycle | End-to-End |
| Documentation | 100% Complete |

---

## Project Goals

This project was designed to:

- Build practical Linux threat hunting skills.
- Simulate realistic attacker behavior in a controlled environment.
- Develop incident investigation and evidence collection workflows.
- Practice mapping attacker techniques to the MITRE ATT&CK framework.
- Improve Blue Team documentation and reporting skills.
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


## Threat Hunting Lab Architecture

```text
         Linux Threat Hunting Home Lab

           Windows 11 Host (VirtualBox)
                     │
      ┌──────────────┴──────────────┐
      │                             │
┌──────────────┐             ┌──────────────┐
│ Kali Linux   │──────────▶  │ Ubuntu Server│
│ Attacker VM  │   Attack    │  Target VM   │
└──────────────┘             └──────┬───────┘
                                    │
                              Linux Auditd
                                    │
                         Threat Hunting & Detection
                                    │
                        Incident Investigation
                                    │
                         MITRE ATT&CK Mapping
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

| Lab | Documentation | Primary Skill |
|-----|---------------|---------------|
| Lab 21 | [Incident Investigation Workflow](Lab21-Incident-Investigation/) | Incident Investigation |
| Lab 22 | [Hypothesis-Driven Threat Hunting](Lab22-Threat-Hunting/) | Threat Hunting |
| Lab 23 | [Cron Persistence Hunting](Lab23-Cron-Persistence/) | Linux Persistence |
| Lab 24 | [SSH Persistence Hunting](Lab24-SSH-Persistence/) | SSH Security |
| Lab 25 | [Lateral Movement & Network Discovery](Lab25-Lateral-Movement/) | Discovery & Enumeration |
| Lab 26 | [Credential Access & Sensitive Data Hunting](Lab26-Credential-Access/) | Credential Access Detection |
| Lab 27 | [Data Staging & Collection Hunting](Lab27-Data-Staging/) | Data Collection & Staging |
| Lab 28 | [Exfiltration Detection Concepts](Lab28-Exfiltration/) | Exfiltration Detection |
| Lab 29 | [End-to-End Attack Chain Simulation](Lab29-Attack-Chain/) | Attack Chain Analysis |
| Lab 30 | [Blue Team Capstone Investigation](Lab30-Capstone-Investigation/) | Incident Response |


---

## Skills Gained

| Domain | Skills |
|---------|--------|
| Linux Security | Auditd, SSH, Cron, Linux Administration |
| Threat Hunting | Hypothesis Development, Log Analysis, IOC Identification |
| Incident Response | Evidence Collection, Timeline Reconstruction |
| Detection | Command Monitoring, Persistence Detection |
| Frameworks | MITRE ATT&CK |
| Documentation | Technical Reporting, Investigation Documentation |

---

## MITRE ATT&CK Coverage

| ATT&CK Tactic | Techniques Practiced |
|--------------|----------------------|
| Discovery | T1033 – Account Discovery, T1082 – System Information Discovery |
| Persistence | T1053.003 – Cron, T1098.004 – SSH Authorized Keys |
| Credential Access | T1552 – Unsecured Credentials |
| Collection | T1074 – Data Staged, T1560.001 – Archive via Utility |
| Exfiltration | T1020 – Automated Exfiltration |

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

## Learning Outcomes

Through this project, I strengthened practical experience in:

- Linux Threat Hunting
- Incident Response Methodology
- Security Investigation
- Linux Auditd Monitoring
- Attack Timeline Reconstruction
- MITRE ATT&CK Mapping
- Blue Team Documentation
- Security Reporting
---


## Future Enhancements

The next phase of this home lab will focus on Cloud & Platform Security, including:

- AWS IAM Security
- CloudTrail Log Analysis
- Amazon GuardDuty
- S3 Security Monitoring
- Cloud Threat Hunting
- Detection Engineering
- Security Automation

---
## Portfolio

This project is part of my cybersecurity learning journey focused on:

- Blue Team Operations
- Detection Engineering
- Threat Hunting
- Security Architecture
- Cloud Security
- Executive Cybersecurity Leadership
  
  More projects will be added as the journey progresses.

---

## Final Thoughts

This project strengthened my practical understanding of Linux threat hunting, incident response, and attacker behavior analysis. Every lab was performed in a self-built home lab and documented to reinforce both technical skills and professional reporting.

I hope this repository is useful to others who are learning Linux security and Blue Team operations.