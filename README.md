# ansible-linux-ready
A small ansible role to make your linux basic packages installtion easy.

## Context 

Usually, all the time I have to work with Linux and mostly Debian. For the past 4 years every time I had to work on a Debian machine I had to install all basic usage packages from scratch. So, I decided to start writing small playbooks for every group of packages I need for most of my machines. This is the most basic ansible role to install packages of my daily usage, fix a mouse-related vim issue, and add a beautiful footer on screen. It's a work in progress

### Packages 
```
  - vim
  - net-tools
  - build-essential
  - htop
  - git
  - make 
  - cmake
  - apt-transport-https
  - ca-certificates
  - pkg-config
  - locate
  - screen
  - tcpdump
  - tshark
  - sngrep
```

### Vimrc changes 

```
runtime! defaults.vim
let g:skip_defaults_vim = 1
set mouse=
```

### Screenrc changes for Screen footer

```
autodetach on 
startup_message off 
hardstatus alwayslastline 
shelltitle 'bash'
hardstatus string '%{gk}[%{wk}%?%-Lw%?%{=b kR}(%{W}%n*%f %t%?(%u)%?%{=b kR})%{= w}%?%+Lw%?%? %{g}][%{d}%l%{g}][ %{= w}%Y/%m/%d %0C:%s%a%{g} ]%{W}'
```

### How to use this ?

Just clone this repo in your ansible machine and change the the ip of the host in inventry file in tests directory(You can add multiple hosts in new lines). Keep in mind these hosts should accessible over ssh without password from ansible.

Copy the linuxready-playbook.yaml and inventry file from tests directory to main directory and use below command.

```
ansible-playbook -i inventory linuxready-playbook.yaml
```
