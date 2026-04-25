# Internet Addresses concepts
Internet addressing is the system used to uniquely identify devices and services on a network (especially the Internet) so that data can be sent and received correctly. It mainly involves **IP addresses, port numbers, and domain names**.
## 1. IP Address (Internet Protocol Address)
An **IP address** uniquely identifies a device (computer, phone, router) on a network.
### Types of IP Addresses:
#### IPv4 Address
<img width="1024" height="718" alt="image" src="https://github.com/user-attachments/assets/31d761ba-865e-4631-9f23-eabf52e01220" />
<img width="604" height="372" alt="image" src="https://github.com/user-attachments/assets/e98ace86-5432-41e1-bdb3-dc183de3ce14" />

- 32-bit address
- Written in **dotted decimal format** (e.g., `192.168.1.1`)
- Divided into network part + host part
##### Example:
- `192.168.1.1`
## IPv6 Address
<img width="800" height="400" alt="image" src="https://github.com/user-attachments/assets/17b4f2f5-ecad-4198-ad57-ecd108bcc388" />

- 128-bit address
- Written in **hexadecimal** separated by colons
- Supports a very large number of devices
### Example:
- `2001:0db8:85a3:0000:0000:8a2e:0370:7334`
## 2. Port Address
- Identifies a **specific application or service** running on a device
- Works along with IP address
### Example:
- `192.168.1.1:80` → Web server (HTTP)
- `192.168.1.1:443` → Secure web (HTTPS)
### Common Port Numbers:
- 80 → HTTP
- 443 → HTTPS
- 21 → FTP
- 25 → SMTP
## 3. Domain Name System (DNS)
<img width="936" height="392" alt="image" src="https://github.com/user-attachments/assets/7d37a732-0d57-4772-8308-38e1b5bd861f" />

- Humans prefer names like `www.google.com`
- Computers use IP addresses
- **DNS converts domain names into IP addresses**
### Example:
- `www.google.com` → `142.250.x.x`
## 4. URL (Uniform Resource Locator)
A **URL** specifies the exact location of a resource on the Internet.
### Structure:
```
protocol://domain_name:port/path
```
### Example:
```
https://www.example.com:443/index.html
```
- **Protocol** → HTTP / HTTPS / FTP
- **Domain name** → Website name
- **Port** → Optional service identifier
- **Path** → Specific resource
## 5. MAC Address (Physical Address)
- A **hardware address** assigned to network interfaces
- Used in **local network communication**
- 48-bit address
### Example:
- `00:1A:2B:3C:4D:5E`
## Summary
- **IP Address** → Identifies device
- **Port Address** → Identifies service
- **Domain Name** → Human-readable name
- **URL** → Complete address of resource
- **MAC Address** → Physical hardware identifier

# IP Address vs H/W address (unicast/broadcast/multicast)
## IP Address vs H/W (MAC) Address
### IP Address (Logical Address)
- Assigned by network (can change)
- Works at **Network Layer (Layer 3)**
- Used for **end-to-end communication across networks**
- Example: `192.168.1.1`
#### Think: “Where is the device in the network?”
## H/W Address (MAC Address)
- Assigned by manufacturer (usually fixed)
- Works at **Data Link Layer (Layer 2)**
- Used for **communication within local network (LAN)**
- Example: `00:1A:2B:3C:4D:5E`
### Think: “Who exactly is the device?”
## Key Differences
| Feature    | IP Address                     | MAC Address                 |
| ---------- | ------------------------------ | --------------------------- |
| Type       | Logical address                | Physical (hardware) address |
| Layer      | Network Layer                  | Data Link Layer             |
| Size       | 32-bit (IPv4) / 128-bit (IPv6) | 48-bit                      |
| Assignment | By network/admin               | By manufacturer             |
| Changeable | Yes                            | No (generally fixed)        |
| Scope      | Global (Internet)              | Local (LAN)                 |
## Addressing Types (Unicast / Broadcast / Multicast)
### 1. Unicast (One-to-One)
- Data sent from **one sender → one receiver**
- Most common communication type
#### Example:
Opening a website (your device ↔ server)
## 2. Broadcast (One-to-All)
- Data sent from **one sender → all devices in network**
- Used in **LAN only**
### Example:
ARP request → “Who has this IP?”
- MAC broadcast address: `FF:FF:FF:FF:FF:FF`
## 3. Multicast (One-to-Group)
- Data sent from **one sender → selected group**
- Efficient for group communication
### Example:
Live video streaming to multiple users
## Quick Comparison
| Type      | Communication      | Example        |
| --------- | ------------------ | -------------- |
| Unicast   | One → One          | Web browsing   |
| Broadcast | One → All          | ARP request    |
| Multicast | One → Many (group) | Live streaming |
## Final Concept Link
- **IP Address → identifies location**
- **MAC Address → identifies device**
- **Unicast/Broadcast/Multicast → defines how data is sent**

# Subnetting/Supernetting
## Subnetting
### What is Subnetting?
Subnetting is the process of **dividing one large network into smaller networks (subnets)**.
- Done by **borrowing bits from the host par**t of an IP address.
## Why Subnetting?
- Improves **network performance** (less traffic)
- Enhances **security** (isolation of networks)
- Efficient use of IP addresses
- Easier **network management**
## Example
- Original network: `192.168.1.0/24`
- After subnetting:
  - `192.168.1.0/26`
  - `192.168.1.64/26`
  - `192.168.1.128/26`
  - `192.168.1.192/26`
