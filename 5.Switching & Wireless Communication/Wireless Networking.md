
---
### **WiFi Channels and Frequency Bands**

WiFi channels are like smaller sections within the bigger "frequency band" that your WiFi network uses. Think of it like lanes on a highway—more lanes allow more cars (networks) to travel without causing traffic (interference).

---
#### 1. **Regulatory Impacts**

- **What is it?**: Governments set rules about which frequencies (radio waves) can be used for WiFi in different countries.
    
- **Why it matters?**: These rules prevent WiFi networks from interfering with other devices like radios or phones.
    

#### 2. **Channel Width**

- **What is it?**: Channel width is the size of the WiFi lane.
    
- **Wide lanes** (like 80 MHz) allow faster speeds but can cause more traffic (interference).
    
- **Narrow lanes** (like 20 MHz) are slower but cause less interference.
    

#### 3. **Frequency Bands in Wireless Networks**

- **2.4 GHz**: Long range but slower speeds and more interference (due to other devices like microwaves).
    
- **5 GHz**: Faster speeds but shorter range.
    
- **6 GHz**: Newer, faster, and can handle more devices at once.
    

#### 4. **Non-Overlapping Channels**

- **What is it?**: Some channels don’t interfere with each other.
    
- **Example**: In the 2.4 GHz band, channels 1, 6, and 11 don’t overlap, so they work better together.
    

#### 5. **2.4 GHz Band**

- **Good for**: Long-distance communication (goes through walls easily).
    
- **Problem**: Slower speeds and more interference from other household devices (like microwaves).
    

#### 6. **5 GHz Band**

- **Good for**: Faster speeds, especially when you’re close to the router.
    
- **Problem**: Shorter range (doesn’t go through walls well).
    

#### 7. **6 GHz Band**

- **What’s new**: This band is really fast and has more space for more devices to connect.
    
- **Best for**: High-speed WiFi and areas with many devices (like offices or crowded places).
    

---
### **WiFi Network**

---

### **1. Band Steering**

- **What it is**: A feature that automatically connects your devices to the best WiFi band (either 5 GHz or 6 GHz) based on which one is less crowded.
    
- **Benefit**: Reduces network congestion on the 2.4 GHz band and improves WiFi speeds and reliability, especially in crowded environments.
    

---

### **2. 802.11h**

- **What it is**: A standard that enhances WiFi by adding two features:
    
    - **Dynamic Frequency Selection (DFS)**: Avoids interference with radar systems on the 5 GHz band.
        
    - **Transmit Power Control (TPC)**: Adjusts the device’s power to minimize interference and save energy.
        
- **Why it matters**: Helps WiFi networks comply with European rules and improve performance in areas with radar systems.
    
---

### **Wireless Standards Comparison Table**

| Standard               | Frequency Band | Max Speed              | Max Range (Indoor) | Year Released  | Key Features                             |
| ---------------------- | -------------- | ---------------------- | ------------------ | -------------- | ---------------------------------------- |
| **802.11a**            | 5 GHz          | 54 Mbps                | ~35 meters         | 1999           | Less interference, but shorter range     |
| **802.11b**            | 2.4 GHz        | 11 Mbps                | ~38 meters         | 1999           | Slower, but longer range than 11a        |
| **802.11g**            | 2.4 GHz        | 54 Mbps                | ~38 meters         | 2003           | Backward compatible with 11b             |
| **802.11n**            | 2.4 & 5 GHz    | 600 Mbps               | ~70 meters         | 2009           | MIMO technology, better range/speed      |
| **802.11ac**           | 5 GHz          | 1.3 Gbps+              | ~35 meters         | 2013           | High speed, beamforming, MU-MIMO         |
| **802.11ax** (Wi-Fi 6) | 2.4 & 5 GHz    | 9.6 Gbps (theoretical) | ~70 meters         | 2019           | High efficiency, better in crowded areas |
| **802.11be** (Wi-Fi 7) | 2.4, 5 & 6 GHz | 30 Gbps+ (theoretical) | ~70 meters+        | 2024 (ongoing) | Ultra-low latency, high capacity         |

---

### **3. WiFi Network Terminology**

- **BSS (Basic Service Set)**: A group of devices connected to the same Access Point (AP). Each AP has a unique identifier, called **BSSID**, which is its MAC address.
    
    ![[Pasted image 20250413095117.png]]
    
- **SSID (Service Set Identifier)**: The name of your WiFi network. It’s what you see when you connect to WiFi.
    
    ![[Pasted image 20250413095132.png]]
    
- **BSSID**: A unique identifier for an individual AP, used to connect devices to the right AP in networks with multiple access points.
    
- **ESS (Extended Service Set)**: A network of multiple APs working together to create one large network. All APs in the ESS broadcast the same SSID for seamless connection across the network.
    
