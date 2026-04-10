# 🏗️ Enterprise Identity & Endpoint Management Lab  
**Active Directory | Group Policy | WSUS | Windows Server**

---

## 📌 Project Overview

This project simulates a real-world enterprise IT environment where I designed, deployed, and supported a Windows-based infrastructure.

The objective was to gain hands-on experience in:
- Enterprise system administration  
- Active Directory management  
- Endpoint configuration and policy enforcement  
- Patch management (WSUS)  
- Real-world IT troubleshooting and help desk workflows  

## 📄 Project Documentation

👉 **[View Full Project Report (PDF)](./Enterprise-Identity-Endpoint-Management-Lab.pdf)**

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
<img width="1906" height="997" alt="Screenshot 2026-04-09 214510" src="https://github.com/user-attachments/assets/f8484382-e706-4f3d-82fd-e55a5878fccb" />


---

## ⚙️ Environment Setup

- Domain: `mty.local`
- Domain Controller IP: `192.168.0.49`
- WSUS Server: `http://192.168.0.49:8530`
- Virtualization: VirtualBox / VMware
- Clients: Windows 10/11 (domain-joined)

---

## 🏢 Infrastructure Built

### 🔐 Active Directory
- Installed AD DS and promoted Windows Server to Domain Controller  
- Created Organizational Units (OUs):
  - IT  
  - Engineering  
  - Finance  
  - Sales  
- Created users and security groups for access control  

📸 AD Configuration  
<img width="975" height="581" alt="image" src="https://github.com/user-attachments/assets/8fb4f508-d5e3-4194-a879-e1e7d28bdc4d" />
<img width="975" height="368" alt="image" src="https://github.com/user-attachments/assets/1565f03d-c636-40c3-b005-e44d20d49ad0" />

---

### 💻 Domain Join
- Configured client DNS to point to Domain Controller  
- Joined multiple client machines to domain  
- Verified authentication using domain credentials  

📸 Domain Join  
<img width="975" height="575" alt="image" src="https://github.com/user-attachments/assets/871fb577-00e6-46b4-9711-6f176c813611" />
<img width="977" height="717" alt="image" src="https://github.com/user-attachments/assets/de49c744-41ec-4361-9463-dba9bfe8dae5" />
<img width="975" height="567" alt="image" src="https://github.com/user-attachments/assets/9159e857-243f-4485-a25c-416c4425f961" />
<img width="975" height="636" alt="image" src="https://github.com/user-attachments/assets/e586ce8e-6235-4527-8c8a-71d04ce1e2b0" />

---

### 📁 File Server & Permissions
- Created shared folder:
```

\192.168.0.49\CompanyShares

```
- Configured:
- NTFS permissions  
- Share permissions  
- Implemented Access-Based Enumeration (ABE) to restrict visibility  

📸 NTFS Permissions  
<img width="975" height="622" alt="image" src="https://github.com/user-attachments/assets/6ba7028a-b71d-425f-81c7-2b0ffcbabe27" />
<img width="975" height="598" alt="image" src="https://github.com/user-attachments/assets/ef9442b2-bdb6-4838-9f40-0b15eca31a14" />
<img width="975" height="598" alt="image" src="https://github.com/user-attachments/assets/e221b06f-4731-4b03-aafe-e55b33248e48" />
<img width="975" height="538" alt="image" src="https://github.com/user-attachments/assets/d42d2247-e022-41fa-a567-bf86a4734f40" />



---

### ⚙️ Group Policy (GPO)
- Created and linked GPOs to Organizational Units  
- Configured:
- Drive mapping  
- Update policies  
- Forced policy updates using:
```

gpupdate /force

```

📸 GPO Configuration  
<img width="975" height="692" alt="image" src="https://github.com/user-attachments/assets/c28bc779-aefc-4a20-9447-ceb9e0418e6c" />
<img width="975" height="691" alt="image" src="https://github.com/user-attachments/assets/9ee9f7be-95fd-4e5c-8ee5-382e331b13fa" />
<img width="975" height="583" alt="image" src="https://github.com/user-attachments/assets/37bbccc2-8781-4111-8054-b8998c412e2e" />
<img width="975" height="511" alt="image" src="https://github.com/user-attachments/assets/982daa80-ac04-4109-9b98-53d9e9b906da" />


---

### 🔄 WSUS (Patch Management)
- Installed and configured WSUS  
- Configured Group Policy for update management:
```

[http://192.168.0.49:8530](http://192.168.0.49:8530)

```
- Enabled automatic updates  
- Implemented client-side targeting (Engineering group)  

📸 WSUS Console  
<img width="975" height="567" alt="image" src="https://github.com/user-attachments/assets/0d55b0df-af98-445c-8e8c-f6d8f08adb19" />
<img width="1123" height="589" alt="image" src="https://github.com/user-attachments/assets/d4998b50-3ccb-42ed-af3b-5dbed5318920" />
<img width="1125" height="664" alt="image" src="https://github.com/user-attachments/assets/435e9e9e-f9f8-44f5-a016-d2dc8f121f38" />
<img width="1125" height="611" alt="image" src="https://github.com/user-attachments/assets/381acce5-1bc8-43ad-9291-e1f5f3e6de49" />




---

# 🎫 Help Desk Simulation (Jira)

## 🧾 Ticket 1: First-Time Login / Password Change

**Issue:**  
User unable to log in due to password change requirement  

