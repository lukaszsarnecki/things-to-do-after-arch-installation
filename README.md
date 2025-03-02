# Things to do after arch installation

## Enable autocmplete in bash

### Install bash-completion

```bash
sudo pacman -S bash-completion
```
### Add the following code to the ~/.bashrc file:

```bash
vim .bashrc
```

```bash
# Enable autocomplete in bash
if [ -f /usr/share/bash-completion/bash_completion ]; then
    . /usr/share/bash-completion/bash_completion
fi
```
Logout and login again

## Install yay and paru

### YAY
```bash
sudo pacman -S --needed git base-devel
```
```bash
git clone https://aur.archlinux.org/yay.git
```
```bash
cd yay && makepkg -si
```
### PARU
```bash
sudo pacman -S --needed git base-devel
```
```bash
git clone https://aur.archlinux.org/paru
```
```bash
cd paru && makepkg -si
```
## Pacman configuration
```bash
sudo vim /etc/pacman.conf
```
And uncomment
```
Color
```
```
ParalleDownloads = 5
```
```
[multilib]
Include = /etc/pacman.d/mirrorlist
```
## Power Profiles Deamon Installation 
```bash
sudo pacman -S power-profiles-daemon
```
## Enable wayland in gdm
```bash
sudo vim /etc/gdm/custom.conf
```
And change **#WaylandEnable=false** to **WaylandEnable=true**
## Remove some unnecessary apps
```bash
sudo rm -Rf org.gnome.Extensions.desktop qv4l2.desktop qvidcap.desktop bvnc.desktop bssh.desktop avahi-discover.desktop
```
```bash
sudo pacman -R epiphany vim
```


