# Route53 - 

![Route53](https://user-images.githubusercontent.com/111989928/210214979-4d985455-596c-4e2d-86ff-96feb260a08e.png)


Amazon Route 53 is a highly available and scalable Domain Name System (DNS) web service. 
Route 53 connects user requests to internet applications running on AWS or on-premises.

## 1 Create a Server for Application on EC2

![httpd](https://user-images.githubusercontent.com/111989928/210217060-f0187c36-dd33-4ef8-8015-bb586c9829db.png)



## 2 Create Rout53 hosted zone

Domain name = saikrishna.ga
Type = Public hosted zone and Save

![RT53](https://user-images.githubusercontent.com/111989928/210216304-595ea4fd-670e-4070-99ba-63ea4d29c9ea.png)

Copy name servers and paste on Domain name servers setting

![SND setting](https://user-images.githubusercontent.com/111989928/210216541-47d9b52a-87e8-46c9-bda3-82e96b095472.png)



## 3 Create Record under Route53 hosted zone to link with EC2 server.

Record name = www
Value = "Pubilc IP" of ec2 server - 3.144.45.230
And Save the record.

![A Record](https://user-images.githubusercontent.com/111989928/210217360-41c2fa80-1fa1-4af2-8151-eb344578730a.png)

Wait for 300 seconds to connect DNS with server.

### Result

![Result](https://user-images.githubusercontent.com/111989928/210217600-5378a53a-61bd-40f5-a12b-4a643e192771.png)

