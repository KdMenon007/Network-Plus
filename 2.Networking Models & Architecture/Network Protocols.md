### **What are Protocols?**

**Protocols** are sets of rules that allow devices on a network to communicate and share data. They ensure that communication between computers, servers, and devices happens in a standardized, reliable, and efficient way.

---

**1. FTP (File Transfer Protocol)**

- **Description:** Transfers files between client and server. Widely used, but lacks encryption.
    
- **Port(s):** TCP 20 (Data), TCP 21 (Control)
    
- **OSI Layer:** Application Layer (Layer 7)
    
- **Devices:** File Server, FTP Clients, Routers, Firewalls
    
- **Security:** ❌ Not encrypted
    
- **Common Attacks:** Brute-force login, FTP bounce attacks, packet sniffing
    
- **Mitigations:**
    
    - Use **SFTP** or **FTPS** for secure file transfers.
        
    - Implement **strong password policies** and **account lockout** mechanisms.
        
    - Use **VPNs** to encrypt the data transmission.
        

---

**2. SFTP (SSH File Transfer Protocol)**

- **Description:** Secure file transfer built on SSH; encrypts all data including commands and credentials.
    
- **Port:** TCP 22
    
- **OSI Layer:** Application Layer (Layer 7)
    
- **Devices:** SSH Server, File Server, Routers, Firewalls
    
- **Security:** ✅ Encrypted
    
- **Common Attacks:** SSH brute-force, misuse of private keys, tunneling misuse
    
- **Mitigations:**
    
    - Use **strong SSH key pairs** and avoid password authentication.
        
    - Disable **root login** via SSH.
        
    - Implement **multi-factor authentication (MFA)**.
        

---

**3. Telnet**

- **Description:** Provides remote terminal access; outdated and insecure due to plaintext transmission.
    
- **Port:** TCP 23
    
- **OSI Layer:** Application Layer (Layer 7)
    
- **Devices:** Networked Devices, Routers, Servers
    
- **Security:** ❌ Not encrypted
    
- **Common Attacks:** Credential sniffing, MITM, session hijacking
    
- **Mitigations:**
    
    - **Avoid using Telnet**; use **SSH** for secure remote access.
        
    - Implement **network segmentation** and firewalls to restrict Telnet access.
        
    - Encrypt communication using **VPNs**.
        

---

**4. SSH (Secure Shell)**

- **Description:** Secure remote login and command execution over an encrypted channel.
    
- **Port:** TCP 22
    
- **OSI Layer:** Application Layer (Layer 7)
    
- **Devices:** SSH Server, Routers, Networked Devices
    
- **Security:** ✅ Encrypted
    
- **Common Attacks:** Brute-force, port forwarding abuse, key compromise
    
- **Mitigations:**
    
    - Use **strong password policies** and **SSH key authentication**.
        
    - Implement **rate limiting** and **fail2ban** to block brute-force attempts.
        
    - Regularly rotate **SSH keys**.
        

---

**5. DNS (Domain Name System)**

- **Description:** Translates domain names into IP addresses. Essential for internet navigation.
    
- **Port:** UDP 53 (TCP 53 for zone transfers)
    
- **OSI Layer:** Application Layer (Layer 7)
    
- **Devices:** DNS Servers, DNS Clients, Routers, Firewalls
    
- **Security:** ⚠️ Not encrypted by default
    
- **Common Attacks:** DNS spoofing, cache poisoning, DNS amplification
    
- **Mitigations:**
    
    - Use **DNSSEC** (DNS Security Extensions) to validate DNS records.
        
    - Implement **rate limiting** on DNS requests to mitigate amplification attacks.
        
    - Configure **firewalls** to restrict unauthorized access to DNS servers.
        

---

**6. DHCP (Dynamic Host Configuration Protocol)**

- **Description:** Automatically assigns IP addresses and other network settings to devices.
    
- **Port(s):** UDP 67 (Server), UDP 68 (Client)
    
- **OSI Layer:** Application Layer (Layer 7)
    
- **Devices:** DHCP Servers, Routers, Switches, Clients
    
- **Security:** ⚠️ Not encrypted
    
- **Common Attacks:** DHCP starvation, rogue DHCP servers, fake gateway attacks
    
- **Mitigations:**
    
    - Use **DHCP snooping** and **IP/MAC binding** on network switches.
        
    - Restrict DHCP traffic to trusted devices only.
        
    - Implement **network segmentation** to separate sensitive networks.
        

---

