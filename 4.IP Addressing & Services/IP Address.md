
An IP address (Internet Protocol address) is a unique identifier assigned to devices connected to a network, allowing them to communicate with each other over the internet or a local network.

---

### 📌 **IPv4 Overview**

- **IPv4** stands for **Internet Protocol version 4**.
    
- It uses a **32-bit** address format (e.g., `192.168.0.1`).
    
- Total possible addresses: **2³² = ~4.3 billion**.
    
- Due to massive internet growth, IPv4 addresses are now **largely exhausted**.
    

---

### 📂 **Types of IPv4 Addresses**

#### 1. **Private IP Address**

- **Used within private networks** (home, office LANs).
    
- Not routable on the public internet.
    
- Must use a **NAT (Network Address Translation)** device to access the internet.
    
- **Ranges:**
    
    - `10.0.0.0` – `10.255.255.255`
        
    - `172.16.0.0` – `172.31.255.255`
        
    - `192.168.0.0` – `192.168.255.255`
        

#### 2. **Public IP Address**

- Assigned by your **Internet Service Provider (ISP)**.
    
- **Globally unique** and **routable** on the internet.
    
- Used to identify your device/network online.
    
- Example: `8.8.8.8` (Google DNS)
    

#### 3. **Automatic IP Address (APIPA)**

- Assigned **automatically** by a system when a DHCP server is not available.
    
- Range: `169.254.0.1` to `169.254.255.254`
    
- Used for **local communication only** (e.g., two PCs on the same switch).
    

#### 4. **Other Address Types (in IPv4):**

- **Loopback Address**: `127.0.0.1` – used to test local network stack (your own device).
    
- **Broadcast Address**: `255.255.255.255` – sends to all hosts on the network.
    
- **Multicast Address**: `224.0.0.0` to `239.255.255.255` – used to send to multiple hosts.
    

---

### 📊 **IPv4 Address Classes Table with Use Cases**

| **Class** | **IP Range**                    | **Bits for Network** | **Default Subnet Mask** | **CIDR** | **Usable Hosts**      | **Use Case**                         | **Example**                   |
| --------- | ------------------------------- | -------------------- | ----------------------- | -------- | --------------------- | ------------------------------------ | ----------------------------- |
| **A**     | `1.0.0.0` – `126.255.255.255`   | 8 bits               | `255.0.0.0`             | `/8`     | ~16.7 million (2³²−2) | Very large networks                  | Google, ISP core networks     |
| **B**     | `128.0.0.0` – `191.255.255.255` | 16 bits              | `255.255.0.0`           | `/16`    | ~65,534               | Medium-sized networks (e.g., campus) | University campus network     |
| **C**     | `192.0.0.0` – `223.255.255.255` | 24 bits              | `255.255.255.0`         | `/24`    | 254                   | Small networks (homes/offices)       | Home Wi-Fi or office LAN      |
| **D**     | `224.0.0.0` – `239.255.255.255` | —                    | _N/A_                   | _N/A_    | _Multicast only_      | Multicasting (one-to-many)           | Live webinar or IPTV          |
| **E**     | `240.0.0.0` – `255.255.255.255` | —                    | _N/A_                   | _N/A_    | _Not for public use_  | Experimental and reserved addresses  | Research/testing (future use) |

---
### 🔢 **What is CIDR?**

**CIDR** stands for **Classless Inter-Domain Routing**.

It’s a way to **represent IP addresses and their subnet masks** more efficiently.

---

### 🧠 **In Simple Terms:**

CIDR is like **shorthand** for writing how many IP addresses are in a group (called a **subnet**).

Instead of writing:

```
IP: 192.168.1.0  
Subnet Mask: 255.255.255.0
```

You can just write:

```
192.168.1.0/24
```

✅ That **`/24`** is the **CIDR notation** — it means the **first 24 bits** are the network part.

---

### 🔍 **How CIDR Works:**

- IP addresses are 32 bits (for IPv4).
    
- CIDR notation says how many bits belong to the **network part**.
    
- The rest are for **hosts** (devices).
    

| CIDR | Subnet Mask     | Number of Hosts |
| ---- | --------------- | --------------- |
| /8   | 255.0.0.0       | ~16 million     |
| /16  | 255.255.0.0     | ~65,000         |
| /24  | 255.255.255.0   | 256             |
| /30  | 255.255.255.252 | 4               |

---

### 🧩 **What is IPv4 Subnetting?**

**IPv4 Subnetting** is the process of dividing a **large IP network** into **smaller, more manageable sub-networks** called **subnets**.

---

### ✅ **Why Subnet?**

| **Purpose**           | **Explanation**                                                         |
| --------------------- | ----------------------------------------------------------------------- |
| 💡 **Efficiency**     | Prevents wasting IP addresses (especially in Class A/B networks).       |
| 🔒 **Security**       | Isolates sensitive departments (e.g., HR, Finance) from general access. |
| 🚀 **Performance**    | Limits broadcast traffic to smaller areas, reducing congestion.         |
| 🛠️ **Manageability** | Easier to troubleshoot and control smaller segments.                    |

