# PRE-BOOTCAMP BTECH ACADEMY 

## Challenge

**Run the lab**
```zsh
nusactl start prbt-001-3
```

**Configure Repository**
```zsh
sudo nano /etc/apt/sources.list.d/local.list
```
```
...
deb http://kartolo.sby.datautama.net.id/ubuntu/ jammy main restricted universe multiverse

deb http://kartolo.sby.datautama.net.id/ubuntu/ jammy-updates main restricted universe multiverse

deb http://kartolo.sby.datautama.net.id/ubuntu/ jammy-security main restricted universe multiverse

deb http://kartolo.sby.datautama.net.id/ubuntu/ jammy-backports main restricted universe multiverse

deb http://kartolo.sby.datautama.net.id/ubuntu/ jammy-proposed main restricted universe 
...
```

**Update Repo**
```zsh
sudo apt update
```

**Install Apache2**
```zsh
sudo apt install apache2 -y
```

**Configure Apache and set the DocumentRoot**
```zsh
sudo nano /etc/apache2/sites-available/000-default.conf
```
```
...
<VirtualHost *:80>
        ServerAdmin webmaster@localhost
        DocumentRoot /var/www/html/pretest/
        ErrorLog ${APACHE_LOG_DIR}/error.log
        CustomLog ${APACHE_LOG_DIR}/access.log combined
</VirtualHost>
...
```

**Create Page**
```zsh
sudo mkdir /var/www/html/pretest/
sudo nano /var/www/html/pretest/index.html
```
```
...
Hallo pretest adinusa, from username
...
```

**Verify**
```zsh
sudo apt list --installed | grep apache2
sudo systemctl restart apache2
curl localhost
```

**Grade and finish**
```zsh
nusactl grade prbt-001-3
nusactl finish prbt-001-3
```