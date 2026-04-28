# OSI Protocol layers
The **OSI (Open Systems Interconnection) model** is a conceptual framework used to understand how data travels across a network. It divides communication into 7 layers, each with a specific function.
## OSI Model Layers (Top to Bottom)
### 1. Application Layer (Layer 7)
- Closest to the end user
- Provides network services to applications
- Examples: Web browsers, email clients
#### Protocols: HTTP, FTP, SMTP, DNS
## 2. Presentation Layer (Layer 6)
- Translates data between formats
- Handles encryption & decryption
- Compression of data
### Examples: SSL/TLS, JPEG, MP3
## 3. Session Layer (Layer 5)
- Establishes, maintains, and terminates sessions
- Controls dialog between devices
### Example: NetBIOS, RPC
## 4. Transport Layer (Layer 4)
- Ensures reliable data transfer
- Error detection & correction
- Flow control and segmentation
### Protocols: TCP, UDP
## 5. Network Layer (Layer 3)
- Handles routing and logical addressing
- Determines best path for data
### Protocols: IP, ICMP
## 6. Data Link Layer (Layer 2)
- Transfers data between directly connected devices
- Uses MAC addresses
- Error detection
### Examples: Ethernet, ARP
## 7. Physical Layer (Layer 1)
- Deals with hardware and transmission media
- Converts data into signals (electrical/optical)
### Examples: Cables, switches, hubs
## Easy Mnemonic to Remember
**Top → Bottom:**
- All People Seem To Need Data Processing
## Quick Summary Table
| Layer | Name         | Key Function               |
| ----- | ------------ | -------------------------- |
| 7     | Application  | User interaction           |
| 6     | Presentation | Data formatting/encryption |
| 5     | Session      | Session management         |
| 4     | Transport    | Reliable delivery          |
| 3     | Network      | Routing & addressing       |
| 2     | Data Link    | MAC & error detection      |
| 1     | Physical     | Signal transmission        |

# Physical layer functionalities
The **Physical Layer** is the lowest layer of the OSI model. It is responsible for **transmitting raw bits (0s and 1s)** over a physical medium like cables or wireless signals.
## Key Functionalities
### 1. Bit Transmission
- Converts data into **binary bits (0s and 1s)**
- Sends these bits over the communication channel
## 2. Physical Medium Definition
- Defines the type of medium used:
  - Copper cables
  - Fiber optics
  - Wireless signals
## 3. Signal Encoding
- Converts bits into signals:
  - Electrical (copper wires)
  - Optical (fiber cables)
  - Radio waves (wireless)
## 4. Data Rate Control
- Determines the speed of data transmission (bits per second)
- Example: 100 Mbps, 1 Gbps
## 5. Bit Synchronization
- Ensures sender and receiver are synchronized
- Uses clock signals to match timing
## 6. Line Configuration
- Defines how devices are connected:
  - Point-to-Point
  - Multipoint
## 7. Physical Topology
- Defines network layout:
  - Bus
  - Star
  - Ring
  - Mesh
## 8. Transmission Mode
- Direction of data flow:
  - Simplex (one-way)
  - Half-duplex (both ways, one at a time)
  - Full-duplex (both ways simultaneously)
## 9. Interface & Hardware Specifications
- Defines:
  - Connectors
  - Pin configurations
  - Voltage levels
## Simple One-Line Definition
Physical layer = "Moves raw bits as signals through hardware"
## Example
When you send a message:
- Physical layer converts your data → electrical signals
- Sends through cable → receiver converts back to bits

