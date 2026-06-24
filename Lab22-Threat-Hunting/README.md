# Lab 22 – Hypothesis-Driven Threat Hunting

## Objective

Perform a hypothesis-driven threat hunt to determine whether an attacker executed reconnaissance commands on a compromised Linux system.

---

## Hunting Hypothesis

An attacker who gains access to a Linux server will perform reconnaissance activities to understand the environment before taking further actions.

---

## Lab Environment

| Component | Technology |
|----------|------------|
| Attacker | Kali Linux |
| Target | Ubuntu Server |
| Monitoring | Linux Auditd |
| Investigation | ausearch |
| Framework | MITRE ATT&CK |

---

## Attack Simulation

After establishing SSH access to the Ubuntu server, the following reconnaissance commands were executed:

```bash
whoami
hostname
id
```


---

## Threat Hunting

Initially, no command execution telemetry was available because Auditd had no active monitoring rules.

Verified using:

```bash
sudo auditctl -l
```

A command execution monitoring rule was then configured:

```bash
sudo auditctl -a always,exit -F arch=b64 -S execve -k command_exec
```

Evidence was collected using:

```bash
sudo ausearch -k command_exec --raw
```

---

## Evidence Collected

Auditd successfully captured execution of:

- `whoami`
- `hostname`
- `id`


This validated that command execution telemetry was being recorded successfully.

---

## MITRE ATT&CK Mapping

| Activity | Technique |
|----------|-----------|
| Account Discovery | T1033 |
| System Information Discovery | T1082 |

---

## Detection Opportunities

- Monitor Linux command execution using Auditd.
- Detect reconnaissance commands executed immediately after login.
- Identify abnormal use of system discovery utilities.
- Correlate command execution with SSH login events.

---

## Key Findings

- The initial threat hunt exposed a telemetry gap.
- Auditd monitoring was configured to capture command execution events.
- Reconnaissance commands were successfully detected.
- The hunting hypothesis was validated using Linux audit logs.

---

## Skills Demonstrated

- Threat Hunting
- Linux Auditd
- Command Execution Monitoring
- Log Analysis
- MITRE ATT&CK Mapping
