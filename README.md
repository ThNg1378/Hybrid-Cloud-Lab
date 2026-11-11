# Hybrid-Cloud-Lab ☁️

## 📖 Project Overview

This project demonstrates the design and implementation of a hybrid cloud infrastructure that combines on-premises infrastructure with Microsoft Azure cloud services. The core objective is to establish a robust security monitoring system while leveraging Active Directory and Azure Cloud (Cloud Sync) for unified identity and management. This setup serves as a sandbox environment to study network traffic flow, user synchronization, and hybrid infrastructure replication, providing a framework to streamline operations and improve manageability in complex server environments.

## 🎯 Project Goals

- Enterprise-Grade Architecture: Designed and built a highly available hybrid cloud infrastructure.
- Multi-Site Directory Services: Deployed Active Directory and Read-Only Domain Controllers (RODC) across distributed sites.
- Secure Connectivity: Configured IPsec VPNs to ensure secure site-to-site communication.
- Modern Identity Management: Integrated Azure Cloud for Single Sign-On (SSO) and Multi-Factor Authentication (MFA).
- Centralized Monitoring: Implemented comprehensive network and system monitoring using PRTG.
- Intrusion Detection: Deployed Snort IDS to monitor, detect, and alert on malicious network traffic.
- Security & Resilience: Conducted rigorous penetration testing and validated disaster recovery protocols.

## 🏗️ Lab Structure

- Hypervisor: VMware Workstation
- Domain Server: Active Directory, OU Management, DNS Server, DHCP Server
- Monitor Server: PRTG, Snort IDS
- File Server: Backup data, file storage, file sharing
- Client VM 01 (HQ User) and Client VM 02 (Branch User): Simulated end-user workstations
- MikroTik Router: IPsec tunnel, IP gateway setup, DHCP relay agent, firewall, internet setup

## 🗺️ Architecture Diagram


## 🔨 Technologies Used

- Azure Cloud tenant 
- MikroTik RouterOS
- Git
- GitHub
- PRTG
- Snort 

## ☁️ Azure Cloud

- Azure AD Connect Cloud Sync: sync users from on-premises Active Directory into Microsoft Entra ID (Azure AD)
- 25 users successfully synced to Azure Entra ID


