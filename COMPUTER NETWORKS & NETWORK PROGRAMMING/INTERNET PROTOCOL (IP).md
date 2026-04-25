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
## ICMP (Internet Control Message Protocol)
**ICMP** is a supporting protocol used in IP networks for **error reporting and diagnostics**. It helps devices understand what went wrong during communication.
- Works at the **Network Layer**
- Used along with IP (not a transport protocol like TCP/UDP)
- Mainly for **control and troubleshooting**, not for sending actual data
## Why ICMP is Needed
IP is **connectionless** and doesn’t guarantee delivery. So ICMP is used to:
- Report errors (e.g., destination unreachable)
- Check network connectivity
- Provide feedback about packet delivery
## How ICMP Works
<img width="1320" height="660" alt="image" src="https://github.com/user-attachments/assets/c7bd0e45-eec3-447a-91e5-84c6d7937671" />

Example:
1. Device A sends data to Device B
2. If something fails, router/device sends an **ICMP message back**
3. This message explains the issue
## Common ICMP Message Types
### 1. Echo Request & Echo Reply
- Used by **ping command**
- Checks if a host is reachable
#### Example:
```
ping google.com
```
## 2. Destination Unreachable
- Sent when packet cannot reach destination
- Reasons:
  - Network unreachable
  - Host unreachable
  - Port unreachable
## 3. Time Exceeded
- When packet’s **TTL (Time To Live)** becomes zero
- Used in **traceroute**
## 4. Redirect Message
- Router tells host to use a better route
## 5. Parameter Problem
- Error in IP header
## ICMP Packet Format
<img width="3401" height="1695" alt="image" src="https://github.com/user-attachments/assets/12aebe16-3722-44a2-99b2-2e4c3238b3e3" />

Main fields:
- **Type** → Defines message type
- **Code** → Gives more details
- **Checksum** → Error checking
- **Data** → Extra information
## Real-Life Tools Using ICMP
### Ping
- Uses Echo Request & Reply
- Tests connectivity
### Traceroute
- Uses Time Exceeded messages
- Finds path to destination
## Key Characteristics
- Connectionless
- No port numbers
- Encapsulated inside IP packet
- Used for **diagnostics, not data transfer**

# Routing concepts
