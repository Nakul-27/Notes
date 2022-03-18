---
aliases: [""] 
tags: [ComputerNetworking] 
dateCreated: 2022-03-13 20:19:06
---
# IPv4
## Formatting
![[Pasted image 20220313202049.png]]
*Type of Service:* included to allow different types of IP datagrams to be distinguished from each other. 

*Time to Live:* Ensures that datagrams don't circulate forever. **Field is decremented by 1 each time the datagram is processed by a router.**

*Protocol:* used when an IP datagram reaches its final destination. Number indicates the specific transport-layer protocol to which the data portion of this IP datagram should be passed.

## Addressing
**Dotted-Decimal Notation:** Each byte of the address is written in its decimal form and is separated by a dot from the other bytes (Ex: 192.168.0.0)

**[[Subnet]]:** Logically visible sub-sections of an Internet Network
**[[Subnet Mask]]:**  indicates the leftmost bits of the 32-bit quantity define the subnet address.

Note that the address 255.255.255.255 indicates that the message will be delivered to all hosts on the same subnet. 

### Block Addressing
Break up the IP addresses allocated from the ISP organizations' subnet.

## NAT 
Maps multiple local private addresses to a public one before transferring the information.

### NAT Table
A table of network translations

