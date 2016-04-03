Debian
==

## First Steps

    Debian GNU/Linux 8 chip ttyGS0
    chip login: chip
    Password: chip
    Last login: Thu Jan  1 00:01:27 UTC 1970 on ttyGS0
    Linux chip 4.2.0-rc1 #1 SMP Tue Nov 3 07:09:51 UTC 2015 armv7l
    
    The programs included with the Debian GNU/Linux system are free software;
    the exact distribution terms for each program are described in the
    individual files in /usr/share/doc/*/copyright.
    
    Debian GNU/Linux comes with ABSOLUTELY NO WARRANTY, to the extent
    permitted by applicable law.
    chip@chip:~$ su
    Password: chip
    root@chip:/home/chip# cd
    root@chip:~# uname -a
    Linux chip 4.2.0-rc1 #1 SMP Wed Oct 21 20:43:17 UTC 2015 armv7l GNU/Linux
    root@chip:~# date -s "10/25/2015 18:41:30"
    root@chip:~# apt-get update
    root@chip:~# apt-get upgrade
    root@chip:~# dpkg-reconfigure tzdata # TimeZone
    root@chip:~# apt-get install wget htop git
    root@chip:~# apt-get install -f
    root@chip:~# hwtest

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

    root@chip:~# df -h
    Filesystem      Size  Used Avail Use% Mounted on
    ubi0:rootfs     3.6G  563M  3.1G  16% /
    devtmpfs        245M     0  245M   0% /dev
    tmpfs           246M     0  246M   0% /dev/shm
    tmpfs           246M  6.6M  239M   3% /run
    tmpfs           5.0M     0  5.0M   0% /run/lock
    tmpfs           246M     0  246M   0% /sys/fs/cgroup
    tmpfs            50M     0   50M   0% /run/user/0
    root@chip:~# cat /proc/cpuinfo
    processor	: 0
    model name	: ARMv7 Processor rev 2 (v7l)
    BogoMIPS	: 1001.88
    Hardware	: Allwinner sun4i/sun5i Families
    root@chip:~# cat /proc/meminfo | head
    MemTotal:         501884 kB
    MemFree:          129604 kB
    MemAvailable:     431712 kB
    Buffers:               0 kB
    root@chip:~# htop
    Mem: 34452K used, 468024K free, 88K shrd, 0K buff, 8148K cached
    CPU:   0% usr   0% sys   0% nic  99% idle   0% io   0% irq   0% sirq
    Load average: 0.00 0.01 0.05 1/48 179
      PID  PPID USER     STAT   VSZ %VSZ %CPU COMMAND
      179   163 root     R     2092   0%   0% top
      120     1 root     S     5944   1%   0% /usr/sbin/connmand -n
      121     1 root     S     5748   1%   0% /usr/sbin/wpa_supplicant -u
      138     1 root     S     4348   1%   0% /usr/sbin/sshd
      162     1 root     S     3676   1%   0% /usr/libexec/bluetooth/bluetoothd
      101     1 dbus     S     2232   0%   0% dbus-daemon --system
      163     1 root     S     2092   0%   0% -sh
      164     1 root     S     1992   0%   0% /sbin/getty -L tty0 115200 vt100
      161     1 root     S     1992   0%   0% /sbin/getty -L ttyS0 115200 vt100
        1     0 root     S     1988   0%   0% init
       83     1 root     S     1988   0%   0% /sbin/syslogd -n
       85     1 root     S     1988   0%   0% /sbin/klogd -n
      156     1 root     S     1408   0%   0% /sbin/rtk_hciattach -n -s 115200 /dev/
       66     2 root     SW       0   0%   0% [kworker/u2:4]
       20     2 root     SW       0   0%   0% [kworker/0:1]
       12     2 root     SW       0   0%   0% [kdevtmpfs]
       70     2 root     SW       0   0%   0% [ubi_bgt0d]
        7     2 root     SW       0   0%   0% [rcu_sched]
       18     2 root     SW<      0   0%   0% [bioset]
       21     2 root     SW       0   0%   0% [kswapd0]
       
## Secure Shell

    root@chip:~# apt-get install openssh-server openssh-client

## WiFi

    root@chip:~# nmcli device wifi list
    *  SSID             MODE   CHAN  RATE       SIGNAL  BARS  SECURITY  
       INFINITUMfjph    Infra  1     54 Mbit/s  62      ▂___  WPA1 WPA2 
       INFINITUM8240C7  Infra  11    54 Mbit/s  55      ▂▄__  WPA1 WPA2 
       17057Abril       Infra  6     54 Mbit/s  50      ▂▄__  WPA1 WPA2 
       INFINITUMndjj    Infra  2     54 Mbit/s  47      ▂▄__  WPA1 WPA2 
       INFINITUMf89t    Infra  9     54 Mbit/s  47      ▂▄__  WPA1 WPA2 
       INFINITUM6d6f    Infra  4     54 Mbit/s  30      ▂___  WPA1 WPA2 
       --               Infra  1     54 Mbit/s  72      ▂▄▆_  --        
       INFINITUME75B40  Infra  6     54 Mbit/s  29      ▂___  WPA1 WPA2 
    
    *  SSID             MODE   CHAN  RATE       SIGNAL  BARS  SECURITY  
       INFINITUMfjph    Infra  1     54 Mbit/s  62      ▂___  WPA1 WPA2 
       INFINITUM8240C7  Infra  11    54 Mbit/s  55      ▂▄__  WPA1 WPA2 
       17057Abril       Infra  6     54 Mbit/s  50      ▂▄__  WPA1 WPA2 
       INFINITUMndjj    Infra  2     54 Mbit/s  47      ▂▄__  WPA1 WPA2 
       INFINITUMf89t    Infra  9     54 Mbit/s  47      ▂▄__  WPA1 WPA2 
       INFINITUM6d6f    Infra  4     54 Mbit/s  17      ▂___  WPA1 WPA2 
       --               Infra  1     54 Mbit/s  72      ▂▄▆_  --        
       INFINITUME75B40  Infra  6     54 Mbit/s  29      ▂___  WPA1 WPA2 
    root@chip:~# nmcli device wifi connect INFINITUMf password 1c28 ifname wlan0
    root@chip:~# nmcli device wifi connect INFINITUMf ifname wlan0
    Connection with UUID '...5d288d5d...' created and activated on device 'wlan0'
    root@chip:~# nmcli device status
    DEVICE   TYPE      STATE         CONNECTION    
    wlan0    wifi      connected     -- 
    wlan1    wifi      disconnected  --            
    ip6tnl0  ip6tnl    unmanaged     --            
    lo       loopback  unmanaged     --            
    sit0     sit       unmanaged     --            
    root@chip:~# nmcli connection show --active
    NAME           UUID                                  TYPE             DEVICE 
    --             dbdf4061-9b7f-4dc2-82aa-5d288d5d15f0  802-11-wireless  wlan0  
    root@chip:~# ping 8.8.8.8
    PING 8.8.8.8 (8.8.8.8) 56(84) bytes of data.
    64 bytes from 8.8.8.8: icmp_seq=2 ttl=57 time=23.6 ms
    ^C
    --- 8.8.8.8 ping statistics ---
    2 packets transmitted, 1 received, 50% packet loss, time 1003ms
    rtt min/avg/max/mdev = 23.637/23.637/23.637/0.000 ms
    
- [Installing Zero Configuration Networking](https://nextthingco.zendesk.com/hc/en-us/articles/212946627-Installing-Zero-Configuration-Networking)

## Audio

sunxi-codec as hardware

    root@chip:~# apt-get install libasound2 alsa-utils mplayer2
    root@chip:~# alsamixer
    root@chip:~# apt-get install portaudio19-dev
    root@chip:~# apt-get install swig
    root@chip:~# apt-get install python-setuptools
    root@chip:~# apt-get install python-dev
    root@chip:~# aplay -lL
    ...
    **** List of PLAYBACK Hardware Devices ****
    card 0: sunxicodec [sunxi-codec], device 0: CDC PCM Codec-0 []
      Subdevices: 1/1
      Subdevice #0: subdevice #0
    root@chip:~# arecord -lL
    ...
    **** List of CAPTURE Hardware Devices ****
    card 0: sunxicodec [sunxi-codec], device 0: CDC PCM Codec-0 []
      Subdevices: 1/1
      Subdevice #0: subdevice #0

    root@chip:~# cat /proc/asound/cards
     0 [sunxicodec     ]: sunxi-codec - sunxi-codec
                          sunxi-codec
    root@chip:~# arecord -f cd -D plughw:0,0 -d 20 test.wav
    Recording WAVE 'test.wav' : Signed 16 bit Little Endian, Rate 44100 Hz, Stereo
    ^CAborted by signal Interrupt...
    root@chip:~# aplay -D hw:0,0 test.wav
    Playing WAVE 'test.wav' : Signed 16 bit Little Endian, Rate 44100 Hz, Stereo

### Testing

    chip@chip:~$ wget -O test.wav https://upload.wikimedia.org/wikipedia/commons/d/db/Descending_thirds.wav
    chip@chip:~$ wget -O test.ogg https://upload.wikimedia.org/wikipedia/commons/e/e7/Agogo.ogg
    chip@chip:~$ mplayer test.ogg
    chip@chip:~$ wget -O test.mp3 http://www.freesound.org/data/previews/315/315618_2050105-lq.mp3
    chip@chip:~$ mplayer test.mp3
    
- [Next Thing Co. Sound Output on Debian ](https://nextthingco.zendesk.com/hc/en-us/articles/212946707-Sound-Output-on-Debian)

## Virtual Network Computing

> In computing, Virtual Network Computing (VNC) is a graphical desktop sharing system that uses the Remote Frame Buffer protocol (RFB) to remotely control another computer. It transmits the keyboard and mouse events from one computer to another, relaying the graphical screen updates back in the other direction, over a network. Wikipedia

### VNC Server @ CHIP X Desktop

    root@chip:~# apt-get install xfce4
    root@chip:~# apt-get install vnc4server
    chip@chip:~$ vnc4passwd 
    Password:
    Verify:
    chip@chip:~$ vnc4server -geometry 800x600 -depth 24
    xauth:  file /home/chip/.Xauthority does not exist
    xauth: (stdin):1:  bad display name "chip:1" in "add" command
    
    New 'chip:1 (chip)' desktop is chip:1
    
    Creating default startup script /home/chip/.vnc/xstartup
    Starting applications specified in /home/chip/.vnc/xstartup
    Log file is /home/chip/.vnc/chip:1.log

### VNC Server @ CHIP Default Desktop

    chip@chip:~$ vnc4server -kill :1
    Killing Xvnc4 process ID 18807
    chip@chip:~$ nano ~/.vnc/xstartup                         
    #!/bin/sh
    # Uncomment the following two lines for normal desktop:
    unset SESSION_MANAGER 
    exec /etc/X11/xinit/xinitrc 
    ...
    chip@chip:~$ vnc4server -geometry 800x600 -depth 24
    xauth: (stdin):1:  bad display name "chip:1" in "add" command
    
    New 'chip:1 (chip)' desktop is chip:1
    
    Starting applications specified in /home/chip/.vnc/xstartup
    Log file is /home/chip/.vnc/chip:1.log

### VNC Viewer @ Host
    
    root@jessie:/home/xe1gyq# apt-get install xvnc4viewer
    Reading package lists... Done
    Building dependency tree       
    Reading state information... Done
    xvnc4viewer is already the newest version.
    0 upgraded, 0 newly installed, 0 to remove and 109 not upgraded.
    root@jessie:/home/xe1gyq# exit
    exit
    xe1gyq@jessie:~$ xvnc4viewer 192.168.1.77:1

## My Stuff

    root@chip:~# apt-get update
    root@chip:~# apt-get install git
    chip@chip:~$ git clone https://github.com/xe1gyq/Intel.IoT.Roadshow.git
    chip@chip:~$ cd Intel.IoT.Roadshow/2015
    chip@chip:~/Intel.IoT.Roadshow$ git clone https://github.com/xe1gyq/core.git
    root@chip:/home/chip/Intel.IoT.Roadshow/2015# apt-get install python-pip
    root@chip:/home/chip/Intel.IoT.Roadshow/2015# pip install plotly
    chip@chip:~/Intel.IoT.Roadshow/2015$ python core/xplotly.py

## Software Define Radio

    root@chip:~# apt-get update
    root@chip:~# apt-get install gnuradio gnuradio-dev
    root@chip:~# apt-get install rtl-sdr gr-osmosdr

