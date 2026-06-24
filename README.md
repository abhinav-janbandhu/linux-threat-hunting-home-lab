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

# Lab Environment

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

# Lab Architecture

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
