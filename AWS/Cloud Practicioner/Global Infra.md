### Route53
- Managed DNS 
- DNS is a collection of rules and records wich helps clients understand how to reach a server through URLs
- Receives requests and maps the request to the correct IP from the ==A Record==
### Routing Policies
- Simple routing
- Weighted Routing (sim to alb)
- Latency Policy
- Failover Policy, choose primary & failover so route 53 routes it
### CloudFront
- Content Delivery Network (CDN)
- Improves performance, content cached at the edge
- DDoS protection (worldwide) integration with Shield, WAF
- By caching it at the edge it allows multiple region users to get the content delivered faster
- You can sync it with a S3 bucket in order to expose data and take advantage of CloudFront (give permissons to S3 using policies)
### S3 Transfer Acceleration
- Upload to edge location
- EL transfer through fast private aws connection to an S3 for example
### Global Accelerator
- Content available using edge location
- content fetched from that edge location
- data moved using aws private fast connection
- Uses 2 Anycast IP for the edge locations.
### Outposts
Physical servers to integrate your aws services with your on-prem servers
### Wavelength
- 5G Networks
- Ultra-low latency using edge location as a middleman for Carrier Gateway (wavelength zone) and the User's Cellphone
### LocalZone
- Another Location outside of the AZ but close to it
- Focus on lowest latency possible
- Available only in some regions
- used as an extension of the infrastructure, LZ can be part of the VPC
### Global App Architecture
![[Pasted image 20240409071151.png]]
![[Pasted image 20240409071253.png]]
