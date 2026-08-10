
---

### 🔄 **Recovery Point Objective (RPO)**

- **What it means**: The maximum time of data you can afford to lose.
    
- **Example**: If your RPO is 4 hours, backups should happen at least every 4 hours so you don’t lose more than that in a disaster.
    

---

### ⏱️ **Recovery Time Objective (RTO)**

- **What it means**: How quickly you need to recover systems after a disaster.
    
- **Example**: If your RTO is 2 hours, systems should be back up within 2 hours to avoid major problems.
    
    ![[Pasted image 20250420052357.png]]
    

---

### ⚙️ **Mean Time Between Failures (MTBF)**

- **What it means**: How long a system usually works before breaking down.
    
- **Higher = Better reliability**
    

---

### 🔧 **Mean Time to Repair (MTTR)**

- **What it means**: How long it takes to fix something once it breaks.
    
- **Lower = Faster recovery**
    

---

### 🏢 **Recovery Sites**

- **Cold Site**: Cheapest, but takes **days to weeks** to set up after a disaster. No equipment or data.
    
- **Warm Site**: Some setup is ready. Takes **hours to days** to recover.
    
- **Hot Site**: Fully ready. Recovery in **minutes to hours**. Most expensive.
    

---

### 🔁 **Active-Active vs. Active-Passive**

- **Active-Active**: Both systems run at the same time. Better performance, no downtime.
    
- **Active-Passive**: One runs, the other waits. The backup kicks in if the main fails, but there might be a short delay.
    

---

### 🧪 **Disaster Recovery Testing**

- **Why it's important**: Helps make sure your recovery plan actually works before a real disaster happens.
    

---

### 🗣️ **Tabletop Exercises**

- **What it is**: A team talks through disaster scenarios to see if the recovery plan is solid.
    
- **Goal**: Spot weaknesses without doing real recovery.
    

---

### ✅ **Validation Tests**

- **What it is**: Actually run the recovery plan to make sure systems and data can be restored as planned.
    
- **Goal**: Practice and confirm everything works.
    

---

