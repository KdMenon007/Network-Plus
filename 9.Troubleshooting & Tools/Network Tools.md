
---

## 🛠️ **Software Tools**

### 🔎 **Protocol Analyzer / Packet Capture**

- **Function:** Captures and analyzes network traffic (e.g., Wireshark).
    
- **Purpose:** Troubleshooting, performance monitoring, and security auditing.
    

---

### 💻 **Command Line Tools**

|Tool|Function|
|---|---|
|`ping`|Tests connectivity and measures round-trip time using ICMP echo requests|
|`traceroute` / `tracert`|Shows each hop in the path from source to destination|
|`nslookup`|DNS lookup for hostname to IP (Windows)|
|`dig`|DNS lookup tool (Linux), provides detailed record queries|
|`tcpdump`|Packet capture tool for CLI (Linux)|
|`netstat`|Displays current connections, ports, and routing tables|
|`ipconfig`|Shows/sets IP config on Windows|
|`ifconfig`|Shows/sets IP config on older Linux/Unix|
|`ip`|Modern alternative to ifconfig on Linux|
|`arp`|Displays/modifies ARP cache (IP ↔ MAC mapping)|
|`nmap`|Scans devices and services on the network|

---

### 🌐 **Discovery Protocols**

|Protocol|Description|
|---|---|
|**LLDP**|Vendor-neutral; shares device info (ID, capabilities, neighbors)|
|**CDP**|Cisco-proprietary; shows directly connected Cisco device info|

---

### 🚀 **Speed Tester**

- **Function:** Measures upload/download speed, latency, and jitter.
    
- **Usage:** Verify ISP SLAs; pinpoint slow segments in the network.
    

---

## 🔧 **Hardware Tools**

|Tool|Function & Use|
|---|---|
|**Toner**|Identifies specific cables in bundles using a tone generator and probe|
|**Cable Tester**|Checks for continuity, signal strength, shorts, opens, and miswiring|
|**Network Tap**|Creates a passive copy of network traffic for monitoring without disruption|
|**Wi-Fi Analyzer**|Detects Wi-Fi signals, strength, interference, and channel usage|
|**Visual Fault Locator**|Identifies faults in fiber optic cables with visible red laser light|

---

## ⚙️ **Basic Networking Device Commands**

These commands are used to **diagnose, monitor, and manage** routers, switches, and network interfaces.

---

### 📘 `show mac-address-table`

- **Purpose:** Displays MAC addresses learned by the switch and their corresponding ports.
    
- **Use Case:** Track devices on the network, troubleshoot port-level issues, detect unauthorized devices.
    

---

### 📘 `show route`

- **Purpose:** Displays the device's routing table.
    
- **Use Case:** Verifies active routes, next-hop info, and route sources. Essential for troubleshooting routing issues.
    

---

### 📘 `show interface`

- **Purpose:** Gives status and statistics of network interfaces.
    
- **Use Case:** Diagnose issues like link failure, errors, speed/duplex mismatch.
    

---

### 📘 `show config`

- **Purpose:** Shows current configuration settings on the device.
    
- **Use Case:** Verify IPs, routing, ACLs, and security settings. Helps audit and find misconfigurations.
    

---

### 📘 `show arp`

- **Purpose:** Displays IP-to-MAC mappings in the ARP table.
    
- **Use Case:** Troubleshoot IP resolution issues and confirm device communication on the local network.
    

---

### 📘 `show vlan`

- **Purpose:** Displays VLAN configuration and associated switch ports.
    
- **Use Case:** Verify VLAN setup, diagnose misrouted traffic or VLAN-related segmentation problems.
    

---

### 📘 `show power`

- **Purpose:** Shows Power over Ethernet (PoE) status and consumption.
    
- **Use Case:** Ensure powered devices (IP phones, cameras, etc.) receive sufficient power, manage PoE budgets.
    

---

## 🧠 **SNORT**

**Type:** Signature-based IDS/IPS

**Purpose:** Detects attacks using _rules/signatures_

**Key Points:**

- Developed by **Martin Roesch**; maintained by **Cisco Talos**.

- Works in **3 modes:** Sniffer, Packet Logger, IDS/IPS.

- **Rule-based detection** — finds known patterns in packets.

- Rules look like:

```

alert tcp any any -> any 80 (msg:"HTTP traffic"; sid:1001;)

```

- Output: Alerts in console or log files.

- Great for **detecting known threats** (SQLi, XSS, port scans, etc).

---

## ⚙️ **SURICATA**

**Type:** Multi-threaded IDS/IPS

**Purpose:** Next-gen Snort (can use Snort rules too).

**Key Points:**

- **Multi-threaded** → handles heavy traffic better.

- Built-in **protocol detection** (HTTP, TLS, DNS, SSH, etc).

- Logs to **EVE JSON** (easy for SIEM tools).

- Can **extract files** and **detect anomalies** automatically.

- Works as IDS, IPS, or packet logger.

---

## 🔍 **ZEEK (formerly Bro)**

**Type:** Network Behavior Analysis Tool

**Purpose:** Monitors network activity & behavior (not signature-based).

**Key Points:**

- Creates detailed logs: `conn.log`, `http.log`, `dns.log`, etc.

- Detects **unusual patterns**, **policy violations**, or **custom events**.

- Uses its own **scripting language** for advanced detections.

- Perfect for **forensics and long-term network monitoring.**

---

## 🧩 **BRIM**

**Type:** GUI tool for Zeek/PCAP data

**Purpose:** Visualizes and filters network traffic easily.

**Key Points:**

- Opens **PCAPs** and **Zeek logs** instantly.

- Uses **ZQL (Zeek Query Language)** to search data.

- Great for **investigating incidents** quickly without CLI mess.

---

## 🧰 **WIRESHARK**

**Type:** GUI Packet Analyzer

**Purpose:** Deep dive into individual packets.

**Key Points:**

- Visual, easy-to-use interface.

- Filters: `ip.addr == 192.168.1.1 && tcp.port == 80`

- Decode every layer (Ethernet → TCP → Application).

- Use for **manual inspection and protocol analysis**.

---

## 🖥️ **TSHARK**

**Type:** CLI version of Wireshark

**Purpose:** Analyze packets via command line (automation-friendly).

**Key Points:**

- Ideal for scripting or remote systems.

- Output to CSV, JSON, or text.

- Example:

```bash

tshark -r capture.pcap -Y "http" -T fields -e ip.src -e http.host

```

- Lightweight and perfect for **batch analysis**.

---

## 🧠 **NETWORKMINER**

**Type:** Passive Network Forensics Tool

**Purpose:** Extracts files, credentials, and metadata from PCAPs.

**Key Points:**

- GUI-based forensic tool.

- Recovers files, images, certificates, etc.

- Detects OS, hostname, and user-agent data.

- Perfect for **incident response and evidence collection**.

---

### 🔐 TL;DR Cheat Sheet

|Tool|Type|Main Use|

|---|---|---|

|**Snort**|IDS/IPS|Signature detection of known threats|

|**Suricata**|IDS/IPS|High-performance, multi-protocol detection|

|**Zeek**|Network Analysis|Behavior & anomaly detection|

|**Brim**|Visualization|GUI for Zeek/PCAP exploration|

|**Wireshark**|GUI Analyzer|Manual deep packet inspection|

|**Tshark**|CLI Analyzer|Automated packet analysis|

|**NetworkMiner**|Forensics|File & credential extraction from traffic|

---