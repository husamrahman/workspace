## Arch Linux Install Guide (on LVM)

https://wiki.learnlinux.tv/index.php/How_to_Install_Arch_Linux_on_LVM

## Linux Packages

Packages to download using pacman: 

*linux
*linux-headers 
*linux-lts
*linux-lts-headers 
*lvm2

*grub
*efibootmgr
*dosfstools
*os-prober
*mtools
*nano
*dialog
*base-devel 
*bluez
*bluez-utils
*pulseaudio
*pulseaudio-bluetooth

*virtualbox-guest-utils
*xf86-video-vmware
*virtualbox
*virtualbox-host-dkms
*intel-uncode
*mesa

*iwd 
*networkmanager
*network-manager-applet
*wpa_supplicant
*netctl
*net-tools
*arch-audit

*xorg-server
*lightdm
*lightdm-gtk-greeter
*gnome-shell

*docker
*git

## Services to Enable

*systemctl enable NetworkManager

## Adjustments to Configuration Files

*/etc/mkinitcpio.conf (to enable lvm)
*/etc/locale.gen

## Install yay


## Packages to install with yay

google chrome
vscode
stacer
vlc
neofetch
nautilus 
material-shell: yay -S gnome-shell-extension-material-shell-git

## Packages to install from git
ulauncher: git clone https://aur.archlinux.org/ulauncher.git && cd ulauncher && makepkg -is


- Additional things to install
Python
R
Rstudio
airflow

- Configurations
* Configure timeshift to backup every week
