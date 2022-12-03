# Post-install process for Ubuntu

## Software

- [Google Chrome](https://www.google.com/intl/en/chrome/)
- [Git](https://git-scm.com/)
- [Telegram](https://desktop.telegram.org/)
- [Zoom](https://zoom.us/download#client_4meeting)
- [Skype](https://www.skype.com/ru/get-skype)
- [VLCPlayer](https://www.videolan.org/vlc/index.ru.html)
- [VSCode](https://code.visualstudio.com/)
- [Docker](https://docs.docker.com/engine/install/ubuntu/)
- [MongoDB](https://docs.mongodb.com/manual/tutorial/install-mongodb-on-ubuntu/)
- [MongoDB-Compass](https://www.mongodb.com/try/download/compass)
- Postman (Ubuntu Software)
- `sudo apt install make gimp`
- `sudo apt-get install jq gnome-tweaks vokoscreen ubuntu-restricted-extras sudo rar unrar p7zip-full jpegoptim optipng curl`
- NodeJS, npm:
```sh
curl -sL https://deb.nodesource.com/setup_14.x | sudo -E bash -
sudo apt-get install nodejs
```
- Some npm stuff:
```sh
sudo npm i -g n parcel webpack webpack-cli pm2 eslint svgo
```

## Settings

- Add Russian keyboard (settings -> region & language)

- For folding apps in one click:
```sh
gsettings set org.gnome.shell.extensions.dash-to-dock click-action 'minimize'
```

- [FiraCode](https://github.com/tonsky/FiraCode) (extract to ~/.local/share/fonts)

- [Non-Root Docker](https://docs.docker.com/engine/install/linux-postinstall/) // xz why but do it

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






