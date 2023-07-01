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

## Fonts

Download fonts

- [Fira Code](https://github.com/tonsky/FiraCode)
- [Martian Mono](https://github.com/evilmartians/mono)

Install using Font Book.

## Configs

### SSH keys

Place keys to `User/.ssh` directory.

Add keys to authentication agent `ssh-add ~/.ssh/{private_key}`

Set directory rights `chmod 700 ~/.ssh/*`