**7. TFTP (Trivial File Transfer Protocol)**

- **Description:** Simplified file transfer with no authentication. Used for boot files or configs.
    
- **Port:** UDP 69
    
- **OSI Layer:** Application Layer (Layer 7)
    
- **Devices:** TFTP Servers, Routers, Networked Devices
    
- **Security:** ❌ Not encrypted
    
- **Common Attacks:** Unauthorized access, config overwrite, sniffing
    
- **Mitigations:**
    
    - Use more secure protocols like **SFTP** or **HTTPS**.
        
    - Restrict access to **trusted devices** with firewalls.
        
    - **Authentication** for accessing sensitive files.
        

---

**8. HTTP (Hypertext Transfer Protocol)**

- **Description:** Foundation of the web; transmits web pages and data in plaintext.
    
- **Port:** TCP 80
    
- **OSI Layer:** Application Layer (Layer 7)
    
- **Devices:** Web Servers, Web Browsers, Routers, Firewalls
    
- **Security:** ❌ Not encrypted
    
- **Common Attacks:** MITM, session hijacking, XSS, cookie theft
    
- **Mitigations:**
    
    - Switch to **HTTPS** for encrypted communication.
        
    - Use **HTTP Strict Transport Security (HSTS)** to force secure connections.
        
    - Implement **Content Security Policy (CSP)** to mitigate XSS.
        

---

**9. HTTPS (HTTP Secure using TLS)**

- **Description:** Secure version of HTTP using TLS for encryption and data integrity.
    
- **Port:** TCP 443
    
- **OSI Layer:** Application Layer (Layer 7)
    
- **Devices:** Web Servers, Web Browsers, Routers, Firewalls
    
- **Security:** ✅ Encrypted
    
- **Common Attacks:** TLS downgrade, expired/spoofed certificates
    
- **Mitigations:**
    
    - Always use **strong TLS configurations** and avoid deprecated protocols (SSL, TLS 1.0/1.1).
        
    - Enforce **certificate pinning** to prevent certificate spoofing.
        
    - Regularly update and monitor **SSL/TLS certificates**.
        

---

**10. SMTP (Simple Mail Transfer Protocol)**

- **Description:** Protocol for sending email messages between servers.
    
- **Port:** TCP 25
    
- **OSI Layer:** Application Layer (Layer 7)
    
- **Devices:** Mail Servers, SMTP Clients, Routers
    
- **Security:** ❌ Not encrypted by default
    
- **Common Attacks:** Email spoofing, open relay, spam distribution
    
- **Mitigations:**
    
    - Use **SMTPS** (with TLS) or **STARTTLS** to encrypt mail transmission.
        
    - Configure **SPF** (Sender Policy Framework) and **DKIM** (DomainKeys Identified Mail) for email validation.
        
    - Implement **rate-limiting** to prevent spam.
        

---

**11. SMTP with TLS (SMTPS)**

- **Description:** Secure version of SMTP using TLS for client-to-server email submission.
    
- **Port:** TCP 587
    
- **OSI Layer:** Application Layer (Layer 7)
    
- **Devices:** Mail Servers, SMTP Clients, Routers
    
- **Security:** ✅ Encrypted
    
- **Common Attacks:** Weak TLS, certificate spoofing, MITM
    
- **Mitigations:**
    
    - Enforce the use of **strong TLS encryption** and avoid outdated ciphers.
        
    - Require **client certificates** for added security in sensitive environments.
        
    - Regularly **rotate** certificates and check for vulnerabilities.
        

---

**12. POP3 (Post Office Protocol v3)**

- **Description:** Retrieves emails from the server and downloads them to a local device.
    
- **Port:** TCP 110
    
- **OSI Layer:** Application Layer (Layer 7)
    
- **Devices:** Mail Servers, POP3 Clients, Routers
    
- **Security:** ❌ Not encrypted
    
- **Common Attacks:** Packet sniffing, credential theft
    
- **Mitigations:**
    
    - Use **POP3S** (POP3 over SSL) to encrypt communications.
        
    - Implement **strong authentication mechanisms**.
        
    - Use **VPN** or **encrypted networks** for communication.
        

---

**13. POP3 over SSL**

- **Description:** Secure version of POP3 using SSL to encrypt communication.
    
- **Port:** TCP 995
    
- **OSI Layer:** Application Layer (Layer 7)
    
- **Devices:** Mail Servers, POP3 Clients, Routers
    
- **Security:** ✅ Encrypted
    
