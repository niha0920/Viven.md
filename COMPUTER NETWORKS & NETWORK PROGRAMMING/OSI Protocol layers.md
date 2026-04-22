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
