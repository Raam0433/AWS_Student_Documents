# Jenkins installation on Linux Server

```sh
#!/bin/bash
wget -O /etc/yum.repos.d/jenkins.repo \
    https://pkg.jenkins.io/redhat-stable/jenkins.repo
rpm --import https://pkg.jenkins.io/redhat-stable/jenkins.io.key
yum upgrade
amazon-linux-extras install java-openjdk11 -y
yum install jenkins -y
systemctl enable jenkins
systemctl start jenkins
yum install git -y
```
Open New tab and paste Public IP :8080 Port (please allow security group for 8080 @ ec2)

Open Page will ask Admin Password 

Connect server and run below command to get Admin Password 

```sh
cat /var/lib/jenkins/secrets/initialAdminPassword
```


![Pass](https://user-images.githubusercontent.com/111989928/210799434-90a6f8bc-7bca-4720-8d45-90f3aeb7083e.png)

Use the above copied Admin password on Jenkins Open page

Go with Suggested plugins and register with  user details 

![Jenkins_App](https://user-images.githubusercontent.com/111989928/210799810-6d4952da-ea98-4f5d-84bd-35b0b6627340.png)