- **Common Attacks:** SSL spoofing, deprecated SSL usage
    
- **Mitigations:**
    
    - Ensure use of **strong encryption standards** like TLS 1.2/1.3.
        
    - Regularly **update certificates** and avoid weak ciphers.
        
    - **Verify server authenticity** using certificate pinning.
        

---

**14. IMAP (Internet Message Access Protocol)**

- **Description:** Allows email clients to access and manage emails on a mail server, supporting folder management and synchronization.
    
- **Port:** TCP 143
    
- **OSI Layer:** Application Layer (Layer 7)
    
- **Devices:** Mail Servers, IMAP Clients, Routers
    
- **Security:** ❌ Not encrypted by default
    
- **Common Attacks:** Credential theft, session hijacking, MITM
    
- **Mitigations:**
    
    - Use **IMAPS** (IMAP over SSL/TLS) for encrypted communications.
        
    - Implement **multi-factor authentication (MFA)** to secure mail client access.
        
    - Configure **firewalls** to restrict access to mail servers from unauthorized IPs.
        

---

**15. IMAP over SSL (IMAPS)**

- **Description:** Secure version of IMAP using SSL/TLS for encrypted email access and management.
    
- **Port:** TCP 993
    
- **OSI Layer:** Application Layer (Layer 7)
    
- **Devices:** Mail Servers, IMAP Clients, Routers
    
- **Security:** ✅ Encrypted
    
- **Common Attacks:** SSL downgrade, certificate spoofing, MITM
    
- **Mitigations:**
    
    - Use **strong SSL/TLS protocols** like TLS 1.2 or 1.3.
        
    - Enforce **certificate validation** and consider using **certificate pinning**.
        
    - Regularly **rotate certificates** and verify secure configurations.
        

---

**16. SNMP (Simple Network Management Protocol)**

- **Description:** Used for managing devices on IP networks, including routers, switches, and servers.
    
- **Port(s):** UDP 161 (Agent), UDP 162 (Trap)
    
- **OSI Layer:** Application Layer (Layer 7)
    
- **Devices:** Network Devices (routers, switches, firewalls), SNMP Managers
    
- **Security:** ❌ Not encrypted (SNMPv1/v2), ⚠️ partially secure in SNMPv3
    
- **Common Attacks:** SNMP flooding, unauthorized access, brute-force, data manipulation
    
- **Mitigations:**
    
    - Use **SNMPv3**, which provides encryption and authentication.
        
    - Limit SNMP access to **trusted IPs** using firewalls.
        
    - Implement **strong community strings** or better yet, avoid using default ones.
        

---

**17. LDAP (Lightweight Directory Access Protocol)**

- **Description:** Protocol used to access and manage directory services, typically for authentication.
    
- **Port:** TCP 389
    
- **OSI Layer:** Application Layer (Layer 7)
    
- **Devices:** LDAP Servers, Clients, Authentication Systems
    
- **Security:** ⚠️ Not encrypted by default
    
- **Common Attacks:** LDAP injection, unauthorized access, credential sniffing
    
- **Mitigations:**
    
    - Use **LDAPS** (LDAP over SSL/TLS) for encryption.
        
    - Implement **strong access control policies**.
        
    - Regularly update and patch **LDAP servers** for vulnerabilities.
        

---

**18. LDAPS (LDAP over SSL)**

- **Description:** Secure version of LDAP that encrypts communication between clients and directory services using SSL/TLS.
    
- **Port:** TCP 636
    
- **OSI Layer:** Application Layer (Layer 7)
    
- **Devices:** LDAP Servers, Clients
    
- **Security:** ✅ Encrypted
    
- **Common Attacks:** SSL downgrade, certificate spoofing, MITM
    
- **Mitigations:**
    
    - Use **strong SSL/TLS configurations** and avoid weak cipher suites.
        
    - Regularly update certificates and monitor for **certificate revocation**.
        
    - Enforce **certificate validation** to prevent MITM attacks.
        

---

**19. RDP (Remote Desktop Protocol)**

- **Description:** Used for providing a graphical interface to connect to another computer over a network.
    
- **Port:** TCP 3389
    
- **OSI Layer:** Application Layer (Layer 7)
    
- **Devices:** Remote Desktop Servers, RDP Clients, Routers
    
- **Security:** ❌ Not encrypted by default (older versions), ⚠️ weak encryption in some cases
    
- **Common Attacks:** Brute-force attacks, RDP exploits, unauthorized access
    
