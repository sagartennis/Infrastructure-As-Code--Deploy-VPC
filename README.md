# Infrastructure-As-Code--Deploy-VPC
The Script is written in YML format. The Infrastructure As a Code tool used for deploying this script is ***AWS CloudFormation***. 

### STEP 1 ###

Under resources section, make sure to name your VPC. Then in the type syntax, add **AWS::EC2::VPC** to deploy a VPC. 

### STEP 2 ###

Under the properties syntax, assing the ** cidrBlock** value to 10.0.0.0/16
CIDR (Classless Inter-Domain Routing) is a range of IPV4 addresses. They all must reside in the same Availability Zones [AZ]

### STEP 3 ###

Use the following commoand to run the IAC script to deploy actual infrastructure. 
```
 aws cloudformation create-stack --stack-name vpc --region us-west-2 --template-body file://createVPC.yml
```
Make sure you are in the same directory as the script is saved in the CMD console. 

### STEP 4 ###

Make sure the VPC is created by viewing it in the AWS Console. 

