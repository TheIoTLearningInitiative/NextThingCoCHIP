Buildroot
==

## WiFi

    root@chip:~# connmanctl technologies
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
    root@chip:~# connmanctl enable wifi
    Enabled wifi
    root@chip:~# connmanctl scan wifi
    Scan completed for wifi
    root@chip:~# connmanctl services
        INFINITUMndjj        wifi_8c18d9f26f78_494e46494e4954554d6e646a6a_managed_psk
        INFINITUM8240C7      wifi_8c18d9f26f78_494e46494e4954554d383234304337_managed_psk
    root@chip:~# connmanctl connect wifi_8c18d9f26f78_494e46494e4954554d666a7068_managed_psk
    Error /net/connman/service/wifi_8c18d9f26f78_494e46494e4954554d666a7068_managed_psk: Not registered


    root@chip:~# connmanctl
    connmanctl> agent on
    Agent registered
    connmanctl> connect wifi_8c18d9f26f78_494e46494e4954554d666a7068_managed_psk
    Agent RequestInput wifi_8c18d9f26f78_494e46494e4954554d666a7068_managed_psk
      Passphrase = [ Type=psk, Requirement=mandatory, Alternates=[ WPS ] ]
      WPS = [ Type=wpspin, Requirement=alternate ]
    Passphrase? 
    Connected wifi_8c18d9f26f78_494e46494e4954554d666a7068_managed_psk
    connmanctl> quit 
    root@chip:~# ifconfig
    root@chip:~# ping -c 4 8.8.8.8
    PING 8.8.8.8 (8.8.8.8): 56 data bytes
    64 bytes from 8.8.8.8: seq=0 ttl=59 time=45.729 ms
    64 bytes from 8.8.8.8: seq=1 ttl=59 time=32.499 ms
    64 bytes from 8.8.8.8: seq=2 ttl=59 time=168.429 ms
    64 bytes from 8.8.8.8: seq=3 ttl=59 time=42.329 ms
    
    --- 8.8.8.8 ping statistics ---
    4 packets transmitted, 4 packets received, 0% packet loss
    round-trip min/avg/max = 32.499/72.246/168.429 ms
    root@chip:~# ifconfig
    lo        Link encap:Local Loopback  
          inet addr:127.0.0.1  Mask:255.0.0.0
    wlan0     Link encap:Ethernet  HWaddr 8C:18:D9:F2:6F:78  
          inet addr:192.168.1.64  Bcast:192.168.1.255  Mask:255.255.255.0
              ...
    wlan1     Link encap:Ethernet  HWaddr 8E:18:D9:F2:6F:78  
          inet6 addr: fe80::8c18:d9ff:fef2:6f78/64 Scope:Link


[Connecting C.H.I.P. to a Wireless Network ](https://nextthingco.zendesk.com/hc/en-us/articles/209758368-Connecting-C-H-I-P-to-a-Wireless-Network)


