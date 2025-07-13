---
description: Alias
---

# Алиасы

## Добавляем Alias (сокращенные команды)

<figure><img src="../../.gitbook/assets/Снимок экрана от 2024-08-09 09-00-14.png" alt=""><figcaption></figcaption></figure>

```bash
    #
    # Timeshift
    #
    alias tm="sudo timeshift"
    alias tmc="sudo timeshift --create"
    alias tmd="sudo timeshift --delete"
    alias tmda="sudo timeshift --delete-all"
    alias tml="sudo timeshift --list"
    #
    # Fastfetch
    #
    alias n="fastfetch --logo PostMarketOS_small -c '/home/plafon/Документы/Fastfetch/plafonfetch.jsonc'"
    alias k="uname -rs"
    alias g="gnome-shell --version"
    alias f="lsb_release -sd"
    alias m="inxi -G | grep mesa"
    alias age="stat / | grep Создан:"
    alias ram="sudo dmidecode -t memory | grep Speed"
    alias cpu="lscpu | grep Имя"
    alias cpuc="lscpu"
    alias w="wine --version"
    alias pc="inxi -Ixxx"
    alias net="inxi -Nxxx"
    #
    # Upgrade System
    #
    alias up="epm update && epm full-upgrade"
    alias cc="sudo apt-get clean && sudo apt-get autoclean && sudo apt-get check && flatpak uninstall --unused -y && sudo journalctl --vacuum-time=1weeks"
    alias c="clear"
    alias find="epmqa"
    alias search="epmqa"
    alias poisk="epmqa"
    #
    # PC
    #
    alias son="sudo systemctl suspend"
    alias reboot="systemctl reboot"
    alias r="systemctrl reboot"
    alias ls="ls --color"
    alias l="lsd --date '+%d.%m.%Y %H:%M' -lah"
    #
    # Flatpak
    #
    alias fli="flatpak install --noninteractive -y flathub"
    alias flr="flatpak remove --noninteractive -y"
    alias fr="flatpak repair"
    alias fl="flatpak list"
    #
    # Gnome Text Editor
    #
    alias gte="gnome-text-editor"
    alias sgte="sudo gnome-text-editor"
    #
    # System folders
    #
    alias fstab="sudo vim /etc/fstab"
    alias bashrc="vim ~/.bashrc"
    alias zshrc="vim ~/.zshrc"
    alias bashrc="vim .bashrc"
    #
    # GRUB
    #
    alias grubedit="sudo vim /etc/default/grub"
    alias editgrub="sudo vim /etc/default/grub"
    alias upgrub="sudo update-grub"
    alias grubup="sudo update-grub"
    #
    # Other
    #
    alias sn="sudo nautilus"
    alias v4="sudo modprobe v4l2loopback"
    alias vmax="sudo sysctl -w vm.max_map_count=2147483642"
    #
    #
    #
    # DaVinci Resolve
    #
    alias convertmp4="find . -name '*.[mM][pP]4' -execdir ffmpeg -i '{}' -c:v mpeg4 -qscale:v 1 -c:a pcm_s32le {}-davinci.mov \;"
    alias convertmkv="find . -name '*.[mM][kK][vV]' -execdir ffmpeg -i '{}' -c:v mpeg4 -qscale:v 1 -c:a pcm_s32le {}-davinci.mov \;"
    alias convertmov="find . -name '*.[mM][oO][vV]' -execdir ffmpeg -i '{}' -c:v mpeg4 -qscale:v 1 -c:a pcm_s32le {}-davinci.mov \;"
    alias davinciconvdir="mkdir davinci;find . -name '*davinci.mov' -execdir mv {} ./davinci/ \;|cd davinci;rm -rf *'davinci.mov-davinci.mov'"
    alias convertall="convertmp4 && convertmkv && convertmov && davinciconvdir"
    #
    #
    #
```

