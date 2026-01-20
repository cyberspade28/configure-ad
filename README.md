<p align="center">
  <img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1 align="center">Deploying On-Premises Active Directory in Microsoft Azure</h1>

<p align="center">
This project demonstrates the deployment of a traditional on-premises Active Directory environment using Microsoft Azure virtual machines.
</p>

---

## 📌 Project Overview

The goal of this lab is to simulate a **real-world enterprise Active Directory environment** by deploying a **Domain Controller** and a **Windows client machine** within Microsoft Azure.

This project focuses on:
- Azure Virtual Machines
- Networking fundamentals
- DNS configuration
- Domain Controller infrastructure preparation

This lab environment will be reused for **future Active Directory labs**, such as user management and Group Policy configuration.

---

## 🧰 Technologies Used

- Microsoft Azure (Virtual Machines & Networking)
- Windows Server 2022
- Windows 10
- Active Directory Domain Services (AD DS)
- PowerShell
- Remote Desktop Protocol (RDP)

---

## 💻 Operating Systems

- **Domain Controller:** Windows Server 2022
- **Client Machine:** Windows 10 (21H2)

---

## 🏗️ High-Level Architecture

- One Azure Resource Group
- One Virtual Network with a single subnet
- One Domain Controller VM (DC-1)
- One Client VM (Client-1)
- Internal DNS handled by the Domain Controller

---

## 🚀 Deployment and Configuration Steps

---

### 1️⃣ Create a Resource Group
<img width="2560" height="1440" alt="Screenshot (46)" src="https://github.com/user-attachments/assets/94c3f799-1c9d-4d2a-b6ed-2e4d58eac618" />


</p>



---

### 2️⃣ Create a Virtual Network and Subnet
<img width="2560" height="1440" alt="Screenshot (38)" src="https://github.com/user-attachments/assets/ed59d3be-43d0-414f-9159-0a8da3729886" />
<img width="2560" height="1440" alt="Screenshot (39)" src="https://github.com/user-attachments/assets/aa4b7c4e-9a02-4a2f-b189-b83adb0001d3" />




### 3️⃣ Create the Domain Controller VM (DC-1)
<img width="2560" height="1440" alt="Screenshot (39)" src="https://github.com/user-attachments/assets/e85fc554-5659-4066-ae62-d4bd04f5640c" />


- **VM Name:** DC-1  
- **OS:** Windows Server 2022  

---

### 4️⃣ Configure Static Private IP Address
<img width="2560" height="1440" alt="Screenshot (40)" src="https://github.com/user-attachments/assets/ac03bd02-e63b-4949-8e78-0a0d04a92d0b" />

The Domain Controller’s private IP address was set to **Static** to ensure consistent DNS functionality.

---

### 5️⃣ Disable Windows Firewall (Testing Only)
<p align="center">
<img src="screenshots/firewall_disabled.png" alt="Firewall Disabled"/>
</p>

The Windows Firewall was temporarily disabled to simplify connectivity testing during the lab.

---

## 🖥️ Client Machine Setup

---

### 6️⃣ Create Client VM (Client-1)
<p align="center">
<img src="screenshots/client1_vm.png" alt="Client VM Overview"/>
</p>

- **VM Name:** Client-1  
- **OS:** Windows 10  
- **Username:** labuser  
- **Password:** Cyberlab123!  

The client machine was deployed in the **same region and virtual network** as the Domain Controller.

---

### 7️⃣ Configure Client DNS Settings
<p align="center">
<img src="screenshots/client_dns.png" alt="Client DNS Settings"/>
</p>

Client-1’s DNS settings were configured to point to DC-1’s **private IP address**.

---

### 8️⃣ Verify Network Connectivity
<p align="center">
<img src="screenshots/ping_test.png" alt="Ping Test"/>
</p>

Connectivity between Client-1 and DC-1 was verified using ICMP ping.

---

### 9️⃣ Verify DNS Configuration
<p align="center">
<img src="screenshots/ipconfig.png" alt="DNS Verification"/>
</p>

The `ipconfig /all` command confirmed that Client-1 is using DC-1 as its DNS server.

---

## 💰 Cost Management

<p align="center">
<img src="screenshots/vm_stopped.png" alt="VMs Stopped"/>
</p>

When not in use, the virtual machines are **stopped (deallocated)** in the Azure Portal to reduce costs.  
The environment was **not deleted** and will be reused for future labs.

---

## ✅ Skills Demonstrated

- Azure Virtual Machine deployment
- Virtual networking and subnet configuration
- DNS configuration
- Infrastructure planning
- Windows Server administration fundamentals
- Troubleshooting network connectivity

---

## 📌 Next Steps

This lab environment will be extended to include:
- Active Directory Domain Services installation
- User and group management
- Organizational Units (OUs)
- Group Policy configuration

---

## 📎 Author

**Shawn Smith**  
Aspiring IT Support / Help Desk Technician  
