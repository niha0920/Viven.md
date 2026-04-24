# Line configurations
**Line configurations** refer to the way communication devices are physically or logically connected using a communication link in a network. It defines how many devices can share a link and how they communicate.
- There are **two main types of line configurations**:
## 1. Point-to-Point Line Configuration
<img width="700" height="365" alt="image" src="https://github.com/user-attachments/assets/98d2ba0c-5b54-4c41-93f0-a42dd7d02a1d" />

### Definition
A **point-to-point** connection provides a **dedicated link between two devices only**.
### Key Features
- Direct connection between two devices
- Full bandwidth available to those two devices
- Simple and fast communication
- More secure (no sharing)
### Examples
- Connection between a computer and printer
- Telephone line between two phones
- Serial cable connection between two systems
### Advantages
- High performance
- Easy to troubleshoot
- Secure communication
### Disadvantages
- Expensive if many devices need connections
- Not scalable
## 2. Multipoint (Multidrop) Line Configuration
<img width="941" height="439" alt="image" src="https://github.com/user-attachments/assets/75e2cd0d-212c-4bf5-89a8-15156f5774df" />

### Definition
A **multipoint** connection allows **multiple devices to share a single communication link**.
### Key Features
- One link shared among many devices
- Bandwidth is divided among devices
- Requires coordination (time-sharing or polling)
### Examples
- Bus topology network
- Wireless networks (Wi-Fi shared medium)
- Old mainframe terminals
### Advantages
- Cost-effective
- Efficient use of resources
### Disadvantages
- Lower performance due to sharing
- Security concerns
- Complex management
## Key Difference
| Feature     | Point-to-Point | Multipoint  |
| ----------- | -------------- | ----------- |
| Devices     | 2 only         | Multiple    |
| Link        | Dedicated      | Shared      |
| Performance | High           | Lower       |
| Cost        | High           | Low         |
| Security    | More secure    | Less secure |

# Network topologies
**Network topology** refers to the **physical or logical arrangement of devices (nodes) and connections (links)** in a network. It defines how devices are connected and how data flows.
## Types of Network Topologies
## 1. Bus Topology
<img width="960" height="720" alt="image" src="https://github.com/user-attachments/assets/e966085c-fe06-4f64-a73d-00159448f87b" />

### Description
All devices are connected to a **single main cable (backbone)**.
### Features
- Data travels in both directions
- Terminators are used at both ends
- Simple design
### Advantages
- Easy to install
- Low cost
### Disadvantages
- Backbone failure = entire network down
- Difficult to troubleshoot
- Performance drops with more devices
## 2. Star Topology
<img width="4449" height="3440" alt="image" src="https://github.com/user-attachments/assets/f1c7022e-7f56-45f6-96e3-1792992ace8d" />

### Description
All devices connect to a **central device** (hub/switch).
### Features
- Centralized control
- Easy to add/remove devices
### Advantages
- Easy troubleshooting
- Failure of one device doesn’t affect others
### Disadvantages
- Central device failure = network failure
- More cabling required
## 3. Ring Topology
<img width="541" height="421" alt="image" src="https://github.com/user-attachments/assets/5b3f87a4-4fdc-492d-9888-44b611e338ee" />

### Description
Devices are connected in a **circular loop**.
### Features
- Data travels in one direction (or both in dual ring)
- Uses token passing
### Advantages
- No data collision
- Predictable performance
### Disadvantages
- Break in one link affects entire network
- Difficult to reconfigure
## 4. Mesh Topology
<img width="768" height="549" alt="image" src="https://github.com/user-attachments/assets/350b5540-152b-4ce8-9f71-e643bfc8529f" />

### Description
Each device is connected to **multiple or all other devices**.
### Features
- Redundant paths
- High reliability
### Advantages
- Fault tolerant
- No single point of failure
### Disadvantages
- Expensive
- Complex installation
## 5. Tree Topology
<img width="700" height="400" alt="image" src="https://github.com/user-attachments/assets/441219f5-dee9-40b5-8bf4-fa34cf86146f" />

### Description
A **hierarchical combination of star and bus topologies**.
### Features
- Root node with branches
- Scalable structure
### Advantages
- Easy expansion
- Structured management
### Disadvantages
- Backbone failure affects segments
- Complex setup
## 6. Hybrid Topology
<img width="673" height="494" alt="image" src="https://github.com/user-attachments/assets/c2cf2a2c-fecd-41a0-b59b-72eeccf420a8" />

