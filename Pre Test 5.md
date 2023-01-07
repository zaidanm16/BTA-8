# PRE-BOOTCAMP BTECH ACADEMY 

## Challenge

**Run the lab**
```zsh
nusactl start prbt-001-5
```

**Install NGINX**
```zsh
sudo apt install nginx -y
```

**Configure NGINX**
```zsh
sudo nano /etc/nginx/sites-enabled/default
```
```
...
server {
        listen 8090 default_server;
        listen [::]:8090 default_server;
...
        root /var/www/html/lab05;
...
```

**Restart NGINX**
```zsh
sudo service nginx reload
```

**Create Page**
```zsh
sudo mkdir /var/www/html/lab05
sudo nano /var/www/html/lab05/index.html
```
```
...
Hallo pretest adinusa, from zaidanmuhammad169 nginx
...
```

**Configure Firewalld**
```zsh
sudo apt install firewalld -y
sudo firewall-cmd --permanent --zone=public --add-port=8090/tcp
sudo systemctl restart firewalld
```

**Verify**
```zsh
curl localhost:8090
```

**Grade and finish**
```zsh
nusactl grade prbt-001-5
nusactl finish prbt-001-5
```