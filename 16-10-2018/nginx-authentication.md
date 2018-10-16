# Nginx Authentication
In this aticles, we will config a http server with nginx with url /private need login to access.
I use debian 9.

First at all, install nginx
`apt-get install nginx -y`

Nginx config file storage at /etc/nginx/nginx.conf, app config storage at /etc/nginx/sites-available and link to /etc/nginx/sites-enable.
This is default config file (/etc/nginx/sites-avaiable/default)

![alt Image 1](img/1.png)

Additionaly, we need to create user/pass file: username is meomeo and password is meoconxinhxinh
```shell
echo -e "meomeo:`openssl passwd -apr1 meoconxinhxan`" >> /etc/nginx/.htpasswd
```
Password was saved in hash digest

![alt Image 1](img/3.png)

Add private path to nginx config with bacsic authentication

![alt Image 1](img/2.png)

Access to private page

![alt Image 1](img/4.png)

Login and view something

![alt Image 1](img/r.png)
