<div align="center">

# 🦉 OArpX

**Network Intelligence Scanner**

![Linux](https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black)
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)

*Part of the [OwlSec](https://owlsec.org) Toolkit*
```
██████╗  █████╗ ██████╗ ██████╗ ███████╗██╗   ██╗███████╗
██╔═══██╗██╔══██╗██╔══██╗██╔══██╗██╔════╝╚██╗ ██╔╝██╔════╝
██║   ██║███████║██████╔╝██████╔╝█████╗   ╚████╔╝ █████╗  
██║   ██║██╔══██║██╔══██╗██╔═══╝ ██╔══╝    ╚██╔╝  ██╔══╝  
╚██████╔╝██║  ██║██║  ██║██║     ███████╗   ██║   ███████╗
 ╚═════╝ ╚═╝  ╚═╝╚═╝  ╚═╝╚═╝     ╚══════╝   ╚═╝   ╚══════╝
        ARP · OS Fingerprint · Ports · Live Monitor
```

</div>

---

## 📌 Overview

**OArpX** is a LAN network intelligence scanner. It uses ARP to discover live hosts, fingerprints operating systems via TTL/TCP window analysis, and probes common ports — all from a single terminal interface.

> ⚠️ Requires **root** privileges for ARP and raw socket operations.

---

## 🖥️ Menu Options

| Option | Name | Description |
|--------|------|-------------|
| `[1]` | Quick Scan | ARP ping entire subnet |
| `[2]` | Deep Scan | ARP + OS fingerprint + port probe |
| `[3]` | Live Monitor | Continuous ARP watcher |
| `[4]` | Device Detail | Inspect a specific IP/MAC |
| `[5]` | Conflict Check | Detect IP/ARP spoofing |
| `[6]` | Export Results | Save last scan to JSON/CSV |
| `[H]` | Help | Show help page |
| `[0]` | Exit | Quit the tool |

---

## 🧠 OS Fingerprint Methods

| Method | Details |
|--------|---------|
| **TTL Heuristic** | `64` = Linux/macOS · `128` = Windows · `255` = Network device |
| **TCP Window** | Identifies OS family from TCP window size |
| **ICMP** | Type/code pattern analysis |

---

## 🔴 Risk Scoring

| Score | Level | Meaning |
|-------|-------|---------|
| `0.0 – 0.3` | 🟢 Low | Normal host |
| `0.3 – 0.6` | 🟡 Medium | Open sensitive ports |
| `0.6 – 1.0` | 🔴 High | Router/gateway or many open ports |

---

## ⚙️ Requirements

- Linux (any distro)
- Root privileges required
- The tool is pre-built — no Python installation needed

---

## ⚠️ Legal Disclaimer

> **THIS TOOL IS FOR EDUCATIONAL AND AUTHORIZED AUDIT PURPOSES ONLY.**  
> Unauthorized scanning of networks is illegal.  
> The developer is not responsible for any misuse.

---

## 📦 Part of OwlSec Toolkit

This tool is part of the **OwlSec** suite — a collection of 300+ security and privacy tools.

> 🔗 [owlsec.org](https://owlsec.org)

---

## ©️ License

MIT License — © Khaled S. Haddad

*Tools are distributed as pre-built executables. Source code is proprietary.*
