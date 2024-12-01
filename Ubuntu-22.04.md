# Post-install process for Ubuntu

⚠️ Warning: The post-install instruction is deprecated

## Software

- [Google Chrome](https://www.google.com/intl/en/chrome/)
- [Git](https://git-scm.com/)
- [Telegram](https://desktop.telegram.org/)
- [Zoom](https://zoom.us/download#client_4meeting)
- [VSCode](https://code.visualstudio.com/)
- [Surfshark VPN](https://support.surfshark.com/hc/en-us/articles/5067279648146-How-to-set-up-Surfshark-on-Linux-)
- [Docker](https://docs.docker.com/engine/install/ubuntu/)
- [MongoDB-Compass](https://www.mongodb.com/try/download/compass)
- Postman (Ubuntu Software)
- VLC Player (Ubuntu Software)
- `sudo apt install make gimp`
- `sudo apt-get install jq gnome-tweaks vokoscreen ubuntu-restricted-extras sudo rar unrar p7zip-full jpegoptim optipng curl unzip`
- NodeJS, npm:
```sh
curl -sL https://deb.nodesource.com/setup_14.x | sudo -E bash -
sudo apt-get install nodejs
sudo apt install npm
```
- Some npm stuff:
```sh
sudo npm i -g n parcel webpack webpack-cli pm2 eslint svgo
```

- MongoDB:
1. Install libssl1.1 package
```
echo "deb http://security.ubuntu.com/ubuntu focal-security main" | sudo tee /etc/apt/sources.list.d/focal-security.list

sudo apt-get update
sudo apt-get install libssl1.1

sudo rm /etc/apt/sources.list.d/focal-security.list
```
2. Follow instructions https://docs.mongodb.com/manual/tutorial/install-mongodb-on-ubuntu/

## Settings

- Add Russian keyboard (settings -> region & language)

- For folding apps in one click:
```sh
gsettings set org.gnome.shell.extensions.dash-to-dock click-action 'minimize'
```

- [FiraCode](https://github.com/tonsky/FiraCode) (extract to ~/.local/share/fonts)

- [Non-Root Docker](https://docs.docker.com/engine/install/linux-postinstall/)

- Set proper access rights for ssh keys and add it:

```sh
chmod =600 ~/.ssh/private_key
ssh-add ~/.ssh/private_key
```

- SSH config (~/.ssh/config):
```
Host github.com
    HostName github.com
    User DRIMchansky
    IdentityFile ~/.ssh/github

Host {name}
    HostName {organization url}
    User {username}
    IdentityFile ~/.ssh/{private_key}
```
- Make Linux Use Local Time (if windows used as second system)
```
timedatectl set-local-rtc 1 --adjust-system-clock
```






