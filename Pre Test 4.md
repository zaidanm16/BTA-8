# PRE-BOOTCAMP BTECH ACADEMY 

## Challenge

**Run the lab**
```zsh
nusactl start prbt-001-4
```

**Creating container**
```zsh
sudo docker run -d --name zaidanmuhammad169-pretest4 -p 80:80 dockercloud/hello-world
```

**Verify**
```zsh
sudo docker container ls -a
curl localhost:80
```

**Grade and finish**
```zsh
nusactl grade prbt-001-4
nusactl finish prbt-001-4
```