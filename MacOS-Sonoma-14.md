# Post-install process for MacOS Ventura

## Software

- [Chrome](https://www.google.com/chrome/)
- [Firefox](https://www.mozilla.org/en-US/firefox/new/)
- [VS Code](https://code.visualstudio.com/)
- [Node JS](https://nodejs.org/en/download/)
- [VLC Player](https://www.videolan.org/vlc/index.ru.html)
- [Zoom](https://zoom.us/download#client_4meeting)
- [Docker](https://docs.docker.com/desktop/install/mac-install/)
- [MongoDB-Compass](https://www.mongodb.com/try/download/compass)
- [Scroll-Reverser](https://github.com/pilotmoon/Scroll-Reverser)
- [AnyDesk](https://anydesk.com/)
- [ImageOptim](https://imageoptim.com/mac)
- [Discord](https://discord.com/)
- [Tuxera](https://ntfsformac.tuxera.com/)
- [Magnet](https://magnet.crowdcafe.com/)
- [Inkscape](https://inkscape.org/)
- [Command X](https://sindresorhus.com/command-x)
- [Postman](https://www.postman.com/downloads/)
- [Clipy](https://clipy-app.com/)
- [Google Drive](https://www.google.com/drive/download/)
- [nvm](https://github.com/nvm-sh/nvm)
- Telegam (App Store)
- Slack (App Store)
- The Unarchiver (App Store)
- Bitwarder (App Store)
- Brew
```
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```
- MongoDB
```
brew tap mongodb/brew
brew update
brew install mongodb-community@6.0
```
- cmake
```
brew install cmake
```
- Transmission
```
brew install --cask transmission
```
- 7z
```
brew install p7zip
```
- pnpm
```
brew install pnpm
```

## Settings

### Add Russian text input.

System Settings -> Keyboard -> Text Input -> Edit -> '+' -> 'Russian' -> 'Russian – PC'.

### Enable natural trackpad scrolling

System Settings -> Trackpad -> Scroll & Zoom: Natural scrolling (ON).

### Add user directory to the Finder

Finder -> Go -> Go to finder -> type `/` -> find user directory and drag it to the Favorites

### Show hidden files always

```
defaults write http://com.apple.Finder AppleShowAllFiles true
```

### Speed up keyboard

System Settings -> Keyboard -> Key repeat rate (fast), Delay until repeat (fast)

## Fonts

Download fonts

- [Fira Code](https://github.com/tonsky/FiraCode)
- [Martian Mono](https://github.com/evilmartians/mono)

Install using Font Book.

## Configs

### SSH keys

1. Place keys to `User/.ssh` directory.

2. Add keys to authentication agent `ssh-add ~/.ssh/{private_key}`

3. Set directory rights `chmod 700 ~/.ssh/*`

4. Create ssh config `.ssh/config`
```
Host {host1}
    HostName {hostname1}
    User {username1}
    IdentityFile ~/.ssh/{filename1}

Host {host2}
    HostName {hostname2}
    User {username2}
    IdentityFile ~/.ssh/{filename2}
```

[Read more about ssh configuration](https://www.digitalocean.com/community/tutorials/how-to-configure-custom-connection-options-for-your-ssh-client)

### Enable commits signing (SSH)

1. Generate SSH key locally
2. Add SSH key to GitHub (Settings -> SSH and GPG keys -> New SSH key (Signing))
3. Update local git settings
```
git config --global gpg.format ssh
git config --global user.signingkey ~/PATH/TO/.SSH/KEY.PUB
git config --global commit.gpgsign true
```

[Read more about commits signing](https://docs.github.com/en/authentication/managing-commit-signature-verification/about-commit-signature-verification)

### Git configs: work/personal

1. Create a root `.gitconfig` file: `touch ~/.gitconfig`
```
[includeIf "gitdir:~/work/"]
    path = .gitconfig-work
[includeIf "gitdir:~/personal/"]
    path = .gitconfig-personal
```

2. Create work and personal files: `touch ~/.gitconfig-personal`, `touch ~/.gitconfig-work`
```
[user]
    email = work/personal@email.com
    name = John Doe
```

[Read more about conditional git configs](https://git-scm.com/docs/git-config#_includes)