### Description
Combination of **two or more different topologies**.
### Features
- Flexible design
- Used in large networks
### Advantages
- Highly scalable
- Reliable
### Disadvantages
- Expensive
- Complex design
## Quick Comparison
| Topology | Structure       | Main Advantage   | Main Disadvantage       |
| -------- | --------------- | ---------------- | ----------------------- |
| Bus      | Single cable    | Low cost         | Backbone failure        |
| Star     | Central hub     | Easy management  | Hub failure             |
| Ring     | Circular        | No collision     | One break stops network |
| Mesh     | Fully connected | High reliability | Expensive               |
| Tree     | Hierarchical    | Scalable         | Complex                 |
| Hybrid   | Mixed           | Flexible         | Costly                  |

# Networking and internetworking devices
**Networking and internetworking devices** are hardware components used to **connect computers and networks**, enabling communication and data transfer.
- **Networking devices** → connect devices **within the same network (LAN)**
- **Internetworking devices** → connect **different networks (LAN ↔ WAN)**
## Networking Devices (Within a Network)
## 1. Repeater
<img width="600" height="358" alt="image" src="https://github.com/user-attachments/assets/2f4b9620-6d2d-4f71-89ef-a3fdf3b7c0f9" />

### Function
Regenerates and amplifies weak signals.
### Key Points
- Works at **Physical Layer (OSI Layer 1)**
- Extends transmission distance
- No filtering or intelligence
## 2. Hub
<img width="1639" height="1012" alt="image" src="https://github.com/user-attachments/assets/b9c923a5-659e-481a-91cf-f5392af953bb" />

### Function
Connects multiple devices and **broadcasts data to all ports**.
### Key Points
- Also works at **Physical Layer**
- No data filtering
- Causes collisions
## 3. Bridge
<img width="708" height="532" alt="image" src="https://github.com/user-attachments/assets/b79bebe3-0aca-4da7-9500-88693af3a25d" />

### Function
Connects two LAN segments and filters traffic.
### Key Points
- Works at **Data Link Layer (Layer 2)**
- Uses **MAC addresses**
- Reduces collisions
## 4. Switch
<img width="1192" height="976" alt="image" src="https://github.com/user-attachments/assets/298b4b50-c56e-45b8-bd9e-2430348fd429" />

### Function
Connects devices and sends data **only to the intended device**.
### Key Points
- Works at **Layer 2 (sometimes Layer 3)**
- Uses MAC address table
- Faster and more efficient than hub
## Internetworking Devices (Between Networks)
## 5. Router
<img width="420" height="476" alt="image" src="https://github.com/user-attachments/assets/bf83c231-342d-4898-bea7-599fb6ef4a74" />

### Function
Connects different networks and routes data packets.
### Key Points
- Works at **Network Layer (Layer 3)**
- Uses **IP addresses**
- Determines best path
## 6. Gateway
<img width="457" height="577" alt="image" src="https://github.com/user-attachments/assets/dffd6ad8-94da-4b03-9fd7-e5bdc071fa9f" />

### Function
Acts as a **protocol converter** between different networks.
### Key Points
- Works across **all OSI layers**
- Connects dissimilar systems
- Example: Email gateway
## 7. Modem (Modulator-Demodulator)
<img width="998" height="558" alt="image" src="https://github.com/user-attachments/assets/7dc554c9-761e-446e-8714-c88108985475" />
<img width="560" height="344" alt="image" src="https://github.com/user-attachments/assets/d31e3cc1-6154-4e3d-ab23-091979d16f6d" />

### Function
Converts **digital signals ↔ analog signals**.
### Key Points
- Used for internet access
- Example: DSL, Cable modem
## 8. Access Point (AP)
<img width="750" height="333" alt="image" src="https://github.com/user-attachments/assets/a23c61f2-7854-4ff8-b5e2-af6e237d0f22" />

