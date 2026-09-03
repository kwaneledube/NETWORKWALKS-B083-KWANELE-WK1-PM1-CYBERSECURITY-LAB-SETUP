# 🔐 Cybersecurity Lab Environment Setup

**Building an isolated virtual lab for penetration testing, SOC analysis, and ethical hacking practice**

![Skill](https://img.shields.io/badge/Skill-Cybersecurity-red)
![Ver](https://img.shields.io/badge/Ver-VirtualBox_v7.2-blue)
![OS](https://img.shields.io/badge/OS-Kali_Linux_2026.2-557C94?logo=kalilinux)
![Skill](https://img.shields.io/badge/Skill-Linux-green)
![Network](https://img.shields.io/badge/Network-10.0.0.0%2F24-orange)
![Type](https://img.shields.io/badge/Type-Penetration_Testing-critical)
![Skill](https://img.shields.io/badge/Skill-SOC_Blue_Team-blue)
![Skill](https://img.shields.io/badge/Skill-GRC-green)
![Skill](https://img.shields.io/badge/Skill-Virtualization-9cf)
![Org](https://img.shields.io/badge/Org-NetworkWalks-black)

---

## 📌 Project Overview

This project focuses on setting up a **virtual cybersecurity and penetration-testing laboratory** using VirtualBox and Kali Linux.

The purpose of the lab is to create a controlled environment where cybersecurity tools, network scanning, reconnaissance, vulnerability assessment, and defensive monitoring activities can be performed safely and repeatedly.

The lab is configured on a private virtual network so that additional machines can be added later and used as targets for authorized security testing, SOC practice, and governance review.

---

## 🎯 Objectives

The main objectives of this project are to:

- Install and configure VirtualBox.
- Install/import Kali Linux as a virtual machine.
- Create a private **NAT Network** for the cybersecurity lab.
- Configure network connectivity for Kali Linux.
- Assign a consistent IP address to the Kali VM.
- Verify network connectivity and DNS resolution.
- Take a clean VM snapshot for recovery.
- Document the complete setup process.
- Prepare the environment for future cybersecurity projects across PT, SOC, and GRC tracks.

---

## 🛡️ Purpose of the Lab

The lab provides an isolated and controlled environment for cybersecurity learning and authorized security testing.

It can be used for activities such as:

- Network reconnaissance
- Port scanning
- Vulnerability assessment
- Packet analysis
- Web security testing
- Exploitation practice
- Security-tool experimentation
- Log and traffic monitoring (SOC practice)
- Risk assessment documentation (GRC practice)

⚠️ **Important:** This laboratory must only be used for systems that you own or have explicit permission to test. Do not use the lab or its tools to attack unauthorized systems.

---

## 🏗️ Lab Architecture

![Lab Architecture Diagram](screenshots/lab-architecture.png)

*Main OS: Windows 10 | Hypervisor: VirtualBox | Network: NATNetwork (10.0.0.0/24)*

| Machine | Role | IP Address | Network |
|---|---|---|---|
| **Kali Linux** | Attacker / Analyst | `10.0.0.2/24` | NAT Network |
| **Windows 11** | Target | `10.0.0.11/24` | NAT Network |
| **Windows 10** | Target | `10.0.0.10/24` | NAT Network |
| **Windows 7** | Target (Optional) | `10.0.0.7/24` | NAT Network |
| **Server 2016** | Target (Optional) | `10.0.0.16/24` | NAT Network |
| **Android** | Mobile Target (Optional) | `10.0.0.9/24` | NAT Network |

Additional target machines can be added to the same virtual network in future projects.

---

## ⚙️ Lab Configuration

| 🧩 Component | ⚙️ Configuration |
|---|---|
| 🖥️ Host OS | Windows 10 Home Single Language 22H2 |
| 🧠 Host RAM | 8 GB DDR3 |
| ⚡ Processor | Intel Core i5-3320M @ 2.60 GHz (2C/4T) |
| 💾 Storage | 466 GB HDD (Toshiba) — ~220 GB free |
| 🎮 Graphics | Intel HD Graphics 4000 (32 MB) |
| 🧰 Hypervisor | VirtualBox 7.2 |
| 🐉 Security OS | Kali Linux 2026.2 |
| 🧠 Kali RAM | 2048 MB |
| 🖥️ Target VM RAM | 2048 MB (Windows 10) |
| 🌐 Virtual Network | NAT Network |
| 📡 Network Address | 10.0.0.0/24 |
| 🐧 Kali IP Address | 10.0.0.2/24 |
| 🚪 Default Gateway | 10.0.0.1 |
| 🌍 DNS Server | 8.8.8.8 |

&gt; ⚠️ **Hardware Note:** This lab runs on a Lenovo ThinkPad T430 (2012-era hardware) with 8 GB RAM and a dual-core CPU. Due to hardware constraints, target VMs are tested **individually** rather than all running simultaneously. The lab is fully functional for sequential testing and learning.

---

## 🪜 Lab Setup Procedure

## Step 1. Install 7-Zip

7-Zip was installed to extract the Kali Linux virtual-machine package, which may be distributed as a `.7z` archive.

**Tool:** 7-Zip  
**Download:** [https://7-zip.org/download.html](https://7-zip.org/download.html)

---

## Step 2. Install VirtualBox

VirtualBox was installed as the hypervisor.

**Download:** [https://virtualbox.org/wiki/Downloads](https://virtualbox.org/wiki/Downloads)  
**Version:** VirtualBox 7.2 with Extension Pack

---

## Step 3. Create the NAT Network

A dedicated NAT Network was created in VirtualBox.

**Configuration:**
