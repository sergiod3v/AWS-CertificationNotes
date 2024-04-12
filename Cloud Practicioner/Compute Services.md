### ECS
- Launch Docker Containers on AWS
- You mumst provision & mantain the infrastructure (the EC2 instances)
- AWS takes care of starting / stopping containers
- Has integrations with the Application Load Balancer

#UnityImprovements 
### Fargate
- Launch Docker containers on AWS
- Yu dont provision the infrastructure (no EC2 instances to manage) - simpler
- Serverless
- AWS Just runs the containers based on the CPU/RAM you need
### ECR Elastic Container Registry
- Private Docker Registry on AWS
- Store your Docker Images so they can be run by ECS or Fargate
--*ECR Stores the image, Fargate looks at it and creates the container based of that*--
