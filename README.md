> ⚠️ **Privacy Notice:**  
> All IP addresses and MAC addresses shown in the screenshots have been **blurred or redacted** to protect sensitive information and ensure privacy.

# 🔍 Nmap Network Port Scanning Report

## 🎯 Objective
To identify open ports on devices within the local network and evaluate potential exposure risks using Nmap and optionally Wireshark.

## 🛠️ Tools Used
- **Kali Linux**
- **Nmap** (Network Mapper)
- **Wireshark** (for optional packet analysis)

## 📋 Steps Performed


1. **Identified Local IP Range**
   Used the `ifconfig` command to view the IP address of my active network interface (e.g., `wlan0` or `eth0`), helping determine the subnet (e.g., `192.168.1.0/24`).
   Used `ip a` or  to determine the local IP range (e.g., `192.168.1.0/24`).

3. **Performed TCP SYN Scan**  
   Executed the command:
nmap -sS 192.168.1.0/24

This performed a stealthy SYN scan across all devices in the subnet.

3. **Collected and Analyzed Results**  
- Recorded the IP addresses that responded.
- Noted open ports on each active host.

  nmap -sS 192.168.1.0/24 

4. **(Optional) Packet Capture with Wireshark**  
Captured traffic while the scan was running to observe mDNS, ARP, or SYN packets.

5. **Researched Common Services**  
Used `nmap --top-ports 1000` and service name resolution to determine likely services (e.g., SSH on port 22, HTTP on 80).

6. **Identified Security Risks**  
- Highlighted unnecessary services that could be exploited if unpatched.


## 🖼️ Included Screenshots
1. IP range identification  
2. TCP SYN scan execution  
3. Scan results  
4. Wireshark traffic capture  
5. Open port/services analysis  
