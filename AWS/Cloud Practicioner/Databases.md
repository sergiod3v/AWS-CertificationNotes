## Aurora
- Supports Postgre & My SQL
- AWS Optimized, claims 5x performance over Postgre & My SQL on RDS
- Aurora is not free, it auto grows in increments of 10gb up to 128TB
- Serverless
### RDS
- YOU CAN CREATE A READ REPLICA TO SCALE YOUR READ CAPABILITY, BASED ON THE MAIN db
- Failover DB can be set in other AZ
- A multiregion replica can be set using a read-replica, but it is going to be more expensive because is cross-region
### ElastiCache
- In memory database
- Cache DB like Redis Memcached
- Load off DB for red intensive workloads
### DynamoDB
- Serverless DB
- Fully managed and highly available across 3 AZ
- 100s TB Storage
- low latency retrieval
- Standard IA Table Class
- Key Value
- DAX Accelerator for DynamoDB exclusively, using in-memory cache 10x 
- Low Latency Access across multiple regions using *Global Table* 
- Active - Active R/W in any region
### Redshift
- OLAP analytics and data warehousing
- Load every hour, not every second
- Columnar
- Quick computation with MPP (massive parallel Query Execution)
- Pay as you go based on instances
- SQL interface
- BI tools such as AWS Quicksight or Tableau integrated with
### Elastic MapReduce EMR
- Hadoop Clusters for data analytics
- Takes care of all the provisioning and configurtion
- Autoscaling and integrated with spot instances
- Data processing, machine learning, web indexing, big data...
### Amazon Athena
- Severless query service to perform analytics against S3 Objects
- $5 per TB of data scanned
- BI, Analytics, Reporting, analyze & query VPC Flow Logs, ELB Logs, CloudTrail trails, etc...
- Analyze data using serverless SQL, Athena
### Quicksight
- Serverless machine learning powered BI service to create interactive dashboards
- Integrated with RDS, Aurora, Athena, RedShift, S3
### Document DB
- Mongo DB 
- Replication across 3 AZ
- automatically grows in increments of 10GB
### Neptune
- Graph DB
- usually used for social media 
### Timestream
- Fully managed, fast, scalable, serverless time series database
### Quantum Ledger Database QLDB
- A book recording financial transaction
- Fully Managed, Serverless, High available, Replication across3 AZ
- Review history of all the changes made to your application data overtime
- Immutable system: Noentru can be removed or modified, it is cryptographicaly verifiable
### Amazon Managed Blockchain
- Join public blockchain networks
- Create your own scalable private network
### Glue
- Managed extract, transform and load (ETL) service
- Fully serverless
- Data wrangling
- You can attach services like RDS & S3 to transform the data, load it to Redshift for example and analyze it
- Glue Catalog: of Datasets
DMS 