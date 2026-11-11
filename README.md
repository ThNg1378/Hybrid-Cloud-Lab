<div align="center">

# ☁️ Hybrid-Cloud-Lab

**Enterprise-grade hybrid network. Secure, monitored, and identity-driven.**

🌐 [Detailed Report (WIP)](#) · 🛡️ [System & Security Focus ](#) · ☁️ [Azure](#)

![Status: Active](https://img.shields.io/badge/Status-Active-success?style=flat-square) ![Topology: Hub-and-Spoke](https://img.shields.io/badge/Topology-Hub--and--Spoke-blue?style=flat-square) ![Cloud: Azure](https://img.shields.io/badge/Cloud-Azure_Entra_ID-0089D6?style=flat-square) ![License: MIT](https://img.shields.io/badge/License-MIT-gray?style=flat-square)

**VMware Workstation · MikroTik RouterOS · Windows Server · PRTG Monitor**

</div>

---

### 🚀 Agile. Secure. Intuitive.
Simulates a real-world enterprise network architecture, addressing Multi-site deployment challenges with a Zero Trust security baseline.

| 🔒 Zero Trust IAM | 🛡️ Site-to-Site VPN | 🚦 Traffic Control | 📈 Deep Visibility |
| :--- | :--- | :--- | :--- |
| **Azure SSO & MFA**<br>Centralized identity management, preventing data breaches and credential leaks. | **IPsec Tunnel**<br>End-to-end encryption for all data traversing between the Headquarters (HQ) and Branch. | **VLAN Segmentation**<br>Strict network isolation for Guest, Staff, and Management traffic. | **PRTG Network**<br>24/7 monitoring for system health, uptime, and bandwidth utilization. |

<div align="center">
  <br>
  <i>Overall Hub-and-Spoke Network Architecture Diagram</i>
  <br><br>
  <b><image src= "Screenshot/02-Network-Architecture/PROJECT_HYBRIDCLOUD.jpg" > </b>
  <br><br>
</div>

---

### ⚡ Why this Architecture?
*Traditional SMB Network vs. Hybrid-Cloud-Lab:*

| Criteria | Traditional Enterprise Network | Hybrid-Cloud-Lab |
| :--- | :--- | :--- |
| **Access Security (IAM)** | Local passwords, highly vulnerable to Brute-force attacks | **Azure Entra ID (MFA & SSO)** |
| **Branch Connectivity** | Public Port Forwarding (NAT), unencrypted (MitM risk) | **IPsec VPN Tunnel** with 256-bit encryption |
| **Network Isolation** | Shared IP range (Flat Network) | Strict **VLAN 10, 20, 30** segmentation |
| **System Monitoring** | Reactive (Waiting for user reports) | Proactive alerting via **PRTG Core Probe** |
| **Scalability** | Patchwork, difficult to manage centrally | **Enterprise-grade**, ready for IDS/IPS integration |

---

### 🖼️ Showcase
*(Real-world projects require proof. Insert your actual deployment screenshots here)*

* 🛡️ **Azure MFA Login:** Mandatory Authenticator prompt during external user login. `[Insert Image]`
* 🔒 **IPsec Tunnel Established:** Encrypted connection status between 2 Routers via Winbox. `[Insert Image]`
* 📊 **PRTG Dashboard:** Red/Green monitoring dashboard tracking VLAN Traffic and Ping. `[Insert Image]`
* 🌐 **VLAN Routing:** Internal routing table at the HQ. `[Insert Image]`

---

### ✨ How does this system work?
This project is not just about software installation; it's a seamless orchestration of multiple technologies:
* **Routing & Switching:** Utilizes MikroTik as the Core Router, configuring Trunking and Access Ports to segment internal VLANs. Departmental data flows are strictly isolated.
* **Remote Connectivity:** Instead of expensive leased lines, the system leverages the public Internet with an established **IPsec VPN** tunnel to seamlessly connect the Branch network to the Headquarters as if they were on the same local LAN.
* **Cloud Sync:** The on-premises Active Directory (Windows Server) is synchronized with the **Azure Cloud**. Users require only a single account (SSO) to access all services and are strictly enforced to use **MFA** when authenticating externally.
* **Proactive Monitoring:** PRTG Network Monitor continuously polls (Ping, SNMP) network devices, ensuring the VPN tunnel remains uninterrupted and bandwidth is never bottlenecked.

---

### 👨‍💻 Repository Layout
The repository structure follows the **Documentation-as-Code** standard, enabling anyone to easily understand and replicate this Lab environment.

| Directory / Component | Purpose (What it is) |
| :--- | :--- |
| `docs/` | Contains design documentation: IP/VLAN planning tables and original network architecture diagrams. |
| `01-network-infrastructure/` | Configuration scripts/exports (`.rsc`) for MikroTik Routers (VLAN, NAT, Firewall). |
| `02-ipsec-vpn/` | Guides and configurations for establishing the encrypted Site-to-Site tunnel between HQ and Branch. |
| `03-identity-and-cloud/` | Active Directory configurations and synchronization policies for Azure Entra ID (MFA, SSO). |
| `04-monitoring/` | Exported sensor lists and reports from the PRTG Core Probe. |

---

## 📂 Expanded Projects & Case Studies
*Click the arrows to view details of component projects and integrated tools within the Lab ecosystem.*

<details>
<summary><b>1. 🛡️ Case Study: Snort IDS Monitoring log</b></summary>

* **Description:** Deployed a Snort 3 in Ubuntu server within the System Cloud Hybrid real-time packet analysis, connected with Zabbix to notification log .
* **Technologies:** VMware ESXi, MikroTik RouterOS, VLAN 10/20/30, Azure/Google Drive Backup, Zabbix.
* **Detailed Documentation:** Available in the [`05-case-studies/saomai-software/`](docs/) directory *(coming soon)*
</details>

