## My post-install process for Fedora

### System update and base sofrware

Remove unnecessary packages:

```sh
sudo dnf remove gnome-boxesd orca gnome-contacts samba-client gnome-getting-started-docs nautilus-sendto gnome-shell-extension-* gnome-characters gnome-maps simple-scan virtualbox-guest-additions gedit gnome-boxes gnome-tour
```

Add RPM Fusion:

```sh
sudo dnf install --nogpgcheck http://download1.rpmfusion.org/free/fedora/rpmfusion-free-release-$(rpm -E %fedora).noarch.rpm http://download1.rpmfusion.org/nonfree/fedora/rpmfusion-nonfree-release-$(rpm -E %fedora).noarch.rpm
```

Install applications from Flatpak:

```sh
flatpak remote-add --if-not-exists flathub https://flathub.org/repo/flathub.flatpakrepo
flatpak install flathub com.transmissionbt.Transmission org.telegram.desktop org.gimp.GIMP us.zoom.Zoom org.freedesktop.Platform.ffmpeg-full/x86_64/19.08 org.inkscape.Inkscape org.gnome.Extensions
```

Update system:

```sh
sudo dnf update --refresh
```

Install Chrome:

```sh
sudo dnf install fedora-workstation-repositories
sudo dnf config-manager --set-enabled google-chrome
sudo dnf install google-chrome-stable
```

Install bluetooth drivers:

```sh
sudo dnf install bluez bluez-tools
```

Disable Software auto-start:

```sh
dconf write /org/gnome/software/allow-updates false
dconf write /org/gnome/software/download-updates false
mkdir -pv ~/.config/autostart && cp /etc/xdg/autostart/gnome-software-service.desktop ~/.config/autostart/
echo "X-GNOME-Autostart-enabled=false" >> ~/.config/autostart/gnome-software-service.desktop
dconf write /org/gnome/desktop/search-providers/disabled "['org.gnome.Software.desktop']"
```

### Base Settings

Disable file system scanning:

```sh
dconf write /org/freedesktop/tracker/miner/files/crawling-interval -2
```

Restart.

### Text Editor

Install VS Code:

```sh
sudo rpm --import https://packages.microsoft.com/keys/microsoft.asc
sudo sh -c 'echo -e "[code]\nname=Visual Studio Code\nbaseurl=https://packages.microsoft.com/yumrepos/vscode\nenabled=1\ngpgcheck=1\ngpgkey=https://packages.microsoft.com/keys/microsoft.asc" > /etc/yum.repos.d/vscode.repo'
sudo dnf install code
```

Enable Sync.

Download [FiraCode](https://github.com/tonsky/FiraCode) and unpack in ./local/share/fonts

### GNOME Settings

Open settings:

* **Notifictions:** disable Lock Screen Notifications.
* **Background:** use standard GNOME wallpaper.
* **Online Accounts:** add Google account.
* **Mouse & Touchpad:** Enable Tap to Click.
* **Users:** Avatar.
* **Power:** Show Battery Percentage.
* **Region & Language:** UK formats.

Nautilus:

* Enable Sort folders before files.

Install extensions from [`GNOME.md`](./GNOME.md).

* **Screenshot Tool:** disable Show Indicator, enable Auto-Save to Downloads
  with `{Y}{m}{d}{H}{M}{S}` name, enable Imgur Upload
  with Copy Link After Upload, set `Print` keyboard binding.

Install GNOME Tweaks:

```sh
sudo dnf install gnome-tweak-tool
```

* **General:** enable Over-Amplification.
* **Top Bar:** enable Weekday, Date and Seconds.
* **Keyboard & Mouse:** enable Adaptive in Acceleration Profile.
* **Fonts:** monospace to JetBrains Mono.
* **Windows:** enable Center New Window.
* **Window Titlebars:** enable Maximize and Minimize buttons

### Additional Software

Install codecs:

```sh
sudo dnf install amrnb amrwb faac faad2 flac gstreamer1-libav gstreamer1-plugins-bad-freeworld gstreamer-ffmpeg gstreamer-plugins-bad-nonfree gstreamer-plugins-espeak gstreamer-plugins-ugly lame libdca libmad libmatroska x264 x265 xvidcore gstreamer1-plugins-bad-free gstreamer1-plugins-base gstreamer1-plugins-good gstreamer-plugins-bad gstreamer1-plugins-ugly-free mpv xorg-x11-drv-intel intel-media-driver
```

Install tools:

```sh
sudo dnf install unrar p7zip p7zip-plugins
```

Install Microsoft fonts:

```sh
sudo dnf install https://downloads.sourceforge.net/project/mscorefonts2/rpms/msttcore-fonts-installer-2.6-1.noarch.rpm
```

Install Vokoscreen

```sh
sudo dnf install vokoscreenNG
```

Install image ootimization tools

```sh
sudo yum install jpegoptim optipng
```

### Development Tools

Install tools:

```sh
sudo dnf install git make xkill
```

Install Node.js:

```sh
sudo dnf install nodejs
```

Install [Docker](https://docs.docker.com/engine/install/fedora/), set [non-root](https://docs.docker.com/engine/install/linux-postinstall/) mode and autostart

Install global npm packages:

```sh
sudo npm i -g n parcel-bundler webpack webpack-cli pm2 eslint svgo
```

Install [FontForge](http://designwithfontforge.com/en-US/Installing_Fontforge.html)

Install [MongoDB](https://www.mongodb.com/try/download/community) (Fedora 34 - RedHat 8.0)

### Notes

Run Extensions

```sh
flatpak run org.gnome.Extensions
```
