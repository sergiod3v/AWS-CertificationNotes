### Organizations
- Multiple AWS accounts
- Consolidated Billing, disccount per large usage
- Automate AWS account creation
- SCP (Service Control Policies)
- Multiple separations for ej. Multiple Projects
- Organization Unit (OU)
### SCP
- Restrict or allow IAM actions
- Does not allow anything by default
- Restrict access to certain services
- Enforce PCI compliance by explicitly disabling services
### Consolidated Billing
- Services become sharable between accounts since they all belong to the same organization, optimizing costs and provissioning (reserved instances)

#UnityImprovements 
### Control Tower - Very interesting service
- Automate multi account / organizations setup
- Runs on top of Organizations so it can automatically use it
- Compliance benefits, monitoring 
### Resource Access Manager (RAM)
- Which resources are being used by multiple accounts
### Service Catalog
- Allow/Ban services to maintain order.
- ==Product== ->CloudFormation templates behind the scenes
- Portfolio -> Collection of ==products==
- Pre-configure products to keep consistency on new launched