- Here, `/26` means more bits used for network → **more subnets, fewer hosts**
## Key Idea
- **More subnet bits → More subnets, fewer hosts per subnet**
## Supernetting (CIDR – Classless Inter-Domain Routing)
### What is Supernetting?
Supernetting is the process of **combining multiple smaller networks into one larger network**.
- Done by **reducing network bits (adding host bits)**
## Why Supernetting?
- Reduces **routing table size**
- Improves **routing efficiency**
- Used in **Internet routing (CIDR)**
## Example
Combine:
- `192.168.0.0/24`
- `192.168.1.0/24`
### Supernet:
- `192.168.0.0/23`
## Key Idea
- **Fewer network bits → Larger network, more hosts**
## Subnetting vs Supernetting
| Feature           | Subnetting       | Supernetting (CIDR) |
| ----------------- | ---------------- | ------------------- |
| Purpose           | Divide network   | Combine networks    |
| Bits Used         | Borrow host bits | Reduce network bits |
| Result            | Smaller networks | Larger network      |
| Hosts per Network | Decreases        | Increases           |
| Routing           | More entries     | Fewer entries       |
## Easy Memory Trick
- **Subnetting = “Split” network**
- **Supernetting = “Merge” networks**
## Final Concept
- Subnetting → Efficient **internal network design**
- Supernetting → Efficient **Internet routing (CIDR)**

# Switching
## Switching in Computer Networks
### What is Switching?
Switching is the technique of **transferring data from source to destination through intermediate nodes (switches)**.
- It ensures data reaches the correct device efficiently.
## Types of Switching
### 1. Circuit Switching
- A **dedicated path** is established before communication starts
- Path remains reserved until communication ends
#### Features:
- Fixed bandwidth
- No delay after connection setup
- Inefficient (resources reserved even if idle)
#### Example:
- Traditional telephone networks (like PSTN)
##### Think: Call connection (fixed path)
## 2. Packet Switching
- Data is broken into **small packets**
- Each packet travels **independently**
- Packets may take different paths
### Features:
- Efficient use of bandwidth
- No dedicated path
- Possible delay, packet loss, or reordering
### Example:
- Internet communication using TCP/IP
#### Think: Sending WhatsApp messages (split & sent separately)
## 3. Message Switching
- Entire message is sent **as one unit**
- No need for dedicated path
- Uses **store-and-forward technique**
### Features:
- High delay (stores full message before forwarding)
- Not used in modern networks
#### Think: Email (store then forward)
## Comparison of Switching Techniques
| Feature    | Circuit Switching  | Packet Switching | Message Switching |
| ---------- | ------------------ | ---------------- | ----------------- |
| Path       | Dedicated          | No fixed path    | No fixed path     |
| Data Unit  | Continuous stream  | Packets          | Entire message    |
| Delay      | Low after setup    | Variable         | High              |
| Efficiency | Low                | High             | Moderate          |
| Usage      | Telephone networks | Internet         | Obsolete          |
## Key Points
- **Switching = Data transfer via intermediate nodes**
- **Circuit switching → fixed path**
- **Packet switching → flexible, efficient**
- **Message switching → outdated**
## Final Concept
Modern networks (like the Internet) mainly use **packet switching** because it is **fast, efficient, and scalable**.

# ARP/RARP
## ARP (Address Resolution Protocol)
<img width="346" height="401" alt="image" src="https://github.com/user-attachments/assets/7ed4719a-f686-4e38-98e2-3158cdf95066" />

### What is ARP?
ARP is used to **find the MAC (hardware) address from a known IP address**.
- Works within a **local network (LAN)**
## How ARP Works (Step-by-Step)
1. Device knows **IP address**, but not MAC
2. Sends **ARP Request (broadcast)** → “Who has this IP?”
3. All devices receive it
4. Target device replies with its **MAC address (unicast)**
5. Sender stores it in **ARP cache**
## Example
- IP: `192.168.1.10`
- MAC found: `00:1A:2B:3C:4D:5E`
## Key Points
- Uses **broadcast (request)** and **unicast (reply)**
- Operates between **Network & Data Link layer**
- Maintains **ARP table (cache)**
## RARP (Reverse Address Resolution Protocol)
<img width="801" height="400" alt="image" src="https://github.com/user-attachments/assets/d2835d4b-c73e-47b0-b149-1d37e7dadee5" />

### What is RARP?
RARP is used to **find the IP address from a known MAC address**.
## How RARP Works
1. Device knows its **MAC address**
2. Sends **RARP request** to server
3. RARP server replies with **IP address**
## Usage
- Used by **diskless workstations** at startup
- Now mostly replaced by newer protocols like DHCP
## ARP vs RARP
| Feature       | ARP                         | RARP                                |
| ------------- | --------------------------- | ----------------------------------- |
| Full Form     | Address Resolution Protocol | Reverse Address Resolution Protocol |
| Purpose       | IP → MAC                    | MAC → IP                            |
| Direction     | Logical → Physical          | Physical → Logical                  |
| Usage         | Commonly used               | Rare/obsolete                       |
| Communication | Broadcast + Unicast         | Server-based                        |
## Easy Memory Trick
- **ARP → Ask MAC from IP**
- **RARP → Reverse (IP from MAC)**
## Final Concept
- ARP is **essential for everyday networking (LAN communication)**
- RARP is **outdated and replaced by DHCP**
