# Hybrid-Cloud-Lab☁️
# 📖 Project Overview
This project demonstrates the design and implementation of a hybrid security architecture that combines on-premises infrastructure with cloud-based management. The core objective is to establish a robust security monitoring system, while leveraging Active Directory and Azure Arc for unified identity and management. This setup serves as a sandbox environment to study network traffic flow, threat detection, and hybrid infrastructure synchronization—providing a framework to streamline operations and improve manageability in complex server environments

This lab focuses on building and penetration testing a hybrid cloud system in a real-world scenario, guaranteeing high availability, disaster recovery, and centralized monitoring.
# 
#🎯 Project Goals
* Enterprise-Grade Architecture: Designed and built a highly available hybrid cloud infrastructure.
* Multi-Site Directory Services: Deployed Active Directory and Read-Only Domain Controllers (RODC) across distributed sites.
* Secure Connectivity: Configured IPsec VPNs to ensure secure site-to-site communication.
* Modern Identity Management: Integrated Azure Cloud for Single Sign-On (SSO) and Multi-Factor Authentication (MFA).
* Centralized Monitoring: Implemented comprehensive network and system monitoring using PRTG.
* Intrusion Detection: Deployed Snort IDS to monitor, detect, and alert on malicious network traffic.
* Security & Resilience: Conducted rigorous penetration testing and validated disaster recovery protocols.
#
#🏗️ Lab Structure
* Hypervisor: VMware workstation
* Domain Server: Active Directory, OU Mangement, DNS Server, DHCP Server
* Monitor Server: PRTG, Snort IDS
* CLient VM 01 (HQ User) & Client VM 02(Branch User): Simulated end-user workstation
* Mikcrotik router: IPsec tunnel, IP gateway setup, DHCP relay agent, firewall, internet setup
#
#☁️ Azure Cloud 
* Azure AD Connect Cloud Sync:  
