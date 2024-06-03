##### **Security groups**
Locked down to a region/VPC combination
Lives outside of the EC2
Timeout->security group issue
Error-> application error/not launched

All inboud is **Blocked**
All outboud is **Allowed**

Security group great feature is the fact that you can allow multiple ec2 instances to communicate with eachother using only groups, no need to specify all the IPs

22 -> SSH secure shell
21 -> FTP file transfer
22 -> SFTP safe file transfer
80 -> HTTP 
443 -> https
3389 -> rdp remote desktop protocol log into windows instance

IAM Roles are very useful for ec2 beacause you can access aws resources from the cli without having to configure the instance with your private ey. 