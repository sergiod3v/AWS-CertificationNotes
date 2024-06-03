### Server-Side Encryption (SSE)
- Using AWS S3 Managed Keys (default)
	- ![[Pasted image 20240426081710.png]]
- Using KMS Keys stored in AWS KMS
	- ![[Pasted image 20240426081821.png]]
	- Each Object read counts as KMS Quota so, be careful
- Customer Provided Key SSE-C
### Encryption
- encryption in flight -> SSL/TLS
- S3 exposes 2 ednpoints
	- HTTP -> not encrypted
	- HTTPS -> encryption in flight
- HTPPS mandatory for SSE-C

#### S3 - Force encryption: Secure Transport 
- Use Bucket Policy to force encryption
- ![[Pasted image 20240426085223.png]]

### S3 Glacier Vault & Object Lock
- Adopt a WORM (Write One Read Many) model
- vault lock policy
- deny deletion of these files so they can never be lost
- versioning must be enabled

### Access Point
- Endpoint for specific prefix -> access policy
### S3 Object Lambda
- u need access points 
- S3 Access point so specify which data
- modify data at time of retrieval using lambda functions
- using S3 Object Lambda Access Point