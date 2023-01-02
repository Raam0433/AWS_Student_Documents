# Load Balancer

![LB](https://user-images.githubusercontent.com/111989928/210196977-950e0707-64ee-470a-8499-d89e7bca7d73.png)




Image result for Load Balancer
A load balancer serves as the single point of contact for clients. 
The load balancer distributes incoming application traffic across multiple targets, such as EC2 instances, 
in multiple Availability Zones. This increases the availability of your application. 
You add one or more listeners to your load balancer.


## Create Servers

1. Create 2 or more ec2 Instances & install nginx/httpd web server

```sh
#!/bin/bash
sudo bash
yum update -y
amazon-linux-extras install nginx1 -y
systemctl enable nginx
systemctl start nginx
```
Edit webpage
```sh
chmod 2775 /usr/share/nginx/html
cd /usr/share/nginx/html
vi index.html
```

![Nginx-Webpage](https://user-images.githubusercontent.com/111989928/210197825-6c159e94-41cf-4745-8883-7b8127e2bbcf.png)


## Create Load Balancer

Go to AWS - `Load Balancing` and Click on `Target Groups`
1. Create LB Group

Choose a target type = Instances
Target group name = My-LBG
Click Save and Select servers which created above, Add selected server to below by clicking "Include as Pending Below" and Save Target Group.

![Target Grp](https://user-images.githubusercontent.com/111989928/210198040-f672e58e-0829-40fe-9e40-4da633b99097.png)

2. Create Load Balancer

Create Load Balancer with "Application Load Balancer"

Name = My-ELB
Select all Available zones
Create New Security group or Browse Existing Security Group 
Listeners and routing = Default action = Browse Target group name 
Save the page and it will create DNS for load balancing. 

![ELB](https://user-images.githubusercontent.com/111989928/210198605-0fa0edb5-1b32-4f88-a64f-9a94bc93664c.png)


## Result : - 

![Results](https://user-images.githubusercontent.com/111989928/210198579-600057a1-0761-4fdb-a214-0ce2cd429bea.png)




