## TCP/IP Suite/Stack
- Application
- TCP/UDP -> Transport Control / User Diagram
- Layers for components
	- Layer 4:
		- TCP/UDP
	- Layer 3:
		- IP
	- Layer 2 
		- Ethernet/Wifi LAN technologies reside
### TCP/UDP Communications
- HTTP -> TCP(80)
- SMTP -> TCP(25)
- DNS -> UDP(53)
- NTP -> UDP(123)
Port can be whichever you want, these are just the default ones.

## DNS
- Nrtwork protocol
- Resolves host names to IP addresses
- Fully Qualified Domain Name (FQDN)
	- Hostname and a domain name
	- Example:
		- Hostname: ftp
		- Domain Name: mydomain.com
		- FQDN: ftp.mydomain.com 
## Common TCP/IP Ports
- 20,21, FTP
	- 1 Port for communication and the other for file transfer
## VPN
- PPTP (Point to Point Tunneling)
	- PPTP VPN sends PPP Packets using GRE (Generic Routing Encapsulation)
## Encapsulation
- ![[Pasted image 20240618103345.png]]

## DMZ
- Bridge between internet and our network
- Usual setup:![[Pasted image 20240618105003.png]]![[Pasted image 20240618105113.png]]
- Architecture example:![[Pasted image 20240618105025.png]]
## Segmentation
- Create "groups" inside of ROUTER
- Data will be broadcasted to just the group
- ![[Pasted image 20240618111407.png]]
## Microsegmentation
- Use of policies to control nodes in segment
- ![[Pasted image 20240618111533.png]]

## Virtual Routing
- multiple virtual routers inside one physical 
- May be implemented with VMware or Hyper-V
- Allow for the creation of multiple logical networks
- Inside CSPs, each VM or instance can be linked to different virtual routers

## MultiProcol Label Switching (MPLS)
- "Layer 2.5"
- Works like:
	- Attaches a label to each datapacket
		- label identifies the path the packet should take 
			- based on policies
		- Its then routed using MPLS Routers
- Uses:
	- Connectivity between CSPs and local end users
	- May provide network segmentation in the cloud with _**VPCs**_
	- Communication between private and public clouds
### Single Root Input / Output Virtualization (SR-IOV)
- Single root input/output virtualization (SR-IOV)
- Same NIC can be shared among VMs
- Allows each VM to access same NIC, better performance

# Network Services
- ### Dynamic Host Configuration Protocol (DHCP)
	- Enables autoasigning IP or other network params
	- Uses client server model, _**client requests**_:
		- config info from server
	- Additional network config params like:
		- Subnet Mask
		- Default Gateways
		- DNS Servers
		- Location of ServerApps
- ### Content Delivery Network (CDN)
	- caches content in edge servers
	- directs request to closest edge server