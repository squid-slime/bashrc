# ~/.bashrc
#

# If not running interactively, don't do anything
[[ $- != *i* ]] && return

[[ $- == *i* ]] && source /usr/share/blesh/ble.sh # --noattach

export EDITOR=/usr/bin/nvim
export VISUAL='nano'
export TERM=xterm-256color

PS1='\[\033[7;32m\]\u@\h \[\033[1;34m\]\d \t \[\033[0;36m\]\w\[\033[0m\]\n\$ \[\033[0m\]' 

if [ $TILIX_ID ] || [ $VTE_VERSION ]; then
        source /etc/profile.d/vte.sh
fi

if [ "$(tty)" = "/dev/tty1" ]; then
        exec dbus-run-session sway
fi

installed() {
    pacman -Qs "$1" | awk -F/ '/^local/ {print $2}' | cut -d' ' -f 1
}

#Aliases
alias htop='btop'${pur}
alias webapp='nativefier'${pur}
alias ls='ls --color=auto'
alias grc='grc --colour=auto'
alias tui="python /home/squid/Documents/pyrunthis"
alias openjpeg='swayimg'
alias openpng='swayimg'
alias jc141='/mnt/f45d633c-17e0-4601-979f-d3976a79a4fb/Games/luancher.sh'

[[ ${BLE_VERSION-} ]] && ble-attach
