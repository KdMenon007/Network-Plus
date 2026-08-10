
---

### **Routing**

- **What it is:** Choosing the best path for data to travel in a network.
    
- **Who does it:** **Routers** handle routing.
    
- **How it works:** Uses **routing tables** and **algorithms** to decide the best way for data to reach its destination.
    
    ![[Pasted image 20250413053455.png]]
    
    ![[Pasted image 20250413053513.png]]
    
    ![[Pasted image 20250413053537.png]]
    
---

### **Static Routing**

- **Manual setup:** Routes are added by a network admin.
    
- **Good for:** Small, simple networks.
    
- **Limitations:**
    
    - Doesn’t change automatically.
        
    - Not good for large or changing networks.
        

---

### **Dynamic Routing**

- **Automatic:** Routers update paths on their own.
    
- **How it works:** Routers share info using **dynamic routing protocols**.
    
- **Benefits:**
    
    - Adapts to network changes (like link failures or traffic).
        
    - Always finds the best route.
        

---
![[Pasted image 20250413053746.png]]

---

### **Routing Protocol Categories**

#### **1. Interior Gateway Protocol (IGP)**

- Used **within** an organization (e.g., New York branch to LA branch).
    
- Routes traffic inside a company’s network.
    
    ![[Pasted image 20250413054021.png]]
    

#### **2. Exterior Gateway Protocol (EGP)**

- Used **between** different organizations (e.g., across the Internet).
    
- **BGP (Border Gateway Protocol)** is the only EGP and powers Internet routing.
    
- Every organization has an **Autonomous System (AS)**—a group of its connected networks.
    

---

### **Interior Gateway Protocol Types**

#### ✅ **Distance-Vector Protocol**

- Chooses the path with the **fewest hops**.
    
- Easy setup, but slower to update routes.
    
    ![[Pasted image 20250413054047.png]]
    

#### ✅ **Link-State Protocol**

- Chooses the path with the **best bandwidth**.
    
- Faster, smarter, and more efficient.
    
    ![[Pasted image 20250413054103.png]]
    
---

### **Popular Routing Protocols**

#### 🔹 **RIP (Routing Information Protocol)**

- **Type:** Distance-vector
    
- **Metric:** Hop count (max 15 hops)
    
- **Versions:**
    
    - **RIPv1:** No subnet info, outdated.
        
    - **RIPv2:** Supports subnetting, uses multicast, basic security.
        
- **Best for:** Small networks
    
- **Limitations:** Slow and not scalable.
    

---

#### 🔹 **OSPF (Open Shortest Path First)**

- **Type:** Link-state
    
- **Key Features:**
    
    - Fast updates only when needed.
        
    - Supports VLSM & CIDR.
        
    - Organized into **areas** for efficiency.
        
- **Best for:** Large and complex networks
    
- **Advantages:** Fast, scalable, and supports load balancing.
    

---

#### 🔹 **EIGRP (Enhanced Interior Gateway Routing Protocol)**

- **Type:** Hybrid (distance-vector + link-state)
    
- **Key Features:**
    
    - Uses multiple metrics (bandwidth, delay, etc.)
        
    - Sends updates only when things change.
        
    - Supports VLSM & CIDR.
        
- **Best for:** Medium to large networks (especially Cisco environments)
    
- **Advantages:** Fast, efficient, scalable, and reliable.
    

---

### 🔹 **Routing Metrics**

- A **metric** is a value used to decide the **best path** for data.
    
- **Lower metric = better path**.
    
- Different protocols use different factors to calculate it:
    
    - **Hop count** (e.g., RIP)
        
    - **Bandwidth, delay, reliability** (e.g., EIGRP)
        
    - **Custom values or path attributes** (e.g., BGP)
        

---

### 🌐 **BGP (Border Gateway Protocol)**

- **Purpose:** Routes traffic between different organizations across the Internet.
    
- **Used by:** ISPs and large networks.
    
- **Key Features:**
    
    - Supports **CIDR** for efficient IP use.
        
    - Uses **policies and path attributes** to pick the best route.
        
    - Runs over **TCP** for reliable connections.
        
