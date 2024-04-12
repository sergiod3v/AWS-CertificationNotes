
1. **Amazon EC2 (Elastic Compute Cloud):**
    - EC2 is a web service that provides resizable compute capacity in the cloud. It allows users to rent virtual machines (instances) and run applications on them. EC2 instances can be configured based on different types, sizes, and operating systems to meet varying computing requirements.
2. **Elastic Load Balancing (ELB):**
    - ELB automatically distributes incoming application traffic across multiple targets (such as EC2 instances, containers, IP addresses) to ensure that no single instance becomes overwhelmed. It enhances the availability and fault tolerance of applications by balancing the load efficiently.
3. **Amazon SQS (Simple Queue Service):**
    - SQS is a fully managed message queuing service that enables decoupling and scaling of microservices, distributed systems, and serverless applications. It allows messages to be sent between different components of an application without requiring them to be directly connected.
4. **Amazon SNS (Simple Notification Service):**
    - SNS is a fully managed pub/sub messaging service that enables the sending of notifications and messages to a variety of endpoints or subscribers. It supports multiple communication protocols, such as HTTP, HTTPS, email, SMS, SQS, Lambda, and more.
5. **AWS Lambda:**
    - Lambda is a serverless computing service that allows users to run code in response to events without managing server infrastructure. It enables you to execute code in a scalable and cost-effective manner, where you only pay for the compute time consumed by the code.


Amazon Beanstalk & Amazon Cloud Formation: Save environment and architecture configurations so it can be launched again easily

For managing the traffic that enters your subnet you use an Internet Gateway 

For security management when receiving a package there are two types of security layers:
- Security Group: StateFUL -> has memory
- Network ACL: StateLESS -> doesn't have memory

Route 53: Amazon DNS  
Amazon CloudFront: Amazon CDN

We have 2 main options for storage, EBS & S3

S3 treats every record of the db as an object (each one up to 5tb) and every time this object is changed, the complete record is re-uploaded which makes it not a great deal for things like video editing for example, where you are going to constantly update a single file but only one portion of it will be really updated.

ECB (elastic block store) in the other hand, has a block-type storage, it breaks every stored record into smaller blocks so when a change occurs you only retrieve/read/update the desired part that was modified, not the entire record. Also, one key attribute of this service is that it can be attached to an EC2 instance so the data lives tightly coupled to the instance, or virtually attached to it so it does not die when the instance does.
(ECB & EC2 need to be in the same Availability Zone)

Amazon EFS (Elastic File System) is similar to ECB because you can attach it to an EC2 instance, but with EFS it can be many EC2 instances. Also, there is no strict need for the EC2 and the EFS to be in the same AZ, as long as it is in the same region. Which means it is available in  multiple Availability Zones and many EC2 instances, it is like a big HDD

Amazon RDS & Aurora
RDS supports various database engines like MySQL, PostgreSQL, MariaDB, Oracle, and SQL Server, offering managed instances with traditional storage and replication methods. On the other hand, Aurora, designed by AWS, is a MySQL and PostgreSQL-compatible database engine that employs a cluster-based storage architecture, replicating data across multiple Availability Zones for higher performance and fault tolerance. Aurora outperforms RDS in scalability, offering up to 15 read replicas with minimal performance impact, while RDS provides compatibility with multiple database engines at potentially lower costs but with less scalability in demanding workloads. The choice between RDS and Aurora hinges on performance needs, scalability, fault tolerance, and compatibility requirements with existing systems. Aurora is generally favored for high-performance, demanding applications, while RDS might be more appropriate for simpler use cases or compatibility with specific database engines.

Amazon RedShit (Data Warehouse as a Service)
You basically are able to run queries across Hexabytes of information of non related data, it is an aplication for Busines Inteligence because you cn enter in the field of data lakes without losing performance or efectiveness when looking for specific data.

Amazon DMS (Data Migration Service): Incase you have the data secured in an On Premises Datacenter you can Use Amazon Data Migration Service DMS you casn also use it to make a copy of the db in order to test functionalities using production data. You can also consolidate multiple databases in one single db.

The statement that best describes IAM Service is: Document that rgants or denies permissions to AWS services and resources.

If an employee needes temporary access to create several Amazon S3 Buckets the best option would be an IAM Role, since rules from the role can be applied to multiple accounts.

The least privilege means giving just enough permissions to an user to perform the desired task, nothing else. 

The best service to protect your application from DDoS atacks is AWS Shield since it can individually scan network activity for your individual AWS Services you attach it to.

Amazon KMS is used to manage the encryption keys for your AWS services and resources.

Amazon CloudWatch helps you keep track of metrics related to your AWS resources, using a Amazon CloudWatch Alarm, you can use an SMS to notify users if a metric is completed.

Amazon CloudTrail Allows you to audit and record every movement any of your services presents, which then can be stored in an S3 buckets so then other services can analize to determine if your cloud resources  behavior make sense. CloudTrail Insights is a feature that can detect unusual API activities in your resources

Amazon Trusted Advisor runs checks in every core concept for a sustainable AWS project
- Cost optimization
- Performance
- Security
- Fault Tolerance
- Service Limits

Amazon support TAM will analyze the key factors or, Six pillars of the Weill Architected Framework:
- Operational Excellence
- Security
- Reliability
- Performance Efficiency
- Cost Optimization
- Sustainability

Amazon CAF (Cloud Adoption Framework): Specific services to migrate on premises to cloud. Having tools like AWS CAF Action Plan to help you guide your organization.






