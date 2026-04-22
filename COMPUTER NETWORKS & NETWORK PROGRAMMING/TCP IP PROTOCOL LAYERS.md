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