- **Advantages:**
    
    - Very **scalable** and **flexible**.
        
    - Handles **huge routing tables**.
        
    - Ideal for managing complex internet connections.
        

---

### 🚦 **Route Selection**

- Routers choose the best path using:
    
    1. **Administrative Distance (AD)** – Trust level of the route source.
        
    2. **Prefix Length** – More specific (longer) match is preferred.
        
    3. **Metric** – Lower metric is better.
        

---

### 📊 **Administrative Distance (AD) – Trust Ranking**

---

### ✅ **What is Administrative Distance (AD)?**

- It’s like a **trust score** for routing protocols.
    
- Routers use it to decide **which route to trust** when they get **multiple routes** to the same destination.
    
- **Lower AD = More Trusted**
    

---

### 🔢 **Common AD Values:**

| Route Source        | AD Value | Trust Level          |
| ------------------- | -------- | -------------------- |
| Connected Interface | 0        | Most trusted         |
| Static Route        | 1        | Very trusted         |
| External BGP        | 20       | Trusted (external)   |
| EIGRP               | 90       | Trusted (internal)   |
| OSPF                | 110      | Medium trust         |
| RIP                 | 120      | Less trusted         |
| Unknown             | 255      | Not used (untrusted) |

---

### 📏 **Prefix Length**

- Shows how many bits in an IP address are used for the **network portion**.
    
- Written as **CIDR notation** (e.g., `192.168.20.0/26`)
    
    - `/26` means the first 26 bits are the **network**.
        
- Helps define **network boundaries** and **host capacity**.
    

---

### 🔁 **FHRP (First-Hop Redundancy Protocols)**

- **Purpose:** Provide backup routers for **high availability**.
    
- If one router fails, another takes over automatically.
    
- Types:
    
    - **HSRP (Host Standby Router Protocol):** Cisco-only protocol
        
    - **VRRP (Virtual Router Redundancy Protocol):** Open standard version
        

---

### 🧍‍♂️ **Virtual IP (VIP)**

- An IP not tied to a **single physical device**.
    
- Shared by multiple devices (e.g., servers or routers).
    
- Used for:
    
    - **Load balancing**
        
    - **Failover/high availability**
        
- Keeps services running even if one server fails.
    
    ![[Pasted image 20250413054406.png]]
    
---

### 🧩 **Subinterface**

- A **virtual interface** created from one **physical interface**.
    
- Used to handle multiple **VLANs** on one router/switch port.
    
- Allows traffic **segregation** and support for different services.
    

---

### 🔄 **Network Address Translation (NAT)**

- **Translates** private IPs to public IPs (and vice versa).
    
- Used by routers or firewalls to manage IP usage.
    

#### ✅ **Advantages:**

- Saves **public IPs**.
    
- Prevents **IP conflicts** with other networks.
    
- Makes **internet access easier**.
    
- Avoids **renumbering** during network changes.
    

#### ❌ **Disadvantages:**

- Adds **processing delay**.
    
- Breaks **end-to-end IP visibility**.
    
- Some applications may **not work** with NAT.
    
---

### 🧍‍♂️ **Static NAT (One-to-One)**

- Maps **one internal IP** to **one public IP**.
    
- **Use Case:** When an internal device (like a web server) must be reachable from the Internet.
    
- **Example:** 192.168.1.10 → 203.0.113.5
    

---

### 👥 **Dynamic NAT (Many-to-Many)**

- Maps **multiple internal IPs** to a **pool of public IPs**.
    
- Each internal device gets a different public IP **from the pool**.
    
- **Less common** – may restrict how many devices can go online.
    
- **Example:** 10 internal IPs → 5 public IPs (mapped as available)
    

---

### 🌐 **Port Address Translation (PAT / Many-to-One)**

- Maps **many internal IPs** to **one public IP**, using **different port numbers**.
    
- **Most commonly used NAT type**.
    
- Also called **Overloading NAT** or **PNAT**.
    
- **Efficient & scalable** – perfect for Internet access.
    
- **Example:**
    
    - 192.168.1.10:1234 → 203.0.113.1:4001
        
    - 192.168.1.11:2345 → 203.0.113.1:4002
        

---
