# maconarch
Make Arch Linux like Mac OS
1. Buat resolusi Grub jadi 1920x1080
2. Tambahkan class di efi
a. cd /etc/grub.d
b. sudo nano 45_uefi-firmware
c. menuentry '$LABEL' ke menuentry '$LABEL' --class efi
d. sudo grub-mkconfig -o /boot/grub/grub.cfg

1. sudo pacman -S grub-customizer
2. 

1. Install Pakku
a. sudo pacman -S base-devel git
b. git clone https://aur.archlinux.org/pakku.git
c. cd pakku
d. makepkg -si

Themes
a. sudo pacman -S gnome-tweaks
install themes
a. https://github.com/vinceliuice/WhiteSur-gtk-theme
b. git clone https://github.com/vinceliuice/WhiteSur-gtk-theme themes
c. cd themes
d. ./install.sh -m -HD -N glassy
f. ./install.sh -l -c Light
g. ./install.sh -l
install gdm
sudo ./tweaks.sh -g

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


Icons
git clone https://github.com/vinceliuice/WhiteSur-icon-theme icons
cd icons
./install.sh

Wallpapper
git clone https://github.com/vinceliuice/WhiteSur-wallpapers wallpapers
cd wallpapers
sudo ./install-gnome-backgrounds.sh

cursor
pakku -S apple_cursor

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

Install Software dan driver bluetooth
1. pakku -S whatsapp-for-linux
2. sudo pacman -S telegram-desktop
3. pakku -S youtube-music-bin
4. sudo pacman -S libreoffice
5. sudo pacman -S bluez bluez-utils
sudo systemctl start bluetooth.service
sudo systemctl enable bluetooth.service
pakku -S ttf-ms-fonts
pakku -S instagram-nativefier
sudo pacman -Rsu lftp
sudo pacman -S alacarte
pakku -S zoom
sudo pacman -S discord
sudo pacman -S vlc

Add no display
NoDisplay=true
Hidden=true
sudo nano /usr/share/applications/avahi-discover.desktop
sudo nano /usr/share/applications/bssh.desktop
sudo nano /usr/share/applications/

sudo systemctl restart gdm
