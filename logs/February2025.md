# February 2025 IT Study Log

## Overview
This document chronicles my IT learning journey throughout February 2025, covering theoretical coursework and hands-on practical configurations across networking, hardware, virtualization, and security domains.

## Daily Learning Activities

**February 1, 2025** *(6.5 hours)*
- Theory:
  - Google IT support fundamentals course (3 hours): Digital logic, computer architecture, troubleshooting best practices, customer service principles
  - CompTIA A+ Exam guide by Mike Meyers (30 minutes): OS installation and backup procedures, CPU selection and installation, RAM selection and installation
- Hands-on:
  - Dell PowerEdge R230 hardware upgrades (3 hours): Installed Intel Xeon E3-1270 V6 processor with thermal paste application, added 32GB ECC UDIMM RAM, installed 2x 1TB SSDs, verified proper component installation in system setup

**February 2, 2025** *(1.25 hours)*
- Theory:
  - CompTIA A+ Core 1 (220-1101) Course by Mike Meyers (1 hour): Network protocols, TCP vs. UDP comparison, DHCP operation
  - CompTIA A+ Exam guide by Mike Meyers (15 minutes): DNS troubleshooting, DNS resolution process

**February 3, 2025** *(4 hours)*
- Theory:
  - CompTIA A+ Core 1 (220-1101) Course by Mike Meyers (3 hours): Subnetting techniques, IPv4/IPv6 addressing, NAT configuration
- Hands-on:
  - Practiced subnetting calculations (1 hour)
  - Assigned static IP addresses to home lab devices

**February 4, 2025** *(1.75 hours)*
- Theory:
  - CompTIA A+ Core 1 (220-1101) Course by Mike Meyers (1 hour): MAC addressing, ARP protocol, switch operations
  - Total Hardware Quiz (15 minutes): Memory types, cache levels, CPU sockets
  - CompTIA A+ Exam guide by Mike Meyers (30 minutes): Motherboard chipsets, BIOS settings and configuration

**February 5, 2025** *(3 hours)*
- Hands-on:
  - Network and VLAN configuration (3 hours): Configured VLANs and verified segmentation on managed switch, set up static routing between VLANs and tested connectivity, verified correct ARP table entries and routing tables, labeled and identified devices in the network, configured Asus ExpertWifi system as an access point, planned VLAN segmentation for IoT devices, personal devices, and home lab, started speed test benchmarking (pre-optimization tests)

**February 6, 2025** *(1.75 hours)*
- Theory:
  - CompTIA A+ Core 1 (220-1101) Course by Mike Meyers (1 hour): Structured cabling, cable categories, crimping techniques
- Hands-on:
  - Verified correct installation of RAM modules in dual-channel mode (30 minutes)
  - Total Hardware Quiz (15 minutes): SSD vs. HDD comparison, RAID configurations, thermal management best practices

**February 7, 2025** *(4 hours)*
- Theory:
  - CompTIA A+ Exam guide by Mike Meyers (1 hour): Security best practices for small networks
- Hands-on:
  - Firewall configuration (3 hours): Configured basic firewall rule set in UFW, allowed SSH, limited ICMP, and logged unauthorized access attempts, tested firewall rules using `sudo ufw status numbered` and `ping`

**February 8, 2025** *(1.5 hours)*
- Theory:
  - CompTIA A+ Core 1 (220-1101) Course by Mike Meyers (1 hour): Router configurations, DHCP settings, Quality of Service (QoS) fundamentals
  - Total Hardware Quiz (30 minutes): Expansion slots, GPU architecture, cooling solutions

**February 9, 2025** *(3.5 hours)*
- Theory:
  - CompTIA A+ Exam guide by Mike Meyers (30 minutes): Ethernet frame structure, network troubleshooting tools
- Hands-on:
  - Switch security configuration (3 hours): Configured and tested port security on the Aruba managed switch, set up an access control list (ACL) to restrict traffic flow, verified security logs for unauthorized access attempts

**February 10, 2025** *(1.25 hours)*
- Theory:
  - CompTIA A+ Core 1 (220-1101) Course by Mike Meyers (1 hour): Network troubleshooting methodologies, diagnostic tools
- Hands-on:
  - Practiced using network diagnostic tools (15 minutes): `ping` for connectivity testing, `traceroute` for path analysis, `netstat` for connection monitoring on Linux

**February 11, 2025** *(2 hours)*
- Hands-on:
  - Patch Panel & Structured Cabling (2 hours): Created custom Ethernet cables with crimped RJ-45 connectors, connected and tested patch panel wiring, routed power and networking cables separately for organization

**February 13, 2025** *(4.5 hours)*
- Theory:
  - CompTIA A+ Core 1 (220-1101) Course by Mike Meyers (2 hours): DNS configuration, router configuration, VLANs implementation, network troubleshooting
  - Google IT course "The Bits and Bytes of Computer Networking" (2 hours): Ethernet standards and frames, MAC addresses, unicast, multicast, and broadcast