---

### 🛠️ **How It Works:**

- Start with a large network (e.g., `192.168.1.0/24`).
    
- Subnet it into smaller parts (e.g., four `/26` subnets: each with 64 IPs).
    
- Each subnet has its own **range**, **broadcast**, and **usable host** IPs.
    

---

### 🧠 **Real-World Use Case:**

A company has:

- HR department with 50 devices
    
- IT with 30 devices
    
- Sales with 60 devices
    

Instead of putting all devices in one network, subnetting allows:

- HR → `192.168.1.0/26`
    
- IT → `192.168.1.64/26`
    
- Sales → `192.168.1.128/26`
    

Each department gets its own subnet, improving **security, control, and performance**.

---

## 🧠 **Full Subnet Table (with Example IPs)**

| **CIDR** | **Subnet Mask** | **# Total IPs** | **Usable IPs** | **First Usable IP** | **Broadcast IP** |
| -------- | --------------- | --------------- | -------------- | ------------------- | ---------------- |
| /32      | 255.255.255.255 | 1               | 0              | -                   | 192.168.0.0      |
| /31      | 255.255.255.254 | 2               | 0              | -                   | 192.168.0.1      |
| /30      | 255.255.255.252 | 4               | 2              | 192.168.0.1         | 192.168.0.3      |
| /29      | 255.255.255.248 | 8               | 6              | 192.168.0.1         | 192.168.0.7      |
| /28      | 255.255.255.240 | 16              | 14             | 192.168.0.1         | 192.168.0.15     |
| /27      | 255.255.255.224 | 32              | 30             | 192.168.0.1         | 192.168.0.31     |
| /26      | 255.255.255.192 | 64              | 62             | 192.168.0.1         | 192.168.0.63     |
| /25      | 255.255.255.128 | 128             | 126            | 192.168.0.1         | 192.168.0.127    |
| /24      | 255.255.255.0   | 256             | 254            | 192.168.0.1         | 192.168.0.255    |
| /23      | 255.255.254.0   | 512             | 510            | 192.168.0.1         | 192.168.1.255    |
| /22      | 255.255.252.0   | 1024            | 1022           | 192.168.0.1         | 192.168.3.255    |
| /21      | 255.255.248.0   | 2048            | 2046           | 192.168.0.1         | 192.168.7.255    |
| /20      | 255.255.240.0   | 4096            | 4094           | 192.168.0.1         | 192.168.15.255   |
| /19      | 255.255.224.0   | 8192            | 8190           | 192.168.0.1         | 192.168.31.255   |
| /18      | 255.255.192.0   | 16,384          | 16,382         | 192.168.0.1         | 192.168.63.255   |
| /17      | 255.255.128.0   | 32,768          | 32,766         | 192.168.0.1         | 192.168.127.255  |
| /16      | 255.255.0.0     | 65,536          | 65,534         | 192.168.0.1         | 192.168.255.255  |
| /15      | 255.254.0.0     | 131,072         | 131,070        | 192.168.0.1         | 192.169.255.255  |
| /14      | 255.252.0.0     | 262,144         | 262,142        | 192.168.0.1         | 192.171.255.255  |
| /13      | 255.248.0.0     | 524,288         | 524,286        | 192.168.0.1         | 192.175.255.255  |
| /12      | 255.240.0.0     | 1,048,576       | 1,048,574      | 192.168.0.1         | 192.183.255.255  |
| /11      | 255.224.0.0     | 2,097,152       | 2,097,150      | 192.168.0.1         | 192.199.255.255  |
| /10      | 255.192.0.0     | 4,194,304       | 4,194,302      | 192.168.0.1         | 192.231.255.255  |
| /9       | 255.128.0.0     | 8,388,608       | 8,388,606      | 192.168.0.1         | 192.255.255.255  |
| /8       | 255.0.0.0       | 16,777,216      | 16,777,214     | 192.168.0.1         | 193.255.255.255  |
| /7       | 254.0.0.0       | 33,554,432      | 33,554,430     | 192.168.0.1         | 195.255.255.255  |
| /6       | 252.0.0.0       | 67,108,864      | 67,108,862     | 192.168.0.1         | 199.255.255.255  |
| /5       | 248.0.0.0       | 134,217,728     | 134,217,726    | 192.168.0.1         | 207.255.255.255  |
| /4       | 240.0.0.0       | 268,435,456     | 268,435,454    | 192.168.0.1         | 223.255.255.255  |
| /3       | 224.0.0.0       | 536,870,912     | 536,870,910    | 192.168.0.1         | 255.255.255.255  |
| /2       | 192.0.0.0       | 1,073,741,824   | 1,073,741,822  | 192.168.0.1         | 255.255.255.255  |
| /1       | 128.0.0.0       | 2,147,483,648   | 2,147,483,646  | 192.168.0.1         | 255.255.255.255  |
| /0       | 0.0.0.0         | 4,294,967,296   | 4,294,967,294  | 192.168.0.1         | 255.255.255.255  |

