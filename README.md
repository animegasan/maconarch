# Make Arch Linux like Mac OS

## Install Drivers and Pakku AUR Helper

### Bluetooth Drivers
```yaml
sudo pacman -S bluez bluez-utils
sudo systemctl start bluetooth.service
sudo systemctl enable bluetooth.service
```

### Pakku AUR Helper
```yaml
sudo pacman -S base-devel git
git clone https://aur.archlinux.org/pakku.git
cd pakku
makepkg -si
```

## Themes Mac on Arch Linux

### Reinstall Grub

### Add Grub Themes
```yaml
sudo pacman -S grub-customizer

Buat resolusi Grub jadi 1920x1080

```
### Add Class for Efi Icons

Add `--class efi` after `menuentry '$LABEL'`
```yaml
cd /etc/grub.d
sudo nano 45_uefi-firmware
sudo grub-mkconfig -o /boot/grub/grub.cfg
```

### Install Tweeks
```yaml
sudo pacman -S gnome-tweaks
```

### Add Themes
```yaml
git clone https://github.com/vinceliuice/WhiteSur-gtk-theme themes
cd themes
./install.sh -m -HD -N glassy
./install.sh -l -c Light
./install.sh -l
```

### Add Gnome Display Manager Themes
```yaml
sudo ./tweaks.sh -g
sudo rm -r /etc/motd
sudo rm -r /usr/share/pixmaps/archlinux-logo.png
```

### Add Wallpapers
```yaml
git clone https://github.com/vinceliuice/WhiteSur-wallpapers wallpapers
cd wallpapers
sudo ./install-gnome-backgrounds.sh
```

### Add Icons
```yaml
git clone https://github.com/vinceliuice/WhiteSur-icon-theme icons
cd icons
./install.sh
```

### Add Cursor
```yaml
pakku -S apple_cursor
```

### Add Extension
```yaml
pakku -S gnome-browser-connector
```
#### List Extension

##### Themes
1. <a href="https://extensions.gnome.org/extension/307/dash-to-dock/" target="_blank">Dash to Dock</a>
2. <a href="https://extensions.gnome.org/extension/3193/blur-my-shell/" target="_blank">Blur my Shell</a>
3. <a href="https://extensions.gnome.org/extension/3724/net-speed-simplified/" target="_blank">Net speed Simplified</a>
4. <a href="https://extensions.gnome.org/extension/4977/sur-clock/" target="_blank">Sur Clock</a>

##### System
1. <a href="https://extensions.gnome.org/extension/97/coverflow-alt-tab/" target="_blank">Coverflow Alt-Tab</a>
2. <a href="https://extensions.gnome.org/extension/3740/compiz-alike-magic-lamp-effect/" target="_blank">Compiz alike magic lamp effect</a>
3. <a href="https://extensions.gnome.org/extension/3210/compiz-windows-effect/" target="_blank">Compiz windows effect</a>
4. <a href="https://extensions.gnome.org/extension/4679/burn-my-windows/" target="_blank">Burn My Windows</a>
5. <a href="https://extensions.gnome.org/extension/5088/muteunmute/" target="_blank">Mute/Unmute</a>
6. <a href="https://extensions.gnome.org/extension/4105/notification-banner-position/" target="_blank">Notification Banner Position</a>
7. <a href="https://extensions.gnome.org/extension/3956/gnome-fuzzy-app-search/" target="_blank">GNOME Fuzzy App Search</a>
8. <a href="https://extensions.gnome.org/extension/5401/gtk3-theme-switcher/" target="_blank">GTK3 Theme Switcher</a>

## Install and Remove Software

### Arch Package Software
```yaml
Telegram Desktop
sudo pacman -S telegram-desktop

Discord
sudo pacman -S discord

VLC
sudo pacman -S vlc

Libre Office
sudo pacman -S libreoffice

Spelling Checker English
sudo pacman -S hunspell-en_us

System Monitoring
sudo pacman -S gnome-system-monitor

Disk Usage Analyzer
sudo pacman -S baobab

R
sudo pacman -S r

Node.js
psudo acman -S nodejs npm

Java
sudo pacman -S jre-openjdk jdk-openjdk

Virtual Box
sudo pacman -S virtualbox

Netbeans
sudo pacman -S netbeans

Cisco Packet Tracer
https://aur.archlinux.org/packages/packettracer
```

### Arch User Repository (AUR) Software 
```yaml
Google Chrome
pakku -S google-chrome

Whatsapp Desktop
pakku -S whatsapp-for-linux

YouTube Music Desktop
pakku -S youtube-music-bin

Zoom
pakku -S zoom

Microsoft Fonts
pakku -S ttf-ms-fonts

Spelling Checker Indonesia
pakku -S hunspell-id-git

Stacer
pakku -S stacer

Visual Studio Code
pakku -S visual-studio-code-bin

yEd Graph Editor
pakku -S yed

XAMP
pakku -S xampp
```

### Remove Software
```yaml
sudo pacman -Rsu lftp grub-customizer alacarte

```

## Setting Display Apps in Gnome Launchers

### Comment in Apps.desktop
```yaml
NoDisplay=true
Hidden=true
```

### List Apps
```yaml
Avahi Zeroconf Browser
sudo nano /usr/share/applications/avahi-discover.desktop

Avahi SSH Server Browser
sudo nano /usr/share/applications/bssh.desktop

Avahi VNC Server Browser
sudo nano /usr/share/applications/bvnc.desktop

Qt V4L2 test Utility
sudo nano /usr/share/applications/qv4l2.desktop

Qt V4L2 video capture utility
sudo nano /usr/share/applications/qvidcap.desktop

Hardware Locality lstopo
sudo nano /usr/share/applications/lstopo.desktop

Disk
sudo nano /usr/share/applications/org.gnome.DiskUtility.desktop

YouTube Music Dekstop
sudo nano /usr/share/applications/youtube-music.desktop
Icon=youtube-music-desktop-app

Whatsapp Desktop
sudo nano /usr/share/applications/com.github.eneshecan.WhatsAppForLinux.desktop
Name=WhatsApp

Telegram Desktop
sudo nano /usr/share/applications/telegramdesktop.desktop
Name=Telegram

VLC
sudo nano /usr/share/applications/vlc.desktop
Name=Media Player

Gedit
sudo nano /usr/share/applications/org.gnome.gedit.desktop
Name=Notes

LibreOffice Start Center
sudo nano /usr/share/applications/libreoffice-startcenter.desktop

LibreOffice Base
sudo nano /usr/share/applications/libreoffice-base.desktop
Name=Base

LibreOffice Calc
sudo nano /usr/share/applications/libreoffice-calc.desktop
Name=Calc

LibreOffice Draw
sudo nano /usr/share/applications/libreoffice-draw.desktop
Name=Draw

LibreOffice Impress
sudo nano /usr/share/applications/libreoffice-impress.desktop
Name=Impress

LibreOffice Math
sudo nano /usr/share/applications/libreoffice-math.desktop
Name=Math

LibreOffice Writer
sudo nano /usr/share/applications/libreoffice-writer.desktop
Name=Writer
```
