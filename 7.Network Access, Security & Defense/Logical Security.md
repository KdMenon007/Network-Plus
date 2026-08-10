
---

## 🔐 **Logical Security**

Logical security includes software-based tools and rules used to protect data, systems, and networks from unauthorized access or attacks.

---

## 🛡️ **CIA Triad** (Three Pillars of Security)

### 1. **Confidentiality**

- Ensures that **only authorized people** can access sensitive information.
    
- Keeps data **private and secure** from those who shouldn’t see it.
    

#### 🔒 How Confidentiality is Protected:

- **Access Controls**: Passwords, biometrics, access cards to limit who can access data.
    
- **Encryption**: Scrambles data so only people with the key can read it.
    
- **Secure Communication**: Uses secure protocols (like **SSL/TLS**) to protect data in transit.
    
- **Policies & Procedures**: Rules about **who** can access what and **how** to handle info.
    
- **Training & Awareness**: Teach people how to protect data.
    
- **Data Classification**: Label data by sensitivity (e.g., Public, Confidential, Secret).
    

---

### 2. **Integrity**

- Ensures that data is **accurate, reliable, and unchanged** unless done by authorized users.
    

#### ✅ How Integrity is Maintained:

- **Data Accuracy, Consistency, and Trustworthiness**: Data should be correct and dependable.
    
- **Checksums & Hash Functions**: Detect changes in data using special codes (hashes). If the data changes, so does the code.
    
- **Digital Signatures**: Prove the data came from a trusted source and hasn’t been tampered with.
    
- **Access Controls**: Prevent unauthorized users from changing the data.
    

---

### 3. **Availability**

- Ensures that systems, data, and services are **available** when authorized users need them.
    

#### 🔄 How Availability is Protected:

- **Redundancy**: Extra copies of systems or data to take over if something fails.
    
- **Fault Tolerance**: Systems designed to keep working even if parts break.
    
- **Backups**: Regularly save copies of data so it can be recovered if lost or damaged.
    
- **Disaster Recovery Plans**: Step-by-step plans to recover from disasters like power outages, cyberattacks, or natural events.
    
- **DDoS Protection**: Prevent attacks that try to overload systems and make them unavailable.
    

---

## ⚠️ **Risk**

Risk is the **chance** that a **threat** will take advantage of a **vulnerability** and cause harm.

📌 **Formula:**  
**Risk = Threat × Vulnerability**

---

### 🧱 **Risk Components**

- **Asset**: Anything valuable that needs protection (e.g., data, hardware).
    
- **Asset Valuation**: The estimated dollar (or business) value of the asset.
    
- **Threat**: Something that could **potentially** harm an asset (e.g., hackers, natural disasters).
    
- **Threat Agent/Actor**: The one causing the harm (e.g., a hacker, malicious software).
    
- **Threat Event**: The actual **incident** that happens (e.g., a phishing attack).
    
- **Threat Vector**: The **path** the attacker uses (e.g., email, USB drive, unpatched software).
    
- **Vulnerability**: A **weak spot** in the system (e.g., outdated software).
    
- **Exposure**: The **damage** that could happen if a threat succeeds.
    
- **Safeguards**: Measures (like firewalls or policies) that reduce or prevent risk.
    
- **Attack**: When a threat successfully uses a vulnerability to cause harm.
    
- **Breach**: When security is **broken** and unauthorized access occurs.
    

---

## 🔐 **AAA: Authentication, Authorization, Accounting**

### ✅ **Authentication**

- Verifies **who** you are.
    
- Happens after identifying yourself (like typing a username).
    

### 🛂 **Authorization**

- Decides **what** you're allowed to do after you're authenticated.
    

### 📜 **Accounting (Auditing)**

- Tracks and logs your **actions** (e.g., login time, file access, commands used).
    

---

## 🔑 **Authentication Factors**

(Multifactor Authentication - MFA uses more than one of these)

### 1. **Something You Know**

- Passwords, PINs, security questions
    
- **Weak alone**, since they can be guessed or stolen
    

### 2. **Something You Have**

- Phone, smart card, security token
    