- **Mitigations:**
    
    - Use **RDP with Network Layer Authentication (NLA)**.
        
    - Implement **strong passwords** and **MFA** for authentication.
        
    - Restrict RDP access with **firewall rules** or use **VPNs** for remote access.
        

---

**20. SIP (Session Initiation Protocol)**

- **Description:** Protocol used for initiating, maintaining, and terminating real-time communication sessions such as voice and video calls.
    
- **Port(s):** UDP 5060 (unsecured), UDP 5061 (secured)
    
- **OSI Layer:** Application Layer (Layer 7)
    
- **Devices:** SIP Servers, SIP Clients, Firewalls, Routers
    
- **Security:** ⚠️ Vulnerable to eavesdropping, spoofing, and fraud
    
- **Common Attacks:** SIP hijacking, denial of service, toll fraud
    
- **Mitigations:**
    
    - Use **SIPS** (SIP over TLS) for encrypted communications.
        
    - Implement **strong authentication mechanisms** for SIP accounts.
        
    - Deploy **firewalls** with SIP-aware filtering.
        

---

**21. ICMP (Internet Control Message Protocol)**

- **Description:** Used for diagnostic functions, such as sending error messages and operational information.
    
- **Port:** N/A (works directly with IP)
    
- **OSI Layer:** Network Layer (Layer 3)
    
- **Devices:** Routers, Firewalls, Hosts
    
- **Security:** ❌ Can be used for malicious purposes like DDoS or reconnaissance
    
- **Common Attacks:** ICMP flooding, Smurf attacks, Ping of Death
    
- **Mitigations:**
    
    - Use **firewall rules** to restrict or block unnecessary ICMP traffic.
        
    - Limit the **rate of ICMP requests** to avoid flooding.
        
    - Disable **ICMP redirects** to avoid route manipulation.
        

---

**22. NTP (Network Time Protocol)**

- **Description:** Used for synchronizing the clocks of computers over a network.
    
- **Port:** UDP 123
    
- **OSI Layer:** Application Layer (Layer 7)
    
- **Devices:** NTP Servers, Clients, Routers
    
- **Security:** ⚠️ Vulnerable to spoofing and reflection attacks
    
- **Common Attacks:** NTP amplification, time manipulation
    
- **Mitigations:**
    
    - Use **NTP authentication** to verify time sources.
        
    - Restrict NTP traffic with **firewalls** to trusted IPs.
        
    - Deploy **rate limiting** to avoid amplification attacks.
        

---

**23. SMB (Server Message Block)**

- **Description:** A network file sharing protocol that allows applications to read and write to files and request services from server programs.
    
- **Port(s):** TCP 445 (Direct SMB over TCP), TCP 139 (NetBIOS over TCP)
    
- **OSI Layer:** Application Layer (Layer 7)
    
- **Devices:** File Servers, Clients, Routers, Switches
    
- **Security:** ⚠️ Vulnerable to exploitation and ransomware attacks
    
- **Common Attacks:** SMB relay, ransomware, man-in-the-middle attacks
    
- **Mitigations:**
    
    - Disable **SMBv1** and use **SMBv2 or SMBv3** for more secure versions.
        
    - Use **strong authentication** and encryption with SMB.
        
    - Regularly **patch SMB services** to protect against vulnerabilities.
        

---

**24. Syslog (System Logging Protocol)**

- **Description:** Used for sending event notification messages to a logging server, commonly used for network devices and servers.
    
- **Port:** UDP 514
    
- **OSI Layer:** Application Layer (Layer 7)
    
- **Devices:** Syslog Servers, Clients, Network Devices
    
- **Security:** ⚠️ Messages sent in plaintext
    
- **Common Attacks:** Log tampering, unauthorized access
    
- **Mitigations:**
    
    - Use **Syslog over TLS** (Syslog-ng or rsyslog) for secure log transport.
        
    - Implement **access controls** to restrict who can send or view logs.
        
    - Regularly **audit and monitor logs** for suspicious activity.

---

**25. SQL Server (Microsoft SQL)**

- **Description:** A database system from Microsoft used to store and manage data. It allows users to query and manage large amounts of data.
    
- **Port:** TCP 1433
    
- **OSI Layer:** Application Layer (Layer 7)
    
- **Devices:** Database Servers, Clients (Applications), Routers
    
- **Security:** ⚠️ Depends on configuration; can be secured with encryption and access control
    
- **Common Attacks:** SQL injection, brute force, credential leaks, buffer overflow attacks
    
