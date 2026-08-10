

1. **TCP (Transmission Control Protocol) Handshake**
    
    - **Purpose**: Ensures reliable communication between devices over a network.
        
    - **Handshake Steps**:
        
        1. **SYN**: Client sends a SYN (synchronize) message.
            
        2. **SYN-ACK**: Server responds with SYN-ACK (synchronize acknowledgment).
            
        3. **ACK**: Client sends ACK (acknowledgment).
            
    - **Similarity to TCP**: Ensures both sides are ready to exchange data.
        
2. **TLS/SSL Handshake**
    
    - **Purpose**: Establishes a secure connection over TCP.
        
    - **Handshake Steps**:
        
        1. **Client Hello**: Client sends supported encryption methods.
            
        2. **Server Hello**: Server responds with chosen encryption method and certificate.
            
        3. **Key Exchange**: Both parties exchange keys.
            
        4. **Finished**: Both confirm the setup is complete.
            
    - **Similarity to TCP**: Like TCP, it ensures both sides are ready, with added encryption for security.
        
3. **SIP (Session Initiation Protocol) Handshake**
    
    - **Purpose**: Establishes multimedia sessions (such as voice or video calls).
        
    - **Handshake Steps**:
        
        1. **INVITE**: Client sends an INVITE message to initiate the session.
            
        2. **200 OK**: Server responds, acknowledging the session request.
            
        3. **ACK**: Client sends an ACK to confirm the session.
            
    - **Similarity to TCP**: Like TCP, SIP requires a handshake to establish a session.
        
4. **PPP (Point-to-Point Protocol) Handshake**
    
    - **Purpose**: Used in dial-up connections, VPNs, and other direct communication links.
        
    - **Handshake Steps**:
        
        1. **Link Establishment**: Client and server exchange configurations and negotiate protocols.
            
        2. **Authentication**: Optional authentication step (e.g., PAP or CHAP).
            
        3. **Network Layer Protocol Negotiation**: Agreement on encapsulating network traffic.
            
    - **Similarity to TCP**: Ensures both sides are ready to communicate.
        
5. **BGP (Border Gateway Protocol) Handshake**
    
    - **Purpose**: Used by routers to exchange routing information between networks.
        
    - **Handshake Steps**:
        
        1. **Open Message**: Routers send an open message to start the session.
            
        2. **Keepalive**: Routers exchange keepalive messages to maintain the session.
            
        3. **Update**: After establishing a session, routing information is exchanged.
            
    - **Similarity to TCP**: Establishes a reliable connection for routing information exchange.
        
6. **FTP (File Transfer Protocol) Control Connection Handshake**
    
    - **Purpose**: Establishes a control connection for file transfer between client and server.
        
    - **Handshake Steps**:
        
        1. Client sends a connection request on port 21.
            
        2. Server responds with a "220 Ready" message.
            
    - **Similarity to TCP**: Uses a handshake to ensure both sides are ready before communication.
        
7. **CHAP (Challenge-Handshake Authentication Protocol)**
    
    - **Purpose**: Authenticates clients to servers in point-to-point connections.
        
    - **Handshake Steps**:
        
        1. **Challenge**: The server sends a challenge message to the client.
            
        2. **Response**: The client responds with a value using a hash function and a shared secret.
            
        3. **Verification**: Server verifies the response; if correct, authentication succeeds.
            
    - **Similarity to TCP**: Authenticates both sides before communication begins.
        
8. **WPA2 (Wireless Protected Access 2) Handshake**
    
    - **Purpose**: Secures wireless networks by authenticating devices and establishing encryption keys.
        
    - **Handshake Steps**:
        
        1. **Message 1**: Access point sends a nonce (random number) to the client.
            
        2. **Message 2**: Client responds with its nonce, encrypted with a pairwise transient key (PTK).
            
        3. **Message 3**: Access point confirms the response.
            
        4. **Message 4**: Client acknowledges the access point's response.
            
    - **Similarity to TCP**: Ensures both sides authenticate and agree on encryption keys before communication.
        
9. **Noise Protocol Framework**
    
    - **Purpose**: A framework for building cryptographic protocols.
        
    - **Handshake Steps**: Various handshake patterns (e.g., IK for key exchange).
        
    - **Similarity to TCP**: Ensures both parties agree on secure communication parameters.
        
10. **L2TP (Layer 2 Tunneling Protocol) Handshake**
    

- **Purpose**: Used for creating VPNs to securely tunnel data.
    
- **Handshake Steps**:
    
    1. **Call Request**: Client sends a connection request.
        
    2. **Call Accept**: Server accepts the connection and establishes a tunnel.
        
    3. **Session Setup**: Final settings are negotiated, and the tunnel is ready.
        
- **Similarity to TCP**: Establishes a secure connection before data transmission.
    

11. **RDP (Remote Desktop Protocol) Handshake**
    

- **Purpose**: Used for remote desktop access.
    
- **Handshake Steps**:
    
    1. Client sends a connection request.
        
    2. Server responds with a version and security settings.
        
    3. Both parties negotiate encryption and authentication.
        
- **Similarity to TCP**: Ensures both sides are ready before establishing a remote session.
    

12. **DHCP (Dynamic Host Configuration Protocol) Handshake**
    

- **Purpose**: Used by clients to obtain an IP address from a DHCP server.
    
- **Handshake Steps**:
    
    1. **DHCP Discover**: Client broadcasts a request for an IP address.
        
    2. **DHCP Offer**: Server replies with an available IP address.
        
    3. **DHCP Request**: Client accepts the offered IP address.
        
    4. **DHCP Acknowledgment**: Server confirms the IP assignment.
        
- **Similarity to TCP**: Both sides agree on parameters (e.g., IP address) before communication starts.
    

