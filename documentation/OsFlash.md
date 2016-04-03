OS Flash
==

https://nextthingco.zendesk.com/hc/en-us/categories/200881468-C-H-I-P-

## Linux Host

### Dependencies

    # apt-get update
    # sudo apt-get install u-boot-tools android-tools-fastboot git build-essential libusb-1.0-0-dev

### SunXi Tools

    $ git clone http://github.com/linux-sunxi/sunxi-tools
    $ cd sunxi-tools
    $ make
    # sudo rm -f /usr/local/bin/fel
    # ln -s $PWD/fel /usr/local/bin/fel
    or
    # cp fel /usr/local/bin/

### Build Tools

    # exit
    $ cd ..
    $ git clone http://github.com/NextThingCo/CHIP-tools
    $ cd CHIP-tools
    $ git pull

### Flash Buildroot
    
    # ./chip-update-firmware.sh
    ...
    589824 bytes (590 kB) copied, 0.0244674 s, 24.1 MB/s
    12+0 records in
    12+0 records out
    196608 bytes (197 kB) copied, 0.0348495 s, 5.6 MB/s
    Image Name:   flash CHIP
    Created:      Sat Oct 10 07:49:05 2015
    Image Type:   ARM Linux Script (uncompressed)
    Data Size:    856 Bytes = 0.84 kB = 0.00 MB
    Load Address: 00000000
    Entry Point:  00000000
    Contents:
       Image 0: 848 Bytes = 0.83 kB = 0.00 MB
    == upload the SPL to SRAM and execute it ==
    == upload images ==
    == execute the main u-boot binary ==
    $ cu -l /dev/ttyACM0 -s 115200
    Connected.
    
    The source code can be downloaded from:
    http://opensource.nextthing.co/chip/buildroot/stable/68/build68.tar.gz
    
    chip login: root
    Password: 
    # hwtest
    
    
    ############################################################
    # [ CHIP HW TEST ]                                         #
    ############################################################
    
    # Turn on wlan0...OK
    # Turn on wlan1...OK
    # Hardware list...OK      
    # I2C bus 0...OK
    # I2C bus 1...OK
    # I2C bus 2...OK
    # testing AXP209 on I2C bus 0...OK
    # GPIO expander test...OK
    # Doing 10s stress test...OK
    # Wifi enumeration test...OK
    ### ALL TESTS PASSED ###
    # 

### Flash Debian
    
    # ./chip-update-firmware.sh -d
    debian selected
    ROOTFS_URL=http://opensource.nextthing.co.s3.amazonaws.com/chip/debian/stable/38
    BUILD=38
    ...
    BUILDROOT_OUTPUT_DIR = /home/xe1gyq/Projects/chip/CHIP-tools/.firmware
    == preparing images ==
    /home/xe1gyq/Projects/chip/CHIP-tools /home/xe1gyq/Projects/chip/CHIP-tools
    gcc    -c -o spl-image-builder.o spl-image-builder.c
    gcc -o spl-image-builder spl-image-builder.o
    /home/xe1gyq/Projects/chip/CHIP-tools
    ...
    == upload the SPL to SRAM and execute it ==
    waiting for fel...............................OK
    == upload spl ==
    == upload u-boot ==
    == upload u-boot script ==
    == upload ubi ==
    100% [============================================================] 
    == execute the main u-boot binary ==
    == write ubi ==
    flashing............................OK
    ...
    $ sudo cu -l /dev/ttyACM17 -s 115200
    [sudo] password for xe1gyq: 
    Connected.
    ebian GNU/Linux 8 chip ttyGS0

    chip login: root
    Password: 
    Linux chip 4.2.0-rc1 #1 SMP Wed Oct 21 20:43:17 UTC 2015 armv7l
    
    The programs included with the Debian GNU/Linux system are free software;
    the exact distribution terms for each program are described in the
    individual files in /usr/share/doc/*/copyright.
    
    Debian GNU/Linux comes with ABSOLUTELY NO WARRANTY, to the extent
    permitted by applicable law.
    root@chip:~# 

### At CHIP

    # hwtest

    ############################################################
    # [ CHIP HW TEST ]                                         #
    ############################################################
    
    # Turn on wlan0...OK
    # Turn on wlan1...OK
    # Hardware list...OK      
    # I2C bus 0...OK
    # I2C bus 1...OK
    # I2C bus 2...OK
    # testing AXP209 on I2C bus 0...OK
    # GPIO expander test...OK
    # Doing 10s stress test...OK
    # Wifi enumeration test...OK
    ### ALL TESTS PASSED ###



