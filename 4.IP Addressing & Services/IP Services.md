
---

## ✅ **Dynamic Addressing & DHCP**

- **Dynamic Addressing**: Automatically gives IP settings to devices (IP, gateway, DNS, etc.) using **DHCP**. Great for networks where devices often join/leave, like Wi-Fi.
    
- **DHCP (Dynamic Host Configuration Protocol)**:
    
    - Assigns IP addresses and other settings automatically.
        
    - Saves time and avoids manual mistakes.
        
- **DHCP Scope**:
    
    - Range of IPs that the DHCP server can assign.
        
    - Includes subnet mask, gateway, DNS, and lease time.
        
- **Reservation**:
    
    - A specific IP is always given to a device (identified by its **MAC address**).
        
    - Used for printers, servers, or devices needing a fixed IP.
        
- **Lease Time**:
    
    - How long a device can use an IP.
        
    - After it expires, the device must renew or get a new one.
        
- **DHCP Options**:
    
    - Extra settings like DNS, NTP, WINS sent along with the IP.
        
- **DHCP Relay**:
    
    - Forwards DHCP requests to a server on a different network.
        
    - Useful in multi-subnet environments.
        
        ![[Pasted image 20250414150655.png]]
        
- **Exclusion Ranges**:
    
    - IPs **within a DHCP scope** that won’t be given out.
        
    - Used for manual/static IPs to avoid conflicts.
        

---

## 📶 **SLAAC (Stateless Address Autoconfiguration)**

- **SLAAC (IPv6 only)**:
    
    - Devices auto-generate their own IP using the router’s info.
        
    - No need for DHCP or manual setup.
        

---

## 🌐 **DNS (Domain Name System)**

- **Name Resolution**: Converts domain names (like google.com) into IP addresses.
    
- **DNS**:
    
    - Translates easy-to-remember names into IPs.
        
    - Core part of how the internet works.
        
- **Recursive DNS Query**:
    
    - DNS server finds the full answer for you by asking other servers.
        
        ![[Pasted image 20250414150713.png]]
        
---

## 📁 **DNS Zones & Types**

- **Zone**: A section of DNS managed by an admin.
    

### ✅ **Zone Types**

- **Forward Zone**: Name ➜ IP (e.g., `google.com ➜ 8.8.8.8`)
    
- **Reverse Zone**: IP ➜ Name (e.g., `8.8.8.8 ➜ google.com`)
    

### ✅ **Authority Types**

- **Authoritative**: The final source of truth for DNS data.
    
- **Non-Authoritative**: Cached copy from another source.
    

### ✅ **Primary vs Secondary**

- **Primary Zone**: Editable, main zone file.
    
- **Secondary Zone**: Read-only copy, for backup/load balancing.
    

---

## 🔐 **DNS Security**

- **DNSSEC (DNS Security Extensions)**: Adds digital signatures to verify DNS data integrity and authenticity. Stops tampering.
    
- **DoH (DNS Over HTTPs) & DoT(DNS Over TLS)**:
    
    - Encrypt DNS queries.
        
    - **DoH** uses HTTPS, **DoT** uses TLS.
        
    - Protects privacy and stops spying.
        

---

## 📄 **Common DNS Records**

- **A Record**: Maps a domain to an **IPv4** address.
    
- **AAAA Record**: Maps a domain to an **IPv6** address.
    
- **CNAME**: Alias name ➜ True domain name.
    
- **MX**: Defines mail servers for a domain.
    
- **TXT**: Text info (e.g., SPF/DKIM for email security).
    
- **NS**: Defines which servers are responsible for DNS.
    
- **PTR**: IP ➜ Domain (reverse DNS).
    

---

## 🧾 **Hosts File**

- A local file that maps domain names to IPs.
    
- Used for:
    
    - Testing websites.
        
    - Blocking domains.
        
    - Overriding DNS.
        

---

## 🕒 **Time Protocols**

### ✅ **NTP (Network Time Protocol)**

- Keeps all devices' clocks in sync.
    
- Accurate to milliseconds.
    

### ✅ **NTS (Network Time Security)**

- A secure version of NTP with **encryption** and **authentication**.
    

### ✅ **PTP (Precision Time Protocol)**

- Very high-precision time sync (nanoseconds).
    
- Used in industries like telecom, finance, and automation.
    

---
