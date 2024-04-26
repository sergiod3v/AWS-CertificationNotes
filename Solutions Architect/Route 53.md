- Records
	- how u want to route traffic for a domain
	- Types
		- A: maps a hostname to a IPv4 IP
		- AAAA: maps a hostname to IPv6
		- CNAME hostname to hostname
		- NS: Name Servers from the Hosted Zone
- Hosted Zones:
	- A container for records that define how to rote traffic to a domain and its subdomains
	- Public: records that specify routing public domain names
	- Private: records to route within VPCs ( private domain names)
	- $0.5 per month hosted zone
	- ![[Pasted image 20240424092025.png]]
	-
- Record names are like sites inside of a domain
	- domain -> unity.com
	- record name -> ==dev.==unity.com :O
- Query the DNS (route 53 domain) as little as possible
	- Record TTL (Time To Live) will cache the connection of the client for some time so it can be retrieved instead of called again 

### CNAME vs Alias 
- Alias points a hostname to an AWS Resource (such as ALB, CloudFront, etc...)
- CNAME: Points hostname to other hostname (app.mydomain.com => blabla.anything.com)

#### Alias Records
- Only to AWS resources
- extension to DNS functionality
- Automatically detects changes in the resource's IP 
- Alias Targets
	- ![[Pasted image 20240424100457.png]]

### CNAME vs Alias
- CNAME: 
	- ![[Pasted image 20240424100636.png]]
	- Can't point to Record Names
- Alias:
	- ![[Pasted image 20240424100731.png]]
	- notice the auto TTL
### Routing
 Works differently than load balancing, using types of records (usually A/AAAA) you can specify how to route the traffic to different record names or subdomains.
 - Weighted: 
	 - Based on the instances you have
	 - Set amount of weight an instance is going to have
	 - Change of getting an IP based on that
- Failover: 
	- based on health checks
	- have a parent health check
	- failover to different specified IPs depending on metrics
	- private resources:
		- cloud watch alarm
		- send it to route53