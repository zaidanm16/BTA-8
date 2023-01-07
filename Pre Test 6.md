# PRE-BOOTCAMP BTECH ACADEMY 

## Challenge

**Run the lab**
```zsh
nusactl start prbt-001-6
```

**Install HAProxy**
```zsh
sudo apt install haproxy -y
```

**Configure Roundrobin**
```zsh
sudo nano /etc/haproxy/haproxy.cfg
```
```
...
frontend web_frontend
    bind localhost:80
    mode http
    default_backend web_backend

backend web_backend
    balance roundrobin
    server web1 localhost:18001
    server web2 localhost:18002
...
```

**Restart HAProxy**
```zsh
sudo systemctl restart haproxy
```

**Verify**
```zsh
curl localhost:80
```

**Grade and finish**
```zsh
nusactl grade prbt-001-6
nusactl finish prbt-001-6
```