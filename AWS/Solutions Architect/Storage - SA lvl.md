- ### FSx for windows
	- file systems
	- can be connected onprem -> aws using direct connect
- ### FSx Lustre
	- HPC - High Performance Computing
	- can scale up to 100s GB/s sub-ms latencies
	- Can read S3 as a FUCKING FILE SYSTEM ?????????
- ### FSx Netapp & FSx OpenZFS
	- point in time instantaneous cloning 

### Storage Gateway

![[Pasted image 20240426135017.png]]

### Transfer Family
- if you just wat to use FTP
- Serverless
- pay per provisioned endpoint/h + data transfers in GB
- integrte with auth systems like cognito
- Flavors:
	1. SFTP
	2. FTPS
	3. FTP (for vpc)

### DataSync
- Move larges amounts fo data to sync it
- can sync to:
	- s3
	- efs
	- fsx
- replication tasks can be scheduled
- ==PRESERVES METADATA==
- Bandwidth limit
