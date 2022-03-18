---
aliases: [""] 
tags: [ComputerNetworking] 
dateCreated: 2022-03-13 13:49:37
---
# Network Layer
*Forwarding:* When a packet arrives at a [[Router]]'s input link, the router must move the packet to the appropriate output link. **Router-local actions of transferring a packer from an input link interface to the appropriate output link interface.**

*Routing:* Determining the route or path taken by packets as they flow from a sender to a receiver. Determined through [[Routing Algorithms]]. **Network-wide process that determined the end-to-end paths that packets take from source to destination.**

## Data Plane

## Control Plane
### Traditional Approach
[[Routing Algorithms]] are used to determine [[Forwarding Table]]s which aids router in determining where to forward a packet. 

### SDN Approach
When a network controller that computes [[Forwarding Table]]s is implemented in software. 
- SDN Code is becoming increasingly more open source. 

### Network Service Model
Answers the question of whether the transport layer can rely on the network layer to deliver the packet to the destination. **Defines characteristics of end-to-end delivery of packets between sending and receiving hosts.**

Services include (but are not limited to):
- Guaranteed Delivery
- Guaranteed Delivery *with bounded delay*: Guaranteed delivery but with a specified host-to-host delay bound
- In-order packet delivery
- Guaranteed minimal bandwidth: Ensures that so long as the sending host transmits bits at a rate below the specified bit rate, then all packets are eventually delivered to the destination host. 
- Security: Can encrypt all datagrams at the source and decrypt them at the destination.

*Best-effort Service:* Packets are neither guaranteed to be received in order, nor is their eventual delivery even guaranteed. (Euphemism for *No service at all*?)
- Combined with adequate bandwidth provisioning and bandwidth-adaptive application-level protocols have been sufficient (Netflix and FaceTime).

## Internet Protocol
*Datagram:* A packet in the Network Layer

[[IPv4]]
[[IPv6]]

### Transitioning from IPv4 to IPv6
**Tunneling:** A Mechanism that is used for encapsulating IPv4 and IPv6 packets within a site-to-site IPv6 VPN.
![[Pasted image 20220313215819.png]]
