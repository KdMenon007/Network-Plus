
---

### 🌐 **Site-to-Site VPN**

- Connects entire **office networks** together over the internet.
    
- Like linking your HQ and branch office into one big private network.
    
- Used for secure, encrypted communication between locations.
    
    ![[Pasted image 20250420052805.png]]
    

---

### 👩‍💻 **Client-to-Site VPN (Remote Access VPN)**

- Lets individual **remote users** (like work-from-home employees) connect securely to the company network.
    
- Requires VPN software on the user's device.
    
    ![[Pasted image 20250420052820.png]]
    

---

### 🌍 **Clientless VPN**

- No need to install software.
    
- Users connect through a **web browser** to access specific internal apps or services securely.
    
    ![[Pasted image 20250420052834.png]]
    

---

### 🔀 **Split Tunnel vs. Full Tunnel VPN**

- **Split Tunnel**: Only work-related traffic goes through the VPN; everything else (like Netflix or Google) uses regular internet.
    
    - Faster, but less secure.
        
- **Full Tunnel**: **All** internet traffic goes through the VPN.
    
    - More secure, but can be slower.
        

---

### 🧩 **Connection Methods (To Manage Network Devices)**

#### 🖥️ **GUI (Graphical User Interface)**

- Point-and-click interface.
    
- Easy to use, visual menus and dashboards.
    

#### 🎛️ **Console Connection**

- Plug directly into the device (with a cable).
    
- Used when setting up a new device or when it's not on the network yet.
    
    ![[Pasted image 20250420052857.png]]
    

#### 🔐 **SSH (Secure Shell)**

- Secure way to connect and manage devices over a network.
    
- Encrypted, safe, and replaces older tools like Telnet.
    
    ![[Pasted image 20250420052908.png]]
    

#### 🔁 **Jump Box (Jump Host)**

- A secure middleman computer.
    
- Admins log into it first, then use it to access more sensitive systems.
    
- Adds an extra layer of security.
    
    ![[Pasted image 20250420052922.png]]
    

---

### 🧑‍💼 **In-Band vs. Out-of-Band Management**

#### 🌐 **In-Band Management**

- Manage devices **over the regular network**.(administering network)
    
- Uses tools like SSH or GUI interfaces.
    
    ![[Pasted image 20250420052937.png]]
    

#### 🔌 **Out-of-Band Management**

- Uses a **separate network path** just for management.
    
- Useful if the main network is down—you can still fix or access devices.
    
    ![[Pasted image 20250420053022.png]]
    

---