- **Mitigations:**
    
    - Use **parameterized queries** to prevent SQL injection.
        
    - Apply **strong passwords** and **account lockouts**.
        
    - **Encrypt** database connections.
        
    - Regularly apply **security patches** and **security updates**.
        
    - Restrict access using **firewalls**.
        
    - **Audit** database activity logs.
        

---
### **Generic Routing Encapsulation (GRE)**

- **Description**: A tunneling protocol developed by Cisco to encapsulate various types of network layer protocol packets inside IP tunnels. It creates a virtual point-to-point link between routers across an IP network.
    
- **Port(s)**: GRE does not use specific port numbers, as it operates directly on IP.
    
- **OSI Layer**: Network Layer (Layer 3)
    
- **Devices**:
    
    - Routers
        
    - VPN Gateways
        
- **Security**: ❌ Not encrypted by default (requires additional encryption like IPSec).
    
- **Common Attacks**:
    
    - GRE tunnel hijacking
        
    - DoS (Denial of Service) attacks
        
- **Mitigations**:
    
    - Use GRE in conjunction with IPSec to encrypt the tunnel.
        
    - Use firewalls and access control to restrict unauthorized GRE traffic.
        

---

### **Internet Protocol Security (IPSec)**

- **Description**: A suite of protocols used to secure IP communications by authenticating and encrypting each IP packet. It operates in two modes: 
### 1. **Transport Mode**

- **Description**: Only the data (payload) of the packet is encrypted or authenticated, while the header of the packet remains intact.
    
- **Use Case**: Typically used for end-to-end communication between two hosts (e.g., between two computers or servers).
    
- **Security**: Encrypts or authenticates the payload, but the packet header remains visible to intermediate devices (routers, etc.).
    
### 2. **Tunnel Mode**

- **Description**: Both the data (payload) and the header of the packet are encrypted and encapsulated in a new IP packet.
    
- **Use Case**: Commonly used for VPNs where data is sent between two networks, such as connecting a remote user to a corporate network.
    
- **Security**: Provides a higher level of security since both the header and payload are encrypted, preventing any information from being visible to external routers or devices.
    
- **Port(s)**:
    
    - IPSec typically uses UDP port 500 for ISAKMP (Internet Security Association and Key Management Protocol) during the initial setup.
        
    - ESP (Encapsulating Security Payload) and AH (Authentication Header) don’t require specific ports.
        
- **OSI Layer**: Network Layer (Layer 3)
    
- **Devices**:
    
    - VPN Gateways
        
    - Routers
        
    - Firewalls
        
- **Security**: ✔️ Provides authentication, integrity, and encryption.
    
- **Common Attacks**:
    
    - Man-in-the-middle (MITM) attacks
        
    - Replay attacks
        
    - Cryptanalysis attacks
        
- **Mitigations**:
    
    - Use strong encryption algorithms (AES, SHA-256).
        
    - Implement mutual authentication and key exchange protocols (IKEv2).
        
    - Regularly update IPSec keys and use secure key management.
        

---

### **Authentication Header (AH) / Encapsulating Security Payload (ESP)**

- **Authentication Header (AH)**:
    
    - **Description**: Provides authentication and integrity for IP packets through digital signatures, ensuring that the packet has not been tampered with.
        
    - **Port(s)**: AH operates over IP and does not rely on specific ports.
        
    - **OSI Layer**: Network Layer (Layer 3)
        
    - **Devices**:
        
        - VPN Gateways
            
        - Routers
            
    - **Security**: ✔️ Provides authentication and integrity.
        
    - **Common Attacks**:
        
        - Replay attacks
            
        - Tampering with packet headers
            
    - **Mitigations**:
        
        - Use secure key management protocols.
            
        - Use sequence numbers to protect against replay attacks.
            
- **Encapsulating Security Payload (ESP)**:
    
    - **Description**: Provides confidentiality through encryption by encrypting the packet’s payload.
        
    - **Port(s)**: ESP operates over IP and does not require specific ports.
        
    - **OSI Layer**: Network Layer (Layer 3)
        
    - **Devices**:
        
        - VPN Gateways
            
        - Routers
            
    - **Security**: ✔️ Provides confidentiality through encryption.
        
    - **Common Attacks**:
        
        - Cryptanalysis attacks
            
        - Man-in-the-middle (MITM) attacks
            
    - **Mitigations**:
        
        - Use strong encryption algorithms (AES, 3DES).
            
        - Use authentication and integrity measures (e.g., AH) to prevent MITM attacks.
            

---
