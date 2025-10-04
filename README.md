# Hotel-Management-Network-Design-Implementation
# 🏨 Hotel Network Project

This project was developed as part of my networking practice to design and implement a **multi-floor hotel network** using Cisco Packet Tracer.  
It demonstrates core networking concepts including **VLAN segmentation, dynamic routing (OSPF), DHCP, SSH remote access, and port security**.

---

## 📋 Project Overview
- **Scenario:** Vic Modern Hotel with 3 floors and multiple departments.
- **Goal:** Design and configure a secure and fully functional network where all devices can communicate seamlessly while enforcing security and scalability.

---

## 🏗️ Network Design
- **Three routers** (one per floor) connected using **Serial DCE cables** with `/30` subnets:
  - 10.10.10.0/30  
  - 10.10.10.4/30  
  - 10.10.10.8/30
- **One switch per floor** connecting department PCs, printers, and access points.
- **Wi-Fi networks** available for laptops and mobile devices on each floor.
- **Printers** provided per department.

---

## 🖧 VLAN Configuration
Each department is placed in a separate VLAN for segmentation:

- **1st Floor**  
  - Reception → VLAN 80 → 192.168.8.0/24  
  - Store → VLAN 70 → 192.168.7.0/24  
  - Logistics → VLAN 60 → 192.168.6.0/24  

- **2nd Floor**  
  - Finance → VLAN 50 → 192.168.5.0/24  
  - HR → VLAN 40 → 192.168.4.0/24  
  - Sales/Marketing → VLAN 30 → 192.168.3.0/24  

- **3rd Floor**  
  - Admin → VLAN 20 → 192.168.2.0/24  
  - IT → VLAN 10 → 192.168.1.0/24  

---

## ⚙️ Key Configurations
- **Dynamic Routing:** Configured **OSPF** to advertise all inter-router networks.  
- **DHCP Services:** Each router acts as a **DHCP server** for its respective VLANs.  
- **SSH Remote Login:** All routers configured for **secure SSH access** (v2) instead of Telnet.  
- **Port Security:** Implemented on IT switch port `fa0/1` to only allow a **Test-PC** (sticky MAC, violation mode = shutdown).  
- **Testing:** Verified inter-VLAN communication, OSPF route propagation, DHCP leases, SSH remote login, and security enforcement.

---

## ✅ Learning Outcomes
- Practical application of **CCNA-level concepts** in routing, switching, and security.  
- Hands-on experience with **network design, segmentation, and services**.  
- Enhanced understanding of **real-world enterprise network deployment** scenarios.  

---

## 🛠️ Tools
- **Cisco Packet Tracer** (simulation environment)

---

## 📷 Screenshots
(Add your topology screenshots here)

---

## 🚀 Future Improvements
- Implement **HSRP/VRRP** for gateway redundancy.  
- Add **ACLs** for access control between VLANs.  
- Explore **QoS policies** for prioritizing critical traffic (e.g., VoIP).

---

