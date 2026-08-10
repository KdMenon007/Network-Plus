
---

### **802.3 Standards (Ethernet)**

- Defines how wired local area networks (LANs) work.
    
- Covers things like data formats and physical wiring rules.
    

---

### **Network Cable Properties**

#### **Speeds**

- **Copper cables:** Up to 40 Gbps.
    
- **Fiber cables:** Over 100 Gbps.
    

#### **Distance**

- **Copper:** Up to 1,100 meters (3,609 feet).
    
- **Fiber:** Over 40 kilometers (25 miles).
    

#### **Duplex Modes**

- **Half duplex:** One-way at a time.
    
- **Full duplex:** Two-way at the same time.
    

---

### **Cable Speeds**

- **Ethernet cables (Cat 5/5e/6/6a):** 100 Mbps to 10 Gbps.
    
- **Coaxial cables:** Used for broadband internet.
    
- **Fiber optic cables:** Highest speeds (up to 100 Gbps) over long distances.
    
- **Factors affecting speed:** Cable quality, setup, and interference.
    

---

### **Network Cable Properties**

#### **Noise Immunity (EMI - Electro-Magnetic Interference)**

- **Copper cables:** Can be affected by interference.
    
    - Use shielded cables to reduce this.
        
- **Fiber cables:** Immune to interference.
    

#### **Frequency**

- Higher frequency = Faster data speeds.
    

#### **Attenuation**

- Longer cables = Weaker signals.
    

---

### **Coaxial Cable (RG-6)**

**Description:**

- A type of electrical cable with **four layers**:
    
    - Central **copper conductor**
        
    - **Insulating dielectric layer**
        
    - **Metallic shield** (for EMI protection)
        
    - **Plastic jacket** (outer protection)
        
- **Used for**:
    
    - **Television**
        
    - **Satellite communication**
        
    - **Broadband internet**
        
- **RG-6** is the most common variant.
    
    ![[Pasted image 20250411040248.png]]
    
    ![[Pasted image 20250411040327.png]]
    
---

### **Advantages:**

- **Excellent shielding** against **electromagnetic interference (EMI)**
    
- **Long transmission distances** (up to **1100 meters**)
    
- **Cheaper than fiber optic** alternatives
    

---

### **Disadvantages:**

- **More expensive than twisted pair** cables
    
- **Fragile copper core** can snap if bent or mishandled
    

---

### **Common Connectors:**

- **BNC Connector:**
    
    - Bayonet-style locking mechanism
        
    - Used in **older bus and ring networks**
        
        ![[Pasted image 20250411040419.png]]
        
- **F Connector:**
    
    - **Twist-on/screw-type**
        
    - Common on **cable modems** and **TV connections**
        
        ![[Pasted image 20250411040437.png]]
        
---

### **Fiber-Optic Cable**

**Overview:**

- Uses **light signals** (instead of electrical signals) to **transmit data**.
    
- Made of **glass or plastic fibers**.
    
- Offers **extremely high speeds** and **large bandwidth**.
    
- Ideal for **telecom** and **internet backbone** infrastructure due to **low signal loss** over long distances.
    
    ![[Pasted image 20250411040912.png]]
    
    ![[Pasted image 20250411041009.png]]
    
---

### **Types of Fiber-Optic Cable**

#### **1. Single-Mode Fiber (SMF):**

- **Single strand** of glass with a **small core diameter (~9 µm)**
    
- **Carries one mode of light**, reducing interference and attenuation.
    
- **Best for**:
    
    - **Long-distance communication**
        
    - **Telecom and cable TV networks**
        
- **Range**: Several **kilometers without repeaters**
    
- **More expensive**, requires **laser-based light source**
    
#### **2. Multimode Fiber (MMF):**

- **Larger core** diameter (~50–62.5 µm)
    
- Allows **multiple modes of light** to travel at once
    
- **Best for**:
    
    - **Short-distance** communication (e.g., within buildings/campuses)
        
    - **LANs and internal networks**
        
