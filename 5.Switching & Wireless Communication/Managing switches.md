A **MAC (Media Access Control) address** is a unique identifier assigned to a network interface card (NIC) for use in communication within a network. It is typically 48 bits long.

### Breakdown:

- **48 bits** = 6 bytes (each byte is 8 bits)
    
- A MAC address is usually represented in **hexadecimal** format, which uses 16 characters (0-9, A-F) to represent 4 bits per character. This means the 48-bit MAC address is typically written as 12 hexadecimal digits.
    

### Example:

A typical MAC address might look like this:

```
00:1A:2B:3C:4D:5E
```

This is a **48-bit** MAC address, where each pair of characters represents a byte (8 bits), and the total is 6 bytes (48 bits).
### Key Points:

1. **Format**: A MAC address is a 12-character code, written in pairs of hexadecimal digits (e.g., `00:1A:2B:3C:4D:5E`).
    
2. **Purpose**: It helps devices identify and communicate with each other on a local network.
    
3. **Permanent**: Typically, a MAC address is hardcoded into the device and doesn't change.
    
4. **Used by**: Switches, routers, and other network devices to send data to the correct device within a network.
    
---

## 🔄 **MAC Address Learning**

- **Switches** learn **source MAC addresses** from incoming frames.
    
- Stored in the **CAM (Content Addressable Memory)** or **MAC address table**.
    
- Enables forwarding decisions based on MAC addresses.
    
    ![[Pasted image 20250413093325.png]]
    
---

## 🧱 **VLANs (Virtual LANs)**

### 🔧 **Purpose**

- Logically segment a switch into **multiple broadcast domains**.
    
    ![[Pasted image 20250413093344.png]]
    
### ✅ **Benefits**

- **Broadcast Control**: Each VLAN is its own **broadcast domain**.
    
- **Improved Security**: Hosts in a VLAN **can’t talk to others** outside the VLAN without a router.
    
- **Flexibility & Scalability**: Devices in the same VLAN can communicate even across switches.
    

---

## 🗂️ **VLAN Database**

- Stores **VLAN IDs and properties** on the switch.
    
- Used to manage VLAN configuration and assignments.
    

---

## 🏷️ **Port Tagging / 802.1Q**

- Adds **VLAN tags** to Ethernet frames.
    
- Enables **multiple VLANs to use a single trunk link**.
    
- Standard: **IEEE 802.1Q**.
    
    ![[Pasted image 20250413093429.png]]
    
---

## 🔌 **Switch Virtual Interface (SVI)**

- Virtual Layer 3 interface on a switch.
    
- Enables **inter-VLAN routing** by assigning **IP addresses to VLANs**.
    

---

## ⚙️ **Interface Configuration**

- Involves settings like:
    
    - VLAN assignment
        
    - Link aggregation
        
    - **Speed** & **duplex mode**
        

---

## 🌐 **Native VLAN**

- VLAN for **untagged traffic** on a trunk port.
    
- Ensures compatibility with **older devices** that don’t support tagging.
    

---

## 📞 **Voice VLAN**

- Dedicated VLAN for **VoIP traffic**.
    
- Prioritizes voice to ensure **QoS (Quality of Service)**:
    
    - Low latency
        
    - Low jitter
        
    - Minimal packet loss
        

---

## 🚀 **Speed & Duplex**

|Term|Meaning|
|---|---|
|**Speed**|Data transfer rate (e.g., **100 Mbps**, **1 Gbps**)|
|**Duplex**|Communication direction: **Full-duplex = simultaneous 2-way**, **Half-duplex = one direction at a time**|

---

## 🌲 **Spanning Tree Protocol (STP)**

- Prevents **network loops** in Ethernet networks.
    
- Blocks redundant paths, **recalculates** on failure to maintain connectivity.
    
    ![[Pasted image 20250413093451.png]]
    
---

## 🧩 **Link Aggregation**

- Combines multiple ports into one logical link.
    
- Increases **bandwidth** and provides **redundancy**.
    
- Also known as **EtherChannel** or **LAG (Link Aggregation Group)**.
    

---

## 🛡️ **Port Security**

- Restricts access to switch ports based on:
    
    - **MAC address**
        
    - **Number of allowed devices**
        
- Helps mitigate **MAC flooding** and **unauthorized access**.
    
    ![[Pasted image 20250413093505.png]]
    
---

## 📡 **Port Mirroring (SPAN/RSPAN)**

- Copies traffic from one port to another.
    
- Used for **monitoring** with tools like:
    
    - **Packet sniffers**
        
    - **IDS/IPS**
        
- **SPAN** = Local monitoring, **RSPAN** = Remote monitoring.
    
    ![[Pasted image 20250413093522.png]]
    
---

## 📏 **MTU (Maximum Transmission Unit)**

- Maximum size of a packet/frame that can be transmitted without fragmentation.
    
- Ethernet standard = **1500 bytes**
    
- Larger packets get **fragmented**, reducing efficiency.
    

---

## 📦 **Jumbo Frames**

- Ethernet frames > 1500 bytes (up to 9000 bytes).
    
- Useful in **high-throughput environments** (e.g., data centers).
    
- Requires **all devices to support it** or it causes issues.
    

---
