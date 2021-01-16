## Arch Linux Install Guide (on LVM)

https://wiki.learnlinux.tv/index.php/How_to_Install_Arch_Linux_on_LVM

## Notes Pre-Install
* After updating the distribution, add server manually to mirror list (https://archlinux.org/mirrorlist/)

## Packages

Packages to download using pacman: 

* Core
  * linux
  linux-headers 
  linux-firmware
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
  intel-ucode
  mesa
  iwd 
  networkmanager
  network-manager-applet
  wpa_supplicant
  netctl
  net-tools
  inetutils
  openssh

* GUI
  * xorg
  gdm
  gnome

* Additional Components
  * docker
  git
  firefox
  arch-audit
 
## Adjustments to Configuration Files

* /etc/mkinitcpio.conf (to enable lvm2)
* /etc/locale.gen

## Services to Enable

* systemctl enable NetworkManager
* systemctl enable bluetooth
* systemctl enable cups
* systemctl enable gdm

## Notes Post-Install
* Currently a bug in gnome where you have to go to settings and select the language manually or else the terminal will not work

## Install yay

1. git clone https://aur-archlinux.org/yay.git
2. cd yay/
3. sudo chown -R {user} /home/{user}/yay
3. makepkg -si PKGBUILD

## Primary UI
* material-shell: yay -S gnome-shell-extension-material-shell-git
* theme: yay -S plata-theme
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