- **Range**: Up to **500m (data)** / **2km (telecom)**
    
- **More affordable** and easier to handle than SMF
    
---

### **Advantages of Fiber-Optic:**

- **Immune to EMI** (electromagnetic interference)
    
- **Highest transmission speed** (into **Tbps** range)
    
- **Longest transmission distances**
    

---

### **Disadvantages of Fiber-Optic:**

- **Most expensive** cable type
    
- **Difficult to install**
    
- **Hard to troubleshoot**
    
- Requires **specialized tools**
    
- **Not easily repaired** in the field
    

---

### **Common Fiber-Optic Connectors:**

| Connector   | Name / Notes                      | Used In               | Features                   |
| ----------- | --------------------------------- | --------------------- | -------------------------- |
| **ST**      | Straight Tip                      | SMF                   | Bayonet-style connector    |
| **SC**      | Subscriber / Square Connector     | SMF, MMF              | Snap-in connector          |
| **LC**      | Lucent / Local / Little Connector | SMF, MMF              | Small form factor, snap-in |
| **Dual LC** | Dual version of LC                | SMF, MMF              | Snap-in, space-saving      |
| **MPO**     | Multi-fiber Push-On               | SMF, MMF (mostly MMF) | High-density, snap-in      |
![[Pasted image 20250411040929.png]]

![[Pasted image 20250411040947.png]]

![[Pasted image 20250411041157.png]]

![[Pasted image 20250411041209.png]]

![[Pasted image 20250411041255.png]]

---

## **Direct Attach Copper (DAC)**

**Overview:**

- **Pre-terminated copper cable** with transceivers on both ends.
    
- Used for **short-range connections** between network devices (e.g., switch-to-switch, switch-to-server).
    
- Offers **low power consumption** and **cost-efficiency** for close-proximity devices.
    
    ![[Pasted image 20250411042126.png]]
    
---

## **Twinaxial (Twinax) Cable**

**Overview:**

- **Shielded copper cable** used in **data centers**
    
- Supports **high-speed (10/40 Gbps)** Ethernet for **short-distance**
    
- Often used with **SFP+/QSFP+** DAC modules
    
    ![[Pasted image 20250411042210.png]]
    
**✅ Advantages:**

- **EMI shielding**
    
- **Cheaper** than fiber optics
    

**❌ Disadvantages:**

- **Short range**: ~**0.5 to 7 meters**
    
- **Costlier than twisted pair or coax**
    

---

## **Twisted Pair Cable**

**Overview:**

- Contains **8 copper wires** twisted into **4 pairs**
    
- **Most common** network cable in homes/offices
    

### **Types:**

- **UTP (Unshielded Twisted Pair)**:
    
    - No shielding
        
    - More susceptible to EMI
        
- **STP (Shielded Twisted Pair)**:
    
    - Shielding provides **EMI protection**
        
        ![[Pasted image 20250411042321.png]]
        
### **✅ Advantages:**

- **Inexpensive**
    
- **Easy to install and manage**
    
- **STP version resists EMI**
    

### **❌ Disadvantages:**

- **Limited distance** (up to **100 meters / 328 feet**)
    
- **UTP offers no EMI protection**
    

---

## **Twisted Pair Connectors**

|Connector|Pins|Common Use Cases|
|---|---|---|
|**RJ11**|4-pin|**Dial-up modems**, **analog phones**|
|**RJ45**|8-pin|**Ethernet**, **computers**, **networking gear**|

---

## **Twisted Pair Categories**:

- **Cat 5e**: Up to 1 Gbps
    
- **Cat 6 / 6a**: Up to 10 Gbps (short range)
    
- **Cat 7 / 8**: High-speed, shielded versions for data centers
    

---

## **RJ45 Wiring Standards: T568A vs T568B**

Both standards define the **color order** for the 8 wires in twisted pair cables terminated with **RJ45 connectors**.

