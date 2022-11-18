# ansible-linux-ready
A small ansible role to make your linux basic packages installtion easy.

## Context 

Usually all the time i have to work with linux and mostly debian. From the past 4 years every time i had to work on a debian machine i had to install all basic usage packages from scratch. So, I decided to start writing small playbooks for every group of packages i need for most of my machines. This is the most basic ansible role to install packages of my daily usage and fixing a mouse related vim issue and also adding a beautiful footer in screen. 


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
