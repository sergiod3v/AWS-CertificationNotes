Multiple AZ
There are 3 types of Load Balancers:
- Application Load Balancer - ALB Layer 7
	- It only handles HTTP/HTTPS/gRPC protocols
	- HTTP routing features
	- Static DNS (URL) - no dynamic IP
	- Usually used to distribute load between EC2 instances
- Network Load Balancer - NLB Layer 4
	- TCP/UDP Protocols 
	- High Performance
	- Static IP (using Elastic IP)
- Gateway Load Balancer - GLB Layer 3
	- GENEVE Protocol on IP Packets
	- *Route Traffic to Firewalls* that you manage on EC2 Instances
	- Intrusion Detection

Target Group refers to the selected EC2 Instances in which the load its going to be distributed in


# ASG

Consists of 3 variables:
- Minimum Size
- Desired Capacity
- Maximum Capacity

Automatic deployment of multiple EC2 Instances depending on traffic
