# Line configurations
**Line configurations** refer to the way communication devices are physically or logically connected using a communication link in a network. It defines how many devices can share a link and how they communicate.
- There are **two main types of line configurations**:
## 1. Point-to-Point Line Configuration
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
### Function
Regenerates and amplifies weak signals.
### Key Points
- Works at **Physical Layer (OSI Layer 1)**
- Extends transmission distance
- No filtering or intelligence
## 2. Hub
### Function
Connects multiple devices and **broadcasts data to all ports**.
### Key Points
- Also works at **Physical Layer**
- No data filtering
- Causes collisions
## 3. Bridge
### Function
Connects two LAN segments and filters traffic.
### Key Points
- Works at **Data Link Layer (Layer 2)**
- Uses **MAC addresses**
- Reduces collisions
## 4. Switch
### Function
Connects devices and sends data **only to the intended device**.
### Key Points
- Works at **Layer 2 (sometimes Layer 3)**
- Uses MAC address table
- Faster and more efficient than hub
## Internetworking Devices (Between Networks)
## 5. Router
### Function
Connects different networks and routes data packets.
### Key Points
- Works at **Network Layer (Layer 3)**
- Uses **IP addresses**
- Determines best path
## 6. Gateway
### Function
Acts as a **protocol converter** between different networks.
### Key Points
- Works across **all OSI layers**
- Connects dissimilar systems
- Example: Email gateway
## 7. Modem (Modulator-Demodulator)
### Function
Converts **digital signals ↔ analog signals**.
### Key Points
- Used for internet access
- Example: DSL, Cable modem
## 8. Access Point (AP)
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
### Overview
Uses a **ring topology** with token passing.
### Key Features
- No collisions
- Controlled access using token
- Speeds: 4 Mbps, 16 Mbps
### Status
- Mostly **obsolete** (replaced by Ethernet)
## 4. Token Bus – IEEE 802.4
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