- Used for codes, app approvals, etc.
    

### 3. **Something You Are**

- Biometrics like fingerprints, facial recognition, iris scans
    
- Very secure but may need special equipment
    

### 4. **Somewhere You Are**

- Based on your **location**, like GPS or IP address
    
- Used to block access from unexpected places
    

### 5. **Something You Do**

- Behavioral traits, like how you type or move your mouse
    
- Still emerging but adds extra security
    

---
### **Authentication**

Authentication is the process of verifying who someone or something is.

#### **Multi-Factor Authentication (MFA)**

- Requires **two or more** independent forms of verification.
    
- Combines:
    
    - **Something you know** – password or PIN
        
    - **Something you have** – token, phone, smart card
        
    - **Something you are** – fingerprint, face, retina (biometric)
        

---

### **Ways to Authenticate People**

- **Biometrics:** Uses physical traits like fingerprints or facial recognition
    
- **Knowledge-Based:** Uses info only the user should know (e.g., passwords, security questions)
    
- **MFA:** Combines two or more of the above methods for added security
    

---

### **Ways to Authenticate Systems**

- **Certificates and Keys:** Use digital certificates and cryptographic keys to build trust
    
- **IP Allow List:** Only allows devices from approved IP addresses
    
- **MAC Address Filtering:** Grants access based on a device's physical MAC address
    

---

### **Authorization**

Authorization defines **what a user or system is allowed to do** after authentication.

#### **Key Components:**

- **Permissions and Privileges:** Grant specific actions like read, write, execute, delete
    
- **Access Control:** Enforced using mechanisms like Access Control Lists (ACLs)
    
- **Authorization Models:**
    
    - **MAC (Mandatory Access Control):** Admin-controlled access
        
    - **DAC (Discretionary Access Control):** Resource owner sets permissions
        

---

### **Identity and Access Management (IAM)**

IAM is a framework of policies, processes, and technologies that manage digital identities and control user access to critical resources.

- Ensures **only the right people** access **the right resources** at **the right time** for **the right reasons**.
    
- Important for **security** and **regulatory compliance**.
    
- Includes tools for:
    
    - Automating user provisioning
        
    - Managing user privileges
        
    - Enforcing security policies
        
    - Auditing user activities
        

---

### **Access Controls**

Access controls are methods to manage and restrict access to resources.  
Types of access controls:

- **DAC (Discretionary Access Control)**
    
- **MAC (Mandatory Access Control)**
    
- **RBAC (Role-Based Access Control)**
    
- **ABAC (Attribute-Based Access Control)**
    

Effective access control balances **security**, **usability**, and **complexity**.

---

### **DAC and MAC**

**Mandatory Access Control (MAC)**

- Central authority sets access levels based on security clearance.
    
- Users **cannot change** permissions.
    
- Used in military/government environments.
    

**Discretionary Access Control (DAC)**

- Resource owner sets permissions.
    
- Most flexible model.
    
- Common in systems like file permissions in OS.
    
- Risk: Users might give excessive access.
    

---

### **RBAC (Role-Based Access Control)**

- Access is based on the user's role in the organization.
    
- Common in corporate environments.
    
- Simplifies management in large user groups.
    

---

### **Rule-Based and ABAC**

**Rule-Based Access Control**

- Access depends on predefined rules (e.g., IP-based firewall rules).
    
- Best for tightly controlled environments.
    

**Attribute-Based Access Control (ABAC)**

- Access based on multiple attributes (user, environment, resource).
    
- Good for complex environments with dynamic needs.
    
- Allows fine-grained, flexible control.
    

---

### **Principle of Least Privilege**

Users, systems, and processes should only have the **minimum** access required to do their job.  
Applications:

- **User Accounts:** Access limited by job role (e.g., marketing doesn’t access finance).
    
- **Admin Accounts:** Use standard accounts for daily tasks; use admin rights only when needed.
    
- **Software:** Should run with minimal required permissions to reduce security risk.
    

---

### **Single Sign-On (SSO)**

SSO allows users to **log in once** and access multiple systems without re-authenticating.  
Benefits:

