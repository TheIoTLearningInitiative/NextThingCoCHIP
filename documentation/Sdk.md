SDK
==

[Installing CHIP SDK](https://nextthingco.zendesk.com/hc/en-us/articles/210863457-Installing-C-H-I-P-SDK-)

## CHIP SDK

### Install VirtualBox 4.3
    
```sh
# nano /etc/apt/sources.list
deb http://download.virtualbox.org/virtualbox/debian vivid contrib
# cd
# wget -q https://www.virtualbox.org/download/oracle_vbox.asc -O- | apt-key add -
# apt-get update
# apt-get install virtualbox-5.0
# apt-get install dkms
```

### Install VirtualBox Extension Pack 4.3

[VirtualBox Extension Pack 4.3](http://download.virtualbox.org/virtualbox/4.3.30/Oracle_VM_VirtualBox_Extension_Pack-4.3.30-101610.vbox-extpack)

### Install Vagrant

```sh
# apt-get install install vagrant
```

### Install Git

```sh
# apt-get install git
```

### Install CHIP-SDK

```sh
$ git clone https://github.com/NextThingCo/CHIP-SDK
```

### Virtual Machine Startup

```sh
$ cd CHIP-SDK
$ vagrant up
$ vagrant ssh
vagrant@vagrant-ubuntu-trusty-32:~$ 
```

### Ubuntu Setup

```sh
vagrant@vagrant-ubuntu-trusty-32:~$ ./CHIP-SDK/setup_ubuntu1404.sh

### Virtual Machine Exit

```sh
vagrant@vagrant-ubuntu-trusty-32:~$ vagrant plugin install vagrant-vbguest
vagrant@vagrant-ubuntu-trusty-32:~$ exit
$ vagrant halt
```

## Issues

In Buildroot

```sh
vagrant@vagrant-ubuntu-trusty-32:~$ usermod -a -G dialout vagrant
vagrant@vagrant-ubuntu-trusty-32:~$ adduser vagrant dialout
vagrant@vagrant-ubuntu-trusty-32:~$ chmod 666 /dev/ttyACM0
vagrant@vagrant-ubuntu-trusty-32:~$ cu -l /dev/ttyACM0 -s 115200
```

## Links

- http://pastebin.com/w5pDhHAe
- https://github.com/NextThingCo/
- https://bbs.nextthing.co/t/unable-to-flash-alpha-c-h-i-p/544/41




