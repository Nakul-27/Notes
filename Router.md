---
aliases: [""] 
tags: [ComputerNetworking] 
dateCreated: 2022-03-13 14:25:49
---
# Router

## Inside a Router
![[Pasted image 20220313142803.png]]
- *Input Ports:* Terminates incoming physical link (Physical Layer), Links to the link layer (Link Layer), **performs a lookup function which interfaces with the forwarding table.**
- *[[Switching Fabric]]:* Connects the router's input ports to the output ports. 
- *Output Ports:* Stores packets that are received from the switching fabric and transmits them to the outgoing link.
- *Routing Processor:* Executes [[Routing Protocols]], maintains [[Routing Table]]s, attached link state information, and computes the Forwarding Table for the router. (SDN - responsible for communicating with a remote controller)

## Prefix Matching
When determining where to send an incoming packet, look at the prefix. In the case of a match, use the longest prefix matching rule.

Ex:
![[Pasted image 20220313144520.png]]

## Queueing 
When there is an excess of queueing that occurs at the input or output ports, **packet loss** might occur. 
![[Pasted image 20220313145202.png]]

**Head of Line (HOL) Blocking:** a queued packet in an input queue must wait for transfer through the fabric because it is blocked by another packet at the head of the line.
![[Pasted image 20220313145618.png]]

## Buffering
For a while, the buffer size was deduced through:
$$
B = RTT \cdot C.
$$
Where $RTT$ referred to the Round Trip Time and $C$ referred to the Capacity. 

According to more recent discussions, when a large number of *independent* TCP flows, denoted by $N$, pass through a link, the new equation is:

$$
B = RTT \cdot C / \sqrt{N}.
$$
Note that larger buffers leads to larger queueing delays. 