- **Reduced Password Fatigue:** Fewer passwords, less chance of weak practices.
    
- **Centralized Authentication:** Easier to apply and manage security policies.
    
- **Reduced IT Workload:** Fewer account management tasks for IT.
    

---

### **LDAP (Lightweight Directory Access Protocol)**

- **What It Is:** A protocol used to access and manage **directory information** over an IP network.
    
- **Use Case:**
    
    - Mainly used for **directory services** (e.g., storing and retrieving user and group information).
        
    - Common in enterprise environments to manage user credentials.
        
- **Examples:**
    
    - **Microsoft Active Directory** is built on LDAP.
        
    - **Linux** uses **OpenLDAP**.
        

---

### **Federation (Identity Federation)**

- **What It Is:** A way to **link user identities** across different systems or organizations.
    
- **Purpose:**
    
    - Lets users **log in once** and access multiple apps across different domains (Single Sign-On).
        
    - Simplifies access while maintaining security and compliance.
        
- **Components:**
    
    - **Identity Providers (IdPs)** – manage and verify user identities.
        
    - **Service Providers (SPs)** – rely on IdPs to grant user access.
        
    - Uses **protocols** (e.g., SAML, OAuth) for secure communication.
        
- **Benefits:**
    
    - Streamlined access
        
    - Reduced login fatigue
        
    - Centralized authentication and management
        

---

### **SAML (Security Assertion Markup Language)**

- **What It Is:** An open standard for exchanging authentication and authorization data between an **identity provider (IdP)** and a **service provider (SP)**.
    
- **Use Case:** Commonly used for **Single Sign-On (SSO)** in enterprise environments.
    
- **Data Format:** Uses **XML** for communication.
    
- **Purpose:** Handles both **authentication** and **authorization**.
    
    ![[Pasted image 20250420054604.png]]
    

#### **Key Components:**

- **Identity Provider (IdP):** Authenticates the user and confirms their identity (e.g., Okta, Azure AD, Google Identity).
    
- **Service Provider (SP):** Relies on the IdP’s authentication to provide user access to apps/services.
    
- **Attestation:** IdP formally verifies the user’s identity and shares it with the SP.
    

---

### **OAuth**

- **What It Is:** An open standard for **access delegation**.
    
- **Purpose:** Allows users to grant third-party apps limited access to their data **without sharing passwords**.
    
- **Use Case:** Used for **authorization**, not authentication (e.g., "Sign in with Google" to authorize access to calendar).
    
- **Key Feature:** Grants access **on behalf of the user** with limited permissions.
    

---

### **OpenID Connect**

- **What It Is:** An identity layer **built on top of OAuth 2.0**.
    
- **Purpose:** Used for **authentication**.
    
- **Use Case:** Verifies the identity of a user logging into web or mobile apps.
    
- **Key Feature:** Combines authentication (via OpenID Connect) with authorization (via OAuth 2.0).
    

---

### **RADIUS and TACACS+ (Remote Authentication Dial-In User Service/Terminal Access Controller Access-Control System Plus )**

- **What They Are:** Protocols used for **centralized AAA (Authentication, Authorization, and Accounting)**.
    
- **Use Case:** Manage access for users connecting to network services (commonly used by ISPs and enterprises).
    
- **Purpose:**
    
    - **Authentication:** Verify user credentials
        
    - **Authorization:** Determine access levels
        
    - **Accounting:** Log user activity
        
        ![[Pasted image 20250420054650.png]]
        

---

### **Time-Based Authentication**

- **What It Is:** Authentication method using **time-limited codes** (e.g., TOTP).
    
- **How It Works:**
    
    - User receives a code that expires quickly (usually through an app like Google Authenticator).
        
    - Enhances security by adding a **time-sensitive** element, making unauthorized access harder.
        

---

### **Geofencing**

- **What It Is:** A technology that creates a **virtual boundary** around a physical location using GPS, RFID, Wi-Fi, or cellular data.
    
- **Use Case:**
    
    - Restrict access based on location
        
    - Monitor movement of users or assets
        
- **Example:** Allowing access to a secure app only when within company premises.
    

---