|**Pin**|**T568A Color**|**T568B Color**|
|---|---|---|
|1|White/Green|White/Orange|
|2|Green|Orange|
|3|White/Orange|White/Green|
|4|Blue|Blue|
|5|White/Blue|White/Blue|
|6|Orange|Green|
|7|White/Brown|White/Brown|
|8|Brown|Brown|

- **T568B** is **more commonly used** in most installations.
    
    ![[Pasted image 20250411043426.png]]
    
---

## **Cable Types**

### ✅ **Straight-Through Cable**

- **Both ends use the same standard** (T568A **or** T568B)
    
- **Used to connect**:
    
    - **Unlike devices** (e.g., computer to switch, router to PC)
        
        ![[Pasted image 20250411043444.png]]
        
        ![[Pasted image 20250411043526.png]]
        
### 🔄 **Crossover Cable**

- **One end is T568A**, **other end is T568B**
    
- **Used to connect**:
    
    - **Like devices** (e.g., switch to switch, PC to PC, router to router)
        
        ![[Pasted image 20250411043551.png]]
        
        ![[Pasted image 20250411043610.png]]
        
---

### 🔌 **Wiring Configurations:**

1. **T568A + T568A = Straight-through cable**
    
    - Both ends use the **T568A** standard.
        
    - Used to connect **unlike devices** (e.g., PC to switch).
        
2. **T568B + T568B = Straight-through cable**
    
    - Both ends use the **T568B** standard (most common).
        
    - Also used for **unlike devices**.
        
3. **T568A + T568B = Crossover cable**
    
    - Each end uses a **different wiring standard**.
        
    - Used to connect **like devices** (e.g., PC to PC, switch to switch).
        
![[Pasted image 20250411043842.png]]

---
## **Quick Device Connection Guide**

|**Device A**|**Device B**|**Cable Type**|
|---|---|---|
|PC|Switch|Straight-through|
|Switch|Switch|Crossover|
|PC|PC|Crossover|
|Router|Switch|Straight-through|
|Router|Router|Crossover|

---

## 🔥 **Plenum Rating (Cable Fire Ratings)**

**Plenum-rated cables** are designed for safety in building air spaces:

|**Type**|**Description**|
|---|---|
|**Plenum-rated**|- Fire-resistant insulation- Emits **low smoke/toxicity**- Used in **air ducts, ceiling spaces**|
|**Non-Plenum**|- **Cheaper** alternative- Emits **more toxic smoke** when burned- Used in areas **not exposed** to air circulation|

**Why it matters:** Fire code regulations often **require plenum-rated cables** in shared air spaces to reduce fire hazards.

![[Pasted image 20250411044056.png]]

---

## 🔁 **Transceivers**

**Transceivers** = Devices that **transmit + receive** signals — especially important for connecting different types of cabling (e.g., copper ↔ fiber).

### 💡 Common Types:

|**Transceiver**|**Full Name**|**Speed**|**Usage**|
|---|---|---|---|
|**SFP**|Small Form-factor Pluggable|Up to **4.25 Gbps**|Ethernet & Fiber interfaces|
|**SFP+**|Enhanced SFP|Up to **10 Gbps**|High-speed data/telecom|
|**QSFP**|Quad Small Form-factor Pluggable|Up to **28 Gbps**|Data centers, high-density connections|
|**QSFP+**|Enhanced QSFP|Up to **40 Gbps**|Backbone links, 40G Ethernet|
![[Pasted image 20250411044114.png]]

---

## 🔄 **Media Converters**

**Media converters** are specialized transceivers that **convert signals** between **different media types**, enabling mixed-network communication.

### 🔧 Examples of Media Conversion:

- **Single-mode fiber** ⟷ **Ethernet**
    
- **Multimode fiber** ⟷ **Ethernet**
    
- **Fiber optic** ⟷ **Coaxial**
    
- **Single-mode fiber** ⟷ **Multimode fiber**
    

**Use Case:** Helps extend a copper network over a long-distance fiber link without replacing existing infrastructure.

![[Pasted image 20250411044224.png]]

---
