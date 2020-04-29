# Infrastructure

export AWS_PROFILE=dev/prod

To create cloudformation using sh command which will create Stack, VPC, SUBNETS, RDS, EC2INSTANCE, SECURITY GROUPS

    - parameters
        - STACK NAME
        - AWS region
        - VPC CIDR block
        - Subnets CIDR block
        - VPC name
        - AMIID
        - ACCESS KEYS
        - Domain Name
        - KeyPair value
        

       

To terminate stack along with entire cloudformation

    - sh terminateapplication-stack.sh newStac us-east-1

    - termination command specifies the stack name and region in which the infrastructure should be built

Cloudwatch policies attached to cloudformation

Loadbalancer and autoscaling resources added to the cloudformation infrasturcture.
Attached policies and using jmeter to put load on the application. Application runs through domain instead of ec2 instance.
Added lambda function resources to the cloudformation template along with its roles and policies.
Added certificate to connect to https and have a secured ssl connection.
Encrypted mysql rds instance with ssl.
Created an RDS ParameterGroup and enabled performance_schema to check if the RDS connection is secured
