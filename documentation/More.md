```sh
########################################################################################
# 
# Installing CHIP-SDK
#
########################################################################################

bokbokbok% vagrant up
Bringing machine 'default' up with 'virtualbox' provider...
==> default: Box 'ubuntu/trusty32' could not be found. Attempting to find and install...
    default: Box Provider: virtualbox
    default: Box Version: >= 0
==> default: Loading metadata for box 'ubuntu/trusty32'
    default: URL: https://atlas.hashicorp.com/ubuntu/trusty32
==> default: Adding box 'ubuntu/trusty32' (v20151007.0.0) for provider: virtualbox
    default: Downloading: https://atlas.hashicorp.com/ubuntu/boxes/trusty32/versions/20151007.0.0/providers/virtualbox.box
==> default: Successfully added box 'ubuntu/trusty32' (v20151007.0.0) for 'virtualbox'!
==> default: Importing base box 'ubuntu/trusty32'...
==> default: Matching MAC address for NAT networking...
==> default: Checking if box 'ubuntu/trusty32' is up to date...
==> default: Setting the name of the VM: CHIP-SDK_default_1444419269042_40304
==> default: Clearing any previously set forwarded ports...
==> default: Clearing any previously set network interfaces...
==> default: Preparing network interfaces based on configuration...
    default: Adapter 1: nat
==> default: Forwarding ports...
    default: 22 => 2222 (adapter 1)
==> default: Running 'pre-boot' VM customizations...
==> default: Booting VM...
==> default: Waiting for machine to boot. This may take a few minutes...
    default: SSH address: 127.0.0.1:2222
    default: SSH username: vagrant
    default: SSH auth method: private key
    default: Warning: Connection timeout. Retrying...
    default:
    default: Vagrant insecure key detected. Vagrant will automatically replace
    default: this with a newly generated keypair for better security.
    default:
    default: Inserting generated public key within guest...
    default: Removing insecure key from the guest if it's present...
    default: Key inserted! Disconnecting and reconnecting using new SSH key...
==> default: Machine booted and ready!
==> default: Checking for guest additions in VM...
    default: The guest additions on this VM do not match the installed version of
    default: VirtualBox! In most cases this is fine, but in rare cases it can
    default: prevent things such as shared folders from working properly. If you see
    default: shared folder errors, please make sure the guest additions within the
    default: virtual machine match the version of VirtualBox you have installed on
    default: your host and reload your VM.
    default:
    default: Guest Additions Version: 4.3.10
    default: VirtualBox Version: 5.0
==> default: Mounting shared folders...
    default: /home/vagrant/CHIP-SDK => /Users/tod/projects/chip/CHIP-SDK
bokbokbok% vagrant ssh
Welcome to Ubuntu 14.04.3 LTS (GNU/Linux 3.13.0-65-generic i686)

 * Documentation:  https://help.ubuntu.com/

  System information as of Fri Oct  9 19:34:50 UTC 2015

  System load:  0.65              Processes:           79
  Usage of /:   2.7% of 39.34GB   Users logged in:     0
  Memory usage: 7%                IP address for eth0: 10.0.2.15
  Swap usage:   0%

  Graph this data and manage this system at:
    https://landscape.canonical.com/

  Get cloud support with Ubuntu Advantage Cloud Guest:
    http://www.ubuntu.com/business/services/cloud

0 packages can be updated.
0 updates are security updates.


vagrant@vagrant-ubuntu-trusty-32:~$ ./CHIP-SDK/setup_ubuntu1404.sh

 Setting up environment in Ubuntu 14.04
Hit http://security.ubuntu.com trusty-security InRelease
Ign http://archive.ubuntu.com trusty InRelease
Get:1 http://security.ubuntu.com trusty-security/main Sources [96.9 kB]
Get:2 http://archive.ubuntu.com trusty-updates InRelease [64.4 kB]
Hit http://archive.ubuntu.com trusty Release.gpg
Get:3 http://security.ubuntu.com trusty-security/universe Sources [31.0 kB]
Get:4 http://archive.ubuntu.com trusty-updates/main Sources [238 kB]
Hit http://security.ubuntu.com trusty-security/main i386 Packages
Hit http://security.ubuntu.com trusty-security/universe i386 Packages
Hit http://security.ubuntu.com trusty-security/main Translation-en
Hit http://security.ubuntu.com trusty-security/universe Translation-en
Get:5 http://archive.ubuntu.com trusty-updates/universe Sources [140 kB]
Get:6 http://archive.ubuntu.com trusty-updates/main i386 Packages [609 kB]
Get:7 http://archive.ubuntu.com trusty-updates/universe i386 Packages [324 kB]
Get:8 http://archive.ubuntu.com trusty-updates/main Translation-en [305 kB]
Get:9 http://archive.ubuntu.com trusty-updates/universe Translation-en [170 kB]
Hit http://archive.ubuntu.com trusty Release
Get:10 http://archive.ubuntu.com trusty/main Sources [1,064 kB]
Get:11 http://archive.ubuntu.com trusty/universe Sources [6,399 kB]
Hit http://archive.ubuntu.com trusty/main i386 Packages
Hit http://archive.ubuntu.com trusty/universe i386 Packages
Hit http://archive.ubuntu.com trusty/main Translation-en
Hit http://archive.ubuntu.com trusty/universe Translation-en
Ign http://archive.ubuntu.com trusty/main Translation-en_US
Ign http://archive.ubuntu.com trusty/universe Translation-en_US
Fetched 9,443 kB in 12s (784 kB/s)
Reading package lists... Done
Reading package lists... Done
Building dependency tree
Reading state information... Done
Note, selecting 'libncurses5-dev' instead of 'libncurses-dev'
The following extra packages will be installed:
  cmake-data crda dpkg-dev fontconfig-config fonts-dejavu-core g++ g++-4.8
  git-man iw libalgorithm-diff-perl libalgorithm-diff-xs-perl
  libalgorithm-merge-perl libarchive13 libdpkg-perl liberror-perl
  libexpat1-dev libfile-fcntllock-perl libfontconfig1 liblzo2-2 libnettle4
  libnl-3-200 libnl-genl-3-200 libpython-dev libpython2.7-dev
  libstdc++-4.8-dev libtcl8.6 libtinfo-dev libtk8.6 libusb-1.0-doc
  libutempter0 libxcb-shape0 libxft2 libxi6 libxinerama1 libxss1 libxtst6
  libxv1 libxxf86dga1 linux-firmware linux-image-extra-3.13.0-65-generic
  linux-image-generic mercurial-common python-chardet-whl python-colorama
  python-colorama-whl python-distlib python-distlib-whl python-html5lib
  python-html5lib-whl python-pip-whl python-requests-whl python-setuptools
  python-setuptools-whl python-six-whl python-urllib3-whl python-wheel
  python2.7-dev python3-pkg-resources tcl tcl8.6 tk tk8.6 wireless-regdb
  x11-utils xbitmaps xterm
Suggested packages:
  codeblocks eclipse debian-keyring g++-multilib g++-4.8-multilib gcc-4.8-doc
  libstdc++6-4.8-dbg git-daemon-run git-daemon-sysvinit git-doc git-el
  git-email git-gui gitk gitweb git-arch git-bzr git-cvs git-mediawiki git-svn
  lrzip ncurses-doc libstdc++-4.8-doc qct kdiff3 kdiff3-qt kompare meld tkcvs
  mgdiff python-mysqldb python-pygments python-genshi python-lxml
  python3-setuptools tcl-tclreadline mesa-utils xfonts-cyrillic
Recommended packages:
  wish python-dev-all
The following NEW packages will be installed:
  android-tools-fastboot build-essential cmake cmake-data crda cu
  device-tree-compiler dpkg-dev fontconfig-config fonts-dejavu-core g++
  g++-4.8 git git-man iw libalgorithm-diff-perl libalgorithm-diff-xs-perl
  libalgorithm-merge-perl libarchive13 libdpkg-perl liberror-perl
  libexpat1-dev libfile-fcntllock-perl libfontconfig1 liblzo2-2
  libncurses5-dev libnettle4 libnl-3-200 libnl-genl-3-200 libpython-dev
  libpython2.7-dev libstdc++-4.8-dev libtcl8.6 libtinfo-dev libtk8.6
  libusb-1.0-0-dev libusb-1.0-doc libutempter0 libxcb-shape0 libxft2 libxi6
  libxinerama1 libxss1 libxtst6 libxv1 libxxf86dga1 linux-firmware
  linux-image-extra-3.13.0-65-generic linux-image-extra-virtual
  linux-image-generic mercurial mercurial-common pkg-config python-chardet-whl
  python-colorama python-colorama-whl python-dev python-distlib
  python-distlib-whl python-html5lib python-html5lib-whl python-pip
  python-pip-whl python-requests-whl python-setuptools python-setuptools-whl
  python-six-whl python-urllib3-whl python-wheel python2.7-dev
  python3-pkg-resources tcl tcl8.6 tk tk8.6 u-boot-tools unzip wireless-regdb
  x11-utils xbitmaps xterm
0 upgraded, 81 newly installed, 0 to remove and 0 not upgraded.
Need to get 116 MB of archives.
After this operation, 340 MB of additional disk space will be used.
Get:1 http://archive.ubuntu.com/ubuntu/ trusty-updates/main liblzo2-2 i386 2.06-1.2ubuntu1.1 [49.9 kB]
Get:2 http://archive.ubuntu.com/ubuntu/ trusty/main libnettle4 i386 2.7.1-1 [125 kB]
Get:3 http://archive.ubuntu.com/ubuntu/ trusty-updates/main libarchive13 i386 3.1.2-7ubuntu2.1 [274 kB]
Get:4 http://archive.ubuntu.com/ubuntu/ trusty/main fonts-dejavu-core all 2.34-1ubuntu1 [1,024 kB]
Get:5 http://archive.ubuntu.com/ubuntu/ trusty-updates/main fontconfig-config all 2.11.0-0ubuntu4.1 [47.4 kB]
Get:6 http://archive.ubuntu.com/ubuntu/ trusty-updates/main libfontconfig1 i386 2.11.0-0ubuntu4.1 [124 kB]
Get:7 http://archive.ubuntu.com/ubuntu/ trusty/main libnl-3-200 i386 3.2.21-1 [45.1 kB]
Get:8 http://archive.ubuntu.com/ubuntu/ trusty/main libnl-genl-3-200 i386 3.2.21-1 [10.3 kB]
Get:9 http://archive.ubuntu.com/ubuntu/ trusty-updates/main libexpat1-dev i386 2.1.0-4ubuntu1.1 [112 kB]
Get:10 http://archive.ubuntu.com/ubuntu/ trusty-updates/main libpython2.7-dev i386 2.7.6-8ubuntu0.2 [21.8 MB]
Get:11 http://archive.ubuntu.com/ubuntu/ trusty/main libtcl8.6 i386 8.6.1-4ubuntu1 [827 kB]
Get:12 http://archive.ubuntu.com/ubuntu/ trusty/main libxft2 i386 2.3.1-2 [35.6 kB]
Get:13 http://archive.ubuntu.com/ubuntu/ trusty/main libxss1 i386 1:1.2.2-1 [8,566 B]
Get:14 http://archive.ubuntu.com/ubuntu/ trusty/main libtk8.6 i386 8.6.1-3ubuntu2 [670 kB]
Get:15 http://archive.ubuntu.com/ubuntu/ trusty/main libxcb-shape0 i386 1.10-2ubuntu1 [5,864 B]
Get:16 http://archive.ubuntu.com/ubuntu/ trusty-updates/main libxi6 i386 2:1.7.1.901-1ubuntu1.1 [27.3 kB]
Get:17 http://archive.ubuntu.com/ubuntu/ trusty/main libxinerama1 i386 2:1.1.3-1 [7,900 B]
Get:18 http://archive.ubuntu.com/ubuntu/ trusty/main libxtst6 i386 2:1.2.2-1 [13.8 kB]
Get:19 http://archive.ubuntu.com/ubuntu/ trusty/main libxv1 i386 2:1.0.10-1 [10.2 kB]
Get:20 http://archive.ubuntu.com/ubuntu/ trusty/main libxxf86dga1 i386 2:1.1.4-1 [13.3 kB]
Get:21 http://archive.ubuntu.com/ubuntu/ trusty-updates/main libstdc++-4.8-dev i386 4.8.4-2ubuntu1~14.04 [1,058 kB]
Get:22 http://archive.ubuntu.com/ubuntu/ trusty-updates/main g++-4.8 i386 4.8.4-2ubuntu1~14.04 [14.8 MB]
Get:23 http://archive.ubuntu.com/ubuntu/ trusty/main g++ i386 4:4.8.2-1ubuntu6 [1,500 B]
Get:24 http://archive.ubuntu.com/ubuntu/ trusty-updates/main libdpkg-perl all 1.17.5ubuntu5.4 [179 kB]
Get:25 http://archive.ubuntu.com/ubuntu/ trusty-updates/main dpkg-dev all 1.17.5ubuntu5.4 [726 kB]
Get:26 http://archive.ubuntu.com/ubuntu/ trusty/main build-essential i386 11.6ubuntu6 [4,824 B]
Get:27 http://archive.ubuntu.com/ubuntu/ trusty/main cmake-data all 2.8.12.2-0ubuntu3 [676 kB]
Get:28 http://archive.ubuntu.com/ubuntu/ trusty/main cmake i386 2.8.12.2-0ubuntu3 [2,641 kB]
Get:29 http://archive.ubuntu.com/ubuntu/ trusty/main wireless-regdb all 2013.02.13-1ubuntu1 [6,456 B]
Get:30 http://archive.ubuntu.com/ubuntu/ trusty/main crda i386 1.1.2-1ubuntu2 [14.7 kB]
Get:31 http://archive.ubuntu.com/ubuntu/ trusty/main liberror-perl all 0.17-1.1 [21.1 kB]
Get:32 http://archive.ubuntu.com/ubuntu/ trusty-updates/main git-man all 1:1.9.1-1ubuntu0.1 [698 kB]
Get:33 http://archive.ubuntu.com/ubuntu/ trusty-updates/main git i386 1:1.9.1-1ubuntu0.1 [2,511 kB]
Get:34 http://archive.ubuntu.com/ubuntu/ trusty/main iw i386 3.4-1 [51.9 kB]
Get:35 http://archive.ubuntu.com/ubuntu/ trusty/main libalgorithm-diff-perl all 1.19.02-3 [50.0 kB]
Get:36 http://archive.ubuntu.com/ubuntu/ trusty/main libalgorithm-diff-xs-perl i386 0.04-2build4 [13.1 kB]
Get:37 http://archive.ubuntu.com/ubuntu/ trusty/main libalgorithm-merge-perl all 0.08-2 [12.7 kB]
Get:38 http://archive.ubuntu.com/ubuntu/ trusty/main libfile-fcntllock-perl i386 0.14-2build1 [16.0 kB]
Get:39 http://archive.ubuntu.com/ubuntu/ trusty/main libtinfo-dev i386 5.9+20140118-1ubuntu1 [71.2 kB]
Get:40 http://archive.ubuntu.com/ubuntu/ trusty/main libncurses5-dev i386 5.9+20140118-1ubuntu1 [166 kB]
Get:41 http://archive.ubuntu.com/ubuntu/ trusty/main libpython-dev i386 2.7.5-5ubuntu3 [7,090 B]
Get:42 http://archive.ubuntu.com/ubuntu/ trusty/main libusb-1.0-0-dev i386 2:1.0.17-1ubuntu2 [52.7 kB]
Get:43 http://archive.ubuntu.com/ubuntu/ trusty/main libusb-1.0-doc all 2:1.0.17-1ubuntu2 [115 kB]
Get:44 http://archive.ubuntu.com/ubuntu/ trusty/main libutempter0 i386 1.1.5-4build1 [8,286 B]
Get:45 http://archive.ubuntu.com/ubuntu/ trusty-updates/main linux-firmware all 1.127.15 [24.3 MB]
Get:46 http://archive.ubuntu.com/ubuntu/ trusty-updates/main linux-image-extra-3.13.0-65-generic i386 3.13.0-65.106 [37.1 MB]
Get:47 http://archive.ubuntu.com/ubuntu/ trusty-updates/main linux-image-generic i386 3.13.0.65.71 [2,388 B]
Get:48 http://archive.ubuntu.com/ubuntu/ trusty-updates/main linux-image-extra-virtual i386 3.13.0.65.71 [1,762 B]
Get:49 http://archive.ubuntu.com/ubuntu/ trusty-updates/universe mercurial-common all 2.8.2-1ubuntu1.3 [1,520 kB]
Get:50 http://archive.ubuntu.com/ubuntu/ trusty-updates/universe mercurial i386 2.8.2-1ubuntu1.3 [39.5 kB]
Get:51 http://archive.ubuntu.com/ubuntu/ trusty/main pkg-config i386 0.26-1ubuntu4 [40.5 kB]
Get:52 http://archive.ubuntu.com/ubuntu/ trusty-updates/main python3-pkg-resources all 3.3-1ubuntu2 [31.7 kB]
Get:53 http://archive.ubuntu.com/ubuntu/ trusty-updates/universe python-chardet-whl all 2.2.1-2~ubuntu1 [170 kB]
Get:54 http://archive.ubuntu.com/ubuntu/ trusty-updates/universe python-colorama all 0.2.5-0.1ubuntu2 [18.4 kB]
Get:55 http://archive.ubuntu.com/ubuntu/ trusty-updates/universe python-colorama-whl all 0.2.5-0.1ubuntu2 [18.2 kB]
Get:56 http://archive.ubuntu.com/ubuntu/ trusty-updates/main python2.7-dev i386 2.7.6-8ubuntu0.2 [269 kB]
Get:57 http://archive.ubuntu.com/ubuntu/ trusty/main python-dev i386 2.7.5-5ubuntu3 [1,176 B]
Get:58 http://archive.ubuntu.com/ubuntu/ trusty-updates/universe python-distlib all 0.1.8-1ubuntu1 [113 kB]
Get:59 http://archive.ubuntu.com/ubuntu/ trusty-updates/universe python-distlib-whl all 0.1.8-1ubuntu1 [140 kB]
Get:60 http://archive.ubuntu.com/ubuntu/ trusty-updates/main python-html5lib all 0.999-3~ubuntu1 [83.5 kB]
Get:61 http://archive.ubuntu.com/ubuntu/ trusty-updates/main python-html5lib-whl all 0.999-3~ubuntu1 [109 kB]
Get:62 http://archive.ubuntu.com/ubuntu/ trusty-updates/main python-six-whl all 1.5.2-1ubuntu1 [10.5 kB]
Get:63 http://archive.ubuntu.com/ubuntu/ trusty-updates/main python-urllib3-whl all 1.7.1-1ubuntu3 [64.0 kB]
Get:64 http://archive.ubuntu.com/ubuntu/ trusty-updates/main python-requests-whl all 2.2.1-1ubuntu0.3 [227 kB]
Get:65 http://archive.ubuntu.com/ubuntu/ trusty-updates/main python-setuptools-whl all 3.3-1ubuntu2 [244 kB]
Get:66 http://archive.ubuntu.com/ubuntu/ trusty-updates/universe python-pip-whl all 1.5.4-1ubuntu3 [111 kB]
Get:67 http://archive.ubuntu.com/ubuntu/ trusty-updates/main python-setuptools all 3.3-1ubuntu2 [230 kB]
Get:68 http://archive.ubuntu.com/ubuntu/ trusty-updates/universe python-pip all 1.5.4-1ubuntu3 [97.2 kB]
Get:69 http://archive.ubuntu.com/ubuntu/ trusty-updates/main python-wheel all 0.24.0-1~ubuntu1 [44.7 kB]
Get:70 http://archive.ubuntu.com/ubuntu/ trusty/main tcl8.6 i386 8.6.1-4ubuntu1 [14.1 kB]
Get:71 http://archive.ubuntu.com/ubuntu/ trusty/main tcl i386 8.6.0+6ubuntu3 [4,884 B]
Get:72 http://archive.ubuntu.com/ubuntu/ trusty/main tk8.6 i386 8.6.1-3ubuntu2 [12.1 kB]
Get:73 http://archive.ubuntu.com/ubuntu/ trusty/main tk i386 8.6.0+6ubuntu3 [3,188 B]
Get:74 http://archive.ubuntu.com/ubuntu/ trusty/main u-boot-tools i386 2013.10-3 [59.7 kB]
Get:75 http://archive.ubuntu.com/ubuntu/ trusty-updates/main unzip i386 6.0-9ubuntu1.3 [150 kB]
Get:76 http://archive.ubuntu.com/ubuntu/ trusty/main x11-utils i386 7.7+1 [221 kB]
Get:77 http://archive.ubuntu.com/ubuntu/ trusty/main xbitmaps all 1.1.1-2 [28.1 kB]
Get:78 http://archive.ubuntu.com/ubuntu/ trusty/main xterm i386 297-1ubuntu1 [652 kB]
Get:79 http://archive.ubuntu.com/ubuntu/ trusty/universe android-tools-fastboot i386 4.2.2+git20130218-3ubuntu23 [45.5 kB]
Get:80 http://archive.ubuntu.com/ubuntu/ trusty/main cu i386 1.07-20.1 [70.0 kB]
Get:81 http://archive.ubuntu.com/ubuntu/ trusty/main device-tree-compiler i386 1.4.0+dfsg-1 [357 kB]
Fetched 116 MB in 32s (3,534 kB/s)
Extracting templates from packages: 100%
Selecting previously unselected package liblzo2-2:i386.
(Reading database ... 61102 files and directories currently installed.)
Preparing to unpack .../liblzo2-2_2.06-1.2ubuntu1.1_i386.deb ...
Unpacking liblzo2-2:i386 (2.06-1.2ubuntu1.1) ...
Selecting previously unselected package libnettle4:i386.
Preparing to unpack .../libnettle4_2.7.1-1_i386.deb ...
Unpacking libnettle4:i386 (2.7.1-1) ...
Selecting previously unselected package libarchive13:i386.
Preparing to unpack .../libarchive13_3.1.2-7ubuntu2.1_i386.deb ...
Unpacking libarchive13:i386 (3.1.2-7ubuntu2.1) ...
Selecting previously unselected package fonts-dejavu-core.
Preparing to unpack .../fonts-dejavu-core_2.34-1ubuntu1_all.deb ...
Unpacking fonts-dejavu-core (2.34-1ubuntu1) ...
Selecting previously unselected package fontconfig-config.
Preparing to unpack .../fontconfig-config_2.11.0-0ubuntu4.1_all.deb ...
Unpacking fontconfig-config (2.11.0-0ubuntu4.1) ...
Selecting previously unselected package libfontconfig1:i386.
Preparing to unpack .../libfontconfig1_2.11.0-0ubuntu4.1_i386.deb ...
Unpacking libfontconfig1:i386 (2.11.0-0ubuntu4.1) ...
Selecting previously unselected package libnl-3-200:i386.
Preparing to unpack .../libnl-3-200_3.2.21-1_i386.deb ...
Unpacking libnl-3-200:i386 (3.2.21-1) ...
Selecting previously unselected package libnl-genl-3-200:i386.
Preparing to unpack .../libnl-genl-3-200_3.2.21-1_i386.deb ...
Unpacking libnl-genl-3-200:i386 (3.2.21-1) ...
Selecting previously unselected package libexpat1-dev:i386.
Preparing to unpack .../libexpat1-dev_2.1.0-4ubuntu1.1_i386.deb ...
Unpacking libexpat1-dev:i386 (2.1.0-4ubuntu1.1) ...
Selecting previously unselected package libpython2.7-dev:i386.
Preparing to unpack .../libpython2.7-dev_2.7.6-8ubuntu0.2_i386.deb ...
Unpacking libpython2.7-dev:i386 (2.7.6-8ubuntu0.2) ...
Selecting previously unselected package libtcl8.6:i386.
Preparing to unpack .../libtcl8.6_8.6.1-4ubuntu1_i386.deb ...
Unpacking libtcl8.6:i386 (8.6.1-4ubuntu1) ...
Selecting previously unselected package libxft2:i386.
Preparing to unpack .../libxft2_2.3.1-2_i386.deb ...
Unpacking libxft2:i386 (2.3.1-2) ...
Selecting previously unselected package libxss1:i386.
Preparing to unpack .../libxss1_1%3a1.2.2-1_i386.deb ...
Unpacking libxss1:i386 (1:1.2.2-1) ...
Selecting previously unselected package libtk8.6:i386.
Preparing to unpack .../libtk8.6_8.6.1-3ubuntu2_i386.deb ...
Unpacking libtk8.6:i386 (8.6.1-3ubuntu2) ...
Selecting previously unselected package libxcb-shape0:i386.
Preparing to unpack .../libxcb-shape0_1.10-2ubuntu1_i386.deb ...
Unpacking libxcb-shape0:i386 (1.10-2ubuntu1) ...
Selecting previously unselected package libxi6:i386.
Preparing to unpack .../libxi6_2%3a1.7.1.901-1ubuntu1.1_i386.deb ...
Unpacking libxi6:i386 (2:1.7.1.901-1ubuntu1.1) ...
Selecting previously unselected package libxinerama1:i386.
Preparing to unpack .../libxinerama1_2%3a1.1.3-1_i386.deb ...
Unpacking libxinerama1:i386 (2:1.1.3-1) ...
Selecting previously unselected package libxtst6:i386.
Preparing to unpack .../libxtst6_2%3a1.2.2-1_i386.deb ...
Unpacking libxtst6:i386 (2:1.2.2-1) ...
Selecting previously unselected package libxv1:i386.
Preparing to unpack .../libxv1_2%3a1.0.10-1_i386.deb ...
Unpacking libxv1:i386 (2:1.0.10-1) ...
Selecting previously unselected package libxxf86dga1:i386.
Preparing to unpack .../libxxf86dga1_2%3a1.1.4-1_i386.deb ...
Unpacking libxxf86dga1:i386 (2:1.1.4-1) ...
Selecting previously unselected package libstdc++-4.8-dev:i386.
Preparing to unpack .../libstdc++-4.8-dev_4.8.4-2ubuntu1~14.04_i386.deb ...
Unpacking libstdc++-4.8-dev:i386 (4.8.4-2ubuntu1~14.04) ...
Selecting previously unselected package g++-4.8.
Preparing to unpack .../g++-4.8_4.8.4-2ubuntu1~14.04_i386.deb ...
Unpacking g++-4.8 (4.8.4-2ubuntu1~14.04) ...
Selecting previously unselected package g++.
Preparing to unpack .../g++_4%3a4.8.2-1ubuntu6_i386.deb ...
Unpacking g++ (4:4.8.2-1ubuntu6) ...
Selecting previously unselected package libdpkg-perl.
Preparing to unpack .../libdpkg-perl_1.17.5ubuntu5.4_all.deb ...
Unpacking libdpkg-perl (1.17.5ubuntu5.4) ...
Selecting previously unselected package dpkg-dev.
Preparing to unpack .../dpkg-dev_1.17.5ubuntu5.4_all.deb ...
Unpacking dpkg-dev (1.17.5ubuntu5.4) ...
Selecting previously unselected package build-essential.
Preparing to unpack .../build-essential_11.6ubuntu6_i386.deb ...
Unpacking build-essential (11.6ubuntu6) ...
Selecting previously unselected package cmake-data.
Preparing to unpack .../cmake-data_2.8.12.2-0ubuntu3_all.deb ...
Unpacking cmake-data (2.8.12.2-0ubuntu3) ...
Selecting previously unselected package cmake.
Preparing to unpack .../cmake_2.8.12.2-0ubuntu3_i386.deb ...
Unpacking cmake (2.8.12.2-0ubuntu3) ...
Selecting previously unselected package wireless-regdb.
Preparing to unpack .../wireless-regdb_2013.02.13-1ubuntu1_all.deb ...
Unpacking wireless-regdb (2013.02.13-1ubuntu1) ...
Selecting previously unselected package crda.
Preparing to unpack .../crda_1.1.2-1ubuntu2_i386.deb ...
Unpacking crda (1.1.2-1ubuntu2) ...
Selecting previously unselected package liberror-perl.
Preparing to unpack .../liberror-perl_0.17-1.1_all.deb ...
Unpacking liberror-perl (0.17-1.1) ...
Selecting previously unselected package git-man.
Preparing to unpack .../git-man_1%3a1.9.1-1ubuntu0.1_all.deb ...
Unpacking git-man (1:1.9.1-1ubuntu0.1) ...
Selecting previously unselected package git.
Preparing to unpack .../git_1%3a1.9.1-1ubuntu0.1_i386.deb ...
Unpacking git (1:1.9.1-1ubuntu0.1) ...
Selecting previously unselected package iw.
Preparing to unpack .../apt/archives/iw_3.4-1_i386.deb ...
Unpacking iw (3.4-1) ...
Selecting previously unselected package libalgorithm-diff-perl.
Preparing to unpack .../libalgorithm-diff-perl_1.19.02-3_all.deb ...
Unpacking libalgorithm-diff-perl (1.19.02-3) ...
Selecting previously unselected package libalgorithm-diff-xs-perl.
Preparing to unpack .../libalgorithm-diff-xs-perl_0.04-2build4_i386.deb ...
Unpacking libalgorithm-diff-xs-perl (0.04-2build4) ...
Selecting previously unselected package libalgorithm-merge-perl.
Preparing to unpack .../libalgorithm-merge-perl_0.08-2_all.deb ...
Unpacking libalgorithm-merge-perl (0.08-2) ...
Selecting previously unselected package libfile-fcntllock-perl.
Preparing to unpack .../libfile-fcntllock-perl_0.14-2build1_i386.deb ...
Unpacking libfile-fcntllock-perl (0.14-2build1) ...
Selecting previously unselected package libtinfo-dev:i386.
Preparing to unpack .../libtinfo-dev_5.9+20140118-1ubuntu1_i386.deb ...
Unpacking libtinfo-dev:i386 (5.9+20140118-1ubuntu1) ...
Selecting previously unselected package libncurses5-dev:i386.
Preparing to unpack .../libncurses5-dev_5.9+20140118-1ubuntu1_i386.deb ...
Unpacking libncurses5-dev:i386 (5.9+20140118-1ubuntu1) ...
Selecting previously unselected package libpython-dev:i386.
Preparing to unpack .../libpython-dev_2.7.5-5ubuntu3_i386.deb ...
Unpacking libpython-dev:i386 (2.7.5-5ubuntu3) ...
Selecting previously unselected package libusb-1.0-0-dev:i386.
Preparing to unpack .../libusb-1.0-0-dev_2%3a1.0.17-1ubuntu2_i386.deb ...
Unpacking libusb-1.0-0-dev:i386 (2:1.0.17-1ubuntu2) ...
Selecting previously unselected package libusb-1.0-doc.
Preparing to unpack .../libusb-1.0-doc_2%3a1.0.17-1ubuntu2_all.deb ...
Unpacking libusb-1.0-doc (2:1.0.17-1ubuntu2) ...
Selecting previously unselected package libutempter0.
Preparing to unpack .../libutempter0_1.1.5-4build1_i386.deb ...
Unpacking libutempter0 (1.1.5-4build1) ...
Selecting previously unselected package linux-firmware.
Preparing to unpack .../linux-firmware_1.127.15_all.deb ...
Unpacking linux-firmware (1.127.15) ...
Selecting previously unselected package linux-image-extra-3.13.0-65-generic.
Preparing to unpack .../linux-image-extra-3.13.0-65-generic_3.13.0-65.106_i386.deb ...
Unpacking linux-image-extra-3.13.0-65-generic (3.13.0-65.106) ...
Selecting previously unselected package linux-image-generic.
Preparing to unpack .../linux-image-generic_3.13.0.65.71_i386.deb ...
Unpacking linux-image-generic (3.13.0.65.71) ...
Selecting previously unselected package linux-image-extra-virtual.
Preparing to unpack .../linux-image-extra-virtual_3.13.0.65.71_i386.deb ...
Unpacking linux-image-extra-virtual (3.13.0.65.71) ...
Selecting previously unselected package mercurial-common.
Preparing to unpack .../mercurial-common_2.8.2-1ubuntu1.3_all.deb ...
Unpacking mercurial-common (2.8.2-1ubuntu1.3) ...
Selecting previously unselected package mercurial.
Preparing to unpack .../mercurial_2.8.2-1ubuntu1.3_i386.deb ...
Unpacking mercurial (2.8.2-1ubuntu1.3) ...
Selecting previously unselected package pkg-config.
Preparing to unpack .../pkg-config_0.26-1ubuntu4_i386.deb ...
Unpacking pkg-config (0.26-1ubuntu4) ...
Selecting previously unselected package python3-pkg-resources.
Preparing to unpack .../python3-pkg-resources_3.3-1ubuntu2_all.deb ...
Unpacking python3-pkg-resources (3.3-1ubuntu2) ...
Selecting previously unselected package python-chardet-whl.
Preparing to unpack .../python-chardet-whl_2.2.1-2~ubuntu1_all.deb ...
Unpacking python-chardet-whl (2.2.1-2~ubuntu1) ...
Selecting previously unselected package python-colorama.
Preparing to unpack .../python-colorama_0.2.5-0.1ubuntu2_all.deb ...
Unpacking python-colorama (0.2.5-0.1ubuntu2) ...
Selecting previously unselected package python-colorama-whl.
Preparing to unpack .../python-colorama-whl_0.2.5-0.1ubuntu2_all.deb ...
Unpacking python-colorama-whl (0.2.5-0.1ubuntu2) ...
Selecting previously unselected package python2.7-dev.
Preparing to unpack .../python2.7-dev_2.7.6-8ubuntu0.2_i386.deb ...
Unpacking python2.7-dev (2.7.6-8ubuntu0.2) ...
Selecting previously unselected package python-dev.
Preparing to unpack .../python-dev_2.7.5-5ubuntu3_i386.deb ...
Unpacking python-dev (2.7.5-5ubuntu3) ...
Selecting previously unselected package python-distlib.
Preparing to unpack .../python-distlib_0.1.8-1ubuntu1_all.deb ...
Unpacking python-distlib (0.1.8-1ubuntu1) ...
Selecting previously unselected package python-distlib-whl.
Preparing to unpack .../python-distlib-whl_0.1.8-1ubuntu1_all.deb ...
Unpacking python-distlib-whl (0.1.8-1ubuntu1) ...
Selecting previously unselected package python-html5lib.
Preparing to unpack .../python-html5lib_0.999-3~ubuntu1_all.deb ...
Unpacking python-html5lib (0.999-3~ubuntu1) ...
Selecting previously unselected package python-html5lib-whl.
Preparing to unpack .../python-html5lib-whl_0.999-3~ubuntu1_all.deb ...
Unpacking python-html5lib-whl (0.999-3~ubuntu1) ...
Selecting previously unselected package python-six-whl.
Preparing to unpack .../python-six-whl_1.5.2-1ubuntu1_all.deb ...
Unpacking python-six-whl (1.5.2-1ubuntu1) ...
Selecting previously unselected package python-urllib3-whl.
Preparing to unpack .../python-urllib3-whl_1.7.1-1ubuntu3_all.deb ...
Unpacking python-urllib3-whl (1.7.1-1ubuntu3) ...
Selecting previously unselected package python-requests-whl.
Preparing to unpack .../python-requests-whl_2.2.1-1ubuntu0.3_all.deb ...
Unpacking python-requests-whl (2.2.1-1ubuntu0.3) ...
Selecting previously unselected package python-setuptools-whl.
Preparing to unpack .../python-setuptools-whl_3.3-1ubuntu2_all.deb ...
Unpacking python-setuptools-whl (3.3-1ubuntu2) ...
Selecting previously unselected package python-pip-whl.
Preparing to unpack .../python-pip-whl_1.5.4-1ubuntu3_all.deb ...
Unpacking python-pip-whl (1.5.4-1ubuntu3) ...
Selecting previously unselected package python-setuptools.
Preparing to unpack .../python-setuptools_3.3-1ubuntu2_all.deb ...
Unpacking python-setuptools (3.3-1ubuntu2) ...
Selecting previously unselected package python-pip.
Preparing to unpack .../python-pip_1.5.4-1ubuntu3_all.deb ...
Unpacking python-pip (1.5.4-1ubuntu3) ...
Selecting previously unselected package python-wheel.
Preparing to unpack .../python-wheel_0.24.0-1~ubuntu1_all.deb ...
Unpacking python-wheel (0.24.0-1~ubuntu1) ...
Selecting previously unselected package tcl8.6.
Preparing to unpack .../tcl8.6_8.6.1-4ubuntu1_i386.deb ...
Unpacking tcl8.6 (8.6.1-4ubuntu1) ...
Selecting previously unselected package tcl.
Preparing to unpack .../tcl_8.6.0+6ubuntu3_i386.deb ...
Unpacking tcl (8.6.0+6ubuntu3) ...
Selecting previously unselected package tk8.6.
Preparing to unpack .../tk8.6_8.6.1-3ubuntu2_i386.deb ...
Unpacking tk8.6 (8.6.1-3ubuntu2) ...
Selecting previously unselected package tk.
Preparing to unpack .../tk_8.6.0+6ubuntu3_i386.deb ...
Unpacking tk (8.6.0+6ubuntu3) ...
Selecting previously unselected package u-boot-tools.
Preparing to unpack .../u-boot-tools_2013.10-3_i386.deb ...
Unpacking u-boot-tools (2013.10-3) ...
Selecting previously unselected package unzip.
Preparing to unpack .../unzip_6.0-9ubuntu1.3_i386.deb ...
Unpacking unzip (6.0-9ubuntu1.3) ...
Selecting previously unselected package x11-utils.
Preparing to unpack .../x11-utils_7.7+1_i386.deb ...
Unpacking x11-utils (7.7+1) ...
Selecting previously unselected package xbitmaps.
Preparing to unpack .../xbitmaps_1.1.1-2_all.deb ...
Unpacking xbitmaps (1.1.1-2) ...
Selecting previously unselected package xterm.
Preparing to unpack .../xterm_297-1ubuntu1_i386.deb ...
Unpacking xterm (297-1ubuntu1) ...
Selecting previously unselected package android-tools-fastboot.
Preparing to unpack .../android-tools-fastboot_4.2.2+git20130218-3ubuntu23_i386.deb ...
Unpacking android-tools-fastboot (4.2.2+git20130218-3ubuntu23) ...
Selecting previously unselected package cu.
Preparing to unpack .../archives/cu_1.07-20.1_i386.deb ...
Unpacking cu (1.07-20.1) ...
Selecting previously unselected package device-tree-compiler.
Preparing to unpack .../device-tree-compiler_1.4.0+dfsg-1_i386.deb ...
Unpacking device-tree-compiler (1.4.0+dfsg-1) ...
Processing triggers for man-db (2.6.7.1-1ubuntu1) ...
Processing triggers for mime-support (3.54ubuntu1.1) ...
Setting up liblzo2-2:i386 (2.06-1.2ubuntu1.1) ...
Setting up libnettle4:i386 (2.7.1-1) ...
Setting up libarchive13:i386 (3.1.2-7ubuntu2.1) ...
Setting up fonts-dejavu-core (2.34-1ubuntu1) ...
Setting up fontconfig-config (2.11.0-0ubuntu4.1) ...
Setting up libfontconfig1:i386 (2.11.0-0ubuntu4.1) ...
Setting up libnl-3-200:i386 (3.2.21-1) ...
Setting up libnl-genl-3-200:i386 (3.2.21-1) ...
Setting up libexpat1-dev:i386 (2.1.0-4ubuntu1.1) ...
Setting up libpython2.7-dev:i386 (2.7.6-8ubuntu0.2) ...
Setting up libtcl8.6:i386 (8.6.1-4ubuntu1) ...
Setting up libxft2:i386 (2.3.1-2) ...
Setting up libxss1:i386 (1:1.2.2-1) ...
Setting up libtk8.6:i386 (8.6.1-3ubuntu2) ...
Setting up libxcb-shape0:i386 (1.10-2ubuntu1) ...
Setting up libxi6:i386 (2:1.7.1.901-1ubuntu1.1) ...
Setting up libxinerama1:i386 (2:1.1.3-1) ...
Setting up libxtst6:i386 (2:1.2.2-1) ...
Setting up libxv1:i386 (2:1.0.10-1) ...
Setting up libxxf86dga1:i386 (2:1.1.4-1) ...
Setting up libstdc++-4.8-dev:i386 (4.8.4-2ubuntu1~14.04) ...
Setting up g++-4.8 (4.8.4-2ubuntu1~14.04) ...
Setting up g++ (4:4.8.2-1ubuntu6) ...
update-alternatives: using /usr/bin/g++ to provide /usr/bin/c++ (c++) in auto mode
Setting up libdpkg-perl (1.17.5ubuntu5.4) ...
Setting up dpkg-dev (1.17.5ubuntu5.4) ...
Setting up build-essential (11.6ubuntu6) ...
Setting up cmake-data (2.8.12.2-0ubuntu3) ...
Setting up cmake (2.8.12.2-0ubuntu3) ...
Setting up wireless-regdb (2013.02.13-1ubuntu1) ...
Setting up crda (1.1.2-1ubuntu2) ...
Setting up liberror-perl (0.17-1.1) ...
Setting up git-man (1:1.9.1-1ubuntu0.1) ...
Setting up git (1:1.9.1-1ubuntu0.1) ...
Setting up iw (3.4-1) ...
Setting up libalgorithm-diff-perl (1.19.02-3) ...
Setting up libalgorithm-diff-xs-perl (0.04-2build4) ...
Setting up libalgorithm-merge-perl (0.08-2) ...
Setting up libfile-fcntllock-perl (0.14-2build1) ...
Setting up libtinfo-dev:i386 (5.9+20140118-1ubuntu1) ...
Setting up libncurses5-dev:i386 (5.9+20140118-1ubuntu1) ...
Setting up libpython-dev:i386 (2.7.5-5ubuntu3) ...
Setting up libusb-1.0-0-dev:i386 (2:1.0.17-1ubuntu2) ...
Setting up libusb-1.0-doc (2:1.0.17-1ubuntu2) ...
Setting up libutempter0 (1.1.5-4build1) ...
Creating utempter group...
Setting up linux-firmware (1.127.15) ...
Setting up linux-image-extra-3.13.0-65-generic (3.13.0-65.106) ...
run-parts: executing /etc/kernel/postinst.d/apt-auto-removal 3.13.0-65-generic /boot/vmlinuz-3.13.0-65-generic
run-parts: executing /etc/kernel/postinst.d/dkms 3.13.0-65-generic /boot/vmlinuz-3.13.0-65-generic
run-parts: executing /etc/kernel/postinst.d/initramfs-tools 3.13.0-65-generic /boot/vmlinuz-3.13.0-65-generic
update-initramfs: Generating /boot/initrd.img-3.13.0-65-generic
run-parts: executing /etc/kernel/postinst.d/update-notifier 3.13.0-65-generic /boot/vmlinuz-3.13.0-65-generic
run-parts: executing /etc/kernel/postinst.d/zz-update-grub 3.13.0-65-generic /boot/vmlinuz-3.13.0-65-generic
Generating grub configuration file ...
Found linux image: /boot/vmlinuz-3.13.0-65-generic
Found initrd image: /boot/initrd.img-3.13.0-65-generic
done
Setting up linux-image-generic (3.13.0.65.71) ...
Setting up linux-image-extra-virtual (3.13.0.65.71) ...
Setting up mercurial-common (2.8.2-1ubuntu1.3) ...
Setting up mercurial (2.8.2-1ubuntu1.3) ...

Creating config file /etc/mercurial/hgrc.d/hgext.rc with new version
Setting up pkg-config (0.26-1ubuntu4) ...
Setting up python3-pkg-resources (3.3-1ubuntu2) ...
Setting up python-chardet-whl (2.2.1-2~ubuntu1) ...
Setting up python-colorama (0.2.5-0.1ubuntu2) ...
Setting up python-colorama-whl (0.2.5-0.1ubuntu2) ...
Setting up python2.7-dev (2.7.6-8ubuntu0.2) ...
Setting up python-dev (2.7.5-5ubuntu3) ...
Setting up python-distlib (0.1.8-1ubuntu1) ...
Setting up python-distlib-whl (0.1.8-1ubuntu1) ...
Setting up python-html5lib (0.999-3~ubuntu1) ...
Setting up python-html5lib-whl (0.999-3~ubuntu1) ...
Setting up python-six-whl (1.5.2-1ubuntu1) ...
Setting up python-urllib3-whl (1.7.1-1ubuntu3) ...
Setting up python-requests-whl (2.2.1-1ubuntu0.3) ...
Setting up python-setuptools-whl (3.3-1ubuntu2) ...
Setting up python-pip-whl (1.5.4-1ubuntu3) ...
Setting up python-setuptools (3.3-1ubuntu2) ...
Setting up python-pip (1.5.4-1ubuntu3) ...
Setting up python-wheel (0.24.0-1~ubuntu1) ...
Setting up tcl8.6 (8.6.1-4ubuntu1) ...
Setting up tcl (8.6.0+6ubuntu3) ...
Setting up tk8.6 (8.6.1-3ubuntu2) ...
Setting up tk (8.6.0+6ubuntu3) ...
Setting up u-boot-tools (2013.10-3) ...
Setting up unzip (6.0-9ubuntu1.3) ...
Setting up x11-utils (7.7+1) ...
Setting up xbitmaps (1.1.1-2) ...
Setting up xterm (297-1ubuntu1) ...
update-alternatives: using /usr/bin/xterm to provide /usr/bin/x-terminal-emulator (x-terminal-emulator) in auto mode
update-alternatives: using /usr/bin/lxterm to provide /usr/bin/x-terminal-emulator (x-terminal-emulator) in auto mode
Setting up android-tools-fastboot (4.2.2+git20130218-3ubuntu23) ...
Setting up cu (1.07-20.1) ...
Setting up device-tree-compiler (1.4.0+dfsg-1) ...
Processing triggers for libc-bin (2.19-0ubuntu6.6) ...

 Adding current user to dialout group

 Adding current user to plugdev group

 Adding udev rule for Allwinner device
SUBSYSTEM=="usb", ATTRS{idVendor}=="1f3a", ATTRS{idProduct}=="efe8", GROUP="plugdev", MODE="0660" SYMLINK+="usb-chip"
SUBSYSTEM=="usb", ATTRS{idVendor}=="18d1", ATTRS{idProduct}=="1010", GROUP="plugdev", MODE="0660" SYMLINK+="usb-chip-fastboot"


 Installing sunxi-tools
Cloning into 'sunxi-tools'...
remote: Counting objects: 1178, done.
remote: Total 1178 (delta 0), reused 0 (delta 0), pack-reused 1178
Receiving objects: 100% (1178/1178), 367.46 KiB | 332.00 KiB/s, done.
Resolving deltas: 100% (698/698), done.
Checking connectivity... done.
~/sunxi-tools ~
gcc -g -O0 -Wall -Wextra -std=c99 -D_POSIX_C_SOURCE=200112L -Iinclude/  -o fexc fexc.c script.c script_uboot.c script_bin.c script_fex.c
ln -s fexc bin2fex
ln -s fexc fex2bin
gcc -g -O0 -Wall -Wextra -std=c99 -D_POSIX_C_SOURCE=200112L -Iinclude/  -o bootinfo bootinfo.c
bootinfo.c: In function ‘print_script’:
bootinfo.c:274:25: warning: unused parameter ‘script’ [-Wunused-parameter]
 void print_script(void *script)
                         ^
gcc -g -O0 -Wall -Wextra -std=c99 -D_POSIX_C_SOURCE=200112L -Iinclude/ `pkg-config --cflags libusb-1.0`  -o fel fel.c  `pkg-config --libs libusb-1.0`
gcc -g -O0 -Wall -Wextra -std=c99 -D_POSIX_C_SOURCE=200112L -Iinclude/  -o pio pio.c
pio.c: In function ‘do_command’:
pio.c:318:57: warning: unused parameter ‘argc’ [-Wunused-parameter]
 static int do_command(char *buf, const char **args, int argc)
                                                         ^
gcc -g -O0 -Wall -Wextra -std=c99 -D_POSIX_C_SOURCE=200112L -Iinclude/ -c -o nand-part-main.o nand-part-main.c
gcc -g -O0 -Wall -Wextra -std=c99 -D_POSIX_C_SOURCE=200112L -Iinclude/ -c -o nand-part-a10.o nand-part.c -D A10
gcc -g -O0 -Wall -Wextra -std=c99 -D_POSIX_C_SOURCE=200112L -Iinclude/ -c -o nand-part-a20.o nand-part.c -D A20
gcc  -o nand-part nand-part-main.o nand-part-a10.o nand-part-a20.o
~

 Installing CHIP-tools
Cloning into 'CHIP-tools'...
remote: Counting objects: 132, done.
remote: Total 132 (delta 0), reused 0 (delta 0), pack-reused 132
Receiving objects: 100% (132/132), 36.13 KiB | 0 bytes/s, done.
Resolving deltas: 100% (61/61), done.
Checking connectivity... done.

 Installing CHIP-buildroot
Cloning into 'CHIP-buildroot'...
remote: Counting objects: 171996, done.
remote: Compressing objects: 100% (15/15), done.
remote: Total 171996 (delta 6), reused 0 (delta 0), pack-reused 171978
Receiving objects: 100% (171996/171996), 41.96 MiB | 6.15 MiB/s, done.
Resolving deltas: 100% (119002/119002), done.
Checking connectivity... done.

########################################################################################
# 
# Flashing CHIP firmware with CHIP-SDK
#
########################################################################################

vagrant@vagrant-ubuntu-trusty-32:~$ cd ~/CHIP-tools/

vagrant@vagrant-ubuntu-trusty-32:~/CHIP-tools$ ./chip-update-firmware.sh

LATEST_URL=http://stak-images.s3.amazonaws.com/firmware/chip/stable/68/
BUILD=68
--2015-10-09 19:43:29--  http://stak-images.s3.amazonaws.com/firmware/chip/stable/68/images/rootfs.ubi
Resolving stak-images.s3.amazonaws.com (stak-images.s3.amazonaws.com)... 54.231.225.42
Connecting to stak-images.s3.amazonaws.com (stak-images.s3.amazonaws.com)|54.231.225.42|:80... connected.
HTTP request sent, awaiting response... 200 OK
Length: 54525952 (52M) [binary/octet-stream]
Saving to: ‘/home/vagrant/CHIP-tools/.firmware/images/rootfs.ubi’

100%[========================================================================================================>] 54,525,952  4.45MB/s   in 16s

2015-10-09 19:43:46 (3.28 MB/s) - ‘/home/vagrant/CHIP-tools/.firmware/images/rootfs.ubi’ saved [54525952/54525952]

--2015-10-09 19:43:46--  http://stak-images.s3.amazonaws.com/firmware/chip/stable/68/images/sun5i-r8-chip.dtb
Resolving stak-images.s3.amazonaws.com (stak-images.s3.amazonaws.com)... 54.231.226.10
Connecting to stak-images.s3.amazonaws.com (stak-images.s3.amazonaws.com)|54.231.226.10|:80... connected.
HTTP request sent, awaiting response... 200 OK
Length: 20463 (20K) [binary/octet-stream]
Saving to: ‘/home/vagrant/CHIP-tools/.firmware/images/sun5i-r8-chip.dtb’

100%[========================================================================================================>] 20,463      --.-K/s   in 0.003s

2015-10-09 19:43:46 (7.17 MB/s) - ‘/home/vagrant/CHIP-tools/.firmware/images/sun5i-r8-chip.dtb’ saved [20463/20463]

--2015-10-09 19:43:46--  http://stak-images.s3.amazonaws.com/firmware/chip/stable/68/images/sunxi-spl.bin
Resolving stak-images.s3.amazonaws.com (stak-images.s3.amazonaws.com)... 54.231.226.10
Connecting to stak-images.s3.amazonaws.com (stak-images.s3.amazonaws.com)|54.231.226.10|:80... connected.
HTTP request sent, awaiting response... 200 OK
Length: 24576 (24K) [binary/octet-stream]
Saving to: ‘/home/vagrant/CHIP-tools/.firmware/images/sunxi-spl.bin’

100%[========================================================================================================>] 24,576      --.-K/s   in 0.001s

2015-10-09 19:43:46 (19.1 MB/s) - ‘/home/vagrant/CHIP-tools/.firmware/images/sunxi-spl.bin’ saved [24576/24576]

--2015-10-09 19:43:46--  http://stak-images.s3.amazonaws.com/firmware/chip/stable/68/images/uboot-env.bin
Resolving stak-images.s3.amazonaws.com (stak-images.s3.amazonaws.com)... 54.231.226.10
Connecting to stak-images.s3.amazonaws.com (stak-images.s3.amazonaws.com)|54.231.226.10|:80... connected.
HTTP request sent, awaiting response... 200 OK
Length: 4194304 (4.0M) [binary/octet-stream]
Saving to: ‘/home/vagrant/CHIP-tools/.firmware/images/uboot-env.bin’

100%[========================================================================================================>] 4,194,304   2.42MB/s   in 1.7s

2015-10-09 19:43:48 (2.42 MB/s) - ‘/home/vagrant/CHIP-tools/.firmware/images/uboot-env.bin’ saved [4194304/4194304]

--2015-10-09 19:43:48--  http://stak-images.s3.amazonaws.com/firmware/chip/stable/68/images/zImage
Resolving stak-images.s3.amazonaws.com (stak-images.s3.amazonaws.com)... 54.231.229.5
Connecting to stak-images.s3.amazonaws.com (stak-images.s3.amazonaws.com)|54.231.229.5|:80... connected.
HTTP request sent, awaiting response... 200 OK
Length: 4216280 (4.0M) [binary/octet-stream]
Saving to: ‘/home/vagrant/CHIP-tools/.firmware/images/zImage’

100%[========================================================================================================>] 4,216,280   1.28MB/s   in 3.6s

2015-10-09 19:43:52 (1.13 MB/s) - ‘/home/vagrant/CHIP-tools/.firmware/images/zImage’ saved [4216280/4216280]

--2015-10-09 19:43:52--  http://stak-images.s3.amazonaws.com/firmware/chip/stable/68/images/u-boot-dtb.bin
Resolving stak-images.s3.amazonaws.com (stak-images.s3.amazonaws.com)... 54.231.230.17
Connecting to stak-images.s3.amazonaws.com (stak-images.s3.amazonaws.com)|54.231.230.17|:80... connected.
HTTP request sent, awaiting response... 200 OK
Length: 581189 (568K) [binary/octet-stream]
Saving to: ‘/home/vagrant/CHIP-tools/.firmware/images/u-boot-dtb.bin’

100%[========================================================================================================>] 581,189      340KB/s   in 1.7s

2015-10-09 19:43:54 (340 KB/s) - ‘/home/vagrant/CHIP-tools/.firmware/images/u-boot-dtb.bin’ saved [581189/581189]

BUILDROOT_OUTPUT_DIR = /home/vagrant/CHIP-tools/.firmware
== preparing images ==
1+0 records in
1+0 records out
8192 bytes (8.2 kB) copied, 0.000723013 s, 11.3 MB/s
1+0 records in
1+0 records out
8192 bytes (8.2 kB) copied, 0.00146401 s, 5.6 MB/s
1+0 records in
1+0 records out
8192 bytes (8.2 kB) copied, 0.000715543 s, 11.4 MB/s
1+0 records in
1+0 records out
8192 bytes (8.2 kB) copied, 0.00171973 s, 4.8 MB/s
1+0 records in
1+0 records out
8192 bytes (8.2 kB) copied, 0.000637459 s, 12.9 MB/s
1+0 records in
1+0 records out
8192 bytes (8.2 kB) copied, 0.00162837 s, 5.0 MB/s
35+1 records in
36+0 records out
589824 bytes (590 kB) copied, 0.00160497 s, 367 MB/s
12+0 records in
12+0 records out
196608 bytes (197 kB) copied, 0.025654 s, 7.7 MB/s
Image Name:   flash CHIP
Created:      Fri Oct  9 19:43:55 2015
Image Type:   ARM Linux Script (uncompressed)
Data Size:    856 Bytes = 0.84 kB = 0.00 MB
Load Address: 00000000
Entry Point:  00000000
Contents:
   Image 0: 848 Bytes = 0.83 kB = 0.00 MB
== upload the SPL to SRAM and execute it ==
== upload images ==
== execute the main u-boot binary ==
vagrant@vagrant-ubuntu-trusty-32:~/CHIP-tools$ cu -l /dev/ttyACM0 -s 115200
cu: open (/dev/ttyACM0): No such file or directory
cu: /dev/ttyACM0: Line in use
vagrant@vagrant-ubuntu-trusty-32:~/CHIP-tools$ cu -l /dev/ttyACM0 -s 115200
cu: open (/dev/ttyACM0): No such file or directory
cu: /dev/ttyACM0: Line in use
vagrant@vagrant-ubuntu-trusty-32:~/CHIP-tools$ cu -l /dev/ttyACM0 -s 115200
Connected.


Welcome to CHIP Buildroot build 68 rev 7c9b1c77

CHIP Buildroot contains various open source software.

The source code can be downloaded from:
http://opensource.nextthing.co/chip/buildroot/stable/68/build68.tar.gz

chip login: root
Password:

# ls -al
total 12
drwx------    2 root     root           448 Jan  1 00:00 .
drwxr-xr-x   19 root     root          1440 Oct  2  2015 ..
-rw-------    1 root     root            10 Jan  1 00:00 .ash_history
-rw-r--r--    1 root     root             0 Oct  2  2015 .bash_history
-rw-r--r--    1 root     root           175 Oct  2  2015 .bash_logout
-rw-r--r--    1 root     root            78 Oct  2  2015 .bash_profile

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
# exit
cu: Got hangup signal

Disconnected.
vagrant@vagrant-ubuntu-trusty-32:~/CHIP-tools$
vagrant@vagrant-ubuntu-trusty-32:~/CHIP-tools$ exit
logout
Connection to 127.0.0.1 closed.

bokbokbok% vagrant halt
==> default: Attempting graceful shutdown of VM...

########################################################################################
# 
# Getting CHIP on WiFi
#
########################################################################################

bokbokbok% ls -al /dev/tty.usbmodem14141
crw-rw-rw-  1 root  wheel   18,  34 Oct  9 12:47 /dev/tty.usbmodem14141

bokbokbok% cu -l /dev/tty.usbmodem14141 -s 115200
cu: creat during lock (/var/spool/uucp/TMP000000bd6a in /Users/tod/projects/chip/CHIP-SDK as uid 502): Permission denied
cu: /dev/tty.usbmodem14141: Line in use

bokbokbok% sudo cu -l /dev/tty.usbmodem14141 -s 115200
Connected.
CHIP Buildroot contains various open source software.

The source code can be downloaded from:
http://opensource.nextthing.co/chip/buildroot/stable/68/build68.tar.gz

chip login: root
Password:
# cat /etc/issue
Welcome to CHIP Buildroot build 68 rev 7c9b1c77

CHIP Buildroot contains various open source software.

The source code can be downloaded from:
http://opensource.nextthing.co/chip/buildroot/stable/68/build68.tar.gz

# ifconfig
lo        Link encap:Local Loopback
          inet addr:127.0.0.1  Mask:255.0.0.0
          inet6 addr: ::1/128 Scope:Host
          UP LOOPBACK RUNNING  MTU:65536  Metric:1
          RX packets:0 errors:0 dropped:0 overruns:0 frame:0
          TX packets:0 errors:0 dropped:0 overruns:0 carrier:0
          collisions:0 txqueuelen:0
          RX bytes:0 (0.0 B)  TX bytes:0 (0.0 B)

wlan0     Link encap:Ethernet  HWaddr 8C:18:D9:F2:D8:6C
          UP BROADCAST MULTICAST  MTU:1500  Metric:1
          RX packets:0 errors:0 dropped:260 overruns:0 frame:0
          TX packets:0 errors:0 dropped:0 overruns:0 carrier:0
          collisions:0 txqueuelen:1000
          RX bytes:0 (0.0 B)  TX bytes:0 (0.0 B)

wlan1     Link encap:Ethernet  HWaddr 8E:18:D9:F2:D8:6C
          inet6 addr: fe80::8c18:d9ff:fef2:d86c/64 Scope:Link
          UP BROADCAST RUNNING MULTICAST  MTU:1500  Metric:1
          RX packets:260 errors:0 dropped:0 overruns:0 frame:0
          TX packets:1 errors:0 dropped:0 overruns:0 carrier:0
          collisions:0 txqueuelen:1000
          RX bytes:0 (0.0 B)  TX bytes:96 (96.0 B)

# connmanctl technologies
/net/connman/technology/bluetooth
  Name = Bluetooth
  Type = bluetooth
  Powered = False
  Connected = False
  Tethering = False
/net/connman/technology/wifi
  Name = WiFi
  Type = wifi
  Powered = False
  Connected = False
  Tethering = False

# connmanctl enable wifi
Enabled wifi

# connmanctl scan wifi
Scan completed for wifi

# connmanctl services
    todbot               wifi_8c18d9f2d86c_746f64626f74_managed_none
                         wifi_8c18d9f2d86c_hidden_managed_none

# connmanctl connect wifi_8c18d9f2d86c_746f64626f74_managed_none
Connected wifi_8c18d9f2d86c_746f64626f74_managed_none

# ifconfig wlan0
wlan0     Link encap:Ethernet  HWaddr 8C:18:D9:F2:D8:6C
          inet addr:192.168.42.198  Bcast:192.168.42.255  Mask:255.255.255.0
          inet6 addr: fe80::8e18:d9ff:fef2:d86c/64 Scope:Link
          UP BROADCAST RUNNING MULTICAST  MTU:1500  Metric:1
          RX packets:225 errors:0 dropped:660 overruns:0 frame:0
          TX packets:30 errors:0 dropped:0 overruns:0 carrier:0
          collisions:0 txqueuelen:1000
          RX bytes:31391 (30.6 KiB)  TX bytes:4051 (3.9 KiB)

# ping 8.8.8.8
PING 8.8.8.8 (8.8.8.8): 56 data bytes
64 bytes from 8.8.8.8: seq=0 ttl=56 time=13.292 ms
64 bytes from 8.8.8.8: seq=1 ttl=53 time=17.802 ms
64 bytes from 8.8.8.8: seq=2 ttl=56 time=14.612 ms
^C
--- 8.8.8.8 ping statistics ---
3 packets transmitted, 3 packets received, 0% packet loss
round-trip min/avg/max = 13.292/15.235/17.802 ms
# exit

Welcome to CHIP Buildroot build 68 rev 7c9b1c77

CHIP Buildroot contains various open source software.

The source code can be downloaded from:
http://opensource.nextthing.co/chip/buildroot/stable/68/build68.tar.gz

chip login:
Welcome to CHIP Buildroot build 68 rev 7c9b1c77

CHIP Buildroot contains various open source software.

The source code can be downloaded from:
http://opensource.nextthing.co/chip/buildroot/stable/68/build68.tar.gz

chip login: ~.

bokbokbok% ping 192.168.42.198
PING 192.168.42.198 (192.168.42.198): 56 data bytes
64 bytes from 192.168.42.198: icmp_seq=0 ttl=64 time=16.310 ms
^C
--- 192.168.42.198 ping statistics ---
1 packets transmitted, 1 packets received, 0.0% packet loss
round-trip min/avg/max/stddev = 16.310/16.310/16.310/0.000 ms

bokbokbok% ssh root@192.168.42.198
The authenticity of host '192.168.42.198 (192.168.42.198)' can't be established.
RSA key fingerprint is c9:87:3f:68:78:13:8f:ff:fd:7f:2a:b7:0b:d9:10:bb.
Are you sure you want to continue connecting (yes/no)? yes
Warning: Permanently added '192.168.42.198' (RSA) to the list of known hosts.
root@192.168.42.198's password:

# cat /etc/issue
Welcome to CHIP Buildroot build 68 rev 7c9b1c77

CHIP Buildroot contains various open source software.

The source code can be downloaded from:
http://opensource.nextthing.co/chip/buildroot/stable/68/build68.tar.gz

## ## # 
```