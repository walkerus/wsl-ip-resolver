## About
Each time you reboot the system or restart WSL, the subsystem changes the ip address. This script will help you resolve the WSL address. (Actual for Windows 10 Version 10.0.19041 Build 19041)

## Install
```
sudo wget https://raw.githubusercontent.com/walkerus/wsl-ip-resolver/master/wsl-ip-resolver -P /usr/bin
sudo chmod +x /usr/bin/wsl-ip-resolver
```

## usage
```
//get wsl ip for host
wsl-ip-resolver --wsl

//get host ip for wsl
wsl-ip-resolver --win

//update C:\Windows\System32\drivers\etc\hosts
wsl-ip-resolver --resolve
```

After resolving, the subsystem can be accessed by dns as wsl. Example http://wsl

for automatic resolving ```@reboot wsl-ip-resolver --resolve``` add to crontab
