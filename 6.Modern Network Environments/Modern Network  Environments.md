
---

### **Software-Defined Networking (SDN)**

**What it is:**  
A new way of managing networks using software instead of hardware.

**Why it matters:**  
It separates how traffic is controlled from how it's actually sent, making it easier to manage and change the network using software tools.

---

### **SD-WAN (Software-Defined Wide Area Network)**

**What it is:**  
A type of SDN that helps manage wide-area networks (like connections between company branches).

**Why it matters:**  
It finds the best path for network traffic automatically, improving speed and reliability for important apps.

---

### **How SDN Works – The 3 Layers:**

1. **Data Plane:**  
    Moves packets from one place to another (like delivery trucks).
    
2. **Control Plane:**  
    Decides _how_ and _where_ to send the packets (like traffic control).
    
3. **Application Plane:**  
    Runs software that uses network services (like the apps you use to check traffic or maps).
    
    ![[Pasted image 20250412043730.png]]
    
---

### **Application-Aware SD-WAN**

**What it is:**  
It can recognize different types of apps and decide which ones are more important.

**Why it matters:**  
It gives more bandwidth and faster routes to critical business apps (like video calls or CRM software).

---

### **Zero-Touch Provisioning (ZTP)**

- **What it does:** Allows network devices to set themselves up automatically.
    
- **Why it’s useful:** No need for manual setup — great for quickly setting up devices in branch offices.
    
- **How it works:** Devices fetch their configuration from a central server as soon as they connect to the network.
    

---

### **Transport Agnostic**

- **Meaning:** SDN (Software-Defined Networking) can use different types of internet connections like:
    
    - MPLS
        
    - Broadband
        
    - LTE (mobile data)
        
- **Benefit:** Gives flexibility to use the most cost-effective or best-performing connection type available.
    

---

### **Central Policy Management**

- **What it is:** A way to manage all SDN devices from one central place.
    
- **Why it’s good:** You can push out updates, apply rules, or change settings across the whole network easily and consistently.
    

---

### **VXLAN (Virtual Extensible LAN)**

- **Purpose:** Used in large cloud networks to support **millions of virtual networks** (way more than traditional VLANs).
    
- **How it works:** It wraps (encapsulates) Layer 2 traffic (like Ethernet frames) inside Layer 3 packets (like IP/UDP) so they can move across different networks.
    

---

### **DCI (Data Center Interconnect)**

- **Why VXLAN helps:** VXLAN makes it possible to link different data centers so they behave like one big network.
    
- **Benefit:** You can move virtual machines (VMs) between data centers **without reconfiguring** the network.
    

---

### **Layer 2 Encapsulation with VXLAN**

- **What happens:** VXLAN wraps regular Layer 2 traffic (Ethernet frames) inside Layer 3 UDP packets.
    
- **Why this matters:** It helps scale beyond the **4096 VLAN limit** up to **16 million networks**, which is important in cloud environments.
    

---

### **Zero Trust Security Model**

- **Basic idea:** **"Never trust, always verify."**
    
- **What it means:** Every person or device must be verified **every time** they try to access anything — even inside the network.
    
- **Why it matters:** Reduces risk of attacks by treating everyone as a potential threat and **enforcing strict access rules**.
    
---

### **Policy-Based Authentication (in Zero Trust)**

**What it means:**  
Everyone—inside or outside the company—must prove who they are **every time** they access anything.

**How it's done:**

- **MFA** (like a password + phone code)
    
- **Biometrics** (like fingerprint or face scan)
    
