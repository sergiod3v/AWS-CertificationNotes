## Performance
- Response Time
	- (Waiting Time / Latency)![[Pasted image 20240710123410.png]]
- Throughput
	-   Actions Performed by our system / unit of time
		- Work Performed:
			- tasks / second
		- Data Processed
			- bits, bytes, etc... / second
- Considerations
	- ![[Pasted image 20240710123905.png]]
	- ![[Pasted image 20240710123911.png]]

- ## Response Time Calculation
	- Response time vary, a lot
	- Histogram showing response time data from a server:
		- ![[Pasted image 20240710124142.png]]
		- nth percentiles:
			- Tail Latency
				- part of the graph that takes the longest
			- ![[Pasted image 20240710124308.png]]
	- You can set percentile goals 
	- ### Performance Degradation:
		- Potential overutilized resources
		- ![[Pasted image 20240710124546.png]]

## Scalability
- thankfully very studied b4 xD ilms
## Availability
- ### Calculation:
	- Type 1
		- Availability (%) = Uptime / (Uptime + Downtime)
			- Uptime: time sys is functional
			- Downtime: time sys is unavailable
	- Type 2
		- Availability (%) = _**MTBF**_ / (_**MTBF**_ + _**MTTR**_)
			- _**MTBF**_ (Mean Time Between Failures)
				- avg time sys is operational
				- useful when:
					- multiple pieces of hardware
					- not using CSP/3rd Party services
						- usually come with these metrics
			- _**MTTR**_ (Mean Time To Recovery)
				- avg downtime of our sys
		- IF _**MTTR**_ /DownTime is 0 (almost impossible) 
			- Availability = 1 -> (Availability = 100%)
			- works to understand how important this metric is for availability context
		- More useful for estimation than calculation
	- ![[Pasted image 20240710132723.png]]
- ### Fault Tolerance & High Availability:
	- Failure Types
		- Human Error
		- Software Errors
		- Hardware Failures
	- ### Strategies
		- Failure Prevention
			- Eliminate SPF (Single Point of Failure)
			- Replication and Redundancy
		- Failure detection and Isolation
		- Recovery
		- Redundancy:
			- Types:
				- Spatial 
					- Replicas of our app running on different computers
	- ### Strategies for redundancy and replication
		- Active Active:
			- Requests go to all the replicas at the same time
			- All replicas must be in sync
		- Active Pasive
			- Requests go to a single DB but state of main db is backedup by rest of replicsa 
		- Failure Detection:
			- Monitoring Service
				- heartbeat -> way to check on servers

## SLAs (Service Level Agreements)
- "Legal" Contract that defines all metrics involving quality of service
- Can lead to penalties such as:
- - Full/Partial refunds
- Subscription/License extensions
- Services credits
- ### SLOs (Service Level Objective)
	- Each "promised" metric becomes an SLO
- ### SLIs (Service Level Indicators)

## Metrics
- Think about the metrics that users care about the must
- Define SLOs around those metrics