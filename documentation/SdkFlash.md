SDK Flash
==

# Virtual Machine Startup

    # cd CHIP-SDK
    # vagrant up
    # vagrant ssh
    vagrant@vagrant-ubuntu-trusty-32:~$

# Fel

    vagrant@vagrant-ubuntu-trusty-32:~$ cd ~/
    vagrant@vagrant-ubuntu-trusty-32:~$ sudo rm -r ~/sunxi-tools
    vagrant@vagrant-ubuntu-trusty-32:~$ git clone https://github.com/NextThingCo/sunxi-tools.git
    vagrant@vagrant-ubuntu-trusty-32:~$ cd sunxi-tools
    vagrant@vagrant-ubuntu-trusty-32:~$ make
    vagrant@vagrant-ubuntu-trusty-32:~$ sudo rm /usr/local/bin/fel
    vagrant@vagrant-ubuntu-trusty-32:~$ sudo ln -s $PWD/fel /usr/local/bin/fel

## Trees Update
    
    vagrant@vagrant-ubuntu-trusty-32:~$ cd ~/CHIP-tools
    vagrant@vagrant-ubuntu-trusty-32:~$ git pull https://github.com/NextThingCo/CHIP-tools.git
    vagrant@vagrant-ubuntu-trusty-32:~$ cd ~/CHIP-SDK
    vagrant@vagrant-ubuntu-trusty-32:~$ git pull https://github.com/NextThingCo/CHIP-SDK.git
    
## Buildroot

    vagrant@vagrant-ubuntu-trusty-32:~$ cd ~/CHIP-tools
    vagrant@vagrant-ubuntu-trusty-32:~$ ./chip-update-firmware.sh

## Debian

    vagrant@vagrant-ubuntu-trusty-32:~$ cd ~/CHIP-tools
    vagrant@vagrant-ubuntu-trusty-32:~$ ./chip-update-firmware.sh -d


