# Transport Layer
Found in **Kurose 8th Edition** #textbook
Resides between the [[Application Layer]] and the [[Network Layer]].

[[TCP]] and [[UDP]] are both on the Transport Layer.

A transport layer protocol provides for **logical communication** between application process running on different hosts. 
**Logical Communication**: Means that from the application's perspective, it is as if the hosts running the process were directly connected, when in reality they may be on different ends of the planet. 

*Segment*: A Transport Layer Packet
## Relationship to Network Layer
![[Pasted image 20220216214313.png]]
### **Transport - *processes***, **Network - *hosts*** 

## UDP in the Transport Layer
### Reasons for UDP
- Offers *Finer application-level control over what data is sent and when*. Unlike TCP, UDP will package data that is sent to it and immediately pass the segment to the Network layer. TCP on the other hand has congestion control and therefore throttles the transport-layer TCP sender when one or more links between the source and destination hosts become excessively congested. **UDP is a no-frills segment-delivery service** 
- Requires *no connection establishment.* TCP uses a 3-way-handshake before it starts to transfer data, whereas UDP just "blasts away." **Reason that DNS runs over UDP and not TCP and HTTP uses TCP instead of UDP.**
- There is *no connection state*.
- UDP has *smaller packet header overhead.* **UDP only has 8 bytes of overhead whereas TCP has 20.**

![[Pasted image 20220216220922.png]]

## TCP in the Transport Layer
Provides a **full-duplex service.** 

![[Pasted image 20220216224037.png]]

### Three-Way Handshake
1. Client sends a special TCP Segment (No Payload)
2. Server responds with a second special TCP Segment (No Payload)
3. Finally the client responds again with a third special TCP Segment (Payload)
