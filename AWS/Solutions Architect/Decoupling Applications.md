### SQS
- Producer sends messages
- Consumers poll them
- Buffer to decouple
- #### Standard Queue
	- Unlimited throughput
	- No limit on messages in queue
	- default retention of 4 days (up to 14)
	- <256KB per message
	- CAN have duplicate messages
	- Up to 10 messages per consumer
- CloudWatch Metric from SQS -> CloudWatch Alarm for ASG
- 30s Message Visibility Timeout
	- becomes insivible while being processed
	- can be changed using ChangeMessageVisibility
### SNS
![[Pasted image 20240502103051.png]]

### Kinesis
- Provide shards to define capacity
- Producers send data to kinesis, can be aws resources
- Consumers
	- Apps (KCL, SDK)
	- Lambda
	- Kinesis Data Firehose
	- Kinesis Data Analytics
- record 
	- part key
	- data blob

### Kinesis Data Stream
- data inserted -> can't be deleted (immutability)
- retention up to 1 year
- Consumers:
	- Write your own: Kinesis Client Library(KCL), AWS SDK
	- Managed: Lambda, Firehose DataAnalytics

### Firehose
![[Pasted image 20240505082722.png]]