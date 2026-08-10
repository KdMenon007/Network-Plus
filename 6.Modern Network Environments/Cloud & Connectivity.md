
---

### 🌐 **Network Functions Virtualization (NFV)**

- Runs **network functions as software** (e.g., firewalls, IDS, load balancers).
    
- No need for physical devices.
    
- Helps with **scaling**, **cost savings**, and **resource efficiency**.
    

---

### ☁️ **Virtual Private Cloud (VPC)**

- A **private network** inside the **public cloud**.
    
- You can:
    
    - Set your own IP range
        
    - Create subnets
        
    - Add route tables and gateways
        
- Works like your own data center in the cloud.
    

---

### 🔒 **Network Security Groups & Lists**

- **Control traffic** in and out of cloud resources.
    
- Work like **virtual firewalls**:
    
    - Based on **IP, port, and protocol rules**
        
- Can be **stateful or stateless** depending on the platform.
    

---

### 🌍 **Internet Gateway**

- Connects your **VPC to the internet**.
    
- Needed for instances that must access the web.
    

---

### 🚪 **NAT Gateway**

- Lets **private subnet** instances **access the internet** (e.g., for updates).
    
- **Blocks inbound connections** from the internet to keep them safe.
    

---

### 🔗 **Cloud Gateways**

- Connect **on-premises**, other clouds, or networks to your cloud.
    
- Used for **data transfer** and **communication** between environments.
    
    ![[Pasted image 20250414145628.png]]
    

---

### 🌐 **Cloud Connectivity Options**

- Methods to connect to the cloud:
    
    - **VPN**
        
    - **Direct/private connections**
        
    - **Cloud gateways**
        
- Focus on **security, speed, and reliability**.
    

---

### 🔐 **Virtual Private Network (VPN)**

- **Secure tunnel** over the internet.
    
- Connects remote users or offices to the main network.
    
    ![[Pasted image 20250414145643.png]]
    
---

### 🧬 **Private-Direct Connection to Cloud**

- Dedicated link from your site to the cloud (not over the public internet).
    
- Offers:
    
    - **Better speed**
        
    - **More security**
        
    - **Higher reliability**
        

---

### 🚀 **Deployment Models**

- Where and how your services run:
    

#### 🔹 Public Cloud

- Shared by many users
    
- Most **affordable**, but **least secure**
    
#### 🔹 Private Cloud

- **Dedicated** to one organization
    
- Most **secure** and **expensive**
    

#### 🔹 Community Cloud

- Shared by organizations with similar needs
    
- Managed by one or all members or a third party
    

#### 🔹 Hybrid Cloud

- Mix of **public, private, or on-premises** environments
    
- Offers **flexibility** (e.g., load balancing across systems)
    

---

### 🛠️ **Service Models**

#### ☁️ Software as a Service (SaaS)

- Access software via browser (e.g., Gmail, Zoom)
    
- No installs, pay-as-you-go
    
    ![[Pasted image 20250414145742.png]]
    

#### ☁️ Platform as a Service (PaaS)

- Devs get tools to **build and run apps** without managing hardware (e.g., Heroku)
    
- Simplifies deployment
    
    ![[Pasted image 20250414145808.png]]
    

#### ☁️ Infrastructure as a Service (IaaS)

- Rent **servers, storage, and networking**
    
- You manage everything except the physical hardware (e.g., AWS EC2)
    
    ![[Pasted image 20250414145756.png]]
    

---

### ⚙️ **Cloud Traits**

- **Multitenancy**: Shared use of cloud by multiple users
    
- **Elasticity**: Automatically adjusts resources as needed
    
- **Scalability**: Easily **add more resources** like CPU, RAM, or servers
    

---

