
Aws lambda can be used to trigger events depending on the services you set whenever you set it to, for example:

You can set a lambda function to trigger when a PUT request is performed to an S3 Bucket to an specific folder.

User Uploads an image to an "input/"-> Lambda triggers img resizing algorithm for the uploaded images to that folder and an output to a "output/" folder 


To handle Public and Private Subnets routing we rely on the route tables inside the vpc

If we have public subnets we want to connect and allow traffic between, we create a route table that allows traffic from everywhere and we attach the public networks we have to that route table, same process would be followed with private subnets and resoruces.

Also, in order to connect those public subnets to the internet, we would bind the public route table we created to the Internet Gateway responsible for accepting that traffic so it can be routed to the desired resources

Security in Subnets is usually handled with ACLs (Access Control Lists)

To control this, in the VPS Service yu goto Security-> Network ACLs and configure which inbound and outbound traffic you want to allow, since the ACLs are Stateless you must configure 

In the next level, Security Groups are always created around an EC2 Instance for, also, Security Groups are Stateful .
The default behavior is allowing all outbound and denying all inbound

There are 2 key factors in the load balancing to use  autoscaling service for EC2 instances, security group so that the load balancer knows exactly what tyo allow and from where, in a normal case for public subnets or access points for the application it will be all the inbound traffic from http & https coming from the vpc (which is also attached to the internet gateway)

Autoscalling groups need launch templates to know which type of ec2 instances should they start when scale is needed, you also want to sync all this with the load baalcner of the application so make sure it is connected to the vpc, target groups, security groups and that the subnets created make sense for that load balancer, after that you bsaically attach everything together
