# pIDS-homelab: Raspberry Pi 5 Detection Engineering Lab

A home lab that captures real attacker activity and turns it into tested detection rules.
A Raspberry Pi 5 runs a honeypot (Cowrie) to attract attackers and a network IDS (Suricata) to watch traffic. I analyze what attackers do, then write and test my own detection rules mapped to MITRE ATT&CK.

## Pipeline
Internet attackers → Cowrie honeypot (isolated) → Suricata IDS → Logs / dashboard → My detection rules (Suricata + Sigma) → Tested, tuned, mapped to ATT&CK

## Goals
- Collect real attack data from an isolated honeypot
- Monitor network traffic with Suricata
- Write custom Suricata and Sigma detection rules based on observed attacks
- Test every rule and record results
- Map detections to MITRE ATT&CK
- Automate reporting with Python
- Document every step

## Project phases
- [ ] Phase 0: Plan and baseline
- [ ] Phase 1: Harden the Pi and install Suricata
- [ ] Phase 2: Deploy Cowrie honeypot (Docker, isolated)
- [ ] Phase 3: Logging and dashboard
- [ ] Phase 4: Detection engineering (write, test, tune rules)
- [ ] Phase 5: Analysis and reporting (attack report, Python automation)
- [ ] Phase 6: Publish final write-up

## Repo layout
| Folder | Contents |
| --- | --- |
| `journal/` | One dated entry per work session |
| `docs/` | Design decisions and research |
| `configs/` | Suricata, Cowrie and Docker configs (secrets removed) |
| `rules/suricata/` | Custom Suricata rules |
| `rules/sigma/` | Custom Sigma rules |
| `reports/` | Attack analysis reports |
| `tickets/` | Alert triage write-ups |
| `scripts/` | Python automation |
| `screenshots/` | Evidence, named by date and topic |

## Tools
Raspberry Pi 5 · Suricata · Cowrie · Docker · Sigma · MITRE ATT&CK · Python · GitHub

## Safety
The honeypot is isolated from my home network. No malware samples, passwords, IP addresses or private data are published in this repo.

## Status
Phase 0: planning. Started November 2026.
