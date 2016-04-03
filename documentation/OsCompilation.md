Os Compilation
==

## Vagrant Up

    $ cd CHIP-SDK
    $ vagrant up
    $ vagrant ssh

## Buildroot Image, Building

    vagrant@vagrant-ubuntu-trusty-32:~$ cd ~/CHIP-buildroot
    vagrant@vagrant-ubuntu-trusty-32:~$ make chip_defconfig
    ...
    # configuration written to /home/vagrant/CHIP-buildroot/.config
    ...
    vagrant@vagrant-ubuntu-trusty-32:~$ make nconfig
    vagrant@vagrant-ubuntu-trusty-32:~$ make
    mkdir -p /home/vagrant/CHIP-buildroot/output/target
    ...
    ...
    ubinize: volume size was not specified in section "ubifs", assume minimum to fit image "/home/vagrant/CHIP-buildroot/output/images/rootfs.ubifs"49545216 bytes (47.2 MiB)
    /usr/bin/install -m 0644 support/misc/target-dir-warning.txt /home/vagrant/CHIP-buildroot/output/target/THIS_IS_NOT_YOUR_ROOT_FILESYSTEM
    vagrant@vagrant-ubuntu-trusty-32:~$ ls /home/vagrant/CHIP-buildroot/.config

# Fel

    vagrant@vagrant-ubuntu-trusty-32:~$ cd ~/
    vagrant@vagrant-ubuntu-trusty-32:~$ sudo rm -r ~/sunxi-tools
    vagrant@vagrant-ubuntu-trusty-32:~$ git clone https://github.com/NextThingCo/sunxi-tools.git
    vagrant@vagrant-ubuntu-trusty-32:~$ cd sunxi-tools
    vagrant@vagrant-ubuntu-trusty-32:~$ make
    vagrant@vagrant-ubuntu-trusty-32:~$ sudo rm /usr/local/bin/fel
    vagrant@vagrant-ubuntu-trusty-32:~$ sudo ln -s $PWD/fel /usr/local/bin/fel


## Buildroot Image, Flashing

    vagrant@vagrant-ubuntu-trusty-32:~$ cd ~/CHIP-tools
    vagrant@vagrant-ubuntu-trusty-32:~$ BUILDROOT_OUTPUT_DIR=../CHIP-buildroot/output ./chip-fel-flash.sh
    BUILDROOT_OUTPUT_DIR = ../CHIP-buildroot/output
    == preparing images ==
    filesize= 3573504
    PADDED_SPL_SIZE=0x000000c6
    ...


### BuildRoot Flash, Old Method

    vagrant@vagrant-ubuntu-trusty-32:~/CHIP-buildroot$ scp -r ../CHIP-buildroot/output/images/ xe1gyq@192.168.1.73:/home/xe1gyq/
    # cd CHIP-tools/.firmware/images
    CHIP-tools/.firmware/images# cp /home/xe1gyq/images/rootfs.ubi .
    CHIP-tools/.firmware/images# cp /home/xe1gyq/images/sun5i-r8-chip.dtb .
    CHIP-tools/.firmware/images# cp /home/xe1gyq/images/sunxi-spl.bin .
    CHIP-tools/.firmware/images# cp /home/xe1gyq/images/u-boot-dtb.bin .
    CHIP-tools/.firmware/images# cp /home/xe1gyq/images/uboot-env.bin .
    CHIP-tools/.firmware/images# cp /home/xe1gyq/images/zImage .
    <Disconnect CHIP>
    <Connect CHIP>
    # cd CHIP-tools
    CHIP-tools$ ./chip-update-firmware.sh
    CHIP-tools$ cu -l /dev/ttyACM0 -s 115200
    <To Validate>
    # cd ~/CHIP-tools
    # BUILDROOT_OUTPUT_DIR=../CHIP-buildroot/output ./chip-fel-flash.sh


## Chroot Debian Tree

- [Flash C.H.I.P. from C.H.I.P. SDK! (Virtual Machine) ](https://nextthingco.zendesk.com/hc/en-us/articles/210864097-Flash-C-H-I-P-from-C-H-I-P-SDK-Virtual-Machine-)
- [Free Electrons Buildroot Training ](http://free-electrons.com/doc/training/buildroot/buildroot-slides.pdf)
- http://www.raspibo.org/wiki/index.php/Chip9%24_How_to_install_a_chroot_Debian_tree


