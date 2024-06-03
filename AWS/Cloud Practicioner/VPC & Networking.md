### HighLevel Overview
• VPC, Subnets, Internet Gateways & NAT Gateways
• Security Groups, Network ACL (NACL),VPC Flow Logs
• VPC Peering, VPC Endpoints
• Site to Site VPN & Direct Connect
• Transit Gateway

### IP Adresses
- Default behavior, if instance stops, IP changes next time it is rebooted
- ==Elastic IP== allows you to attach a fixed public IPv4 address to EC2 instance
- ***ALL Public IPv4 on AWS will be charged ==$0.005== per hour*** 
- AWS passively encouraged the usage of IPv6 ***==Free==***
### VPC & Subnets
- VPC is the environment in which you deploy your aws services, the highest tier
- VPC Attached to specific region
- Subnets are tied to an AZ, they serve as partitioners for specific use cases
- Private & Public subnets
- Private for a DB instance for example
- Public for HTTPS Server for example
- ***Access between subnets is managed by ==Route Tables==***
- ![[Pasted image 20240410094806.png]]
### Internet Gateway & NAT Gateways
- IG Helps our VPC instances connect with the internet 
- Public SN (subnets) have a route to the IG
- NAT GW (gateways) & NAT Instances, allow your instances in your Private Subnets to access the internet while remaining private
### CIDR - Classeless Inter-Domain Routing
- Its a IPv4 range, IPs within that range are allowed in the VPC
- CIDR.xyz, rgeat site to know ranges for IPs
##### ==NOTE==: Everytime you create an EC2 Instance, it HAS to be assigned to an specific subnet created inside your VPC, this will assign an _IP_ within the ==CIDR Range of that Subnet== 

> *Subnets are registered in a Route Tables which dictates the permissions for that subnet, which IPs, ranges, protocols, and all that it accepts *


### Security Groups & Network ACL (NACL)

- NACL - Stateless:
	1. Return Traffic must be explicitily allowed by rules
	2. Firewall which controls traffic from and to a subnet
	3. Can have ***ALLOW & DENY rules***
	4. Attached to a ==Subnet Level== 
	5. Only IP Addresses
- SG Security Groups Stateful:
	1. Return Traffic is automatically allowed, regardless of any rules
	2. Firewall that controls traffic to and from an Elastic Network Interface (ENI) / EC2 Instance
	3. Can only have ***ALLOW Rules***
	4. IP addresses and other SGs

- NACL are like security groups but for subnets

### VPC Peering
- Conect 2 VPC, privately using AWS network
- Make them behave as if they were in the same network
- ==Must not have overlapping CIDR==
- Not transitive: a new VPC is not going to be automatically linked to all the other VPCs in the network
### VPC Endpoints
- Allow you to connect to Services using a private network instead of the public network
- Enhanced security and lower latency
- VPC Endpoint ***Gateway***: S3 & DynamoDB
- VPC Endpoint ***Interface (ENI)***: the rest
### Private Link 
- ![[Pasted image 20240410103339.png]]
### Site to Site & Direct Connect
- **Site to Site**:
	1. Connect an on premises VPN to AWS
	2. Automaticlly encrypted
	3. Goes over the public Internet
- Direct Connect
	1. Physical connection
	2. More secure and faster
	3. Takes at least a month
	4. Private network

### Transit Gateway
- Network gateway so you can manage multiple types of connections between your network components/services
- ![[Pasted image 20240410111851.png]]
- 