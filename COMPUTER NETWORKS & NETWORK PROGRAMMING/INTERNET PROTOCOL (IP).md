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
## Routing Concepts (Computer Networks)
Routing is the process of **selecting the best path** for data (packets) to travel from source to destination across interconnected networks.
## What is Routing?
- Performed by **routers**
- Uses **IP addresses** to forward packets
- Ensures data reaches the correct destination efficiently
## How Routing Works
<img width="980" height="1074" alt="image" src="https://github.com/user-attachments/assets/0cabb54c-a256-411c-845c-64a8ecc27ffc" />

### Steps:
1. Sender sends packet with destination IP
2. Router checks its **routing table**
3. Chooses the best path
4. Forwards packet to next router
5. Process continues until destination is reached
## Routing Table
A **routing table** is a list stored in routers containing:
- Destination network
- Next hop (next router)
- Metric (cost of path)
- Interface to use
* It is like a **map** for routers
## Types of Routing
### 1. Static Routing
- Routes are **manually configured**
- No automatic updates
* Simple but not scalable
* Used in small networks
## 2. Dynamic Routing
- Routes are **automatically updated**
- Routers communicate with each other
* Suitable for large networks
* Adapts to failures
## 3. Default Routing
- Used when no specific route is found
- Packet is sent to a **default gateway**
## Routing Algorithms
### Distance Vector Routing
- Shares routing table with neighbors
- Example: **RIP**
- Uses **hop count** as metric
### Link State Routing
- Builds full network topology
- Uses shortest path algorithm
#### Example protocols:
- **OSPF**
- **IS-IS**
## Routing Protocols
### Interior Gateway Protocols (IGP)
Used **within a network (Autonomous System)**:
- RIP
- OSPF
- EIGRP
### Exterior Gateway Protocol (EGP)
Used **between networks**:
- BGP (used on the Internet)
## Key Routing Terms
- **Hop** → One router to another
- **Metric** → Cost of path (hop count, bandwidth, delay)
- **Next Hop** → Next router in path
- **Convergence** → Time taken for routers to update routes
## Routing vs Forwarding
- **Routing** → Decides path (control plane)
- **Forwarding** → Sends packet to next hop (data plane)

# Autonomous systems
## Autonomous Systems (AS) in Computer Networks
An **Autonomous System (AS)** is a collection of IP networks and routers under a **single administrative control** that follow a common routing policy.
### In simple terms:
A large network (like an ISP or organization) managed by one entity.
## Real-World Idea
- Each ISP (like Airtel, Jio) is an **Autonomous System**
- Big companies (Google, Amazon) also have their own AS
- The entire Internet = **many AS connected together**
## How Autonomous Systems Work
- Each AS has:
  - Its own routers
  - Internal routing protocol
- AS communicate with each other using special protocols
## Autonomous System Number (ASN)
- Every AS has a unique **ASN (Autonomous System Number)**
- Used to identify AS on the Internet
### Example:
- AS15169 → Google
- AS16509 → Amazon
## Types of Autonomous Systems
### 1. Stub AS
- Connected to only **one other AS**
- No transit traffic
* Example: Small organization network
## 2. Multihomed AS
- Connected to **multiple AS**
- Does not allow transit traffic
* Improves reliability
## 3. Transit AS
- Connected to multiple AS
- Allows traffic to pass through
* Example: Internet Service Providers (ISPs)
## Routing Inside vs Between AS
### Intra-AS Routing (Within AS)
- Uses **Interior Gateway Protocols (IGP)**
  - RIP
  - OSPF
  - EIGRP
## Inter-AS Routing (Between AS)
- Uses **Exterior Gateway Protocol (EGP)**
### Most important protocol:
- **BGP (Border Gateway Protocol)**
## Role of BGP
- Connects different AS
- Decides best path based on:
  - Policies
  - Path length
  - Network rules
* BGP is the **backbone of the Internet**
## Key Components
- **Border Routers (Edge Routers)**
  - Connect one AS to another
- **AS Path**
  - List of AS numbers a packet travels through
## Example Flow
1. Data leaves your ISP (AS1)
2. Travels through multiple AS (AS2, AS3)
3. Reaches destination AS

# Routing Algorithms
## Routing Algorithms (Computer Networks)
Routing algorithms determine **how routers choose the best path** for forwarding packets from source to destination.
- Goal: **Efficient, fast, and reliable data delivery**
## How Routing Algorithms Work
- Network is viewed as a **graph**
  - Routers → Nodes
  - Links → Edges
- Each link has a **cost (metric)**
- Algorithm finds the **shortest/optimal path**
## Classification of Routing Algorithms
### 1. Static vs Dynamic
- **Static Routing Algorithm**
  - Manually configured
  - No automatic updates
