
### 🕸️ 1. Spanning Tree Protocol (STP)

- **Purpose**: Prevents **network loops** and **broadcast storms** by creating a **loop-free logical topology**.
    
- **Common Issues**:
    
    - Incorrect **root bridge** selection
        
    - Misconfigured **port roles** or **states**
        

#### 🌲 STP Key Concepts

- **Root Bridge**: Central reference switch in STP.
    
    - Chosen using the **lowest Bridge ID** (priority + MAC).
        
    - ✅ _Best practice_: Set priority to force a preferred switch as root.
        
        ![[Pasted image 20250420062858.png]]
        
- **Port Roles**:
    
    - **Root Port**: Best path **toward** the root bridge
        
    - **Designated Port**: Best path **outward** to a segment
        
    - **Blocked Port**: Prevents loops by not forwarding
        
- **Port States**:
    
    1. **Blocking** – No traffic forwarded
        
    2. **Listening** – Prepares to forward; no MAC learning yet
        
    3. **Learning** – Learns MACs, no forwarding
        
    4. **Forwarding** – Fully active
        
    
    - 🚫 _Issue_: Wrong port state = traffic disruption
        

---

### ⚙️ 2. Incorrect VLAN Assignment

- **Issue**: Devices placed in the wrong VLAN
    
    - Breaks **connectivity** between intended hosts
        
    - Can cause **unauthorized access** to sensitive segments
        
- **Fix**:
    
    - Audit switch port VLAN assignments
        
    - Enforce strict segmentation and verify tagging
        

---

### 🛡️ 3. Access Control Lists (ACLs)

- **Function**: Define rules that **permit or deny** traffic based on IPs, ports, protocols, etc.
    
- **Issues**:
    
    - Misconfigured ACLs block valid users or allow threats
        
- **Fix**:
    
    - Review ACLs line-by-line
        
    - Test rules before deployment
        
    - Conduct **regular audits** to align with policies
        

---

## 🧭 Routing Issues

### 🚦 4. Route Selection Issues

- **Impact**: Incorrect routes cause:
    
    - **High latency**
        
    - **Packet loss**
        
    - **Routing loops or blackholes**
        
- **Fix**:
    
    - Check routing tables (static/dynamic)
        
    - Validate metrics and administrative distances
        
    - Use route summarization and avoid route flapping
        

---

## 📘 Routing Table Issues

### 🧊 1. **Stale Routes**

- **What it is**: Old or invalid routes still present in the routing table.
    
- **Impact**: Can cause **packet misrouting**, blackholes, or dropped connections.
    
- **Fix**:  
    ✅ Regularly **refresh routing tables** (manual or via dynamic protocols).
    

---

### 🛣️ 2. **Misconfigured Static Routes**

- **What it is**: Manually entered routes with wrong destination or next-hop info.
    
- **Impact**:
    
    - **Packet loss**
        
    - **Routing loops**
        
    - **Connectivity issues**
        
- **Fix**:  
    ✅ Double-check static routes for **correct IP, subnet, and next-hop**  
    ✅ Match routes with the **actual network topology**
    

---

### 🔄 3. **Dynamic Routing Protocol Conflicts**

- **What it is**: Issues arise from:
    
    - **Conflicting route advertisements**
        
    - **Mismatched configurations** between routers using OSPF, EIGRP, BGP, etc.
        
- **Impact**:
    
    - Inconsistent routing tables
        
    - Instability in route selection
        
- **Fix**:  
    ✅ Ensure **protocols are configured consistently** across routers  
    ✅ Avoid overlapping or contradictory route advertisements
    

---

## 🧭 Default Route Issues

### 🚫 4. **Missing Default Route**

- **What it is**: No route for unknown or external destinations.
    
- **Impact**:
    
    - **Internet traffic fails**
        
    - Packets for unfamiliar networks are **dropped**
        
- **Fix**:  
    ✅ Set a **default route** (e.g., `0.0.0.0/0`) to the appropriate **gateway**
    

---

### 🧍‍♂️ 5. **Incorrect Default Route**

- **What it is**: Default route points to the **wrong gateway**.
    
- **Impact**:
    
    - Packets **leave the network incorrectly**
        
    - **No return traffic** = broken communication
        
- **Fix**:  
    ✅ Verify **gateway IP**, interface, and **next-hop reachability**
    

---

## 🧠 **1. Address Pool Exhaustion**

### 🔍 **What Happens:**

The **DHCP server runs out of IPs** to assign to devices.

### ⚠️ **Causes:**

- Too many devices (over-subscription)
    
- Small DHCP scope
    
- Devices holding on to leased IPs
    

### ✅ **Fix:**

- Expand the DHCP scope/subnet
    
- Use IP Address Management (**IPAM**)
    
- Set proper lease times & ensure devices release IPs properly
    

---

## 🌐 **2. Incorrect Default Gateway**

### 🔍 **What Happens:**

Devices **can't reach external networks**, including the internet.

### ⚠️ **Causes:**

- Wrong gateway IP address
    
- Gateway IP not in the same subnet
    
- Conflicting multiple gateways
    

### ✅ **Fix:**

- Verify correct default gateway IP
    
- Ensure it's within the device's subnet
    
- Standardize gateway settings across devices
    

---

## 🏷️ **3. Incorrect IP Address**

### 🔍 **What Happens:**

Device **fails to connect** to the network.

### ⚠️ **Causes:**

- Manual entry mistakes
    
- Static IP conflicts with DHCP
    

### ✅ **Fix:**

- Double-check IP configurations
    
- Use **DHCP reservations** for devices needing static IPs
    

---

## 📛 **4. Duplicate IP Address**

### 🔍 **What Happens:**

**IP conflict** causes connection loss for one or both devices.

### ⚠️ **Causes:**

- Manually assigning same IP to multiple devices
    
- DHCP server reassigning already-in-use IP
    

### ✅ **Fix:**

- Use **IPAM tools** to detect duplicates
    
- Avoid overlap between static and DHCP scopes
    
- Regular network scans for conflicts
    

---

## 🧮 **5. Incorrect Subnet Mask**

### 🔍 **What Happens:**

Devices **can’t communicate** properly due to incorrect network boundaries.

### ⚠️ **Causes:**

- Subnet mask typed incorrectly
    
- Subnet mask doesn’t match the rest of the network
    

### ✅ **Fix:**

- Verify subnet mask during config
    
- Train admins on proper subnetting
    
- Use planning tools to design valid subnet schemes
    