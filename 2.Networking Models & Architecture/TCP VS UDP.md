
---
### **TCP (Transmission Control Protocol)**

- **Description:** A reliable, connection-oriented protocol used for data delivery between applications on hosts over an IP network. It ensures data integrity by retransmitting lost data, sequencing packets, and using flow control.
    
- **Port:** Various (e.g., HTTP on TCP 80, HTTPS on TCP 443)
    
- **OSI Layer:** Transport Layer (Layer 4)
    
- **Devices:** Servers, Routers, Switches, Clients
    
- **Common Uses:** Web browsing, email, file transfers
    
- **Key Features:**
    
    - **Acknowledgments:** Verifies data transmission.
        
    - **Flow Control:** Prevents buffer overflow.
        
    - **Windowing:** Determines the amount of data to send before acknowledgment.
        
    - **Sequencing:** Ensures data is received in the correct order.
        

---

### **UDP (User Datagram Protocol)**

- **Description:** A connectionless, unreliable protocol used for fast communication where speed is prioritized over reliability. It doesn’t ensure packet delivery or order and is often used for streaming or gaming.
    
- **Port:** Various (e.g., DNS on UDP 53)
    
- **OSI Layer:** Transport Layer (Layer 4)
    
- **Devices:** Servers, Routers, Switches, Clients
    
- **Common Uses:** Audio/video streaming, online gaming, VoIP
    
- **Key Features:**
    
    - **Unreliable:** No guarantee of packet delivery.
        
    - **Connectionless:** No need to establish a connection before sending data.
        
    - **No Acknowledgments:** Data isn’t confirmed as received.
        
    - **No Flow Control:** Data can be sent without waiting for confirmation.
        

| **Feature**                   | **TCP**                                                  | **UDP**                                   |
| ----------------------------- | -------------------------------------------------------- | ----------------------------------------- |
| **Connection Type**           | Connection-oriented (requires handshake)                 | Connectionless (no handshake)             |
| **Reliability**               | Reliable (guarantees delivery, retransmits lost packets) | Unreliable (no guarantee of delivery)     |
| **Speed**                     | Slower (due to overhead for reliability)                 | Faster (no reliability checks)            |
| **Flow & Congestion Control** | Yes (manages flow and congestion)                        | No (doesn’t manage flow or congestion)    |
| **Use Cases**                 | Web browsing (HTTP), email (SMTP), file transfer (FTP)   | Video streaming, VoIP, online gaming, DNS |
| **Header Size**               | Larger (20-60 bytes)                                     | Smaller (8 bytes)                         |

# **TCP 3-Way Handshake:**

1. **Client sends SYN**: The client sends a "SYN" message to the server, saying "Let's start a connection."
    
2. **Server responds with SYN-ACK**: The server replies with "SYN-ACK," saying "Okay, I'm ready and I acknowledge your request."
    
3. **Client sends ACK**: The client sends an "ACK" message back to the server, saying "I got your response, we're connected!"
    

![[Pasted image 20250410125155.png]]