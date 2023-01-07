# PRE-BOOTCAMP BTECH ACADEMY 

## Guided Exercise

**Run the lab**
```zsh
nusactl start prbt-001-1
```

**Generate SSH Keys**
```zsh
ssh-keygen
```

**Send the public key**
```zsh
ssh-copy-id -p 2279 lab@lab2.adinusa.id
```

**Execute 'hostname' command via SSH**
```zsh
ssh lab@lab2.adinusa.id -p 2279 hostname
```

## Challenge

**Copy private key to VM**
```zsh
scp challage student@10.10.10.11:/home/student/
```

**Create Directory and put the private key inside**
```zsh
mkdir zaidanmuhammad169
mv challage zaidanmuhammad169/pretest.pem
chmod 600 zaidanmuhammad169/pretest.pem
```

**Access SSH using private key**
```zsh
ssh -i zaidanmuhammad169/pretest.pem challenge@lab2.adinusa.id -p 2279
```

**Grade and finish**
```zsh
nusactl grade prbt-001-1
nusactl finish prbt-001-1
```