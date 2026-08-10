# What is a Network?

A **network** is a group of two or more connected systems or devices that can communicate and share resources with each other. These systems can include computers, servers, phones, or other hardware.

# What is on a network?

### **Hosts**

- Devices on a network (like computers, phones, printers).
    
- Use or share resources.
    
- Have an IP address.
    

---
### **Server**

- A computer that gives data or services to others.
    
- Helps **clients** (like your phone or PC) over a network.
    

---
### **Client Machine**

- A computer or device that **uses** services from a **server**.
    
- Connects over a network.
    
- Examples: laptops, phones, tablets.
    

---
### **Workstation**

- A powerful computer for one person.
    
- Used for tasks like design, engineering, or science.
    

---
### **Network Devices**

- Help connect everything in a network.
    
- Examples:
    
    - **Router** – connects to the internet.
        
    - **Switch** – connects multiple devices inside a network.
        
    - **Access Point (AP)** – gives wireless connection (Wi-Fi).
        
    - **Firewall** – protects the network from threats.
        

---
# Types of Networks

**1. Local Area Network (LAN):**

- Small area (home, office)
    
- Shares files, printers, and internet
    

**2. Wide Area Network (WAN):**

- Large area (country or world)
    
- The **Internet** is the biggest WAN
    

**3. Metropolitan Area Network (MAN):**

- Medium area (city)
    
- Connects LANs across a city
    

**4. Campus Area Network (CAN):**

- Limited area (university, corporate campus)
    
- Connects multiple LANs in one location
    

**5. Storage Area Network (SAN):**

- High-speed network for data storage
    
- Makes storage devices act like local drives to servers
    

**6. Personal Area Network (PAN):**

- Very small area (within a room)
    
- Example: Bluetooth between phone and headset
    

---
# Network Architecture

### **Peer-to-Peer (P2P) Network**

- No central server.
    
- Every device can share and access files directly.
    
- _Example: Sharing music or files between two computers._ Bittorent
    
    ![[Pasted image 20250405061925.png]]

---

### **Client-Server Network**

- Has a central server.
    
- Clients (like computers or phones) request services from the server.
    
- _Example: Logging into a website from your phone._
    
    ![[Pasted image 20250405061952.png]]

---
# Backbone & Segments

![[Pasted image 20250405062308.png]]
### **Network Backbone**

- The main high-speed path in a network.
    
- Connects different parts (segments) and carries most of the data.
    
- _Like a highway for network traffic._
    

---

### **Network Segments**

- Smaller parts of a network connected to the backbone.
    
- Include devices like computers and switches.
    
- _Example: Each office department can be a segment._
    

---

# **What is Network Topology?**

The layout or structure of how devices are connected in a network. It affects speed, reliability, and how easy it is to manage.

---

### **1. Point-to-Point Topology**

- Direct connection between two devices.
    
- _Example: A link between a main office and a branch office._
    
    ![[Pasted image 20250405062344.png]]


---

### **2. Mesh Topology**

- Every device connects to every other device.
    
- Very reliable, but complex and costly.
    
- _Used in military or critical systems._
    
    ![[Pasted image 20250405062431.png]]

---

### **3. Star Topology (Hub-and-Spoke)**

- All devices connect to a central hub/switch.
    
- Easy to manage, but the hub is a single point of failure.
    
- _Common in home and office networks._
    
    ![[Pasted image 20250405062451.png]]

---

### **4. Hybrid Topology**

- Mix of two or more topologies.
    
- Flexible and customizable for large or complex networks.
    
- _Example: Combining star and mesh in a large company._
    

---
# **Three-tier Hierarchical Model**

A structured network design with **three layers**, each with a clear role—helps with **performance, scalability, and easier management**.

![[Pasted image 20250405062523.png]]

---

### **1. Core Layer**

- **Backbone** of the network.
    
- Handles **high-speed data transfer** across the entire network.
    
- Needs to be **fast and reliable**.
    
- _Think of it like a highway system._
    

---

### **2. Distribution Layer**

- **Middle layer** between core and access.
    
- **Manages traffic** and applies rules (like routing and filtering).
    
- _Like a traffic controller directing data where it needs to go._
    

---

### **3. Access Layer**

- Where **devices connect** to the network (e.g., PCs, phones).
    
- Uses **switches and access points**.
    
- _Like entrances to a building for users to come in._
    

---
# **Spine and Leaf Architecture**

A **two-layer network design** that is fast, scalable, and low-latency.

![[Pasted image 20250405062633.png]]
---

### **Leaf Switches**

- Connect to **end devices** (like servers, computers).
    
- Form the **access layer**.
    

### **Spine Switches**

- Connect **only to leaf switches**, not to each other.
    
- Act as the **backbone**, handling high-speed data transfer.
    

---

# **Collapsed Core Architecture** 

![[Pasted image 20250405062704.png]]

- **Definition:** Combines core and distribution layers into one.
    
- **Purpose:** Simplifies network design.
    
- **Best for:** Small to medium-sized networks.
    
- **Benefits:**
    
    - Reduces hardware costs
        
    - Easier to manage and maintain
        
    - Improves performance (lower latency)
        


# **North-South Traffic & East-West Traffic**

![[Pasted image 20250405062943.png]]

---

### **North-South Traffic** 

- **Definition:** Traffic between the data center and external networks (e.g., internet).
    
- **Direction:** Inbound and outbound.
    
- **Example:** Client accessing a web server in the data center.
    
- **Focus:** External communication.
    

---

### **East-West Traffic

- **Definition:** Traffic within the data center.
    
- **Direction:** Lateral/internal.
    
- **Examples:**
    
    - Server-to-server
        
    - Server-to-storage
        
    - VM-to-VM
        
- **Focus:** Efficient internal data exchange.
    
---
# Traffic Flow -Transmission Methods

---
### **Unicast – One-to-One**

- **Definition:** Sends data from one source to one specific destination.
    
- **Use Cases:** Web browsing, email, file transfers.
    
- **IP Type:** Common in both IPv4 and IPv6.
    
- **Example:** A user visiting a website.
    
    ![[Pasted image 20250405063638.png]]
    
---

### **Multicast – One-to-Many (Selected Group)**

- **Definition:** Sends data from one (or more) source(s) to multiple specific recipients.
    
- **Efficiency:** Saves bandwidth vs unicast when sending the same data to many.
    
- **Use Cases:** Video/audio streaming, IPTV, online conferencing.
    
- **IP Type:** Used in both IPv4 and IPv6.
    
    ![[Pasted image 20250405063707.png]]
    
---

### **Anycast – One-to-Nearest (Best Path)**

- **Definition:** Sends data to the **nearest** or **best** destination out of many sharing the same address.
    
- **Use Cases:** DNS, CDN (Content Delivery Networks), IPv6 routing.
    
- **Benefit:** Faster access and high availability.
    
    ![[Pasted image 20250405063754.png]]
    
---

### **Broadcast – One-to-All (Same Network Segment)**

- **Definition:** Sends data from one sender to **all devices** in a network segment.
    
- **Use Cases:** DHCP requests, ARP announcements.
    
- **IP Type:** IPv4 only (not used in IPv6).
    
- **Note:** Replaced by multicast in IPv6.
    
    ![[Pasted image 20250405063817.png]]
    
---
