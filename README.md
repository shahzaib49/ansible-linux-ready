# ansible-linux-ready
A small ansible role to make your linux basic packages installtion easy.

## Context 

Usually all the time i have to work with linux and mostly debian. From the past 4 years every time i had to work on a debian machine i had to install all basic usage packages from scratch. So, I decided to start writing small playbooks for every group of packages i need for most of my machines. This is the most basic ansible role to install packages like 

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
