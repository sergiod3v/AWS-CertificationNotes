### DDoS Protection: WAF & Shield
- ***Shield***:
	1. Standard: Protects against DDOS attack for your website and applications, for all customers at ==no additional costs==
	2. Advanced: 24/7 premium DDoS protection $3000/month/org
- WAF: filter specific requests based on rules
- ![[Pasted image 20240410113535.png]]
- WAF: Layer 7 (HTTPS) common web exploits protection
- Deploy WAF on ALB API GW, CloudFront
- WEB ACL
### Network Firewall
-  Layer 3-7 protection
- VPC to VPC traffic
- Outbound to internet
- Inbound from internet
- To / from Direct Connect & Site-
- to-Site VPN
- ![[Pasted image 20240410114619.png]]


### Firewall Manager
- Manage security rules in all accounts of an AWS Organization
- ***Security Policy***:
	1. VPC Security Groups for EC2, ALB, etc...
	2. WAF Rules
	3. Shield Advanced
	4. Network Firewall
> _**Rules are applied to new resources as they are created**_

### Penetration Testing
- Without prior approval:
	1. EC2
	2. RDS
	3. CloudFront
	4. Aurora
	5. API GW
	6. Lambda & Lambda Edge
	7. Lightsail
	8. Elastic Beanstalk envs
- ❌ DNS Zone Walking using Route53 Hosted Zones
- ❌ DoS, DDoS, simulated DoS, simulated DDoS
- ❌Port flooding
- ❌ Protocol Flooding
- ❌ Request Flooding

## Encryption
- 2 states, rest & transit
- Using encryption keys
- ### KMS
	- Manages ecryption keys for us
	- _Opt In_:
		- EBS, encrypt volumes
		- S3: Serverside encryption for objects
		- Redshift: data
		- RDS: data
		- EFS: data
	- Automatically
		- CloudTrail Logs
		- S3 Glacier
		- Storage Gateway
- ### CloudHSM
	- Hardware
	- Level 3 Compliance
- ### KMS
	- *Types*:
		- Customer Managed -> possible rotation policy, bring your own key _==***NOT FREE***==_  
		- AWS Managed -> created, managed and used on the cust behalf
		- Owned Key -> Collection of CMKs to use in multiple accounts
		- CloudHSM -> generated from the hardware device
- ### ACM - Certificate Manager
	- provission. manage & deploy SSL/TLS Certificates
	- In-flight encryption for websites HTTPS
	- Auto TLS renewal
- ### Secrets Manager
	- Sort of ENV variables
	- encryption done with KMS
	- Possible forced automatic rotation of secrets using Lambda
- ### Artifact
	- Compliance needs
	- View reports and agreements 
	- Both Organizations and Agreements
- ### GuardDuty
	- Inteligent threat discovery for multiple services
	- Very good for CryptoCurrency attacks, special method for it
	- Eventbridge rules can be automated in case of findings, shutting down an instance for example
	
> _***Since it is ann Inteligent detection system, it receives inputs such as VPC Flow Logs, CloudTrail Logs, DNS Logs (by default). You can also choose S3 Logs, EBS Volumes Logs, Lambda Network Activity, RDS & Aurora Login Activity, EKS Audit Logs & Runtime Monitoring, in order to refine the software to your specific achitecture

#UnityImprovements 
- ### Inspector
	- Automated Security Assessments
	- For things like network accessibility, known vulnerabilities, threats in lambda code & package dependencies
	- _***Exclusive***_ for EC2 instances, Container Images & Lambda functions
	- Report Integration with AWS Security Hub
	- You can send findings to eventbridge to perform respective actions
- ### Config
	- Record of all the configurations to track changes
	- Receieve alerts if changes made
	- CloudTrail API calls to track specific activity 
	- Analyzes things like Unrestricted Access trough port 22 (SSH unfiltered access enabled ) and point all these problems to the exact resource
	- Summarize the threats or non-compliance configurations so they are easy to detect
- ### Macie
	- Serverless discovering of unprotected data using ML
	- Identifies PPI Personally Identifiable Information
- ### Security Hub
	- Enabling Config is necessary 
	- Unified center of security tools such as:
		1.  Config
		2. GuardDuty
		3. Inspector
		4. Macie
		5. IAM Access Analyzer
		6. Systems Manager
		7. Firewall Manager
		8. Health
		9. Partner Network Solutions
- ### Detective
	- Getting to the root cause of the security issues found on other Security Tools like Macie, GuarDuty, etc...
- Root User permissions
	- Change acc settings
	- Close acc
	- Restore IAM user permissions
	- Change support plan
	- configure S3 to enable MFA
	- GovCloud
- ### IAM Access Analyzer
	- Know if recources are being accessed outside of the zone of Trust (Account or Organization)
	- Know if services have general access (public for everyone inside of account/organization)