# **January 2025 Study Log**

## **Daily Log**

### **2025-01-15**
- **Networking:**
  - (1hr 20mins) CompTIA A+ Core 1 (220-1101) Course by Mike Meyers and supplemental reading: studied cables and connectors, structured 
cabling, and crimping cables, reviewed previous notes on networking essentials and flash cards
  - (3 hrs) Hands on Basic Network configuration: Resolving DNS resolution issues, checking device connectivity, Resolving DNS loop
- **Hardware:**
  - (34 min) Intermediate Harware Quiz: BIOS/UEFI, power supply, memory, RAID, peripherals,cooling, troubleshooting (Note: Improvement needed:USB length standards, Disk initialization, SSD vs. HDD in heavy write environments) 
  - (30 min) CompTIA A+ Exam guide textbook by Mike Meyers reading: Motherboard components, PCIe lanes, expansion busses.

### **2025-01-16**
- **Networking:**
  - (4 hrs) CompTIA A+ Core 1 (220-1101) Course by Mike Meyers and supplemental reading: studied networking fundamentals, network cards, 802 standards, and troubleshooting.
  - (15 min) CompTIA A+ Exam guide textbook by Mike Meyers reading: T568A and T568B wiring standards.
- **Hardware:**
  - (30 mins) Intermediate Total Harware Quiz: motherboards, CPUs, RAM, Power Supplies, fans, heat sinks, expansion cards, cables, ports, HDDs, SSD, chipsets, i/o.

### **2025-01-20**
- **Networking:**
  - (1.5 hrs)  CompTIA A+ Core 1 (220-1101) Course by Mike Meyers and supplemental reading:Studied and recorded notes on local area networks, TCP/IP, dynamic IP addressing, IPv4 & IPv6. Supplemental network reading from https://learn.microsoft.com/en-us/training/modules/network-fundamentals/5-ip-tcp-basics
  - CompTIA A+ Exam guide textbook by Mike Meyers reading: Read about UTP & STP cabling, fiber optic, coaxial, and Cat(x) ratings.
  - (1 hour) Verified hardware connections and tested device connectivity.
- **Hardware:**
  - (30 mins) Intermediate Total Harware Quiz: motherboards, CPUs, RAM, Power Supplies, fans, heat sinks, expansion cards, cables, ports, HDDs, SSD, chipsets, i/o.
 
### **2025-01-24**
- **Networking:**
  - (2 hrs)  CompTIA A+ Core 1 (220-1101) Course by Mike Meyers and supplemental reading:Studied and recorded notes on local area networks, TCP/IP, Port numbers, UDP, ICMP. Supplemental network reading from https://learn.microsoft.com/en-us/training/modules/network-fundamentals/4-network-protocols
  - CompTIA A+ Exam guide textbook by Mike Meyers reading: Read about structured cabling, networking hardware, crimping, and troubleshooting
- **Hardware:**
  - (30 mins) Intermediate Total computer Harware Quiz and flashcard review: motherboards, CPUs, RAM, Power Supplies, fans, heat sinks, expansion cards, cables, ports, HDDs, SSD, chipsets, i/o.
 
### **2025-01-25**
- **Networking:**
  - (3 hrs)  Hands-on network configuration: Advanced firewall configuration, (1) Allowed Essential Ports – Opened port 22 (SSH) and port 53 (DNS) for secure remote access and DNS resolution. (2) Limited SSH Login Attempts – Applied rate-limiting to port 22 to mitigate brute-force attacks. (3) Implemented ICMP Rate Limiting – Restricted excessive ping requests to prevent abuse. (4) Configured Firewall Logging – Enabled logging to monitor traffic and security events. (5) Restricted SSH Access by Subnet – Allowed SSH connections only from 10.0.0.0/24 for added security. (6) Applied Outbound Rules – Allowed necessary outbound traffic for DNS, web traffic (80/443), and SSH. (7) Tested & Verified Rules – Used sudo ufw status numbered, ping, and iptables logs to confirm configurations.
 
### **2025-01-26**
- **Networking:**
  - (3 hrs)  CompTIA A+ Core 1 (220-1101) Course by Mike Meyers and supplemental reading:Studied and recorded notes on DNS, router configuration, and VLANS
  - (30 mins CompTIA A+ Exam guide textbook by Mike Meyers reading: Read about structured cabling, LAN vs. WAN, MAC vs IP, switches and routers
  - (3 hrs)  **Hands-on network configuration:** Hands-on network security: **SSH Hardening** (1) Disabled Root Login – Prevented direct root access via SSH by setting PermitRootLogin no in /etc/ssh/sshd_config. (2) Enabled Key-Based Authentication – Generated an SSH key pair on the local machine and copied the public key to the Raspberry Pi for secure login. (3) Disabled Password Authentication – Enforced key-based login by setting PasswordAuthentication no in SSH config. (4) Restricted SSH Access by Subnet – Allowed SSH connections only from 10.0.0.0/24 to limit access. (5) Restarted SSH Service – Applied changes with sudo systemctl restart ssh and verified proper functionality.
  - **Fail2Ban Configuration** (1) Configured SSH Jail – Created a custom jail.local file to define SSH security rules.
(2) Set Ban Time and Retry Limits – Restricted repeated login attempts by setting maxretry = 5, bantime = 10m, and findtime = 10m.
(3) Verified Fail2Ban Status – Checked active jails with sudo fail2ban-client status sshd.
(4) Monitored Logs for Intrusion Attempts – Used sudo tail -f /var/log/fail2ban.log to track blocked IPs and verify effectiveness.

### **2025-01-27**
- **Networking:**
  - (3 hrs)  CompTIA A+ Core 1 (220-1101) Course by Prof. Messer and supplemental reading:Studied and recorded notes on peripherial cables, SATA, SCSI, PATA, and video cables.


 



---

## **Summary**
- **Total Hours Logged:** 12 hours
  - **Hardware:** 2 hours
  - **Networking:** 10 hours
- **Key Accomplishments:**
  - Successfully established a functional home lab network with a subnet of `10.0.0.0/24`.
  - Configured static and dynamic IPs for devices to ensure consistent operation.
  - Gained hands-on experience in hardware setup and network troubleshooting.

This month’s activities provided foundational skills in hardware and networking, directly aligned with real-world IT support and system administration scenarios.
