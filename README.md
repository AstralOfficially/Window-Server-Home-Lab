# Window-Server-Home-Lab
Active Directory DS deployment, Group Policy enforcement, and telemetry logging lab

## Environment & Tools Used
* **Operating Systems:** Windows Server 2025, Windows 10/11, Ubuntu Linux
* **Security Tools:** Microsoft Defender, Wireshark, Splunk / Wazuh SIEM
* **Networking & Protocols:** TCP/IP, DNS, DHCP, Active Directory Domain Services (AD DS)
* **Frameworks Aligned:** NIST CSF, CIA Triad

## Architecture & Lab Topology
# 🛡️ Active Directory & Windows Server Security Homelab

## 📌 Overview
This project documents the deployment, configuration, and hardening of a virtualized **Active Directory Domain Services (AD DS)** environment. Built from scratch using Windows Server 2025, this lab simulates an enterprise network to practice identity and access management (IAM), Group Policy Object (GPO) security baselines, PowerShell automation, and centralized telemetry collection.

---

## Screeshots
![Static IP Configuration](Static%20IP.png)

## Frequently Asked Questions (FAQ)

### Key Concepts

<details>
<summary><b>Why promote a server to a Domain Controller?</b></summary>
<br>
Promoting a server to a Domain Controller is a pivotal step in establishing centralized network administration and security management. Key benefits include:<br>
* **Centralized Identity & Access Management (IAM):** Transforms the server into the central authority for authenticating identities and managing access across the entire network.<br>
* **Domain Creation & Security:** Creates a domain—a logical grouping of resources—providing a secure, unified environment to manage users, endpoints, and network assets.<br>
* **Core Infrastructure Integration:** Establishes the necessary foundation for enterprise features, including **DNS integration**, **Group Policy Management (GPO)**, and **Active Directory Federation Services (AD FS)**.
---
</details>

## 📐 Architecture & Topology

```text
               +-------------------------------------------------+
               |             Internal Virtual Network            |
               +-------------------------------------------------+
                                        |
                 +----------------------+----------------------+
                 |                                             |
  +------------------------------+              +------------------------------+
  |  Windows Server 2025 DC      |              |  Windows 10/11 Workstation   |
  |  Hostname: DC-01             |              |  Hostname: WS-01             |
  |  IP: 192.168.1.10 /24        |              |  IP: DHCP (192.168.10.100+)  |
  |  Roles: AD DS, DNS, DHCP     |              |  Domain Joined               |
  +------------------------------+              +------------------------------+


