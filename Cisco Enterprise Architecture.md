# Cisco Enterprise Architecture Model
[[Networking]]
![[Pasted image 20211117110300.png]]
## [[Modular Design]]
### Access-Distribution
### Services
- Identify services
	- Lightweight Acess Point Protocol (LWAPP)
	- Wireless controllers
	- Unified communications services
	- Policy gateways
### Data Center ([[Server Farm]])
- Managing and maintaining many data systems that are vital to business
### Enterprise Edge
- Internet Edge and the WAN Edge
- Conectivity to voice, video, and data services

# Enterprise Campus
- Building(s) conencted into one enterprise network that consists of many [[LAN]]s
### Building Acess
### Building Distribution
### Campus Core
### Data Center ([[Server Farm]])

# Enterprise Edge
## E-Commerce
- Components
	- Firewall/Firewall Routers
	- Network intrusion prevention systems (IPS)
## Internet Connectivity and [[DMZ]]
- Provides internal users with secure connectivity to Internet services such as public servers, email, and [[DNS]].
- Components
	- Firewall/Firewall Routers
	- Internet Edge Routers
	- FTP and HTTP Servers
	- SMTP Relay Services
	- DNS Servers
##  Remote Access and VPN
- Authentication for remote users and sites
## Wide Area Network [[WAN]]
- Routing traffic between remote sites and central site

# Service Provider Edge
- [[ISP]] to link to other sites
- WAN Services
- Public Switch Telephone
## Remote 
- Enterprise Branch
- Telework
- Data Center
## An Organization has...
||Single|Dual
|-----|-----|-----|
|Home| 1 Connection to **1 ISP** | Many Connections to **1 ISP** |
|Multi-Home| 1 Connection to **Many ISPs** | Many Connections to **Many ISPs** |