- Hands-on:
  - Proxmox VE optimization (30 minutes): Configured VM backup strategy, optimized VM performance through CPU optimizations, enabled TRIM for SSDs

**February 14, 2025** *(2 hours)*
- Hands-on:
  - Proxmox VE installation (2 hours): Installed Proxmox VE as primary hypervisor on Dell PowerEdge R230, verified installation and initial web GUI access, planned VM deployments for testing different operating systems

**February 16, 2025** *(1.5 hours)*
- Hands-on:
  - Raspberry Pi configurations (1.5 hours): Planned repurposing to offload services from Dell PowerEdge R230, set up initial configurations for future automation

**February 18, 2025** *(2 hours)*
- Hands-on:
  - Created Windows 11 virtual machine on Proxmox (2 hours): Configured resource allocation for optimal performance, tested VM functionality and network connectivity

**February 19, 2025** *(1 hour)*
- Theory:
  - CompTIA A+ Core 1 (220-1101) Course by Mike Meyers (1 hour): Router configurations, DHCP settings, Quality of Service (QoS) fundamentals

**February 20, 2025** *(1 hour)*
- Theory:
  - CompTIA A+ Core 1 (220-1101) Course by Mike Meyers (1 hour): Structured cabling standards, cable categories and specifications, proper crimping techniques

**February 21, 2025** *(2 hours)*
- Hands-on:
  - Security & Firewall testing (2 hours): Continued UFW firewall configuration on Raspberry Pi, installed tcpdump for network monitoring, planned ICMP rate-limiting testing

**February 22, 2025** *(2 hours)*
- Hands-on:
  - Network segmentation implementation (2 hours): Implemented network segmentation for improved security, configured firewall rules to isolate sensitive systems, tested inter-VLAN communication restrictions

**February 24, 2025** *(2.5 hours)*
- Theory:
  - CompTIA A+ Core 1 (220-1101) Course by Professor Messer (2 hours): Common/well-known ports including FTP, SSH, RDP, LDAP, etc.
  - Google IT course "The Bits and Bytes of Computer Networking" (30 minutes): Ethernet standards and frames, MAC addresses, unicast, multicast, and broadcast communication

**February 25, 2025** *(4 hours)*
- Theory:
  - CompTIA A+ Core 1 (220-1101) Course by Mike Meyers (2 hours): DHCP operation and configuration, IPv6 addressing and transition mechanisms, port numbers, TCP, UDP, and ICMP protocols
  - Google IT course "The Bits and Bytes of Computer Networking" (2 hours): TCP/IP model, networking cables and tools, server and client relationship

**February 26, 2025** *(2 hours)*
- Theory:
  - CompTIA A+ Core 1 (220-1101) Course by Mike Meyers (2 hours): DNS configuration and troubleshooting, router configuration best practices, VLAN implementation, network troubleshooting methodologies

**February 28, 2025** *(3 hours)*
- Theory:
  - Comprehensive review of CompTIA A+ networking objectives (2 hours)
  - Practice exam covering networking fundamentals (1 hour)
  - Identified knowledge gaps for future study

**February 29, 2025** *(2 hours)*
- Review and Planning:
  - Consolidated notes from the month's study (1 hour)
  - Created study plan focusing on (1 hour): Advanced VLAN configuration techniques, inter-VLAN routing optimization, hardware troubleshooting methodologies, network diagnostic procedures

## Monthly Summary

**Total Hours Studied: 60.25 hours**
- Theoretical Study: 32.25 hours
- Hands-on Practice: 28 hours

**Learning Accomplishments**
1. Hardware Configuration
   - Successfully upgraded Dell PowerEdge R230 server with new processor, memory, and storage
   - Verified proper installation and operation of all components
   - Established solid understanding of server hardware architectures

2. Virtualization Platform
   - Deployed Proxmox VE as primary hypervisor
   - Created and optimized virtual machines
   - Implemented VM backup strategies and performance optimizations

3. Networking
   - Configured VLANs for network segmentation
   - Implemented proper security measures including ACLs
   - Gained proficiency in network diagnostics and troubleshooting
   - Designed structured cabling system with patch panel

4. Security Implementation
   - Established firewall rules and security policies
   - Configured network traffic monitoring
   - Implemented network isolation for sensitive systems

5. Certification Progress
   - Completed approximately 25% of CompTIA A+ Core 1 course material
   - Reinforced learning with hands-on application of concepts
   - Identified areas for focused study in March

**Next Steps for March**
- Focus on advanced networking configurations:
  - Complex VLAN topologies and trunking
  - Dynamic routing protocols (OSPF, BGP)
  - Deep packet analysis with Wireshark
- Develop hardware troubleshooting skills:
  - Component-level diagnostics
  - System performance analysis
  - BIOS/UEFI configuration optimization
- Enhance network troubleshooting capabilities:
  - Physical layer diagnostics
  - End-to-end connectivity analysis
  - Performance bottleneck identification
- Continue practical implementation of CompTIA A+ concepts