- **Behavior analysis** (checking if you're acting like the usual user)
    

**Why it matters:**  
It prevents unauthorized access, even if someone gets your password.

---

### **Authorization in Zero Trust Architecture (ZTA)**

**What it means:**  
Even after you’re authenticated, **you’re only allowed access to what you actually need**, and only **while you need it**.

**How it works:**  
It checks:

- Who you are
    
- Where you're logging in from
    
- What device you're using
    
- What you’re trying to access
    
- If anything looks unusual
    

**Why it matters:**  
It blocks suspicious activity and reduces chances of a breach.

---

### **Least Privilege**

**What it means:**  
Give people and systems **only the access they absolutely need**—nothing more.

**Example:**  
If someone only needs to read files, they shouldn’t have permission to delete or change them.

**Why it matters:**  
Limits damage if someone’s account gets compromised or they make a mistake.

---

### **SASE (Secure Access Service Edge)**

**What it means:**  
A framework that combines **networking + security** into one cloud-based service.

**Why it matters:**  
No matter where your users are (office, home, café), they get **safe and fast** access to company resources.

![[Pasted image 20250412050041.png]]

---

### **SSE (Security Service Edge)**

**What it is:**  
It’s like the security half of SASE. Focuses only on **cloud-based security services** like:

- Secure Web Gateways (block dangerous websites)
    
- CASB (protect cloud apps like Google Drive)
    
- ZTNA (secure access based on Zero Trust)
    

**Why it matters:**  
Keeps users safe **even outside traditional network boundaries**.

---

### **Infrastructure as Code (IaC)**

**What it means:**  
Instead of setting up servers and networks manually, you write code that does it for you.

**Why it matters:**

- Saves time
    
- Avoids human error
    
- Makes setups consistent every time
    

**Example:**  
Imagine clicking one button and your entire app environment (servers, storage, firewalls) is ready.

![[Pasted image 20250412050122.png]]

---

### **Automation in IaC**

**What it means:**  
IaC uses automation to create and manage infrastructure **fast and accurately**.

**Why it matters:**

- Speeds up deployments
    
- Keeps environments consistent
    
- Frees up human time from repetitive setup tasks
    
---

### **Playbooks, Templates, and Reusable Tasks**

**What they are:**

- **Playbooks**: Step-by-step instructions (like a recipe) to set up or manage systems.
    
- **Templates**: Pre-made setups you can customize and reuse.
    
- **Reusable Tasks**: Common actions (like installing software) that can be reused across multiple setups.
    

**Why they matter:**  
They make deployments faster, consistent, and easy to repeat on many systems.

---

### **Configuration Drift and Compliance**

**Configuration Drift:**  
When someone manually changes a system, it might not match the original setup anymore.

**How IaC helps:**  
IaC automatically applies the correct settings every time, keeping everything as planned.

**Compliance:**  
IaC helps you follow company or legal rules by automating correct setups every time.

---

### **Upgrades with IaC**

**What it means:**  
Upgrading systems becomes as easy as updating the code.

**Benefits:**

- Changes are **planned** and **controlled**
    
- If something breaks, you can **roll back** to the previous version
    
- Keeps systems updated **safely**
    

---

### **Dynamic Inventories**

**What it is:**  
Automatically keeping track of all the servers or devices in your network in real-time.

**Why it matters:**  
If your environment changes often (like in the cloud), you don’t need to manually update your inventory—it’s always up to date and ready for deployment.

---
### **Source Control in IaC**

**What it means:**  
Just like developers use code to build apps, IaC uses code to build infrastructure. So, we need a way to track and manage that code. That’s where **source control** comes in.

**Why it matters:**

- Keeps track of all infrastructure changes
    
- Helps teams work together smoothly
    
- Prevents mistakes and makes recovery easy
    

---

### **Version Control**

**What it does:**

- Tracks every change made to the infrastructure code
    
- Saves older versions so you can roll back if something goes wrong
    
- Shows who made what change and when
    

**Why it matters:**  
Helps fix mistakes quickly and keeps everything organized.

---

### **Central Repository**

**What it is:**  
A shared online space (like GitHub or GitLab) where all team members store and access the same code.

**Why it matters:**

- Everyone works from the same version of the code
    
- Makes teamwork and collaboration easier
    
- Increases security and consistency
    

---

### **Conflict Identification**

**What happens:**  
If two people change the same part of the code at the same time, the system spots the **conflict** and alerts you.

**Why it matters:**  
Prevents one person’s work from accidentally deleting or overwriting someone else’s work.

---

### **Branching**

**What it is:**  
Lets developers create a separate copy (a **branch**) of the main code so they can:

- Try out new ideas
    
- Fix bugs
    
- Make changes safely
    

**Why it matters:**  
You can work on improvements without breaking the main system. Once everything is tested, changes can be added back to the main code.

---

### **IPv6 Addressing**

- **What it is:** The newer version of IP (Internet Protocol) that replaces IPv4.
    
- **Why we need it:** IPv4 only supports about 4.3 billion addresses, and we’ve run out!
    
- **IPv6 uses:** 128-bit addresses — which means **trillions of possible IPs**.
    
- **Other benefits:** Better security, easier configuration, and more efficient routing.
    

---

### **Mitigating Address Exhaustion**

- IPv6 gives us **more than enough addresses** to handle the growing number of devices worldwide.
    
- Solves the problem of **IP address shortages** that IPv4 couldn’t handle.
    

---

### **Compatibility Requirements**

- Not all systems support IPv6 yet.
    
- So we need ways to **run IPv4 and IPv6 side-by-side** while the internet gradually shifts to IPv6.
    
- This transition will take years, so both protocols need to work together.
    

---

### **Tunneling**

- Helps send **IPv6 data through IPv4 networks**.
    
- IPv6 packets are **wrapped inside IPv4 packets**, like a letter inside another envelope.
    
- Useful when parts of a network **don’t support IPv6** yet.
    

---

### **Dual Stack**

- Devices run **both IPv4 and IPv6 at the same time**.
    
- They can talk to either type of device depending on what’s available.
    
- Makes the transition smoother without cutting off IPv4 users.
    

---

### **NAT64**

- A translator between IPv6 and IPv4 networks.
    
- **IPv6-only devices** can still talk to **IPv4-only devices** by converting the addresses.
    
- Helps during the time when **not everything supports IPv6** yet.
    

---
