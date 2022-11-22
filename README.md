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