- **Dynamic Routing Algorithm**
  - Automatically updates routes
  - Adapts to network changes
## Main Types of Routing Algorithms
## 1. Distance Vector Routing
### Concept:
- Each router shares its **routing table with neighbors**
- Uses **Bellman-Ford algorithm**
### Features:
- Simple
- Uses **hop count** as metric
- Periodic updates
### Example Protocol:
- RIP (Routing Information Protocol)
### Problems:
- Slow convergence
- Count-to-infinity issue
## 2. Link State Routing
### Concept:
- Each router builds a **complete map of the network**
- Uses **Dijkstra’s algorithm**
### Features:
- Faster convergence
- More accurate
- Uses **Link State Advertisements (LSA)**
### Example Protocol:
- OSPF (Open Shortest Path First)
## 3. Path Vector Routing
### Concept:
- Maintains **entire path (list of AS)**
- Used for inter-domain routing
### Features:
- Avoids loops
- Policy-based routing
### Example Protocol:
- BGP (Border Gateway Protocol)
## Comparison of Algorithms
| Feature   | Distance Vector | Link State    | Path Vector |
| --------- | --------------- | ------------- | ----------- |
| Knowledge | Neighbor only   | Full topology | Path info   |
| Algorithm | Bellman-Ford    | Dijkstra      | Path-based  |
| Speed     | Slow            | Fast          | Moderate    |
| Example   | RIP             | OSPF          | BGP         |
## Key Terms
- **Metric** → Cost of path (hop, delay, bandwidth)
- **Convergence** → Time to update routing info
- **Loop** → Packet circulates endlessly
- **Scalability** → Works for large networks

# Routing protocols
## Routing Protocols (Computer Networks)
**Routing protocols** are rules and procedures that routers use to **exchange information and determine the best path** for forwarding data across networks.
- Without routing protocols, routers wouldn’t know **where to send packets**.
## Why Routing Protocols are Needed
- Automatically discover routes
- Adapt to network changes (failures, congestion)
- Maintain updated **routing tables**
- Choose optimal path using metrics
## How Routing Protocols Work
- Routers **communicate with each other**
- Share routing information
- Update routing tables dynamically
- Select best path based on algorithm
## Classification of Routing Protocols
## 1. Interior Gateway Protocols (IGP)
Used **within an Autonomous System (AS)**
### RIP
- Type: Distance Vector
- Metric: Hop count
- Max hops: 15
- Simple but slow
## OSPF
- Type: Link State
- Uses Dijkstra algorithm
- Fast convergence
- Suitable for large networks
## EIGRP
- Type: Hybrid
- Combines Distance Vector + Link State features
- Faster and efficient
## 2. Exterior Gateway Protocol (EGP)
Used **between Autonomous Systems**
### BGP
- Type: Path Vector
- Used on the Internet
- Maintains AS path
- Policy-based routing
## Types Based on Algorithm
| Protocol | Algorithm       |
| -------- | --------------- |
| RIP      | Distance Vector |
| OSPF     | Link State      |
| EIGRP    | Hybrid          |
| BGP      | Path Vector     |
## Key Metrics Used
- Hop count
- Bandwidth
- Delay
- Reliability
- Cost
## Important Concepts
### Convergence
- Time taken for all routers to update routes
### Scalability
- Ability to handle large networks
### Loop Prevention
- Avoid packets circulating endlessly
## Quick Comparison
| Feature | RIP             | OSPF           | EIGRP      | BGP         |
| ------- | --------------- | -------------- | ---------- | ----------- |
| Type    | Distance Vector | Link State     | Hybrid     | Path Vector |
| Speed   | Slow            | Fast           | Very Fast  | Moderate    |
| Use     | Small networks  | Large networks | Enterprise | Internet    |

# Interior/Exterior routing protocols
## Interior vs Exterior Routing Protocols
Routing protocols are broadly classified based on **where they operate:**
- **Interior Routing Protocols (IGP)** → within an Autonomous System
- **Exterior Routing Protocols (EGP)** → between Autonomous Systems
## 1. Interior Gateway Protocols (IGP)
- Used **inside a single Autonomous System (AS)**
- Managed by **one organization** (like a company network or ISP internal network)
### Common IGP Protocols
- **RIP**
  - Distance Vector
  - Uses hop count
  - Suitable for small networks
- **OSPF**
  - Link State
  - Uses shortest path (Dijkstra)
  - Fast and scalable
- **EIGRP**
  - Hybrid
  - Very fast convergence
  - Used in enterprise networks
