## Arch Linux Install Guide (on LVM)

https://wiki.learnlinux.tv/index.php/How_to_Install_Arch_Linux_on_LVM

## Packages

Packages to download using pacman: 

* Core
  * linux
  linux-headers 
  linux-lts
  linux-lts-headers 
  lvm2

* Drivers
  * grub
  efibootmgr
  dosfstools
  os-prober
  mtools
  nano
  dialog
  base-devel 
  reflector
  bluez
  bluez-utils
  cups
  hplip
  xdg-utils
  xdg-user-dirs
  pulseaudio
  pulseaudio-bluetooth
  xf86-video-intel
  virtualbox-guest-utils
  xf86-video-vmware
  virtualbox
  virtualbox-host-dkms
  intel-uncode
  mesa
  iwd 
  networkmanager
  network-manager-applet
  wpa_supplicant
  netctl
  net-tools
  inetutils

* GUI
  * xorg
  gdm
  gnome

* Additional Components
  * docker
  git
  firefox
  arch-audit
  
## Services to Enable

* systemctl enable NetworkManager
* systemctl enable bluetooth
* systemctl enable cups
* systemctl enable gdm

## Adjustments to Configuration Files

* /etc/mkinitcpio.conf (to enable lvm)
* /etc/locale.gen

## Install yay

1. git clone https://aur-archlinux.org/yay
2. cd yay/
3. makepkg -si PKGBUILD

## Primary UI
* material-shell: yay -S gnome-shell-extension-material-shell-git
* theme: yay -S palata-theme
* icons: yay -S tela-icons

## Packages to install from git
* ulauncher: git clone https://aur.archlinux.org/ulauncher.git && cd ulauncher && makepkg -is
* timeshift: git clone https://aur.archlinux.org/timeshift.git && cd timeshift && makepkg -is

## Packages to install with yay

* google-chrome
* vscode
* stacer
* vlc
* neofetch
* nautilus 

## Additional Configurations

* Configure timeshift to backup every week

## Additional things to install (work in progress)
Python
R
Rstudio
airflow


