# SNS - Simple Notification Service

![SNS](https://user-images.githubusercontent.com/111989928/210209650-5a7de758-49c9-4a8a-9bba-3661e17aa47e.png)


Amazon `Simple Notification Service` is a web service that makes it easy to set up, operate, and send notifications from the cloud.

## 1. Create `S3 Bucket`


## 2. Create `SNS` 

Type = Standard
Name = Devops-SNS

Access Policy = Select "Everyone for both options" and Save the topic creation.

### Create Subcription

Select Protocol = Email and SMS
add mail id and contect number and submit confirmation OTP.

![Sub](https://user-images.githubusercontent.com/111989928/210212717-969a5b9b-3b85-4ec3-8239-a511551e05ca.png)

![sub list](https://user-images.githubusercontent.com/111989928/210212988-6990e466-8197-4532-a30b-e5be05520836.png)



## 3 Create Event

Go to AWS - S3 bucket's "Properties" to create "Event notifications".

Name = my-s3-sns
Click on Event types for required services.
Destination = SNS Topic
Specify SNS topic = Devops-SNS


add or Delete files from S3 bucket you will get notification to registered mobile and mail.

### Result


![Mail](https://user-images.githubusercontent.com/111989928/210213649-069c2e3a-4453-4409-87eb-de73b6734c29.png)

