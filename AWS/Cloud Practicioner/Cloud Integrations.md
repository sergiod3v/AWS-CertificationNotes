### SQS
- Producer (sends) Consumer (pulls) messages
- Serverless, decouple applications
- max 14 days
- Consumers share the work and scale horizontally
- Decoupling Example
	- ![[Pasted image 20240409072114.png]]
	- ide Processing layer scales independently thanks to SQS, each leayer's functionality segregated from the other
- FiFo

### Kinesis
- real-time big data streaming
- ![[Pasted image 20240409072606.png]]

### SNS
- Publish messages to sbscribers ofthe topic, this can either be sending an email, returning something for a server or directly to SQS
- mailinator (temporary mail) <- not related, just note in case of tests
### Amazon MQ
- Like RDS but for Qeue services
- RabbitMQ ActiveMQ message broker service
- dont re-engineer your queue/notificaition service