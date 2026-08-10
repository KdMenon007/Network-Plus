
---
### **SNMP & Network Monitoring**

---

#### **1. SNMP (Simple Network Management Protocol)**

- Protocol for **monitoring, configuring**, and **controlling network devices**.
    
- Operates at the **application layer** (OSI Layer 7).
    
- Provides a **standard framework** for network management.
    

---

#### **2. SNMP Traps**

- **Unsolicited messages** from devices to the SNMP manager.
    
- Notify about **important events or faults** instantly.
    
    ![[Pasted image 20250419065656.png]]
    

---

#### **3. MIBs (Management Information Bases)**

- Databases of **device information** (status, capacity, performance).
    
- Use **data objects** to describe each device's attributes.
    
    ![[Pasted image 20250419065712.png]]
    

---

#### **4. SNMP Versions**

- **SNMP v2c**:
    
    - Adds features like **bulk data retrieval**.
        
    - **Lacks encryption**, uses **plain-text community strings**.
        
- **SNMP v3**:
    
    - Supports **authentication and encryption**.
        
    - Provides **secure** and **robust** network management.
        

---

#### **5. SNMP Community Strings**

- Act like **passwords** for SNMP access:
    
    - `public`: **Read-only** access.
        
    - `private`: **Read-write** access.
        

```bash
Router(config)#snmp-server community public RO
Router(config)#snmp-server community private RW
```

---

#### **6. SNMP v3 Authentication**

- Verifies the identity of devices.
    
- Adds **strong authentication and encryption** for data protection.
    

---

### **Flow & Traffic Monitoring**

---

#### **7. Flow Data**

- Captures **metadata** about traffic (e.g., source/destination IPs, ports, protocol).
    
- Helps analyze:
    
    - **Traffic patterns**
        
    - **Bandwidth usage**
        
    - **Security threats**
        
        ![[Pasted image 20250419065741.png]]
        

---

#### **8. Packet Capture (pcap)**

- Logs **raw network traffic** for analysis.
    
- Used to:
    
    - **Troubleshoot issues**
        
    - **Detect malicious behavior**
        
    - **Verify data transmission**
        
        ![[Pasted image 20250419065804.png]]
        

---

#### **9. Baseline Metrics**

- Define **"normal" performance levels**:
    
    - Traffic volume
        
    - Speed
        
    - Error rates
        
- Helps detect **deviations and performance issues** early.
    

---

#### **10. Anomaly Alerting/Notifications**

- Automatically **detects deviations** from baseline.
    
- Sends alerts for:
    
    - **Unusual traffic patterns**
        
    - **Potential security threats**
        
- Ensures **quick response and network stability**.
    

---
# Logs Management

---

#### **1. Log Aggregation**

- **Centralized collection** of log messages from various devices.
    
- Helps with:
    
    - **Troubleshooting**
        
    - **Security monitoring**
        
    - **Compliance reporting**
        

---

#### **2. SIEM (Security Information and Event Management)**

- Analyzes **security alerts** in real time.
    
- Key features:
    
    - **Log aggregation + correlation**
        
    - **Automated alerts and reports**
        
    - **Threat detection via behavior analysis**
        
        ![[Pasted image 20250419065831.png]]

---

#### **3. Syslog Collector**

- Tool that **gathers syslog messages** from multiple devices.
    
- Centralizes log data for:
    
    - **Simplified analysis**
        
    - **Security tracking**
        
    - **Faster troubleshooting**
        

---

#### **4. API Integration**

- **APIs connect** network tools and systems.
    
- Benefits:
    
    - **Automation** of tasks like config changes and data pulling
        
    - **Streamlined operations**
        
    - **Scalable management**
        
        ![[Pasted image 20250419065900.png]]
        

---

### **Network Visibility & Optimization**

---

#### **5. Network Solutions**

- Encompass tools and methods for:
    
    - **Monitoring**
        
    - **Managing**
        
    - **Securing** the network
        
- Ensure **optimal performance, uptime, and protection**.
    

---

#### **6. Network Discovery**

- Identifies all connected **devices and infrastructure**.
    
- Types:
    
    - **Ad hoc**: Manual checks when needed
        
    - **Scheduled**: Regular automated scans
        
- Keeps network **inventory current and accurate**.
    

---

#### **7. Traffic Analysis**

- Examines data packets for:
    
    - **Bandwidth usage**
        
    - **Traffic trends**
        
    - **Bottlenecks**
        
- Helps **optimize network speed and load balancing**.
    

---

### **Monitoring Types**

---

#### **8. Performance Monitoring**

- Tracks:
    
    - **Response time**
        
    - **Throughput**
        
    - **Error rates**
        
- Assesses overall **network health**.
    

---

#### **9. Availability Monitoring**

- Ensures **network components are up and reachable**.
    
- Detects **downtime** and supports **fast recovery**.
    

---

#### **10. Configuration Monitoring**

- Monitors **device setting changes**.
    
- Prevents **unauthorized edits** and ensures **policy compliance**.
    
---