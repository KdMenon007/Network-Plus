
---

### **Hardening Techniques**

- **Encryption**
    
    - Converts data into a secure format.
        
    - Protects data at rest (e.g., hard drives) and in transit (e.g., over the internet).
        
- **Disabling Ports/Protocols**
    
    - Disable unused or unnecessary ports and protocols to minimize vulnerabilities.
        
- **Endpoint Protection**
    
    - Install security software (antivirus, anti-malware, firewalls, IDS) on individual devices (endpoints).
        
- **Host-Based Firewalls**
    
    - Controls network traffic to and from individual hosts based on predefined security rules.
        
- **Host Intrusion Prevention System (HIPS)**
    
    - Monitors and analyzes system behaviors to prevent unauthorized access and anomalous activities.
        
- **Default Password Changes**
    
    - Alter default passwords on devices to prevent easy exploitation by attackers.
        
- **Removal of Unnecessary Software**
    
    - Uninstall outdated or unnecessary software to reduce attack surfaces and improve system performance.
        
- **Network Access Control (NAC)**
    
    - Prevents unauthorized access to network resources.
        
    - Includes health checks and compliance monitoring for devices.
        
- **802.1X (Port-Based Network Access Control)**
    
    - Authenticates devices before granting network access, blocking all traffic except authentication traffic until verified.
        
- **Extensible Authentication Protocol (EAP)**
    
    - Supports various authentication methods (passwords, tokens, certificates).
        
    - Used in conjunction with 802.1X for network access control.
        
- **MAC Filtering**
    
    - Allows only devices with specific MAC addresses to access the network.
        
    - Prevents unauthorized access but can be bypassed with MAC address spoofing.
        
- **Key Management**
    
    - Securely creates, stores, and maintains cryptographic keys.
        
    - Includes key rotation, revocation, and backup to protect data.
        
- **Firewalls**
    
    - Monitors and controls network traffic based on security rules.
        
    - Creates a barrier between a trusted internal network and untrusted external networks.
        

---

### **Firewalls**

- **Definition**:
    
    - A network security system that monitors and controls incoming and outgoing network traffic based on predetermined security rules.
        
    - Establishes a barrier between a trusted internal network and an untrusted external network (e.g., the internet).
        
    - Can be implemented in hardware (appliances) or software.
        
- **Firewall Features**:
    
    - Enforces security policies on traffic.
        
    - Controls the flow of traffic.
        
    - Does not differentiate between data and commands.
        
    - Manages traffic flow between networks or hosts.
        

---

### **Firewall Types**

- **Packet Filtering Firewalls**:
    
    - Basic type that inspects packets.
        
    - Allows or denies traffic based on source/destination IP addresses, ports, and protocols.
        
- **Stateful Inspection Firewalls**:
    
    - More advanced than packet filtering.
        
    - Tracks the state of active connections and makes decisions based on the context of traffic.
        
- **Web Application Firewall (WAF)**:
    
    ![[Pasted image 20250420061702.png]]
    
    - Protects web applications by filtering and monitoring HTTP traffic.
        
    - Effective against attacks like cross-site scripting (XSS), SQL injection, and session hijacking.
        
    - Operates at the application layer, with rules customized for the application.
        
    - Can be deployed as hardware, software, or a cloud service.
        
- **Unified Threat Management (UTM)**:
    
    - Combines multiple security features in one device (e.g., antivirus, anti-spyware, firewall, IDS/IPS, content filtering).
        
    - Simplifies management and is ideal for small-to-medium-sized businesses.
        
- **Next-Generation Firewalls (NGFW)**:
    
    - Advanced firewalls that integrate deep packet inspection, intrusion prevention systems, and application awareness.
        
    - Uses **Deep Packet Inspection** (DPI) to inspect data within packets.
        
    - Often integrates with threat intelligence services for up-to-date threat information.
        

---

### **Firewall Components**

- **Rules**:
    
    - Configurations that control how a firewall operates.
        
    - Example: Allow inbound traffic on port 80 (HTTP) but block traffic on port 23 (Telnet).
        
- **Access Lists**:
    
    - A set of commands applied to firewalls to filter traffic based on source/destination addresses, protocols, and ports.
        
- **Ports/Protocols**:
    
    - Essential components in network communications that firewalls secure.
        
- **Screened Subnets (DMZ)**:
    
    - A subnetwork that exposes an organization's external-facing services to an untrusted network (usually the internet).
        
    - Firewalls allow limited traffic from the DMZ to the internal network, with strict rules controlling interactions.
        
        ![[Pasted image 20250420061720.png]]
        

---

### **Access Control List (ACL)**

- **Definition**:
    
    - A list used by routers and network devices to authorize or deny traffic based on a set of rules.
        
    - Can also be used in file systems for managing permissions and controlling access to directories/files.
        

---

### **Web Filter**

- **Function**:
    
    - Controls websites and content users can access to mitigate the risk of exposure to malicious content.
        
- **Types of Web Filtering**:
    
    - **Agent-Based Web Filtering**:
        
        - Involves installing software agents on individual user devices to enforce web access policies, useful for remote/mobile employees.
            
    - **Centralized Proxy**:
        
        - Acts as an intermediary between users and the internet, enforcing web filtering policies.
            
        - Offers centralized management and control, making it easier to enforce consistent web access policies across the organization.
            

---

### **Universal Resource Locator (URL) Scanning**

- **Function**:
    
    - Involves examining URLs requested by users to determine if they should be allowed or blocked.
        
    - Based on a database of categorized URLs.
        
- **Application**:
    
    - Prevents access to known malicious or inappropriate websites.
        
    - A fundamental component of most web filtering solutions.
        

---

### **Content Categorization**

- **Definition**:
    
    - Classifies web pages into categories (e.g., social media, adult content, gaming) based on their content.
        
- **Purpose**:
    
    - Enables organizations to block or allow entire categories of websites.
        
    - Streamlines and ensures consistent policy enforcement.
        

---

### **Block Rules**

- **Definition**:
    
    - Specific criteria set to block access to certain websites or content.
        
- **Criteria for Block Rules**:
    
    - Based on URLs, keywords, categories, or other identifiable aspects of web content.
        
- **Customization**:
    
    - Organizations can customize block rules to align with their security policies, regulatory compliance, and organizational culture.
        

---

### **Reputation-Based Filtering**

- **Definition**:
    
    - Uses reputation scores to determine whether websites should be allowed or blocked.
        
- **Mechanism**:
    
    - Reputation scores are derived from factors like the website’s history, presence of malware, and user feedback.
        
- **Effectiveness**:
    
    - Particularly effective against newly created malicious sites that may not yet be categorized or have a known URL pattern.
        

---