### Function
Provides **wireless connectivity** to devices.
### Key Points
- Extends wired network to wireless
- Used in Wi-Fi networks
## Summary Table
| Device       | Type            | OSI Layer  | Function                 |
| ------------ | --------------- | ---------- | ------------------------ |
| Repeater     | Networking      | Layer 1    | Signal regeneration      |
| Hub          | Networking      | Layer 1    | Broadcast data           |
| Bridge       | Networking      | Layer 2    | Filters traffic          |
| Switch       | Networking      | Layer 2/3  | Intelligent forwarding   |
| Router       | Internetworking | Layer 3    | Routing between networks |
| Gateway      | Internetworking | All layers | Protocol conversion      |
| Modem        | Internetworking | Layer 1    | Signal conversion        |
| Access Point | Networking      | Layer 2    | Wireless access          |
## Quick Understanding
- **Same network?** → Use **Hub / Switch / Bridge**
- **Different networks?** → Use **Router / Gateway**
- **Wireless?** → Use **Access Point**
- **Long distance signal?** → Use **Repeater**

# LAN, MAN, WAN
**LAN, MAN, and WAN** are categories of computer networks based on their **geographical coverage, size, and purpose**.
## 1. Local Area Network (LAN)
<img width="518" height="430" alt="image" src="https://github.com/user-attachments/assets/98e661a1-87cd-4c41-a50b-1505d13dd64e" />

### Definition
A **LAN (Local Area Network)** connects devices within a **small geographic area** like a room, building, or campus.
### Examples
- Home Wi-Fi network
- Office network
- Computer lab in a college
### Characteristics
- High speed (100 Mbps to several Gbps)
- Low latency
- Privately owned
- Uses Ethernet or Wi-Fi
### Devices Used
- Switch
- Router
- Access Point
### Advantages
- Fast communication
- Easy resource sharing (printers, files)
- Low cost
### Disadvantages
- Limited coverage
- Requires maintenance
## 2. Metropolitan Area Network (MAN)
<img width="913" height="736" alt="image" src="https://github.com/user-attachments/assets/90aa40d6-b5f3-47d1-b81d-30a15e92abaf" />

### Definition
A **MAN (Metropolitan Area Network)** covers a **city or large town**.
### Examples
- City-wide internet service
- Cable TV network
- Smart city infrastructure
### Characteristics
- Medium to high speed
- Covers larger area than LAN
- Usually managed by service providers
### Technologies Used
- Fiber optic cables
- Microwave links
### Advantages
- Connects multiple LANs
- High data transfer rates
### Disadvantages
- Expensive
- Complex to manage
## 3. Wide Area Network (WAN)
### Definition
A **WAN (Wide Area Network)** spans **large geographic areas**, such as countries or continents.
### Examples
- The Internet
- Bank networks
- Airline reservation systems
### Characteristics
- Slower than LAN (but improving with technology)
- High latency compared to LAN
- Uses public and private infrastructure
### Technologies Used
- Satellites
- Leased lines
- MPLS
### Advantages
- Global connectivity
- Supports large-scale communication
### Disadvantages
- High cost
- Complex setup and maintenance
- Security concerns
## Key Differences
| Feature   | LAN                   | MAN            | WAN           |
| --------- | --------------------- | -------------- | ------------- |
| Coverage  | Small (room/building) | City           | Country/World |
| Speed     | Very High             | High           | Moderate      |
| Ownership | Private               | Public/Private | Mostly Public |
| Cost      | Low                   | Medium         | High          |
| Example   | Office network        | City network   | Internet      |
## Quick Memory Trick
- **LAN** → Local (small area)
- **MAN** → Metropolitan (city)
- **WAN** → Wide (global)

