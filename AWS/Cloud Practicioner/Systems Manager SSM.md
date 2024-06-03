- Helps you manage your EC2 and On-Premises systems at scale 
- Hybrid
- Operational insights about infra
- Features:
	- Patching automation
	- Run commands across an entire fleet of servers
	- Store parameter configuration
- Works for Linux, Windows, MacOS & RaspberryPi OS
- You only need to install the SSM Agent to manage that Instance

#UnityImprovements
### Session Manager 
- You can create a SSH access to your instances without the need to use .pem, .ppk -> No port 22 needed ( better security)
- Send session log data to S3 or CloudWatch Logs
- SSM -> Fleet Manager, manage all the EC2 Instances that have Session Manager active
- ==**IMPORTANT** -> Enable SSMManagedInstnceCore permission for the EC2 Instance that you want to access==

#UnityImprovements
### Parameter Store
- Secure strage for configuration and secrets
- API Keys, passwords, configurations
- Serverless, scalable, durable, easy SDK
- Controll access using ==*IAM*==  