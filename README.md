# Source

```sh
alias "ㅊㅇ"="cd"
alias "챙ㄷ"="code"

# Directories
alias ..="cd ../"
alias ...="cd ../../"
alias ....="cd ../../../"
alias .....="cd ../../../../"
alias home="cd ~"
alias sites="cd ~/Sites"
alias slowquery="cd /usr/local/var/mysql/slowqueries/"

# Commands
alias ll='ls -FGlAhp'
alias finder="open -a 'Finder' ."
alias updatedb="sudo /usr/libexec/locate.updatedb"
alias hosts="sudo vi /etc/hosts"

# Various
alias localip="ifconfig | grep -Eo 'inet (addr:)?([0-9]*\.){3}[0-9]*' | grep -Eo '([0-9]*\.){3}[0-9]*' | grep -v '127.0.0.1'"
alias ip="curl icanhazip.com"
alias aliasup="source ~/.aliases"

# CakePHP
alias cbake='app/Console/cake bake'

# Laravel
alias ppu="./vendor/bin/phpunit"
alias art="php artisan"
alias packagistkr="composer config -g repos.packagist composer https://packagist.kr"
alias packagistorg="composer config -g --unset repos.packagist"

function routes()
{
    if [ $# -eq 0 ]; then
        php artisan route:list
    else
        php artisan route:list | grep ${1}
    fi
}

function port()
{
    if [ $# -eq 0 ]; then
        echo 'Port need.'
    else
        curl http://portquiz.net:${1}
    fi
}
```

# Usage

## .aliases

Add .zshrc

```sh
source ~/.aliases
```

and make .aliases into ~/ directory

# Example

## localip

```sh
➜  ~ localip
192.168.75.228
```

## ip

```sh
➜  ~ ip
123.123.123.123
```

## port

```sh
➜  ~ port 80
Port 80 test successful!
Your IP: 218.239.130.8

➜  ~ port 22
(If port 22 blocked, none)
```