# Data link layer functionalities
The **Data Link Layer** is responsible for **node-to-node delivery** of data and ensures that data is transferred **reliably between two directly connected devices**. It converts raw bits from the Physical layer into **frames**.
## Key Functionalities
### 1. Framing
- Breaks data into manageable units called **frames**
- Adds headers and trailers (like source/destination MAC address)
## 2. Physical Addressing (MAC Addressing)
- Uses **MAC addresses** to identify devices on the same network
- Ensures correct delivery within a LAN
## 3. Error Detection & Correction
- Detects errors using techniques like **CRC (Cyclic Redundancy Check)**
- May request retransmission if errors are found
## 4. Flow Control
- Controls the rate of data transmission
- Prevents the receiver from being overwhelmed
## 5. Access Control (Media Access Control)
- Decides **who can use the communication medium** when multiple devices are connected
- Example: CSMA/CD (Ethernet), CSMA/CA (Wi-Fi)
## 6. Reliable Delivery (Optional)
- Ensures frames are delivered correctly using acknowledgments and retransmissions
## 7. Synchronization
- Maintains proper sequencing of frames
- Ensures sender and receiver stay in sync
## 8. Link Management
- Establishes, maintains, and terminates the link between nodes
## Sublayers of Data Link Layer
1. **MAC (Media Access Control) Layer**
- Handles addressing and access control
2. **LLC (Logical Link Control) Layer**
- Handles flow control and error management
## Simple One-Line Definition
Data Link Layer = "Ensures reliable frame delivery between two directly connected devices"
## Example
When sending data over Wi-Fi or Ethernet:
- Data Link Layer:
  - Adds MAC address
  - Creates frames
  - Checks errors
- Then sends it to the Physical layer for transmission

# Network layer functionalities
The **Network Layer** is responsible for **end-to-end delivery of packets across multiple networks**. It decides the **best path** for data to travel from source to destination.
## Key Functionalities
### 1. Logical Addressing (IP Addressing)
- Assigns unique **IP addresses** to devices
- Identifies source and destination across networks
## 2. Routing (Path Determination)
- Determines the **best route** for data transmission
- Uses routing algorithms and routing tables
## 3. Packet Forwarding
- Moves packets from one router to another toward the destination
- Uses **next-hop** information
## 4. Fragmentation & Reassembly
- Breaks large packets into smaller ones (fragmentation)
- Reassembles them at the destination
## 5. Internetworking
- Connects different types of networks (LAN, WAN, etc.)
- Enables communication across heterogeneous networks
## 6. Congestion Control
- Manages network traffic to avoid overload
- May delay or drop packets when congestion occurs
## 7. Error Handling & Diagnostics
- Reports errors using protocols like ICMP
- Helps in troubleshooting (e.g., ping)
## Simple One-Line Definition
Network Layer = "Handles routing and delivery of packets across networks"
## Example
When you send data to a website:
- Network Layer:
  - Adds IP address
  - Chooses best route
  - Sends packets through routers
- Finally reaches the destination network

# Transport layer functionalities
The **Transport Layer** ensures **end-to-end communication** between devices. It provides **reliable or fast delivery**, depending on the protocol used.
## Key Functionalities
### 1. Segmentation & Reassembly
- Breaks large data into smaller units called **segments**
- Reassembles them at the destination in the correct order
## 2. Service Point Addressing (Port Numbers)
- Uses **port numbers** to identify specific applications
- Example: Web (port 80), HTTPS (port 443)
## 3. Connection Control
- Establishes, maintains, and terminates connections
- Types:
  - Connection-oriented (e.g., TCP)
  - Connectionless (e.g., UDP)
## 4. Flow Control
- Controls the rate of data transmission
- Prevents receiver overload (e.g., sliding window mechanism)
## 5. Error Control
- Detects and corrects errors
- Uses acknowledgments (ACKs) and retransmissions
## 6. Reliable Data Transfer
- Ensures data arrives:
  - Without loss
  - In correct order
  - Without duplication
## 7. Multiplexing & Demultiplexing
- Combines data from multiple applications (sender side)
- Separates them correctly at receiver side
## Simple One-Line Definition
Transport Layer = "Ensures reliable end-to-end delivery of data between applications"
## Example
When you open a website:
- Transport Layer:
  - Breaks data into segments
  - Uses port number (e.g., 80/443)
  - Ensures all data reaches correctly
