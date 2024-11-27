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
