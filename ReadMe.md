# Ubuntu upgrade notes

## Ubuntu Zesty 17.04 to bionic 18.04

```bash
lsb_release -a
sudo sed -i 's/zesty/bionic/g' /etc/apt/sources.list
sudo apt upgrade -y
sudo apt upgrade -y
# you may encounter troubles with 'plymouth-theme-ubuntu-text', see bellow notes, then continue
sudo apt autoremove -y
do-release-upgrade
sudo apt dist-upgrade -y
sudo apt clean
sudo restart now
```

## Troubles with `plymouth-theme-ubuntu-text`

> Package lsb-release is not configured yet.

https://askubuntu.com/questions/892501/apt-get-command-returning-error-in-plymouth-theme-ubuntu-text`

```bash
sudo dpkg --configure -a
```