## Common Protocols
- **TCP (Transmission Control Protocol)** → Reliable
- **UDP (User Datagram Protocol)** → Fast but unreliable

# Presentation layer functionalities
The **Presentation Layer** acts as a **translator** between the application and the network. It ensures that data sent by one system is **understandable by another**, regardless of differences in format.
## Key Functionalities
### 1. Data Translation / Format Conversion
- Converts data into a **standard format**
- Handles differences in:
  - Character encoding (ASCII, Unicode)
  - Data formats (JSON, XML, etc.)
## 2. Encryption & Decryption
- Secures data during transmission
- Encrypts data at sender and decrypts at receiver
- Example: SSL/TLS
## 3. Data Compression & Decompression
- Reduces size of data to improve transmission speed
- Decompresses data at the destination
## 4. Character Encoding
- Ensures correct interpretation of characters
- Converts between encoding standards
## 5. Data Formatting
- Structures data in a way that the application layer can understand
- Example: formatting images, audio, video
## Simple One-Line Definition
Presentation Layer = "Formats, encrypts, and compresses data for proper communication"
## Example
When you send a secure message:
- Presentation Layer:
  - Encrypts the message
  - Compresses it
  - Converts it into standard format
- At receiver:
  - Decrypts and decompresses
## Examples
- SSL/TLS (encryption)
- JPEG, MP3, MPEG (data formats)
- ASCII, Unicode (encoding)

# Session layer functionalities
The **Session Layer** is responsible for **establishing, managing, and terminating communication sessions** between applications. It ensures that communication stays organized and synchronized.
## Key Functionalities
### 1. Session Establishment, Maintenance & Termination
- Creates a session between sender and receiver
- Keeps it active during communication
- Properly closes it after completion
## 2. Dialog Control
- Manages how data flows between devices
- Supports:
  - Half-duplex (one at a time)
  - Full-duplex (both directions simultaneously)
## 3. Synchronization (Checkpoints)
- Inserts **checkpoints** in data streams
- If failure occurs, resumes from last checkpoint instead of restarting
## 4. Session Recovery
- Restores sessions after interruptions or failures
- Prevents complete data loss
## 5. Token Management
- Controls which device can transmit at a given time
- Prevents data collision in communication
## Simple One-Line Definition
Session Layer = "Manages and controls communication sessions between devices"
## Example
While downloading a large file:
- Session Layer:
  - Maintains the session
  - Adds checkpoints
  - If connection drops → resumes from last checkpoint
## Examples
- NetBIOS
- RPC (Remote Procedure Call)

# Application layer functionalities
The **Application Layer** is the **topmost layer** of the OSI model. It provides **network services directly to end users and applications**, acting as the interface between user applications and the network.
## Key Functionalities
### 1. Network Service Provision
- Provides services like:
  - Web browsing
  - Email
  - File transfer
## 2. User Interface to Network
- Acts as a bridge between user applications and network
- Example: Web browser accessing a website
## 3. File Transfer, Access & Management
- Allows users to upload, download, and manage files
- Example: FTP
## 4. Email Services
- Enables sending and receiving emails
- Example: SMTP, POP3, IMAP
## 5. Directory Services
- Provides resource lookup and name resolution
- Example: DNS
## 6. Remote Access
- Allows users to access remote systems
- Example: Telnet, SSH
## 7. Network Virtual Terminal
- Enables remote login and command execution on another system
## Simple One-Line Definition
Application Layer = "Provides network services directly to end-user applications"
## Example
When you open a website:
- Application Layer:
  - Uses HTTP protocol
  - Sends request to server
  - Receives webpage data
## Common Protocols
- HTTP / HTTPS → Web browsing
- FTP → File transfer
- SMTP → Email sending
- DNS → Domain name resolution
