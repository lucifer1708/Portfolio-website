+++
author = "Sumit Dhiman"
title = "Setting up a simple webserver using Nginx"
date = "2023-02-14"
description = "This article helps you in setting up a simple HTML website on a webserver using nginx reverse proxy."
tags = [
   "Hosting",
   "Web Server",
   "Nginx",
]
categories = [
    "Coding",
    "syntax",
]
+++

## First Step:
First of all, we need to access our server's shell. So, we will use SSH to do so. 
type following command in your local computer's terminal:
```bash
ssh <username>@<ip-addresss>
```
then, enter your password if you havn't added your ssh key on the remote server.

## Second Step:
Now , we will be installing our requirements:
```sh
# apt install nginx vim
```
Following command will start the nginx daemon in background and set the service to autostart.
```sh
# systemctl enable --now nginx
```

## Third Step:
create a file as follows:
```sh
# vim /etc/nginx/sites-available/mywebsite
```
You can change `mywebsite` to any thing you want.

Add following content in your file.
```sh
server {
        listen 80 ;
        listen [::]:80 ;
        server_name example.org ;
        root /var/www/mywebsite;
        index index.html index.htm index.nginx-debian.html ;
        location / {
                try_files $uri $uri/ =404 ;
        }
}
```

Now, we have to add our HTML.
Create a index.html file using below command:
```sh
# mkdir /var/www/mywebsite
# vim /var/www/mywebsite/index.html
```
Add following html syntax in it.
```html
<h1>Your website is running</h1>
```
## Final step:
Run below command to enable your site config:
```sh
# ln -s /etc/nginx/sites-available/mywebsite /etc/nginx/sites-enabled
```
Now, reload the nginx daemon using below command:
```sh
# systemctl restart nginx
```

### Now, visit your the url as `http://<ip-addresss>`. And, you will see your website running.



