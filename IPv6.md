---
aliases: [""] 
tags: [ComputerNetworking] 
dateCreated: 2022-03-13 21:49:13
---
# IPv6
## Differences from IPv4
- Increases the size of the IP address from 32 to 128 bits. 
- Streamlined 40-byte header
- "Flow" labeling (Allows for distinguishing between things like Audio/Video, File Transfer, etc.)
### Header
![[Pasted image 20220313215312.png]]
- Version
- Traffic Class (Can be used to give priority to certain datagrams within a flow)

Note that the following are no longer present in IPv6:
- Fragmentation/reassembly
- Header Checksum
- Options
