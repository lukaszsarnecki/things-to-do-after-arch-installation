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
pacman -S --needed git base-devel
```
```bash
git clone https://aur.archlinux.org/yay.git
```
```bash
cd yay && makepkg -si
```
### PARU
```bash
pacman -S --needed git base-devel
```
```bash
git clone https://aur.archlinux.org/paru
```
```bash
cd yay && makepkg -si
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
