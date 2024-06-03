### Read Replicas 
- Up to 15 replicas
	- Replication is ASYNC (eventually consistent)
- you can then promote a replicated DB to be its own DB
- Use cases:
	- Read Replica for a reporting application so it doesnt load in te main DB
- Network Cost:
	- Same region -> no cost in data transfer
### Multi AZ
- SYNC replication
- One DNS name, automatic failover
- ==Read Replicas can be setup as MultiAZ for Disaster Recovery==
### Single -> Multi AZ
- Zero downtime
- Just click Modify
	1. Snapshot taken
	2. new DB restored from that snapshot
	3. SYNC is allowed 
- SQL Electron great 2 access rdsdb using its dns name

### RDS Custom
- Oracle & MySQL Server
	- OS & DB customization
- RDS automates setup
- u can access underlying instances using SSH or SSM Session Manager !!!


### Aurora
- Up to 128TB
- Up to 15 replicas
- Faster replica - 10ms replica lag
- Instant failover - HA native
- 20% more cost over RDS
- #### High Availability
	- 6 copies of your data across 3AZ
	- Storage striped across 100s volumes
	- 1 Master DB to write on (dns name on it)
	- ##### _**R/W ENDPOINTS**_ 
		- ![[Pasted image 20240423140233.png]]
- #### Disaster Recovery
	- Automatic Failover
	- Automated Patching with Zero Downtime
	- Backtrack: restore data aat any point of time without using backups
- #### Advanced
	- Custom endpoint
	- Define Aurora subset
	- Instances can hace different sizes
	- Distribute workload depending on sizes
	- #### Serverless
		- autoscaling based on usage
			- ![[Pasted image 20240423153034.png]]
	- Aurora Global Database (recommended)
		- 1 Primary region (r/w)
		- Up to 5 read-only _**regions**_ replication
		- Up to 16 Read Replicas per _**region**_
		- rep time<5s -> Aurora


### RDS / Aurora -Backups
- Daily full backup
- Tx logs are autobacked up by rds
- Aurora DB cloning 
	- faster than snapshot & restore

### Security
- Ecryption using KMS
- !master.encrypted -> !readReplicas.encrypted
- to encrypt -> DBsnapshot ->restore from encrypted
- Inflight Encyption -> TLS ready by def, AWS TLS root certificates
- IAM -> IAM Roles to connect to ur db
- Security Groups to control access
### RDS Proxy
- More failover protection
- Minimize open connections
- improve db efficiency
- Supports RDS and Aurora
- Enfoce IAM Auth -> Store credentials in Secrets Manager
