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
