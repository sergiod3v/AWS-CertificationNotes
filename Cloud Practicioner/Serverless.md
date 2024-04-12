Basically when you dont have to manage servers and you just have the usage of the tool there.
Something like Lambda
Such as
- S3
- DynamoDB
- Fargate
- Lambda
### Lambda
- FaaS Function as a Service
- Free -> 1M AWS Lambda Requests and 400.000GBs of compute time
- up to 10GB of RAM
- Can run Multiple Languages
- Autoscaling, serverless perk
### API Gateway
- Serverless API
![[Pasted image 20240408110842.png]]

### Batch 
- Full managed batch processing for any scale
- Dynamically launches EC2 Instances or Spot Instances
- right amount of compute/memory
- Submit or Schedule the Job and will run automatically
- Batch jobs are Docker images and run on ECS
- ![[Pasted image 20240408111534.png]]
- vs Lambda
	- Lambda
		1. Time Limit
		2. Limited runtimes
		3. Limited temporary disk space
		4. Serverless
	- Batch
		1. No time limit
		2. Any runtime as long as it's packaged as a Docker Image
		3. Rely on EBS / instacnce store for disk space

### Lightsail
- Basically a incredible simplfied version to use AWS with a very simple architecture and don't know much of AWS

