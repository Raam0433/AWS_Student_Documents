# AWS - Servers Creation


`AWS` - Open `EC2` Instance
1. Create new server With Linux and Connect to server. (Port ranges allowed - 22,80,443,8080,8090)



2. Commands for Installing Web servers

## 1`Httpd Web Server`
```sh
sudo bash
yum update -y
yum install httpd -y
systemctl enable httpd
systemctl start httpd
```

After installation of server in public IP Test page will be displayed.
![Test Page](https://user-images.githubusercontent.com/111989928/209919944-4faea2e4-a87f-4622-b735-43087b0f0fd9.png)

Deploy your application on Web Server
```sh
cd /var/www/html/
vi index.html
```
It will open html page for Edit. 

Add below content to deploy on html page
```sh
<Body background="https://luckmoneymyth.com/wp-content/uploads/2022/03/sai-baba-images-full-hd22-1024x576.jpg">
        <br>
        <br>
</Body>
<!DOCTYPE html>
<html>
<head>
  <meta charset="utf-8">
  <title>SAI TECH</title>
  <style>
    body {
      color: #ffffff;
      background-color: #000000;
      font-family: Arial, sans-serif;
      font-size: 14px;
    }

    h1 {
      font-size: 500%;
      font-weight: normal;
      margin-bottom: 0;
    }

    h2 {
      font-size: 200%;
      font-weight: normal;
      margin-bottom: 0;
    }
  </style>
</head>
<body>
  <div align="center">
    <h1><strong>SAI TECH TRAINING</strong></h1>
    <h2>Welcome to DevOps</h2>
  <p>Call Mr. Ramesh N for enquiries <a href="tel:9902163099"style="color:#0AFFFF"><strong>9902163099</strong></a>.</p>


          <a href="https://sai-tech-training.learnyst.net/"><img src="https://i.ibb.co/k9Kg62B/RAMESH-N.jpg" alt="RAMESH-N" border="0"></a>

  </div>
</body>
</html>
```

## 2 `Nginx Web Server`

Commands for Installation of Nginx Web server
```sh
sudo bash
yum update -y
amazon-linux-extras install nginx1 -y
systemctl enable nginx
systemctl start nginx
```
After successful installation of Nginx "Welcome page will be displayed on public IP"

![NGINX Welcome Page](https://user-images.githubusercontent.com/111989928/209923994-bdfa5e54-a871-4065-8bfb-99f0f25a8f72.png)

Deploy application on nginx html page
```sh
chmod 2775 /usr/share/nginx/html
cd /usr/share/nginx/html
vi index.html
```
Change content with above html code or add new 

Results 

![Nginx - Result](https://user-images.githubusercontent.com/111989928/209925139-936229d6-3be2-4831-b554-f0269a9a0937.png)



Thanks 
