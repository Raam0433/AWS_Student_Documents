# Auto Scaling

![Auto Scaling](https://user-images.githubusercontent.com/111989928/210201361-cda29938-48a3-4138-8518-3a464bd3b968.png)

AWS Auto Scaling monitors your applications and automatically adjusts capacity to maintain steady, 
predictable performance at the lowest possible cost. Using AWS Auto Scaling, it's easy to setup application scaling for multiple resources across multiple services in minutes.


## Create Servers on Ec2 

1. Httpd web server on ec2
```sh
#!/bin/bash
sudo bash
yum update -y
yum install httpd -y
systemctl enable httpd
systemctl start httpd
```

## Create Auto Scaling

1. Create Security Group with All Traffic 0.0.0.0:0

2. Create Launch Configuration

Name = My-LC

AMI = Copy AMI ID from EC2 (ami-0a606d8395a538502)

Instance type = t2.micro

Security groups = Browse and select existing SG or create new SG

Key Pair = Browse and Select Key Pair

![SL](https://user-images.githubusercontent.com/111989928/210202918-05d7cf98-497c-4336-b122-775e08f9af27.png)



3. Cretae Auto Scaling Groups
Auto Scaling group name = My-ASG
Click on `Switch to launch configuration` and  browse "Ramesh-LC" Launch configuratiopn templete ( created above)

![ASG](https://user-images.githubusercontent.com/111989928/210203030-af0cd6d5-e78b-41d3-94e1-c484ba1191ec.png)

Select all Available zones and cick next 


Group Sizes

Desired capacity = 2
Minimum capacity = 1
Maximum capacity = 4

Save it 
