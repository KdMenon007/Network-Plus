
---

### **Physical Security**

- Protects **assets, people, and data** from physical threats.
    
- Involves tools like:
    
    - **Surveillance cameras**
        
    - **Locks**
        
    - **Access control systems**
        
- Goal: Prevent unauthorized access and ensure safety.
    

---

### **Security Cameras**

- Provide **real-time monitoring** and video recording.
    
- **Deter malicious activity** and offer **evidence** during incidents.
    

---

### **Locks**

- Basic yet essential for controlling physical access.
    
- Modern locks often integrate with **electronic access systems**:
    
    - Manage who enters
        
    - Track access history
        

---

### **Deception and Disruption Technology**

- Tools designed to **mislead or disrupt attackers**.
    
- Protect real systems by creating **fake environments**.
    

---

### **Honeypot**

- A **decoy system** set up to mimic a real one.
    
- **Attracts attackers** and gathers data on their behavior.
    
- Isolated and monitored—**no real risk to the network**.
    

---

### **Honeynet**

- A **network of honeypots** simulating a full environment.
    
- Used to study attacker behavior and **lateral movement**.
    

---

### **Honeyfile**

- A **fake file** that looks important.
    
- Placed in the network to detect unauthorized access.
    
- Access triggers **alerts to security teams**.
    

---

### **Honeytoken**

- General term for **fake digital bait**:
    
    - Could be a fake user, DB record, file, etc.
        
- If accessed, it signals a **possible compromise**.
    

---

### **Audits & Regulatory Compliance**

- Regular **security audits** help:
    
    - Ensure legal and industry compliance
        
    - Identify and fix vulnerabilities
        
- Necessary for protecting **sensitive data**.
    

---

### **Data Locality**

- Refers to **where data is stored and processed** (geographically).
    
- Important for meeting **regional data protection laws** and regulations.
    

---
#### **PCI DSS (Payment Card Industry Data Security Standard)**

- Ensures safe handling of **credit card data**.
    
- Applies to companies that **accept, process, store, or transmit** card data.
    
- Requires:
    
    - **Encryption**
        
    - **Access control**
        
    - **Monitoring**
        
- Goal: **Prevent data breaches and fraud**.
    

---

#### **GDPR (General Data Protection Regulation)**

- EU regulation for **personal data protection**.
    
- Key requirements:
    
    - **Consent** before data collection
        
    - **Accuracy** and **security**
        
    - User rights: **Access**, **correction**, **deletion**
        
- Applies **within and outside the EU** if handling EU citizens' data.
    

---

### 🌐 **Network Architecture & Segmentation**

#### **Network Segmentation**

- Breaks a network into **smaller zones**.
    
- Benefits:
    
    - Better **security**
        
    - Improved **performance**
        
    - Limits **breach spread**
        

---

#### **Guest Network**

- Offers **internet access to visitors**.
    
- Segmented to **protect internal systems** and data.
    

---

#### **BYOD Segmentation**

- Supports employees using **personal devices** at work.
    
- Places BYOD on **separate segments** to reduce risk.
    

---

### ⚙️ **Industrial & Emerging Technologies**

#### **ICS (Industrial Control Systems)**

- Found in **industrial sectors**: power, oil, water, etc.
    
- Includes:
    
    - **SCADA**
        
    - **DCS**
        
    - **PLC**
        
- Controls operations like **valves, sensors**, **alarms**.
    

---

#### **IoT (Internet of Things)**

- Network of **connected physical devices** (e.g., appliances, vehicles).
    
- Features:
    
    - Embedded with **sensors, software, and connectivity**
        
    - Supports **automation and remote control**
        
- Expands across homes, offices, and industries.
    

---

## 🔐 Encryption in Logical Security

**Encryption** converts readable data (plaintext) into unreadable data (ciphertext) to protect it from unauthorized access. Only someone with the right decryption key can read it.

- **Cryptographic key**: A set of values known to both sender and receiver to encrypt and decrypt data.
    

**Example**:  
Plaintext: `Hello` → Encrypt → Ciphertext: `Olssv`  
Ciphertext: `Olssv` → Decrypt → Plaintext: `Hello`

![[Pasted image 20250420055622.png]]

---

## 🔄 Encryption of Data in Transit

**Data in transit** is data moving across a network or the internet.  
**Encrypting it** protects it from interception or tampering.

- Common protocols: **HTTPS**, **SSL/TLS**, **VPN**
    

---

## 💾 Encryption of Data at Rest

**Data at rest** is stored data (e.g., on a hard drive or USB).  
**Encrypting it** ensures only authorized users with the correct key can access it.

- Techniques: **Full Disk Encryption (FDE)**, **Encrypted File Systems**
    

---

## 🎯 Goals of Cryptography

1. **Confidentiality**: Only authorized people can access data (achieved through encryption).
    
2. **Integrity**: Data hasn’t been changed (ensured using cryptographic hashes).
    
3. **Authentication**: Verifies identities (e.g., digital certificates).
    
4. **Non-repudiation**: Prevents denying actions (e.g., digital signatures).
    

---

## 🔐 Symmetric Encryption

- Uses **one shared key** for both encryption and decryption.
    
- **Fast and efficient** – ideal for large data volumes.
    

### ✅ Benefits:

- Great for storage encryption, VPNs, wireless networks, etc.
    

### ⚠️ Challenges:

- **Key sharing**: Must be done securely.
    
- **Key management**: Harder with more users (N users need N(N−1)/2 keys).
    
- **Key protection**: If someone steals the key, they can decrypt everything.
    
- **No non-repudiation**: Everyone has the same key, so you can't tell who did what.
    

---

## 🔑 Asymmetric Encryption (Public Key Cryptography)

- Uses **two keys**:
    
    - **Public key** (shared with everyone)
        
    - **Private key** (kept secret)
        

### How it works:

- **Encrypt** with recipient's **public key**.
    
- **Decrypt** with recipient's **private key**.
    

### ✅ Advantages:

- Solves key sharing problem.
    
- Supports digital signatures for authentication & non-repudiation.
    

### ⚠️ Disadvantages:

- Slower than symmetric encryption.
    
- If the private key is leaked, security is broken.
    

---

## 🏛️ Public Key Infrastructure (PKI)

**PKI** is a system that manages digital certificates and public key encryption.

### Functions:

- **Encrypt/Decrypt data**
    
- **Digital signatures** for authenticity and integrity
    
- **Manage certificates** (issue, revoke, renew)
    

---

## 🧾 X.509 Digital Certificates

**Attributes include**:

- Version, subject name, common name, issuer name
    
- Validity period, public key, signature algorithm, serial number
    

**Types of Certificates**:

- **CA Certificate**: Allows issuing other certificates.
    
- **End-Entity Certificate**:
    
    - **DV (Domain Validation)**: Confirms domain ownership.
        
    - **EV (Extended Validation)**: Confirms legal entity behind the domain.
        
- **Wildcard Certificate**: Secures multiple subdomains (e.g., `*.tiaedu.com`)
    

---

## 🧾 Self-Signed vs. Third-Party Certificates

| Feature         | Self-Signed              | Third-Party (CA-Signed)           |
| --------------- | ------------------------ | --------------------------------- |
| **Signed by**   | The same entity using it | A trusted Certificate Authority   |
| **Trust Level** | Not inherently trusted   | Trusted by browsers/systems       |
| **Use Case**    | Internal, testing        | Public websites, secure services  |
| **Cost**        | Free                     | Paid (varies by validation level) |
