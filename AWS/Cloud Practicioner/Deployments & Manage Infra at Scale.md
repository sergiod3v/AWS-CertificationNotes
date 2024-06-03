### Cloud Formation
- Declarative way of utlining your AWS
- You say what you want to have in your infra and CloudFormation creates it for you in the correct order
- Infrastructure as Code IaaC 
- Easily estimate costs using CloudFormation template
- Scheduling of dletion of templates & services
- Automated generation of Diagram of your templates!
- Yaml script that defines all the services to use + the regions and required IDs 
- Complex template example: 
	- ![[Pasted image 20240408115229.png]]

### Cloud Development Kit (CDK)
- CloudFormation but with known languages, not YAML
- Use known languages to create a template that is then translated into a CF Template

### Beanstalk
- Launch template for specific languages to launch a complete environment for an specific usage
- CloudFormation template usage behind the scenes
- its like CDK + CF
- Environment lives inside of an Application on ElasticBeanstalk

### CodeDeploy
- Auto deploy
- Works to EC2
- Works on premises
- Hybrid Service
### CodeCommit
- Github competing product
### Code Build
- Build code, run tests, highly available and automatic
### Code Pipeline Orchestration Layer
- A complete pipeline that can be integrated with different 3rd party platforms 
### Code Artifact
- Dependencies repository that can interact with code build to create a complete code build process

#UnityImprovements 
### Code Star
- Unified UI to manage all above services, Deploy, Commit, Build, Pipeline, Artifact
### Cloud9
- IDE in AWS