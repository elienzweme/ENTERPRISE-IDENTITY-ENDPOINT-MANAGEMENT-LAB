# 🏗️ Enterprise Identity & Endpoint Management Lab  
**Active Directory | Group Policy | WSUS | Windows Server**

---

## 📌 Project Overview

This project simulates a real-world enterprise IT environment where I designed, deployed, and supported a Windows-based infrastructure.

The goal was to gain hands-on experience in:

- System administration  
- Enterprise troubleshooting  
- Help desk workflows  
- Patch management and endpoint support  

📄 Full Documentation: [View Project Report](./Enterprise%20Identity%20%26%20Endpoint%20Management%20Lab.pdf)

---

## 🧩 Technologies Implemented

### 🔐 Identity & Access Management
- Active Directory Domain Services (AD DS)

### 💻 Endpoint Management
- Group Policy (GPO)  
- Windows Server Update Services (WSUS)

### 🖥️ Systems & Infrastructure
- Windows Server 2022 (Domain Controller)  
- Windows 10/11 Client Machines  

### 📁 File Services
- NTFS Permissions  
- Access-Based Enumeration (ABE)  

### 🎫 Support & Ticketing
- Jira Service Management  

---

## ⚙️ Environment Setup

- Domain: `dc.local`
- Domain Controller IP: `192.168.0.49`
- Virtualization: VirtualBox / VMware
- Clients: Windows 10/11 (domain-joined)

---

## 🏢 Infrastructure Built

### 🔐 Active Directory
- Deployed AD DS and promoted Domain Controller  
- Created OUs:
  - IT  
  - Engineering  
  - Finance  
  - Sales  
- Created users and security groups  

📸 Example (AD Configuration):  
![AD Setup](screenshots/ad-users.png)

---

### 💻 Domain Join
- Configured client DNS to point to Domain Controller  
- Joined multiple clients to domain  
- Verified authentication  

📸 Example (Domain Join):  
![Domain Join](screenshots/domain-join.png)

---

### 📁 File Server & Permissions
- Created shared folder:
