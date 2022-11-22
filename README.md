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