## How IGP Works
- Routers share routing info **within the same AS**
- Maintain internal routing tables
- Choose best path using metrics
## 2. Exterior Gateway Protocols (EGP)
- Used **between different Autonomous Systems**
- Connects **large networks (Internet)**
### Main EGP Protocol
- **BGP**
  - Path Vector protocol
  - Maintains **AS path**
  - Policy-based routing
  - Backbone of the Internet
## How EGP Works
- Exchanges routing info between AS
- Uses **AS numbers (ASN)**
- Selects best route based on policies
## Key Differences (IGP vs EGP)
| Feature           | IGP              | EGP                   |
| ----------------- | ---------------- | --------------------- |
| Scope             | Within AS        | Between AS            |
| Example Protocols | RIP, OSPF, EIGRP | BGP                   |
| Algorithm         | DV / LS / Hybrid | Path Vector           |
| Speed             | Faster           | Slower (policy-based) |
| Complexity        | Lower            | Higher                |
| Use Case          | Internal routing | Internet routing      |
## Simple Analogy
- **IGP** → Roads inside a city 
- **EGP (BGP)** → Highways connecting cities

# Unicast/Multicast Routing protocols
## Unicast vs Multicast Routing Protocols
Routing can be classified based on **how data is delivered**:
- **Unicast Routing** → one sender → one receiver
- **Multicast Routing** → one sender → multiple selected receivers (group)
## 1. Unicast Routing Protocols
- Used for **one-to-one communication**
### How it Works
- Packet is sent from **source → single destination**
- Routers forward based on **destination IP address**
- Each destination requires a **separate packet**
## Examples of Unicast Routing Protocols
- **RIP**
- **OSPF**
- **EIGRP**
- **BGP**
## Features
- Most common routing type
- Used in:
  - Web browsing
  - Email
  - File transfer
## 2. Multicast Routing Protocols
- Used for one-to-many communication (group communication)
### How it Works
- Sender sends **one packet**
- Network creates a **distribution tree**
- Packet is delivered only to **group members**
## Examples of Multicast Routing Protocols
- **DVMRP**
- **PIM**
- **MOSPF**
## Features
- Efficient (saves bandwidth)
- Uses **multicast group addresses**
- Builds **multicast trees**
## Key Differences
| Feature         | Unicast                  | Multicast                          |
| --------------- | ------------------------ | ---------------------------------- |
| Communication   | One-to-one               | One-to-many (group)                |
| Bandwidth Usage | High (duplicate packets) | Efficient (single stream)          |
| Routing Path    | Single path              | Tree structure                     |
| Use Cases       | Web, email               | Live streaming, video conferencing |
## Simple Example
- **Unicast** → Sending a message to one friend
- **Multicast** → Sending one message to a WhatsApp group

# IGMP
## IGMP (Internet Group Management Protocol)
**IGMP** is a protocol used in IP networks to manage **multicast group membership**.
- In simple terms:
###
It tells routers **which devices want to receive multicast data** (like live streaming).
## Why IGMP is Needed
In multicast communication:
- Data is sent to a **group address**, not individual devices
- Routers must know **who is interested**
### IGMP helps routers:
- Add devices to a multicast group
- Remove devices from the group
- Avoid sending unwanted traffic
## How IGMP Works
<img width="547" height="585" alt="image" src="https://github.com/user-attachments/assets/d197b4d8-48f8-4a10-99dc-0ed64f70e5a0" />

### Step-by-step:
1. Host wants to join a multicast group
2. Host sends **IGMP Membership Report (Join)**
3. Router records membership
4. Router forwards multicast traffic to that host
#### When leaving:
- Host sends **Leave message**
- Router stops forwarding traffic
## IGMP Message Types
### 1. Membership Query
- Sent by router
- Asks: “Who wants multicast data?”
## 2. Membership Report
- Sent by host
- Says: “I want to join this group”
## 3. Leave Group
- Sent by host
- Says: “I no longer need this data”
## IGMP Versions
| Version | Features                           |
| ------- | ---------------------------------- |
| IGMPv1  | Basic membership management        |
| IGMPv2  | Adds Leave message                 |
| IGMPv3  | Supports source-specific multicast |
## IGMP and Multicast Routing
- IGMP works between:
  - **Host ↔ Router**
- Multicast routing protocols (like PIM) work between:
  - **Router ↔ Router**
### So:
- IGMP = group membership
- Multicast routing = data delivery
## Key Characteristics
- Works at **Network Layer**
- Uses **multicast IP addresses**
- Does not route data itself
- Only manages group membership
## Real-Life Example
- Watching a live cricket match on Hotstar
- Your device joins a multicast group
- IGMP tells router to send that stream to you