# Typical media and Protocols used in each
You’re usually expected to map **each network type (LAN, MAN, WAN)** to the **transmission media** and the **protocols/technologies** commonly used.
## LAN (Local Area Network)
### Typical Media
- **Twisted Pair Cable (UTP/STP)** – most common (Cat5e, Cat6)
- **Fiber Optic Cable** – used in high-speed LANs
- **Wireless (Wi-Fi)** – radio waves
### Protocols / Technologies
- **Ethernet (IEEE 802.3**) – wired LAN standard
- **Wi-Fi (IEEE 802.11)** – wireless LAN
- **ARP (Address Resolution Protocol)**
- **IP (Internet Protocol)**
- **TCP/UDP**
### Key Idea
- High-speed, short distance → simple and fast technologies
## MAN (Metropolitan Area Network)
### Typical Media
- **Fiber Optic Cabl**e – primary medium
- **Microwave Links** – for wireless city connections
- **Coaxial Cable** (older systems)
### Protocols / Technologies
- **Metro Ethernet**
- **MPLS (Multiprotocol Label Switching)**
- **ATM (Asynchronous Transfer Mode) (older)**
- **Frame Relay** (legacy)
### Key Idea
- Connects multiple LANs across a city using high-capacity backbone
## WAN (Wide Area Network)
### Typical Media
- **Fiber Optic (submarine cables, long-distance)**
- **Satellite Communication**
- **Leased Telephone Lines**
- **Cellular Networks (4G/5G)**
### Protocols / Technologies
- **IP (Internet Protocol)**
- **TCP/UDP**
- **PPP (Point-to-Point Protocol)**
- **HDLC (High-Level Data Link Control)**
- **MPLS**
- **BGP (Border Gateway Protocol)** – routing on the Internet
### Key Idea
- Long distance + global connectivity → complex routing and multiple technologies
## Quick Comparison Table
| Network | Media Used                 | Protocols / Technologies          |
| ------- | -------------------------- | --------------------------------- |
| **LAN** | Twisted pair, Fiber, Wi-Fi | Ethernet, Wi-Fi, ARP, IP, TCP/UDP |
| **MAN** | Fiber, Microwave, Coaxial  | Metro Ethernet, MPLS, ATM         |
| **WAN** | Fiber, Satellite, Cellular | IP, TCP/UDP, PPP, MPLS, BGP       |
## Easy Way to Remember
- **LAN** → Cables + Wi-Fi → Ethernet
- **MAN** → Fiber city backbone → MPLS / Metro Ethernet
- **WAN** → Global links → IP + routing protocols

# LAN Standards
**LAN standards** define the **rules, formats, speeds, and media** used for communication within a Local Area Network. Most widely accepted LAN standards are developed by the IEEE under the **IEEE 802 series**.
## Major LAN Standards (IEEE 802)
## 1. Ethernet – IEEE 802.3
### Overview
The most widely used LAN standard for **wired networks**.
### Key Features
- Uses **CSMA/CD** (Collision Detection)
- Works with **twisted pair & fiber cables**
- High speed: 10 Mbps → 100 Mbps → 1 Gbps → 10+ Gbps
### Variants
- 10BASE-T (10 Mbps)
- 100BASE-T (Fast Ethernet)
- 1000BASE-T (Gigabit Ethernet)
### Usage
- Offices, homes, campus networks
## 2. Wi-Fi – IEEE 802.11
### Overview
Standard for **wireless LAN (WLAN)**.
### Key Features
- Uses **radio waves**
- Supports mobility
- Operates in **2.4 GHz / 5 GHz / 6 GHz bands**
### Variants
- 802.11a/b/g/n/ac/ax (Wi-Fi 6, Wi-Fi 6E)
### Usage
- Home Wi-Fi, public hotspots, enterprises
## 3. Token Ring – IEEE 802.5
<img width="789" height="791" alt="image" src="https://github.com/user-attachments/assets/f5472223-4d79-445e-8031-65c4a4a328b7" />

### Overview
Uses a **ring topology** with token passing.
### Key Features
- No collisions
- Controlled access using token
- Speeds: 4 Mbps, 16 Mbps
### Status
- Mostly **obsolete** (replaced by Ethernet)
## 4. Token Bus – IEEE 802.4
<img width="938" height="428" alt="image" src="https://github.com/user-attachments/assets/d2ea83b2-8918-4c93-9d94-5d46c7c4a1ee" />

### Overview
Combines **bus topology** with **token passing**.
### Key Features
- Logical ring over physical bus
- Deterministic access
### Usage
- Industrial environments
### Status
- Rarely used today
## 5. FDDI (Fiber Distributed Data Interface)
<img width="537" height="577" alt="image" src="https://github.com/user-attachments/assets/3d5c4783-3b1a-4ccb-95cd-dee361aa5e6f" />

### Overview
High-speed LAN using **fiber optics**.
### Key Features
- Dual ring topology (fault tolerance)
- Speed: 100 Mbps
- Token passing
### Usage
- Backbone networks (earlier)
### Status
- Replaced by modern Ethernet
## Summary Table
| Standard   | IEEE No. | Media              | Speed              | Status      |
| ---------- | -------- | ------------------ | ------------------ | ----------- |
| Ethernet   | 802.3    | Twisted pair/Fiber | Up to 100+ Gbps    | Widely used |
| Wi-Fi      | 802.11   | Wireless           | Up to several Gbps | Widely used |
| Token Ring | 802.5    | Twisted pair       | 4–16 Mbps          | Obsolete    |
| Token Bus  | 802.4    | Coaxial            | ~10 Mbps           | Obsolete    |
| FDDI       | —        | Fiber              | 100 Mbps           | Obsolete    |

