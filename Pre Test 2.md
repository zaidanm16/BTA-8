# PRE-BOOTCAMP BTECH ACADEMY 

## Challenge

**Run the lab**
```zsh
nusactl start prbt-001-2
```

**Add pretest user and set password to btacademy**
```zsh
sudo useradd pretest
sudo passwd pretest
```

**Configure sudo access**
```zsh
sudo usermod -aG sudo pretest
sudo nano /etc/sudoers.d/pretest
```
```
...
# User rules for pretest
pretest ALL=(ALL) NOPASSWD:ALL
...
```

**Verify**
```zsh
cat /etc/passwd
sudo su - pretest
sudo su
exit
```

**Grade and finish**
```zsh
nusactl grade prbt-001-2
nusactl finish prbt-001-2
```