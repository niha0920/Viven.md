# IP Concepts
IP (Internet Protocol) concepts are fundamental to computer networking. They define how data is addressed, transmitted, and routed across networks like the Internet. Let’s break the key ideas clearly and logically.
## 1. What is IP (Internet Protocol)?
**Internet Protocol (IP)** is a set of rules used to send data from one device to another over a network.
- Works at the **Network Layer** of the OSI model
- Responsible for **logical addressing** and **routing**
- Ensures data packets reach the correct destination
## 2. IP Address
An **IP address** uniquely identifies a device on a network.
### Types of IP Addresses:
#### IPv4 (most common)
- 32-bit address
- Written in **dotted decimal format**
  - Example: `192.168.1.1`
#### IPv6 (modern)
- 128-bit address
- Written in **hexadecimal format**
  - Example: `2001:0db8::1`
## 3. Logical Address vs Physical Address
- **IP Address (Logical Address)**
  - Used for communication across networks
  - Assigned by software (can change)
- **MAC Address (Physical Address)**
  - Hardcoded into device hardware
  - Used within local network (LAN)
- IP works with **ARP (Address Resolution Protocol)** to map IP → MAC.
## 4. Types of IP Addresses (Based on Communication)
### Unicast
- One sender → one receiver
- Example: Opening a website
### Broadcast
- One sender → all devices in network
- Example: ARP request
### Multicast
- One sender → group of devices
- Example: Live streaming
## 5. IP Classes (Classful Addressing - IPv4)
| Class | Range     | Usage           |
| ----- | --------- | --------------- |
| A     | 1 – 126   | Large networks  |
| B     | 128 – 191 | Medium networks |
| C     | 192 – 223 | Small networks  |
| D     | 224 – 239 | Multicast       |
| E     | 240 – 255 | Reserved        |
## 6. Subnetting
Dividing a large network into smaller networks.
### Why?
- Improves performance
- Enhances security
- Efficient IP usage
#### Example:
- Network: `192.168.1.0/24`
- Can be divided into multiple smaller subnets
## 7. Packet Structure (IP Datagram)
Main fields:
- Source IP
- Destination IP
- Header
- Data (payload)
## 8. Routing
Routing is the process of selecting the best path for data.
- Done by **routers**
- Uses routing protocols like:
  - RIP
  - OSPF
  - BGP
## 9. Important Supporting Protocols
- **ARP** – IP → MAC mapping
- **RARP** – MAC → IP (obsolete)
- **ICMP** – Error reporting (used in ping)
- **DHCP** – Automatically assigns IP addresses
## 10. Key Points to Remember
- IP is **connectionless** (no guaranteed delivery)
- Works with **TCP/UDP** for transport
- Core function: **Addressing + Routing**

# ICMP
