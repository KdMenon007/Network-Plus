
---

## **Malware**

**Malware** is any software created to harm or disrupt a computer system. It includes various types, each with unique behaviors and ways of attacking systems:

---

### **1. Virus**

- **What It Does**: A virus attaches to files or programs and spreads when the infected program runs.
    
- **How It Spreads**: Needs user action like opening a file or running a program.
    

**Types**:

- **File Infector**: Attaches to executable files.
    
- **Macro Virus**: Spread through documents like Word files.
    
- **Boot Sector Virus**: Infects the computer’s startup process.
    

**Protection**:

- Use **antivirus software**.
    
- Regularly **update** antivirus definitions.
    
- Perform **system scans**.
    

---

### **2. Worm**

- **What It Does**: A worm spreads across networks by exploiting weaknesses in software. It doesn't need a file or user to spread.
    
- **How It Spreads**: Automatically spreads through networks.
    

**Protection**:

- Regular **patch management** to fix vulnerabilities.
    
- Use **antivirus** and **antimalware** tools.
    
- Set up **firewalls** and **network segmentation**.
    

---

### **3. Trojan Horse**

- **What It Does**: A Trojan pretends to be legitimate software but is actually malicious. It tricks users into installing it.
    
- **How It Spreads**: User unknowingly runs or installs it.
    

**Protection**:

- Keep software up to date with **patches**.
    
- Use **antivirus** and **firewalls**.
    
- Educate users to avoid **untrusted downloads**.
    

---

### **4. Ransomware**

- **What It Does**: Encrypts your files and demands money (often in cryptocurrency) to restore access.
    
- **How It Spreads**: Often through **phishing emails**, malicious ads, or software vulnerabilities.
    

**Protection**:

- Keep software updated.
    
- Use **backup systems** to recover data.
    
- Train users to spot **phishing** attempts.
    

---

### **5. Spyware**

- **What It Does**: Gathers personal or sensitive information without your knowledge. It can track browsing, log keystrokes, and steal login details.
    
- **How It Spreads**: Installed unknowingly by the user.
    

**Protection**:

- Use **antivirus and anti-spyware** tools.
    
- Practice **secure browsing**.
    
- Set up **firewalls** and **traffic filtering**.
    

---

### **6. Rootkit**

- **What It Does**: Hides malicious activity and allows attackers to maintain access to a system while avoiding detection.
    
- **How It Spreads**: Installed after an attacker gains unauthorized access.
    

**Protection**:

- Use **anti-rootkit** tools.
    
- Regularly **patch** and **secure** systems.
    
- Enable **secure boot** to prevent unauthorized code from running.
    

---

### **7. Logic Bomb**

- **What It Does**: A piece of code that causes harm when specific conditions are met (like a certain time or user action).
    
- **How It Spreads**: It's often hidden in software until triggered.
    

**Protection**:

- Perform **code reviews** and audits.
    
- Use **access control** to limit who can make changes to the system.
    
- Ensure **regular backups** to recover data if triggered.
    

---

### **Distributed Denial-of-Service (DDoS)**

![[Pasted image 20250420060456.png]]


A **DDoS** attack aims to disrupt a target server or network by flooding it with excessive traffic, causing it to crash or become unresponsive.

- **Botnet**: A network of compromised devices (like computers or IoT devices) used to launch the attack.
    
- **UDP Flood**: The attacker sends a large number of UDP packets to random ports on the target, overwhelming its network.
    
    ![[Pasted image 20250420060513.png]]
    
- **SYN Flood**: Exploits the TCP three-way handshake to overload the target with connection requests, preventing legitimate connections.
    
    ![[Pasted image 20250420060527.png]]
    
- **Amplification Attacks**: The attacker uses protocols like DNS to magnify traffic and overwhelm the target.
    
- **Reflected DDoS**: Uses third-party servers to send traffic to the victim, often through IP spoofing.
  
  ![[Pasted image 20250420060547.png]]
  
#### **Mitigation Techniques**:

- Increase bandwidth.
    
- Use DDoS protection services like **Cloudflare**.
    
- Use network hardware (e.g., routers, firewalls) with built-in DDoS protection.
    

**More info**:

- [Live DDoS Map](https://www.netscout.com/ddos-attack-map)
    
- [UDP Flood DDoS](https://www.akamai.com/glossary/what-is-udp-flood-ddos-attack)
    
- [SYN Flood Attack](https://www.researchgate.net/figure/The-TCP-SYN-flood-attack-Hands-on-lab-exercise-on-TCP-SYN-flood-attack_fig3_320654932)
    

---

### **VLAN Hopping**

An attack that allows a malicious user to send data from one **VLAN** (Virtual Local Area Network) to another, bypassing Layer 2 security.

**Protection**:

- Proper VLAN configuration and access controls.
    

**More info**: [VLAN Hopping Explanation](https://networklessons.com/cisco/ccnp-switch/vlan-hopping)

![[Pasted image 20250420060634.png]]

---

### **MAC Flooding**

An attacker floods a **switch** with fake **MAC addresses**, causing the switch to act like a hub and broadcast all traffic, potentially allowing sensitive data interception.

**Protection**:

- Limit MAC addresses per port.
    
- Enable **port security** on switches.
    

**More info**: [MAC Flooding Prevention](https://www.geeksforgeeks.org/how-to-prevent-mac-flooding/)

![[Pasted image 20250420060651.png]]

---

### **ARP Spoofing**

An attacker sends false **ARP** (Address Resolution Protocol) messages, linking their **MAC address** to the IP of a legitimate device, allowing them to intercept or alter data.

**Protection**:

- Use **static ARP entries** and **packet filtering**.
    

**More info**: [ARP Spoofing](https://en.wikipedia.org/wiki/ARP_spoofing)

![[Pasted image 20250420060702.png]]

---

### **ARP Poisoning**

A malicious ARP attack where the attacker associates their **MAC address** with a legitimate IP address, allowing them to manipulate or block traffic.

**Protection**:

- Implement **dynamic ARP inspection**.
    

---

### **Domain Name System (DNS) Security Risks**

**DNS** translates human-readable domain names into IP addresses. There are several attack types related to DNS:

1. **DNS Spoofing (Cache Poisoning)**: The attacker sends false DNS data to redirect traffic to a fake website (commonly used in phishing).
    
    - **Protection**: Use **DNSSEC** to verify DNS data authenticity.
        
        ![[Pasted image 20250420060730.png]]
        
2. **DNS Amplification Attacks**: A DDoS attack where attackers use publicly accessible DNS servers to flood the target with traffic.
    
    - **Protection**: Block recursive queries from unauthorized sources.
        
3. **DNS Tunneling**: Uses DNS queries to exfiltrate data from a compromised system.
    
    - **Protection**: Monitor DNS traffic for unusual patterns.
        
4. **DNS Hijacking**: Redirects DNS queries to a malicious DNS server, leading users to fraudulent sites.
    
    - **Protection**: Secure DNS servers and regularly patch vulnerabilities.
        
        ![[Pasted image 20250420060752.png]]
        

**Mitigation Strategies**:

- Use **DNSSEC** (DNS Security Extensions).
    
- Regularly patch DNS servers.
    
- Monitor DNS traffic for signs of compromise.
    

---

### **Rogue Devices and Services**

1. **Rogue Devices**: Unauthorized devices, such as access points or DHCP servers, that connect to a network without permission and can cause security breaches.
    
    - Examples: Rogue DHCP servers, rogue access points.
        
2. **Rogue DHCP Server**: An unauthorized DHCP server that provides incorrect IP addresses to clients, leading to possible network disruption and attacks.
    
    - **Protection**: Use DHCP snooping to block unauthorized servers.
        
    
    **More info**: [Rogue DHCP Server](https://www.auvik.com/franklyit/blog/rogue-dhcp-server/)
    
    ![[Pasted image 20250420060821.png]]
    
3. **Rogue Access Point**: An unauthorized Wi-Fi access point that can be used to gain unauthorized network access.
    
    - **Protection**: Regularly scan for unauthorized APs and disable **SSIDs** that aren’t in use.
        
    
    **More info**: [Rogue Access Point](https://www.sciencedirect.com/topics/computer-science/rogue-access-point)
    
    ![[Pasted image 20250420060845.png]]
    
4. **Evil Twin**: A malicious Wi-Fi AP that mimics a legitimate one, tricking users into connecting to it, allowing the attacker to intercept sensitive data.
    
    ![[Pasted image 20250420060900.png]]
    

**Protection**:

- Use strong encryption (e.g., WPA3).
    
- Regularly check for rogue APs.
    

---

### **On-Path Attack**

![[Pasted image 20250420060918.png]]

An **on-path attack** (formerly called **Man-in-the-Middle (MitM)**) happens when an attacker intercepts the communication between two parties. The attacker places themselves between the two parties, allowing them to listen in on or alter the communication.

**How it Works:**

- **Intercepting Communication**: The attacker intercepts the data flow between a user and a website, often through methods like compromising network equipment, exploiting unsecured Wi-Fi, or using ARP spoofing.
    
- **Eavesdropping**: The attacker listens in on the communication and can access sensitive information such as login credentials, personal data, or corporate secrets.
    
- **Session Hijacking**: The attacker steals session tokens to impersonate the victim and gain unauthorized access to systems or information.
    
- **Data Manipulation**: The attacker may alter or inject malicious content into the data being exchanged, potentially redirecting users to fraudulent websites.
    
- **SSL Stripping**: In this attack, the attacker downgrades a secure HTTPS connection to HTTP, allowing them to view and manipulate unencrypted data.
    

---

### **Social Engineering**

**Social Engineering** refers to attacks that trick people into breaking security procedures to gain unauthorized access or for financial gain. These attacks rely on exploiting human behavior rather than technical vulnerabilities.

---

### **Phishing**

Phishing is a type of social engineering attack where attackers trick individuals into disclosing sensitive information.

**Common Objectives**:

- **Credential Theft**: Stealing usernames and passwords.
    
- **Financial Fraud**: Gaining unauthorized access to financial accounts.
    
- **Malware Distribution**: Delivering malicious software.
    
- **Identity Theft**: Stealing personal information for illegal purposes.
    

**Mitigation Measures**:

- **User Education**: Teach users how to recognize phishing attempts.
    
- **Email Filtering**: Block suspicious emails.
    
- **Two-Factor Authentication (2FA)**: Adds an extra layer of security.
    
- **Incident Response**: Have a plan to respond to phishing attacks.
    

---

### **Dumpster Diving**

**Dumpster Diving** is when attackers search through discarded materials (like documents or hardware) to find sensitive information, such as passwords or financial records, that can be used for future attacks.

**Mitigation**:

- **Secure Disposal**: Shred sensitive documents, wipe data from devices, and use locked bins for disposal.
    

---

### **Shoulder Surfing**

**Shoulder Surfing** is when an attacker watches over someone's shoulder to see sensitive information being entered, like passwords or PINs, in public places.

**Protection**:

- Be cautious when entering sensitive data in public places.
    
- Use screen privacy filters.
    

---

### **Tailgating**

**Tailgating** is when an unauthorized person follows an authorized individual into a restricted area, gaining access without permission.

**Protection**:

- Ensure employees don't allow others to follow them into secure areas.
    
- Use security measures like keycards to restrict access.
    

---
