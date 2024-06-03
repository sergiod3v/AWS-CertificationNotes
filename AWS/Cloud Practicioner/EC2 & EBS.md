EC2 - IaaS

The first letter determines which is the scope for resource selection for the instances.

EBS Snapshots is a way to migrate EBS data from AZ -> AZ

### AMI - Amazon Machine Image
Is a way to replicate an ec2 instance with specific configurations, this also enables ec2 image replication across different az's


## EC2 Image Builder
Automate the creation of VMs pr Container Images
## EC2 Instance Store (i3)
Works like a RAM, terminate/stop instance will delete data in this instance

## EFS Elastic File System
Shared network file system 
Works only on linux
pay per use, no capacity planning
Multi AZs
This will require a Launch Template that will determine what type of instances will be deployed, this can be synced with Image Builder in order to optimized the images of the instances deployed
