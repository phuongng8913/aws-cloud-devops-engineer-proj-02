# Udacity AWS Devops - Project 02 - PhuongNTM18

Deploy a high-availability web app using CloudFormation

## Resources

1. [Diagram](diagram.png)
2. [Infra template](infra.yml)
3. [Infra parameters](infra-parameters.json)
4. [Servers template](servers.yml)
5. [Servers parameters](servers-parameters.json)
6. [Web app](web-app)

## Scripts

```bash
# Create infra stack
aws cloudformation create-stack --region=us-east-1 --stack-name phuongntm18-project02-infra --template-body file://infra.yml --parameters file://infra-parameters.json

# Create servers stack
aws cloudformation create-stack --region=us-east-1 --stack-name phuongntm18-project02-servers --template-body file://servers.yml --parameters file://servers-parameters.json

# Update infra stack
aws cloudformation update-stack --region=us-east-1 --stack-name phuongntm18-project02-infra --template-body file://infra.yml --parameters file://infra-parameters.json

# Update servers stack
aws cloudformation update-stack --region=us-east-1 --stack-name phuongntm18-project02-servers --template-body file://servers.yml --parameters file://servers-parameters.json

# Delete infra stack
aws cloudformation delete-stack --region=us-east-1 --stack-name phuongntm18-project02-infra --template-body file://infra.yml --parameters file://infra-parameters.json

# Delete servers stack
aws cloudformation delete-stack --region=us-east-1 --stack-name phuongntm18-project02-servers --template-body file://servers.yml --parameters file://servers-parameters.json
```
