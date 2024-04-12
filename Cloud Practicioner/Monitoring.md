### CloudWatch
- Monitor every service
- Billing metric (us-east-1)
- Detailed monitoring (expensive)
- Alarms for almost every part of every service for a notification service to monitor
### CloudWatch Logs
- a stream of logs is created depending on the events inside of the targeted services
### CloudWatch Events - EventBridge
- Serverless event reaction
- Cron jobs
- Similar to Lambda in event reaction
- Receive events from 3rd party services using Partner Event Bus
- Custom Event Bus 
- You can use ***event bridge*** scheduler job to triger a lambda function that does specific job every x time
- Specific functions triggered based on specific services events 
### CloudTrail
- Enable by default
- ==API calls== history in your AWS acc
- Export to S3 and audit them there
### X-RAY
- Deep Debugging in production
- Trace and debug Monolith & Microservices
- UI Interface to aanalyze microservices metrics
- Understand dependencies
- Requests behavior
- Are we meeting SLA server level agreement
### CodeGuru
- ML powered for automated code reviews
- Can be added to pipeline when building, testing and deploying the app
- Recommendation for in-production apps as well
### Health Dashboard
- All regions, all services health