# Ethernet, Token Ring, Token bus, FDDI
## 1. Ethernet (IEEE 802.3)
### Overview
The **most widely used LAN technology** today.
### Working Principle
- Uses **CSMA/CD (Carrier Sense Multiple Access with Collision Detection)**
- Devices check if the medium is free before sending data
### Features
- Originally bus → now mostly **star topology (with switches)**
- Speeds: **10 Mbps → 100 Mbps → 1 Gbps → 10+ Gbps**
- Uses **MAC addresses**
### Advantages
- High speed and reliable
- Low cost
- Easy to install
### Disadvantages
- Collisions (in old hub-based networks)
### Status
- **Dominant LAN technology**
## 2. Token Ring (IEEE 802.5)
### Overview
Developed by IBM, uses a **ring topology**.
### Working Principle
- Uses **token passing**
- A special token circulates → only holder can transmit
### Features
- No collisions
- Deterministic (predictable performance)
- Speeds: **4 Mbps, 16 Mbps**
### Advantages
- Efficient under heavy load
- No data collision
### Disadvantages
- Expensive
- Failure of one node affects network
### Status
- **Obsolete**
## 3. Token Bus (IEEE 802.4)
### Overview
A mix of **bus topology + token passing**.
### Working Principle
- Physically bus, but logically behaves like a ring
- Token is passed in a predefined order
### Features
- Deterministic access
- Used in industrial automation
### Advantages
- No collisions
- Predictable communication
### Disadvantages
- Complex to manage
- Limited flexibility
### Status**
- **Rarely used today
## 4. FDDI (Fiber Distributed Data Interface)
### Overview
High-speed LAN using **fiber optic cables**.
### Working Principle
- Uses **token passing**
- Dual ring system:
  - Primary ring (data transmission)
  - Secondary ring (backup)
### Features
- Speed: **100 Mbps**
- Long-distance support
- Fault tolerance (self-healing)
### Advantages
- Very reliable
- High speed (for its time)
### Disadvantages
- Expensive
- Complex setup
### Status
- **Replaced by modern Ethernet**
## Comparison Table
| Feature       | Ethernet        | Token Ring    | Token Bus          | FDDI           |
| ------------- | --------------- | ------------- | ------------------ | -------------- |
| IEEE Standard | 802.3           | 802.5         | 802.4              | ANSI (not 802) |
| Topology      | Bus/Star        | Ring          | Bus (logical ring) | Dual Ring      |
| Access Method | CSMA/CD         | Token Passing | Token Passing      | Token Passing  |
| Speed         | Up to 100+ Gbps | 4–16 Mbps     | ~10 Mbps           | 100 Mbps       |
| Media         | Copper/Fiber    | Twisted Pair  | Coaxial            | Fiber Optic    |
| Status        | Active          | Obsolete      | Obsolete           | Obsolete       |

# Ethernet Media (Thick, Thin, Twisted pair)
Ethernet has evolved through different **physical media types**. The classic ones you’re expected to know are **Thick Ethernet, Thin Ethernet, and Twisted Pair Ethernet**.
## 1. Thick Ethernet (10BASE5)
### Overview
Also called **Thicknet**, it was the **earliest Ethernet medium**.
### Media
- Thick **coaxial cable** (yellow cable)
- Uses external transceivers (vampire taps)
### Characteristics
- Speed: **10 Mbps**
- Maximum length: **500 meters per segment**
- Very robust and less signal loss
### Advantages
- Long distance support
- Strong signal quality
### Disadvantages
- Expensive
- Difficult to install
- Not flexible
### Status
- **Obsolete**
## 2. Thin Ethernet (10BASE2)
### Overview
Also called **Thinnet or Cheapernet**, a cheaper version of Thick Ethernet.
### Media
- Thin **coaxial cable (RG-58)**
- Uses **BNC connectors and T-connectors**
### Characteristics
- Speed: **10 Mbps**
- Maximum length: **185 meters per segment**
- Bus topology
### Advantages
- Cheaper than Thick Ethernet
- Easier to install
### Disadvantages
- Shorter distance
- Cable break affects entire network
### Status
- **Obsolete**
## 3. Twisted Pair Ethernet (10BASE-T and beyond)
### Overview
The **most commonly used Ethernet medium today**.
### Media
- **UTP (Unshielded Twisted Pair)**
- **STP (Shielded Twisted Pair)**
- Uses **RJ-45 connectors**
### Characteristics
- Speed: **10 Mbps → 100 Mbps → 1 Gbps → 10 Gbps+**
- Maximum length: **100 meters per segment**
- Uses **star topology (with switches)**
### Advantages
- Low cost
- Easy installation
- Flexible and scalable
### Disadvantages
- Limited distance compared to coaxial/fiber
- More susceptible to interference (UTP)
### Status
- **Widely used**
## Comparison Table
| Feature      | Thick Ethernet | Thin Ethernet | Twisted Pair Ethernet  |
| ------------ | -------------- | ------------- | ---------------------- |
| Standard     | 10BASE5        | 10BASE2       | 10BASE-T and above     |
| Cable Type   | Thick Coaxial  | Thin Coaxial  | Twisted Pair (UTP/STP) |
| Speed        | 10 Mbps        | 10 Mbps       | Up to 10+ Gbps         |
| Max Length   | 500 m          | 185 m         | 100 m                  |
| Cost         | High           | Medium        | Low                    |
| Installation | Difficult      | Easier        | Very easy              |
| Status       | Obsolete       | Obsolete      | Widely used            |