---

## 🌐 **IPv6 (Internet Protocol Version 6)**

IPv6 is the **newest version** of the Internet Protocol, created to **replace IPv4**, which has run out of available addresses.

---

### 📌 **Why IPv6 was created:**

- **IPv4 = 32-bit** (≈ 4.3 billion addresses)
    
- **IPv6 = 128-bit** (≈ 340 undecillion addresses → 3.4 × 10³⁸)
    
- More devices (phones, cars, smart homes) = more IPs needed!
    
    ![[Pasted image 20250409050824 1.png]]
    
    ![[Pasted image 20250409051045 1.png]]
    

---

### 🆚 **IPv4 vs IPv6 Quick Compare**

| Feature         | IPv4                          | IPv6                               |
| --------------- | ----------------------------- | ---------------------------------- |
| Address Length  | 32 bits                       | 128 bits                           |
| Address Format  | Decimal (e.g., `192.168.0.1`) | Hexadecimal (e.g., `2001:0db8::1`) |
| Total Addresses | ~4.3 billion                  | ~340 undecillion                   |
| Security        | Optional IPSec                | IPSec is mandatory                 |
| Broadcast       | Supported                     | **No Broadcast**, uses **Anycast** |
| Configuration   | Manual / DHCP                 | Supports **Autoconfiguration**     |
| Efficiency      | Limited multicast             | **Multicast and Anycast built-in** |

---

### ✅ **IPv6 Key Benefits**

#### 🔢 **1. More Addresses**

- 128-bit space = unlimited future device support.
    
- Every person on Earth could have trillions of IPs!
    

#### 🔐 **2. Built-in Security**

- IPSec (encryption/authentication) is native in IPv6.
    

#### ⚡ **3. Better Performance**

- No more broadcast storms.
    
- Uses **multicast** and **anycast** for efficient routing.
    

#### 🔌 **4. Easier to Configure**

- Devices can **auto-configure** themselves using:
    
    - **Link-local address**
        
    - Their **MAC address**
        

---

## 🧭 **IPv6 Address Types**

| **Type**           | **Prefix / Example** | **Purpose / Notes**                                                            |
| ------------------ | -------------------- | ------------------------------------------------------------------------------ |
| **Unicast**        | —                    | One-to-one communication (single unique device)                                |
| **Multicast**      | `FF00::/8`           | One-to-many (group of devices) — replaces broadcast in IPv6                    |
| **Anycast**        | —                    | One-to-nearest — multiple devices share address, nearest one responds          |
| **Link-Local**     | `FE80::/10`          | Local LAN only — auto-assigned for neighbor discovery, not routable externally |
| **Unique Local**   | `FC00::/7`           | Private/internal use only — like IPv4 `192.168.x.x` or `10.x.x.x`              |
| **Loopback**       | `::1`                | Refers to the same local machine — like `127.0.0.1` in IPv4                    |
| **Unspecified**    | `::`                 | All zeros — used when a device doesn’t yet have an IP (e.g., DHCPv6 request)   |
| **Global Unicast** | `2000::/3`           | Publicly routable address on the internet — like IPv4 public IPs               |

## 🧠 **Classful vs Classless Networking**

---

### 🔸 **Classful Networking (Old-School Way)**

- Think of this like **preset boxes** for IP addresses.
    
- IPs were split into **Class A, B, and C**, each with a **fixed size**.
    

|Class|Range|Default Subnet Mask|IPs per Network|
|---|---|---|---|
|A|1.0.0.0 – 126.255.255.255|`255.0.0.0` or `/8`|~16 million|
|B|128.0.0.0 – 191.255.255.255|`255.255.0.0` or `/16`|~65,000|
|C|192.0.0.0 – 223.255.255.255|`255.255.255.0` or `/24`|254|

✅ **Easy idea:** You had to use the whole box even if you only needed a little — which wasted a lot of IPs.

❌ **Problem:** Not flexible — small networks had to use a big block of IPs even if they didn’t need them.

---

### 🔹 **Classless Networking (CIDR/VLSM)**

This is the **modern, smarter way** to use IP addresses.

---

### 📌 **CIDR (Classless Inter-Domain Routing)**

- Uses **slash notation** like `/24`, `/28`, etc.
    
- You can pick exactly **how many IPs** you want.
    

✅ Example:

- `192.168.1.0/24` → 256 IPs
    
- `192.168.1.0/30` → just 4 IPs
    

🔧 Much more flexible = no wasted space!

---

### 📌 **VLSM (Variable Length Subnet Mask)**

- Lets you **break up one network** into **different-sized pieces**, depending on what you need.
    

✅ Example:  
You have `192.168.1.0/24` and divide it like:

- A subnet for 50 devices → `/26`
    
- Another for 10 devices → `/28`
    
- One for 2 devices → `/30`
    

💡 VLSM = Efficient use of every IP address.

---
