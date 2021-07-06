# Nginx Template

- Launch the Amzon EC2
- Connect the instance with SSH

## Installing and Configuring NGINX Web Server to Run
- Update the installed packages
```
	- sudo yum update -y
	- sudo amazon-linux-extras install nginx1.12
	- sudo systemctl start nginx
```
- Check from browser with public IP/DNS
- Show content of folder
```
	- sudo chmod -R 777 /usr/share/nginx/html
	- sudo rm index.html
```
- Upload new `index.html` and `ryu.jpg` files with `wget`

```
wget https://raw.githubusercontent.com/awsdevopsteam/ngniex/master/index.html
wget https://raw.githubusercontent.com/awsdevopsteam/ngniex/master/ryu.jpg
```
## Restart the Nginx Web Server
```
 sudo systemctl restart nginx
```
## Enable Nginx
```
sudo systemctl enable nginx
```
## Add another `index.html`
```
echo "Second Page" > /usr/share/nginx/html/index_2.html
```
## `add "/index_2.html" at the end of the the public DNS `

## Automation of Web Server Installation through Bash Script (User data)
- Configure instance to automate web server installation with `user data` script.
```
#! /bin/bash

yum update -y
amazon-linux-extras install nginx1.12
systemctl start nginx
cd /usr/share/nginx/html
chmod -R 777 /usr/share/nginx/html
rm index.html
wget https://raw.githubusercontent.com/awsdevopsteam/ngniex/master/index.html
wget https://raw.githubusercontent.com/awsdevopsteam/ngniex/master/ryu.jpg
systemctl restart nginx
systemctl enable nginx
```