# Ethernet frame formats
**Ethernet frame formats** define how data is **encapsulated at the Data Link Layer (Layer 2)** before transmission. The two main formats you need to know are:
- **Ethernet II (DIX)** – most widely used today
- **IEEE 802.3 frame** – used with IEEE standards
## 1. Ethernet II Frame (DIX Format)
<img width="1440" height="526" alt="image" src="https://github.com/user-attachments/assets/855caad3-3df3-4d13-b11b-70ccf05da380" />

### Structure
| Field                       | Size          | Description              |
| --------------------------- | ------------- | ------------------------ |
| Preamble                    | 7 bytes       | Synchronization          |
| SFD (Start Frame Delimiter) | 1 byte        | Start indicator          |
| Destination MAC             | 6 bytes       | Receiver address         |
| Source MAC                  | 6 bytes       | Sender address           |
| **Type**                    | 2 bytes       | Protocol (IP, ARP, etc.) |
| Data (Payload)              | 46–1500 bytes | Actual data              |
| FCS                         | 4 bytes       | Error detection          |
### Key Point
- The **Type field identifies the upper-layer protocol** (e.g., IP, ARP)
### Example
- Type = 0x0800 → IP
- Type = 0x0806 → ARP
## 2. IEEE 802.3 Frame
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/6c7f15ec-6b51-4250-818d-b1fdcec9f4a4" />

### Structure
| Field           | Size               | Description             |
| --------------- | ------------------ | ----------------------- |
| Preamble        | 7 bytes            | Synchronization         |
| SFD             | 1 byte             | Start indicator         |
| Destination MAC | 6 bytes            | Receiver                |
| Source MAC      | 6 bytes            | Sender                  |
| **Length**      | 2 bytes            | Length of data field    |
| LLC Header      | 3 bytes            | Logical Link Control    |
| SNAP Header     | 5 bytes (optional) | Protocol identification |
| Data            | 46–1500 bytes      | Payload                 |
| FCS             | 4 bytes            | Error detection         |
### Key Point
- Uses **Length field instead of Type**
- Protocol is identified using **LLC/SNAP headers**

# WAN Standards
**WAN standards** define the **protocols and technologies used to communicate over long distances** (between cities, countries, or globally). These standards are developed by organizations like ITU-T, IEEE, and ISO.
## Major WAN Standards
## 1. PPP (Point-to-Point Protocol)
<img width="395" height="628" alt="image" src="https://github.com/user-attachments/assets/2088366f-4348-4831-9132-8ca062c89603" />

### Overview
A protocol used for **direct communication between two nodes**.
### Features
- Works over serial links
- Supports **authentication (PAP, CHAP)**
- Error detection and encapsulation
### Usage
- Dial-up connections
- Router-to-router links
## 2. HDLC (High-Level Data Link Control)
<img width="2048" height="1152" alt="image" src="https://github.com/user-attachments/assets/5562c818-6641-46ba-8ce5-76d1d872849d" />

