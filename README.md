# maconarch
Make Arch Linux like Mac OS

1. buka extension
2. aktifkan user-themes
1. buka tweek
2. windows titlebars
3. aktifkan semuanya
4. posisi tombol di kiri
5. Appearance
6. ganti shell dan legacy application ke whitesur

1. pakku -S gdm-settings
2. sudo rm -r /etc/motd

pakku -S gnome-browser-connector
1. https://extensions.gnome.org/extension/307/dash-to-dock/
2. https://extensions.gnome.org/extension/3193/blur-my-shell/
3. https://extensions.gnome.org/extension/97/coverflow-alt-tab/
4. https://extensions.gnome.org/extension/3740/compiz-alike-magic-lamp-effect/
5. https://extensions.gnome.org/extension/3724/net-speed-simplified/
6. https://extensions.gnome.org/extension/5088/muteunmute/
7. https://extensions.gnome.org/extension/4679/burn-my-windows/
8. https://extensions.gnome.org/extension/3956/gnome-fuzzy-app-search/
9. https://extensions.gnome.org/extension/5401/gtk3-theme-switcher/
10. https://extensions.gnome.org/extension/3210/compiz-windows-effect/
11. https://extensions.gnome.org/extension/4105/notification-banner-position/
12. https://extensions.gnome.org/extension/4977/sur-clock/

## Themes Mac on Arch Linux

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

### Install Tweeks and Git
```yaml
sudo pacman -S gnome-tweaks git
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

## Install/Remove Drivers and Software

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

### Arch User Repository (AUR) Software 
```yaml
Whatsapp Desktop
pakku -S whatsapp-for-linux

Instagram Desktop
pakku -S instagram-nativefier

YouTube Music Desktop
pakku -S youtube-music-bin

Zoom
pakku -S zoom

Microsoft Fonts
pakku -S ttf-ms-fonts
```

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

System Monitoring
sudo pacman -S gnome-system-monitor

Main Menu Editor
sudo pacman -S alacarte
```

### Remove Software
```yaml
sudo pacman -Rsu lftp
```

## Add No Display for Apps in Gnome Launchers

Comment in Apps.desktop
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

LibreOffice Start Center
sudo nano /usr/share/applications/libreoffice-startcenter.desktop
```
