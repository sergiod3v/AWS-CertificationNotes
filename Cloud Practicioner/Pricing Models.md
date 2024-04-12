- Pay as you go
- Save when you reserve
- Pay Less by using more
- Pay less as AWS Grows
### Free Services[https://aws.amazon.com/free/]:
- IAM
- VPC
- Consolidated Billing
- Elastic Beanstalk
- CloudFormation
- Auto Scaling Group
> You obviously have to pay for the underlying resources

### EC2 Pricing
- On demand instances:
	- Minimum of 60s
	- Pay per second (Linux/Windows) or per hour (others)
- Reserved
	- Up to 75% compared to On-demand
	- 1-3 year commitment
	- All up, partial no up
- Spot:
	- Up to 90%
	- Bid for unused capacity
- Dedicated Host
	- On demand
	- Reservation for 1-3 year commitment

### Compute Pricing - Lambda ECS
- Up to 66% discount for this method
- Lambda:
	- per call / duration
- ECS:
	- EC2 Launch type model, no aditional fees, you pay for  aws resources stored and created in your application
- Fargate
	- Fargate Launch Type: Pay for vCPU and memory resources allocated to your applications in your containers

### S3
- Storage Class:
	- Standard
	- IA
	- One-Zone IA
	- Intelligent Tiering
	- Glacier
	- Glacier DA
- Transfer OUT of the S3 Region
### EBS
- Volume Type
- Storage volume in GB/mo provisioned
- Outbound costs
- Inbound doesn't

>_**A lot more details, read docs for specific service costs**_

### Savings Plan
- Budget plan, dont think in specific metrics, only in dollars
- Time of commitment
- Partial, full, no upfront key for price

### Compute Optimizer
- Reduce costs and improve performance based on AWS recommendations
- Recognize over/under - provision services 

### Billing & Costing Tool
- Estimating:
	- Pricing CALACULATOR
- Tracking:
	- Billing Dashboard
	- Cost Allocation Tags
	- Cost & Usage Reports
	- Cost Explorer
- Monitoring gainst costs plans
	- Billing alarms
	- Budgets

# [calculator.aws]

### Tags
- Used to track specific metrics, you can create groups so you can organize what you want to track
- Organize types of service so you can track them correctly
### Cost & Usage Reports - Most granular
- Dive deeper into your AWS costs and usage
- The AWS Cost & Usage Report contains the most comprehensive set of AWS cost and usage data available, including additional metadata  about AWS services, pricing, and reservations (e.g., Amazon EC2
- Reserved Instances (Rls)).
- The AWS Cost & Usage Report lists AWS usage for each service category used by an account and its IAM users in hourly or daily line items, as well as any tags that you have activated for cost allocation purposes.
- Can be integrated with Athena, Redshift or QuickSight
- ==__***Forecast Costs***__==

### Budgets
- Specific metric explorer 
- Alarms for specific cost exceeding
### Cost anomaly detection
- Using ML to monitor your costs and find patterns
- Alarm and action in case of anomaly
### Service Quotas
- Notify when you are about to reach max of service limits
### Trusted Advisor
- Cost Optimization
- Performance
- Security
- Fault Tolerance
- Service Limits
- Operational Excellence
- All these metrics are tracked and analyzed by thisservice so it recommends actions
- ***Business & Enterprise Support Plan***
	- Full set of checks
	- Progrannatic Access using AWS Support API

### Support Plans
- Basic:
	- 24x7 access to customer service
	- Trusted Advisor 7 core checks
	- Personal Health Dashboard
- Developer:
	- Opening tickets to direct Cloud Support Associates
	- Unlimited ammount of cases / 1 primary contact
- Business
	- Production workloads
	- Trusted Advisor - All checks
	- 24x7 phone, email, and chat access to Cloud Support Engineers
	- Unlimited contacts
	- Production system issue max 4h response time
	- Prod. Sys max time down -> 1h
- Enterprise On-ramp
	- Pool of Techincal Account Managers
	- Concierge Support Team (for billing and account best practices)
	- Best Practices review
- Enterprise Full
	- Designated Techincal Account Manager
	- Max of 15minutes when prod sys is down