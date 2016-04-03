# SandBox

http://www.instructables.com/id/Turn-your-Raspberry-Pi-into-a-Portable-Bluetooth-A/
https://wiki.archlinux.org/index.php/Bluetooth#Configuration_via_the_CLI

    root@chip:~# dmesg
    [35340.574607] usb 2-4.1: USB disconnect, device number 15
    [35340.852245] usb 2-4.1: new full-speed USB device number 16 using ehci-pci
    [35340.940107] usb 2-4.1: device descriptor read/64, error -32
    [35341.132104] usb 2-4.1: device descriptor read/64, error -32
    [35341.324103] usb 2-4.1: new full-speed USB device number 17 using ehci-pci
    [35341.412102] usb 2-4.1: device descriptor read/64, error -32
    [35341.604099] usb 2-4.1: device descriptor read/64, error -32
    [35341.796099] usb 2-4.1: new full-speed USB device number 18 using ehci-pci
    [35342.204038] usb 2-4.1: device not accepting address 18, error -32
    [35342.292093] usb 2-4.1: new full-speed USB device number 19 using ehci-pci
    [35342.700030] usb 2-4.1: device not accepting address 19, error -32
    [35342.700094] usb 2-4-port1: unable to enumerate USB device
    [35377.892165] usb 2-4.1: new high-speed USB device number 20 using ehci-pci
    [35377.984784] usb 2-4.1: New USB device found, idVendor=0525, idProduct=a4a7
    [35377.984787] usb 2-4.1: New USB device strings: Mfr=1, Product=2, SerialNumber=0
    [35377.984790] usb 2-4.1: Product: Gadget Serial v2.4
    [35377.984792] usb 2-4.1: Manufacturer: Linux 4.2.0-rc1 with musb-hdrc
    [35377.994941] cdc_acm 2-4.1:2.0: This device cannot do calls on its own. It is not a modem.
    [35377.995007] cdc_acm 2-4.1:2.0: ttyACM0: USB ACM device
    [36565.268967] usb 2-4.1: USB disconnect, device number 20
    [36565.271198] cdc_acm 2-4.1:2.0: failed to set dtr/rts
    [36566.764088] usb 2-4.1: new full-speed USB device number 21 using ehci-pci
    [36566.873213] usb 2-4.1: New USB device found, idVendor=1f3a, idProduct=efe8
    [36566.873217] usb 2-4.1: New USB device strings: Mfr=0, Product=0, SerialNumber=0
    [36594.708877] usb 2-4.1: USB disconnect, device number 21
    [36616.428097] usb 2-4.1: new full-speed USB device number 22 using ehci-pci
    [36616.537097] usb 2-4.1: New USB device found, idVendor=1f3a, idProduct=efe8
    [36616.537102] usb 2-4.1: New USB device strings: Mfr=0, Product=0, SerialNumber=0
    [36791.059440] usb 2-4.1: USB disconnect, device number 22
    [36791.276070] usb 2-4.1: new full-speed USB device number 23 using ehci-pci
    [36791.364063] usb 2-4.1: device descriptor read/64, error -32
    [36791.556192] usb 2-4.1: device descriptor read/64, error -32
    [36791.748193] usb 2-4.1: new full-speed USB device number 24 using ehci-pci
    [36791.836190] usb 2-4.1: device descriptor read/64, error -32
    [36792.028187] usb 2-4.1: device descriptor read/64, error -32
    [36792.220190] usb 2-4.1: new full-speed USB device number 25 using ehci-pci
    [36792.628026] usb 2-4.1: device not accepting address 25, error -32
    [36792.716182] usb 2-4.1: new full-speed USB device number 26 using ehci-pci
    [36793.124035] usb 2-4.1: device not accepting address 26, error -32
    [36793.124181] usb 2-4-port1: unable to enumerate USB device
