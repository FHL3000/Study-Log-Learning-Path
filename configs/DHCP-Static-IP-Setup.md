# **DHCP and Static IP Setup**

## **Objective**
This project documents the configuration of DHCP and static IP addressing within a home lab network. The goal was to ensure consistent device connectivity, specifically for the Raspberry Pi, while maintaining flexibility for other devices through dynamic addressing.

---

## **Tools and Technologies Used**
- **ISP Router:** Kinetic WiFi 6 Modem (T3280)
- **Secondary Router:** Asus RT-AX3000
- **Switch:** Netgear 8-Port Gigabit Ethernet Unmanaged Switch (300 series)
- **Device:** Raspberry Pi

---

## **Network Topology**
1. **ISP Router:** Acts as the primary internet gateway for the main network.
2. **Secondary Router:** Acts as the DHCP server and gateway for the home lab subnetwork.
3. **Switch:** Connected to the secondary router to distribute connections to multiple devices, including the Raspberry Pi.

---

## **Configuration Steps**

### **1. Connecting Devices**
- **ISP Router:** LAN 1 port connected to the WAN port of the secondary router (Asus RT-AX3000).
- **Secondary Router:** Connected to port 1 of the Netgear switch.
- **Raspberry Pi:** Connected to port 8 of the Netgear switch.

### **2. Configuring DHCP on the Secondary Router**
- Logged into the Asus RT-AX3000’s admin panel via its default gateway IP (`10.0.0.1`).
- Configured the subnetwork with the range `10.0.0.0/24`.
- Enabled DHCP to assign dynamic IP addresses to devices in the range of `10.0.0.100` to `10.0.0.200`.
- Disabled DHCP on the ISP router to avoid conflicts with the secondary router.

### **3. Assigning Static IPs**
- **Router:** Assigned a static IP address of `10.0.0.1` to the secondary router as the gateway for the home lab subnetwork.
- **Raspberry Pi:** Reserved a static IP address of `10.0.0.2` for the Raspberry Pi in the secondary router's DHCP settings to ensure consistent connectivity.
- Saved and applied the changes.

---

## **Challenges and Troubleshooting**
- **IP Conflict:** Initially faced issues with IP conflicts due to DHCP being enabled on both the ISP and secondary routers. Resolved by disabling DHCP on the ISP router and delegating the task to the secondary router.
- **Connectivity Issues:** The Raspberry Pi failed to connect initially due to incorrect subnet mask settings. Corrected it by ensuring the subnet mask (`255.255.255.0`) matched the subnetwork configuration.

---

## **Outcomes**
- Successfully configured the secondary router to manage DHCP and assign static IPs within the `10.0.0.0/24` subnetwork.
- Ensured the Raspberry Pi remains consistently reachable at `10.0.0.2` for DNS services and other configurations.
- Gained practical experience in setting up and managing DHCP and static IP configurations in a subnetwork.

---

## **Future Enhancements**
- Explore VLANs for further network segmentation.
- Implement monitoring tools to track network activity and detect potential conflicts.

---

This project served as a foundational exercise in networking and system administration, aligning with real-world IT support scenarios.
