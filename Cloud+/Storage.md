## Network Attached Storage (NAS)
- Provide access to storage using varying protocols
	- SMB
	- NFS
	- HTTP/HTTPS
	- FTP
		- No encryption
	- SFTP
		- SSH Tunnel
	- FTPS
		- SSL or TLS encryption
>S-FTP: SSH Tunnel
>FTP-S: SSL or TLS encryption
>if the "S" is before is SSH Tunnel
>if the "S" is *after* is SSL/TLS encryption

## Direct Attached Storage (DAS)
- Storage attached directly to computers

##  Storage Area Network (SAN)
- A network providing shared storage 
- Common protocols include fibre channel and iSCSI
- Locally, required a hardware host-bus adapter 
	- Like a "network card"
	- if not using IP-SAN
- _**Provides block level storage**_ 
## SMB (hopefully 3.x)
- Server-Client
- mostly windows
## NFS (etwork File System)
- Usually Unix/Linux
- Based on RPC (Remote Procedure Calls) 
