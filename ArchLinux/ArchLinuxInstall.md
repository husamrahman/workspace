## Arch Linux Install Guide (on LVM)

https://wiki.learnlinux.tv/index.php/How_to_Install_Arch_Linux_on_LVM

## Linux Packages

Packages to download using pacman: 

linux
linux-headers 
linux-lts
linux-lts-headers 

grub
efibootmgr
nano
base-devel 
bluez
bluez-utils

virtualbox
virtualbox-host-dkms

iwd 
networkmanager
wpa_supplicant
wireless_tools
netctl
net-tools
arch-audit

lightdm
lightdm-gtk-greeter
gnome-shell

docker
git

## Packages to install with yay

google chrome
vscode
stacer
vlc
neofetch
nautilus 
material-shell: yay -S gnome-shell-extension-material-shell-git

- Packages to install from git
ulauncher: git clone https://aur.archlinux.org/ulauncher.git && cd ulauncher && makepkg -is


- Additional things to install
Python
R
Rstudio
airflow

- Configurations
* Configure timeshift to backup every week
