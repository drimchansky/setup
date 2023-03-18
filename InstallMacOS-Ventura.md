# Post-install process for MacOS

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
- [Starship](https://starship.rs/guide/#%F0%9F%9A%80-installation)
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

- Keyboard: Text input - Add "Russian -- PC"
- Trackpad: Scroll & Zoom: Natural scrolling (ON)
- Add user directory to the finder: Finder => Go => Go to finder => type `/`, find user directory and drag it to Favorites
- Always show hidden files
```
defaults write http://com.apple.Finder AppleShowAllFiles true
```

## Other

### Fonts

- [Fira Code](httpss://github.com/tonsky/FiraCode)

Install via Font Book

### SSH keys

After adding ssh keys to `User/.ssh` directory:
- Add ssh keys ssh-add `~/.ssh/private_key`
- Update ssh directory rights `chmod 700 ~/.ssh/*`
