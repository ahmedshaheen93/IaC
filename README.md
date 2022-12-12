## Create Stack
```bash
aws cloudformation create-stack --stack-name testIaC --template-body file://VPC-Example.yaml --profile IaC
```
## Create stack with EC2 with passing external parameters
```bash
aws cloudformation create-stack --stack-name IaC-EC2 --template-body file://EC2-Example.yaml  --parameter file://EC2-Examples-Parameters.json --profile IaC
```
- you can replace create-stack by update-stack to update current exist stack with updated info


### Moving forward, we will learn and add an additional option, --capabilities "CAPABILITY_IAM" "CAPABILITY_NAMED_IAM", in these commands as:

```bash
aws cloudformation create-stack --stack-name $1 --template-body file://$2  --parameters file://$3 --capabilities "CAPABILITY_IAM" "CAPABILITY_NAMED_IAM" --region=us-east-1 --profile IaC
```