**Root Cause:**  
Active Directory policy required password reset at first login
<img width="975" height="734" alt="image" src="https://github.com/user-attachments/assets/72fe0217-29c0-4774-b765-fec0ac171a03" />
<img width="975" height="499" alt="image" src="https://github.com/user-attachments/assets/3b45700d-af39-4857-a2c5-fd43d6734f52" />
<img width="975" height="505" alt="image" src="https://github.com/user-attachments/assets/e501c34a-3062-4c90-a131-24ced30a7778" />
<img width="975" height="735" alt="image" src="https://github.com/user-attachments/assets/b7ed4753-63bd-40e7-ae02-837446e0d44e" />

**Resolution:**  
- Guided user through password change  
- Verified successful login  
<img width="975" height="503" alt="image" src="https://github.com/user-attachments/assets/1d9d6166-7850-44c3-9cb4-5e44aa31cb3a" />

---

## 🧾 Ticket 2: Shared Folder Access Issue

**Issue:**  
User unable to access department shared folder 
<img width="975" height="598" alt="image" src="https://github.com/user-attachments/assets/2fa417d2-54a1-4769-92a9-c1e8878e3163" />
<img width="975" height="658" alt="image" src="https://github.com/user-attachments/assets/5e8b37dc-393e-4107-9b85-d4057aaeed34" />

**Root Cause:**  
Incorrect NTFS permissions and group membership  

**Troubleshooting Steps:**  
- Verified user group membership in Active Directory  
- Reviewed NTFS permissions on shared folder  
- Tested access using multiple accounts

**Resolution:**  
- Updated security group membership  
- Corrected NTFS permissions  
- Enabled Access-Based Enumeration (ABE)
<img width="1125" height="650" alt="image" src="https://github.com/user-attachments/assets/3c49f977-6012-4d5c-a76b-cbaf9b2b4936" />
<img width="975" height="691" alt="image" src="https://github.com/user-attachments/assets/7560a7d0-c0db-471b-9281-e4997b49bf61" />
<img width="975" height="498" alt="image" src="https://github.com/user-attachments/assets/f5a08b7b-cef0-4bc5-87b1-b0e4f5056803" />
<img width="975" height="555" alt="image" src="https://github.com/user-attachments/assets/e9be651d-8925-4b63-84cd-ef6d162bfbae" />

---

## 🧾 Ticket 3: Slow Computer Performance (WSUS Issue)

**Issue:**  
User reported slow system performance after login:
- Delayed applications  
- System lag  
<img width="975" height="505" alt="image" src="https://github.com/user-attachments/assets/b9acf999-a837-4c70-81cd-19a2f4094405" />
<img width="964" height="584" alt="image" src="https://github.com/user-attachments/assets/8a47c60a-74e9-4c20-940a-8d1411b878bb" />


---

### 🔍 Troubleshooting Steps

**1. Initial Assessment**
- Verified system performance after login  
- Checked Windows Update status
<img width="975" height="550" alt="image" src="https://github.com/user-attachments/assets/3e8f9e6c-476a-4af4-98a0-36d191b19c92" />
- <img width="975" height="609" alt="image" src="https://github.com/user-attachments/assets/3848bf0a-d7f5-4139-bea5-9383e01f47f4" />

**2. Group Policy Investigation**
- Identified GPO not applying correctly  
- Ran:
<img width="973" height="561" alt="image" src="https://github.com/user-attachments/assets/d56507fd-4e8c-4db9-844e-3dac4043116a" />
<img width="975" height="597" alt="image" src="https://github.com/user-attachments/assets/ae527216-5499-419a-a19a-334499ad0088" />

```


gpupdate /force

```
- Observed inconsistent policy behavior  

**3. Administrative Access Issue**
- Encountered UAC/elevation issues  
- Verified domain admin credentials  
- Confirmed elevation after system fixes  

**4. Network & Firewall Troubleshooting**
- Attempted remote management → RPC errors  
- Identified firewall blocking communication  

**Firewall Rules Enabled:**
- Remote Event Log Management (RPC)  
- Remote Service Management  
- File and Printer Sharing (SMB)
<img width="975" height="603" alt="image" src="https://github.com/user-attachments/assets/b9b1bb67-dffe-41d1-9c8e-a63f6c8a2f3c" />


**5. Group Policy Reapplication**
- Re-ran:
```

gpupdate /force

```
- Restarted system  

**6. WSUS Validation**
- Triggered update detection:
```

usoclient StartScan
wuauclt /reportnow

```
- Confirmed client reporting to WSUS
<img width="1123" height="589" alt="image" src="https://github.com/user-attachments/assets/58941f4b-1aab-41a5-b950-d3f0f337475a" />
<img width="1125" height="664" alt="image" src="https://github.com/user-attachments/assets/d29d0123-e901-493d-917d-cf552d7925f8" />
<img width="1125" height="611" alt="image" src="https://github.com/user-attachments/assets/5f0f4dbf-0125-45f8-8356-50cdf0c59630" />


---

### 🧠 Root Cause

Firewall rules blocked RPC communication, preventing:
- Group Policy application  
- WSUS update communication  

---

### ✅ Resolution

- Enabled required firewall rules  
- Forced Group Policy update  
- Restarted system  
- Verified WSUS communication  

---

### 🎯 Result

- Group Policy successfully applied  
- WSUS reporting restored  
- System performance improved  

---

## 🧠 Troubleshooting Approach

Throughout this project, I applied:
- Root cause analysis  
- Step-by-step troubleshooting  
- Validation after each fix  
- Documentation of incidents in Jira  

---

## 🚀 Skills Demonstrated

- Active Directory Administration  
- DNS & Networking Troubleshooting  
- Group Policy (GPO)  
- NTFS Permissions & Access Control  
- WSUS Patch Management  
- Firewall & RPC Troubleshooting  
- Help Desk Ticket Management (Jira)  
- System Performance Analysis  

---
## 👤 Author

**Elie Nzweme**  
Aspiring IAM Engineer| Cybersecurity Professional
```