### Overview
A **bit-oriented protocol** used for reliable data transfer.
### Features
- Works at **Data Link Layer**
- Supports synchronous communication
- Provides error detection
### Usage
- Leased line connections
- Router communication
## 3. Frame Relay
### Overview
A **packet-switched WAN technology** using virtual circuits.
### Features
- Uses **DLCI (Data Link Connection Identifier)**
- Faster than older technologies
- Minimal error checking
### Usage
- Enterprise WANs (earlier)
### Status
- Mostly obsolete
## 4. ATM (Asynchronous Transfer Mode)
### Overview
High-speed switching technology using **fixed-size cells (53 bytes)**.
### Features
- Supports **QoS (Quality of Service)**
- Used for voice, video, and data
- Connection-oriented
### Usage
- Telecom backbone networks
### Status
- Rarely used now
## 5. ISDN (Integrated Services Digital Network)
### Overview
Digital communication over telephone lines.
### Features
- Supports voice + data
- Types:
  - BRI (Basic Rate Interface)
  - PRI (Primary Rate Interface)
### Usage
- Early digital telephony
### Status
- Obsolete
## 6. MPLS (Multiprotocol Label Switching)
### Overview
Modern WAN technology for **fast packet forwarding using labels**.
### Features
- Uses **labels instead of IP lookup**
- High performance
- Supports QoS and traffic engineering
### Usage
- ISP backbone networks
- Enterprise WANs
## 7. SONET/SDH
### Overview
High-speed **fiber optic transmission standards**.
### Features
- Very high data rates
- Ring topology with fault tolerance
- Used in telecom infrastructure
### Usage
- Backbone networks
## Summary Table
| Standard    | Type              | Key Feature            | Status      |
| ----------- | ----------------- | ---------------------- | ----------- |
| PPP         | Point-to-point    | Authentication         | Active      |
| HDLC        | Data link         | Reliable communication | Active      |
| Frame Relay | Packet switching  | Virtual circuits       | Obsolete    |
| ATM         | Cell switching    | Fixed 53-byte cells    | Rare        |
| ISDN        | Digital telephony | Voice + data           | Obsolete    |
| MPLS        | Label switching   | Fast routing           | Widely used |
| SONET/SDH   | Optical fiber     | High-speed backbone    | Active      |

# Dial-up, Leased Line
## 1. Dial-up Connection
<img width="1000" height="400" alt="image" src="https://github.com/user-attachments/assets/a5983efa-f715-4e45-b34c-4dc235841810" />

### Definition
A **Dial-up connection** uses a **telephone line** to connect to the Internet by dialing an ISP (Internet Service Provider).
### Working
- Computer connects to a **modem**
- Modem dials ISP number
- Converts **digital ↔ analog signals**
### Features
- Temporary connection (not always active)
- Speed up to **56 kbps**
- Uses **PSTN (Public Switched Telephone Network)**
### Advantages
- Low cost
- Available in remote areas
### Disadvantages
- Very slow speed
- Cannot use phone and internet simultaneously
- Unstable connection
### Status
- **Obsolete**
## 2. Leased Line Connection
<img width="1536" height="724" alt="image" src="https://github.com/user-attachments/assets/f7c47b3b-5791-4863-af08-0c228a18b26c" />

### Definition
A **Leased line** is a **dedicated, permanent connection** between two locations or between a user and ISP.
### Working
- Direct connection using **fiber/copper line**
- Always active (no dialing required)
- Often uses protocols like **PPP or HDLC**
### Features
- High speed (Mbps to Gbps)
- Dedicated bandwidth
- Reliable and secure
### Advantages
- Stable and fast
- No congestion (not shared)
- Suitable for businesses
### Disadvantages
- Expensive
- Requires installation
### Status
- **Widely used in enterprises**
## Dial-up vs Leased Line
| Feature     | Dial-up               | Leased Line            |
| ----------- | --------------------- | ---------------------- |
| Connection  | Temporary (dialing)   | Permanent (always on)  |
| Speed       | Very slow (≤ 56 kbps) | High (Mbps–Gbps)       |
| Cost        | Low                   | High                   |
| Reliability | Low                   | High                   |
| Usage       | Old home internet     | Businesses, ISPs       |
| Line Type   | Telephone line        | Dedicated fiber/copper |

# ISDN, DSL, PPP
## 1. ISDN (Integrated Services Digital Network)
### Definition
**ISDN** is a digital communication technology that transmits **voice, data, and video over telephone lines**.
### Types
- **BRI (Basic Rate Interface)**
  - 2B + 1D channels
  - Each B = 64 kbps → Total = 144 kbps