- **ESSID**: The network name for the entire ESS (Extended Service Set), allowing devices to roam between different APs.
    

---

### **4. Wireless Network Interface Card (NIC)**

- **What it is**: A component in devices (like laptops or phones) that allows them to connect to WiFi networks.
    
- **Functions**: Supports different WiFi standards (e.g., 802.11a/b/g/n/ac/ax), manages wireless encryption, and connects your device to the wireless network.
    

---

### **5. Wireless Access Point (WAP)**

- **What it is**: A device that connects wireless devices (like laptops, phones) to the wired network using radio frequencies.
    
- **Functions**:
    
    - Acts as a bridge between the wireless devices and the wired network.
        
    - Creates a central point where all wireless devices connect (star topology).
        
    - Manages data transmission and minimizes network collisions using CSMA/CA (Carrier Sense Multiple Access with Collision Avoidance).
        
- **Autonomous Access Points**: These APs manage all tasks (security, routing) independently. They are best for small networks where individual management of each AP is manageable.
  
- Lightweight Access Points (LAP):A type of Access Point (AP) managed by a **Wireless LAN Controller (WLC)**.
    - Increases network coverage, availability, and performance.
    - Cannot be managed directly; all management happens through the WLC.

---

# WiFi Network Components and Security

---
### **1. Wireless Antennas**

- **Omni-directional Antennas**:
    
    - Transmit signals in all directions, covering a 360-degree area.
        
    - Common in consumer and business wireless devices.
        
    - Range is shorter than directional antennas due to broad signal distribution.
        
- **Directional Antennas**:
    
    - Focus the signal in one direction, providing a longer range.
        
    - **Yagi-Uda Antennas**: Can extend signal range up to 1 mile.
        
    - **Parabolic Antennas**: Can extend signal range up to 8 miles, focusing the signal to a specific point.
        

---

### **2. Wireless Network Types**

- **Point-to-Point Networks**:
    
    - Establish a direct connection between two wireless devices.
        
    - Used to link two locations in a WAN or provide a dedicated communication path.
        
        ![[Pasted image 20250413095217.png]]
        
- **Mesh Networks**:
    
    - Consist of interconnected nodes that dynamically communicate with each other.
        
    - Provide redundancy and self-healing capabilities, making them ideal for large-scale applications like smart cities and IoT.
        
        ![[Pasted image 20250413095233.png]]
        
- **Ad Hoc Networks**:
    
    - Decentralized network where nodes communicate directly without infrastructure.
        
    - Suitable for temporary setups, such as in emergency response or military situations.
        
        ![[Pasted image 20250413095246.png]]
        
- **Infrastructure Networks**:
    
    - Use fixed routers and access points to manage traffic and communication.
        
    - Common in residential and commercial settings for stable and controlled connectivity.
        
        ![[Pasted image 20250413095257.png]]
        
---

### **3. Encryption**

- **Purpose**: Ensures that data transmitted over the wireless network is protected by converting it into a coded format.
    
- **Importance**: Prevents unauthorized access to the network and data, keeping information secure during transmission.
    

---

### **4. WPA2 and WPA3 Security Protocols**

- **WPA2**:
    
    - Uses a **pre-shared key (PSK)** for authentication and **AES encryption** for data security.
        
    - Vulnerable to the **KRACK (Key Reinstallation Attack)**, which can compromise the security of the encryption.
        
- **WPA3**:
    
    - Improved security over WPA2, with **Simultaneous Authentication of Equals (SAE)** for authentication and **GCMP encryption** for data protection.
        
    - Vulnerable to the **Dragonblood attack**, a potential security flaw discovered in WPA3.
        

---

### **5. Guest Networks**

- **Purpose**: Provides internet access for visitors while keeping the main network secure.
    
- **Function**: Isolates guest traffic from critical internal resources, ensuring the integrity and security of the primary network.
    

---

### **6. Captive Portals**

- **What it is**: A web page that appears automatically when a user connects to a public or semi-public Wi-Fi network.
    
- **Purpose**: Requires user interaction (such as authentication, accepting terms, or payment) before granting network access.
    
- **Use Case**: Commonly used in guest networks to manage access and provide security controls.
    

---

### **7. Authentication in Wireless Networks**

- **Purpose**: Ensures that only authorized devices can connect to the network, preventing unauthorized access.
    
- **Methods**:
    
    - **Pre-shared Key (PSK)**: A simple shared key used by all network users, commonly used in home or small office networks. While easy to set up, it offers lower security as the same key is shared by everyone.
        
    - **Enterprise Authentication**: Uses a **RADIUS server** to manage individual user credentials, offering more secure access management. This method is more suitable for larger organizations, providing stronger security and control over network access.
        

---