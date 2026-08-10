
---

### 🔌 **What is a Protocol?**

- A **protocol** is a **set of rules** for formatting and processing data in networking.
    
- Think of it as a **common language** for computers.
    
- It allows **different hardware and software** to communicate.
    
- Source: [Cloudflare](https://www.cloudflare.com/learning/network-layer/what-is-a-protocol/)
    

---

### 🌐 **Common Network Protocols:**

- **HTTP** – Web browsing (insecure)
    
- **HTTPS** – Secure web browsing
    
- **SMTP** – Email sending
    
- **FTP** – File transfers
    
- **TCP** – Reliable data delivery
    
- **UDP** – Faster, but less reliable delivery
    

---
### 🔒 **Encapsulation**

Encapsulation is the process of **adding headers (and sometimes trailers)** to data as it moves **down** the layers of the network stack (from application to physical layer).

#### Example (Sending Data):

1. **Application Layer**: Creates the original message (e.g., an email).
    
2. **Transport Layer**: Breaks data into segments and adds a transport header (like TCP/UDP info).
    
3. **Network Layer**: Adds an IP header to form packets.
    
4. **Data Link Layer**: Adds MAC address info in a frame header and trailer (e.g., Ethernet).
    
5. **Physical Layer**: Converts the frame into bits and transmits over the medium.
    

Each layer wraps the data from the previous layer with its own header (and sometimes trailer).

---

### 🔓 **De-encapsulation**

De-encapsulation is the reverse process, occurring as data moves **up** the layers at the receiver's side. Each layer **removes and interprets** its corresponding header/trailer.

#### Example (Receiving Data):

1. **Physical Layer**: Receives the bit stream.
    
2. **Data Link Layer**: Converts bits into frames and removes the data link header/trailer.
    
3. **Network Layer**: Removes the IP header to get the packet.
    
4. **Transport Layer**: Processes the segment and hands off the message to the...
    
5. **Application Layer**: Delivers the original data to the user.
    

![[Pasted image 20250407050305.png]]

---


Let me know if you'd like a diagram or a real-world analogy!
### 🧱 **OSI Model Overview (7 Layers):** **( Open System Interconnection )

A model used to organize and describe how data moves through a network.

![[Pasted image 20250407045423.png]]

![[Pasted image 20250405065427 1.png]]


**Layers (Top to Bottom):**

1. **Application**
    
2. **Presentation**
    
3. **Session**
    
4. **Transport**
    
5. **Network**
    
6. **Data Link**
    
7. **Physical**
    

🧠 **Mnemonic:**  
**Please Do Not Throw Sausage Pizza Away**  
(Physical, Data Link, Network, Transport, Session, Presentation, Application)

---
### **🔹 Layer 1 – Physical Layer**

**Description:**  
This layer deals with the physical transmission of raw bits over a communication medium. It includes cables, connectors, and the actual signals (electrical, light, or radio).

**Key Functions:**

- Converts data bits into electrical or optical signals
    
- Defines hardware standards
    
- Handles physical topology
    

**Common Devices:**

- Hubs
    
- Cables (Ethernet, fiber)
    
- Wireless Access Points (WAPs)
    
- Network Interface Cards (NICs)
    
- Modems
    

**Protocols/Standards:**

- RS-232
    
- DSL
    
- USB
    
- Ethernet (physical layer specs)
    

**Common Attacks:**

- Wiretapping (intercepting signals)
    
- Jamming (signal interference)
    
- Physical tampering or damage
    

---

### **🔹 Layer 2 – Data Link Layer**

**Description:** 
Responsible for node-to-node data transfer and error detection. It packages data into frames and uses MAC addresses for delivery on the same network segment.

**Key Functions:**

- Transfers frames between directly connected nodes
    
- Error detection and correction
    
- MAC addressing
    
- Includes two sublayers: **MAC** and **LLC**
    

**Common Devices:**

- Switches
    
- Bridges
    
- NICs
    

**Protocols:**

- Ethernet
    
- PPP (Point-to-Point Protocol)
    
- ARP (Address Resolution Protocol)
    
- HDLC
    

**Common Attacks:**

- ARP Spoofing/Poisoning
    
- MAC Flooding
    
- Switch spoofing
    

Exactly! In the **OSI Model**, **Layer 2 – Data Link Layer** is divided into **two sublayers**:

---

### 🔸 **1. Media Access Control (MAC) Sublayer**

- **Function:** Controls how devices on a network gain access to the medium and permission to transmit data.
    
- **Key Points:**
    
    - Works **closer to the Physical Layer**.
        
    - Uses **MAC addresses** (hardware addresses).
        
    - Determines **who gets to transmit data** and when.
        
    - Responsible for **channel access** and **collision detection** (like CSMA/CD in Ethernet).
        

**Example Use:** Ethernet networks use MAC to allow devices to take turns sending data.

---

### 🔸 **2. Logical Link Control (LLC) Sublayer**

- **Function:** Manages communication between the Data Link Layer and the Network Layer.
    
- **Key Points:**
    
    - Provides **error detection** and **flow control**.
        
    - Allows **multiple network protocols** (like IP, IPX) to use the same physical network.
        
    - Adds headers to frames to identify the Network Layer protocol (e.g., IP, AppleTalk).
        

**Example Use:** Ensures that packets are handed off to the correct protocol (e.g., IPv4 vs IPv6).

---
### **🔹 Layer 3 – Network Layer**

**Description:**  
Handles routing, logical addressing, and delivery of packets between networks. It uses IP addresses to determine the best path for data.

**Key Functions:**

- IP addressing
    
- Routing and path selection
    
- Packet forwarding
    

**Common Devices:**

- Routers
    
- Layer 3 switches
    
- Firewalls
    

**Protocols:**

- IP (IPv4, IPv6)
    
- ICMP (for ping/traceroute)
    
- OSPF, BGP, RIP (routing protocols)
    

**Common Attacks:**

- IP Spoofing
    
- DDoS attacks (e.g., Ping Flood)
    
- Route injection
    

---

### **🔹 Layer 4 – Transport Layer**

**Description:**  
Ensures reliable data transfer between devices. It breaks data into segments, handles flow control, and retransmits lost data.

**Key Functions:**

- End-to-end connection
    
- Flow and error control
    
- Segmentation and reassembly
    

**Common Devices:**

- Firewalls (perform Layer 4 inspection)
    

**Protocols:**

- TCP (Transmission Control Protocol) – reliable, connection-oriented
    
- UDP (User Datagram Protocol) – faster, connectionless
    
- SCTP
    

**Common Attacks:**

- TCP SYN Flood
    
- Port Scanning
    
- UDP Flood
    

---

### **🔹 Layer 5 – Session Layer**

**Description:**  
Manages sessions between applications. It establishes, maintains, and terminates communication sessions.

**Key Functions:**

- Session control
    
- Supports full-duplex, half-duplex, and simplex communication
    
- Syncs data streams
    

**Protocols:**

- NetBIOS
    
- RPC (Remote Procedure Call)
    
- PPTP
    

**Common Attacks:**

- Session Hijacking
    
- Session Replay
    

---

### **🔹 Layer 6 – Presentation Layer**

**Description:**  
Formats data to be readable by the application layer. It handles encryption, compression, and translation.

**Key Functions:**

- Data formatting and translation
    
- Encryption/Decryption
    
- Compression
    

**Protocols/Data Types:**

- SSL/TLS
    
- JPEG, PNG, MP4
    
- ASCII, EBCDIC
    

**Common Attacks:**

- SSL Stripping
    
- Exploits through improperly parsed data (e.g., file format attacks)
    

---

### **🔹 Layer 7 – Application Layer**

**Description:**  
Closest to the end-user, this layer provides services for applications to communicate over the network (e.g., web, email, file transfer).

**Key Functions:**

- Interfacing with user applications
    
- Providing network services like email, web, FTP
    
- Network management and file sharing
    

**Common Devices:**

- User devices (PCs, smartphones)
    
- Proxies
    
- Application Gateways
    

**Protocols:**

- HTTP/HTTPS (web)
    
- FTP/SFTP (file transfer)
    
- SMTP, POP3, IMAP (email)
    
- DNS, DHCP
    

**Common Attacks:**

- Phishing
    
- DNS Poisoning
    
- Malware
    
- Application-layer DDoS attacks
    

---
