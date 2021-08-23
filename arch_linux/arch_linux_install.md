## Arch Linux Install Guide (on LVM)

* Youtube: https://www.youtube.com/watch?v=stI0Cazy8H0
* Notes from Youtube video: https://wiki.learnlinux.tv/index.php/How_to_Install_Arch_Linux_on_LVM

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
  cups-pdf
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
  netctl
  net-tools
  inetutils
  openssh
  xorg-apps
  avahi
  wget

* GUI
  * xorg
  gdm
  gnome
  gnome-tweaks

* Additional Components
  * docker
  git
  firefox
  arch-audit
  zoom
  flameshot
  node
  nvm

 
## Adjustments to Configuration Files

* /etc/mkinitcpio.conf (to enable lvm2)
* /etc/locale.gen
* If using an intel processor, you might need to adjust the grub config to avoid the freezing issues (bug in kernel)
  - sudo nano /etc/default/grub
  - Add "intel_idle.max_cstate=1" under GRUB_CMDLINE_LINUX_DEFAULT
  - Update grub: sudo grub-mkconfig -o /boot/grub/grub.cfg
  - Restart the system

## Services to enable during install

* systemctl enable NetworkManager
* systemctl enable bluetooth
* systemctl enable cups
* systemctl enable gdm
* systemctl enable sshd

## Notes Post-Install
* Currently a bug in gnome where you have to go to settings and select the language manually or else the terminal will not work

## Install yay

1. sudo chown -R {user} /home
2. mkdir /home/programs
3. cd /home/programs
4. git clone https://aur.archlinux.org/yay.git && cd yay && makepkg -si PKGBUILD


## Primary UI
* material-shell: 	yay -S gnome-shell-extension-material-shell-git
* theme: yay -S plata-theme
* tela icons: 
  1. git clone https://github.com/vinceliuice/Tela-icon-theme.git
  2. sudo -s
  3. cd Tela-icon-theme
  3. ./install.sh -d /usr/share/icons

## Packages to install from git
* ulauncher: git clone https://aur.archlinux.org/ulauncher.git && cd ulauncher && makepkg -is
* timeshift: git clone https://aur.archlinux.org/timeshift.git && cd timeshift && makepkg -is
* bash-it: https://bash-it.readthedocs.io/en/latest/installation/

## Packages to install with yay

* google-chrome
* visual-studio-code-bin
* stacer
* vlc
* neofetch
* nautilus 
* displaylink
* ms-office-online
* spotify
* zoom
* python37
* figma

## Services to enable after install
* systemctl enable displaylink

## Permissions after install
* Add users to docker group
  1. sudo usermod -a -G docker {user}
  2. restart machine

## Additional Configurations

* Configure timeshift to backup every week
* Chrome Extensions:
  * Momentum
  * Lastpass
* Flameshot keyboard shortcut:
  * Command: flameshot gui
  * Keyboard: CTRL + S

## Additional things to install (work in progress)
R
Rstudio
airflow


