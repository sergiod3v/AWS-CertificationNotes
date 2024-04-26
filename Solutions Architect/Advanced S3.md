#### Lifecycle
- S3 analytics recommends tiers depending on the history of the bucket
- DOES NOT work for OneZone IA or Glacier

#### Requester Pays
- literally what it sounds it is
- requester has to be auth in aws
#### Event Notifications
- Infinite n events 
- can be send to s3, sns, sqs, lambda function 
	- Resource Polciy instead of IAM permissions
- S3 Event can be sent to EventBridge and directly send it to over 18 services
### Batch
- S3 Inventory -> S3 Select (FilteredList) ->  -> S3 Batch Operations -> Processed Objects
### Storage Lens
 Metrics for your objects
 Paid version has very specific metrics
