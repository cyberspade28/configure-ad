<p align="center">
  <img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1 align="center">Deploying On-Premises Active Directory in Microsoft Azure</h1>

<p align="center">
This project demonstrates the deployment of a traditional on-premises Active Directory environment using Microsoft Azure virtual machines.
</p>

---

##  Project Overview

The goal of this lab is to simulate a **real-world enterprise Active Directory environment** by deploying a **Domain Controller** and a **Windows client machine** within Microsoft Azure.

This project focuses on:
- Azure Virtual Machines
- Networking fundamentals
- DNS configuration
- Domain Controller infrastructure preparation

This lab environment will be reused for **future Active Directory labs**, such as user management and Group Policy configuration.

---

##  Technologies Used

- Microsoft Azure (Virtual Machines & Networking)
- Windows Server 2022
- Windows 10
- Active Directory Domain Services (AD DS)
- PowerShell
- Remote Desktop Protocol 

---

##  Operating Systems

- **Domain Controller:** Windows Server 2022
- **Client Machine:** Windows 10 

---

## objetive 

- One Azure Resource Group
- One Virtual Network with a single subnet
- One Domain Controller VM (DC-1)
- One Client VM (Client-1)
- Internal DNS handled by the Domain Controller

---

##  Deployment and Configuration Steps

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
<img width="2560" height="1440" alt="Screenshot (42)" src="https://github.com/user-attachments/assets/855b496c-e789-4171-9760-aa68e6872967" />
<img width="2560" height="1440" alt="Screenshot (43)" src="https://github.com/user-attachments/assets/e9af820a-0a9e-4a1a-aab3-a62acd0ae520" />


---

## 🖥️ Client Machine Setup

---

### 6️⃣ Create Client VM (Client-1)
<img width="2560" height="1440" alt="Screenshot (44)" src="https://github.com/user-attachments/assets/12c8520f-5bba-4a80-96aa-bcd4c83c0fa7" />

- **VM Name:** Client-1  
 

The client machine was deployed in the **same region and virtual network** as the Domain Controller.

---

### 7️⃣ Configure Client DNS Settings
<img width="2560" height="1440" alt="Screenshot (47)" src="https://github.com/user-attachments/assets/026650ef-997f-42b5-bdc1-eb66b0ad0069" />
<img width="2560" height="1440" alt="Screenshot (48)" src="https://github.com/user-attachments/assets/e68a324f-25b5-4830-a546-e38a473a1dd2" />

---

### 8️⃣ Verify Network Connectivity
<img width="2560" height="1440" alt="Screenshot (55)" src="https://github.com/user-attachments/assets/8a8f9490-32cd-463b-8481-8ef9260c9959" />


Connectivity between Client-1 and DC-1 was verified using ICMP ping.

---

### 9️⃣ Verify DNS Configuration
<img width="2560" height="1440" alt="Screenshot (56)" src="https://github.com/user-attachments/assets/e75545ab-534b-45b2-b272-979c40e358d8" />

The `ipconfig /all` command confirmed that Client-1 is using DC-1 as its DNS server.



---

## ✅ Skills Demonstrated

- Azure Virtual Machine deployment
- Virtual networking and subnet configuration
- DNS configuration
- Infrastructure planning
- Windows Server administration fundamentals
- Troubleshooting network connectivity

---

