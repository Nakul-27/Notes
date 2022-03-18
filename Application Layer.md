# Application Layer
**Uses services** from the Transport Layer
**Provides Services** to the User

Uses [[Sockets]] to identify necessary information coming from the Transport Layer.

## Protocols
### Open Protocols
Defined in RFCs (public)
Allows for Interoperability

### Proprietary Protocols
Pay-to-access

## TCP
Connection-oriented reliable data

## UDP
Connection-less, without guarantees

## Client Server Paradigm
### Always on Server
#### Server
Always-on Host
Permanent IP Address
Often in Data centers for scaling

#### Client
Contact and communicate with the server
Could be intermittently connected and have a dynamic IP Address
*DO NOT* communicate with each other directly

### [[Peer-to-Peer]] architecture
*NO* always-on server
computers act as both server and clients
*Self-Scalability*: new peers bring new service capacity, as well as new service demands.
Peers are intermittently connected and change IP addresses.