- **PRI (Primary Rate Interface)**
  - 23B + 1D (US) / 30B + 1D (Europe)
  - Much higher speed
### Features
- Digital (better than analog dial-up)
- Faster call setup
- Supports multiple services
### Advantages
- Better quality than dial-up
- Simultaneous voice + data
### Disadvantages
- Expensive
- Replaced by modern broadband
### Status
- **Obsolete**
## 2. DSL (Digital Subscriber Line)
### Definition
**DSL** provides **high-speed internet over telephone lines** without blocking voice calls.
### Types
- **ADSL (Asymmetric DSL)** → Download > Upload
- **VDSL (Very-high-bit-rate DSL)** → Faster speeds
### Features
- Always ON connection
- Uses **different frequency bands** for voice & data
- Requires DSL modem
### Speed
- From **Mbps to 100+ Mbps** (depends on type & distance)
### Advantages
- Faster than dial-up
- Can use phone and internet together
### Disadvantages
- Speed decreases with distance
- Limited availability in some areas
### Status
- Still used (but being replaced by fiber)
## 3. PPP (Point-to-Point Protocol)
### Definition
**PPP** is a **data link layer protocol** used for communication between **two directly connected node**s.
### Features
- Encapsulation of network layer protocols (like IP)
- Supports authentication:
  - PAP (Password Authentication Protocol)
  - CHAP (Challenge Handshake Authentication Protocol)
- Error detection
### Working Phases
- Link establishment (LCP)
- Authentication
- Network layer configuration (NCP)
### Usage
- Dial-up connections
- DSL connections
- Router-to-router WAN links
### Advantages
- Reliable and secure
- Supports multiple protocols
### Disadvantages
- Only point-to-point (not multi-point)
### Status
- **Widely used (especially in WAN links)**
## Comparison Table
| Feature    | ISDN                  | DSL                  | PPP                   |
| ---------- | --------------------- | -------------------- | --------------------- |
| Type       | Network technology    | Broadband technology | Protocol              |
| Medium     | Telephone line        | Telephone line       | Works over many media |
| Speed      | Up to Mbps            | Mbps to 100+ Mbps    | Depends on link       |
| Connection | Dialed/Switched       | Always ON            | Point-to-point        |
| Usage      | Old digital telephony | Home/office internet | WAN communication     |
| Status     | Obsolete              | Active               | Active                |

# ATM
## ATM (Asynchronous Transfer Mode)
### Definition
**ATM (Asynchronous Transfer Mode)** is a **high-speed, connection-oriented WAN technology** that transmits data in **fixed-size cells of 53 bytes**.
## ATM Cell Structure (Very Important)
ATM Cell Size=53 bytes=5 (Header)+48 (Payload)
### Cell Fields
- **Header (5 bytes)** → routing and control information
- **Payload (48 bytes)** → actual data
#### Fixed size makes ATM fast and predictable
## Key Features
- **Connection-oriented** (virtual circuits required)
- Uses **fixed-length cells (53 bytes)**
- Supports **QoS (Quality of Service)**
- Works for **voice, video, and data**
- High speed (155 Mbps, 622 Mbps and more)
## ATM Working
1. Data is divided into **small fixed cells**
2. Cells are transmitted through **virtual circuits**
3. Each cell follows the **same predefined path**
4. Reassembled at destination
## Types of Connections
- **PVC (Permanent Virtual Circuit)**
  - Fixed path, always available
- **SVC (Switched Virtual Circuit)**
  - Established when needed
## ATM Layers
1. **ATM Adaptation Layer (AAL)**
   - Converts data into ATM cells
   - Types: AAL1, AAL2, AAL5
2. **ATM Layer**
   - Handles cell switching and routing
3. **Physical Layer**
   - Transmission over medium (fiber, etc.)
## Advantages
- High speed and efficiency
- Low delay (good for real-time traffic)
- Supports QoS
- Handles multiple data types
## Disadvantages
- Complex technology
- Expensive implementation
- Fixed cell size → overhead for large data
## ATM vs Packet Switching
| Feature    | ATM              | Packet Switching (IP) |
| ---------- | ---------------- | --------------------- |
| Data Unit  | Fixed (53 bytes) | Variable size packets |
| Speed      | High             | Moderate              |
| QoS        | Strong           | Limited               |
| Complexity | High             | Lower                 |
## Status
- ATM is **mostly obsolete today**
- Replaced by:
  - Ethernet
  - MPLS
  - IP-based networks
