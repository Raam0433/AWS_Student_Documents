# VPC - Virtual Private Cloud

![VPC](https://user-images.githubusercontent.com/111989928/210042161-9fe587d5-4a0a-46a6-9a9d-f813b9975a46.png)




A `Virtual Private Cloud` is a secure, isolated private cloud hosted within a public cloud. 
VPC customers can run code, store data, host websites, and do anything else they could do in an ordinary private cloud, 
but the private cloud is hosted remotely by a public cloud provider.


## VPC Creation

Open AWS - "Networking and Content Delivery" Category and Open "VPC" service

1. Click on Create VPC
2. Resources to create = `VPC Only`
3. Name = `My-VPC`
4. IPv4 CIDR = `10.10.0.0/16` Save and Create
After saved click on "Actions" > Edit VPC Setting > Enable "DND Hostnames"

## Subnets
1. Create Subnets
2. Browse subnet ID > "My-VPC"
3. Name = `App-subnet`
4. Availability Zone = `us-east-2a`
5. IPv4 CIDR block = `10.10.1.0/24`

Add one more subnet 

1. Name = `DB-subnet`
2. Availability Zone = `us-east-2b`
3. IPv4 CIDR block = `10.10.2.0/24`
After creation select the VPC and go to Actins select "Edit subnet setting" 

![Subnet](https://user-images.githubusercontent.com/111989928/210043617-bcd9a7dd-6cd2-4195-9f50-9fee33ceae75.png)




## Internet Gateway
1. Create IGW
2. Name = My-IGW and go for creation after create Click on Action for "Atatch VPC"


## Route Table
1. Create route table
2. Name = My-RT
3. Browse VPC
After creation go to Edit routes n 
 
Dest = 0.0.0.0/0
Target = Inteenet gateway (MY-IGW browse and select)

![IGW](https://user-images.githubusercontent.com/111989928/210044209-14bd9d9a-f51b-4f03-8095-30192ac0790c.png)


Edit subnet associations Select both subnets App-subnet & Db-subnet and save it

Go for EC2 Instances creation and browse My-VPC whle creating.


