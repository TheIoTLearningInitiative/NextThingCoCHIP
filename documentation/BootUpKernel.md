Kernel
==

    root@chip:~# dmesg | grep sunxi
    [    1.660000] sunxi-wdt 1c20c90.watchdog: Watchdog enabled (timeout=16 sec, nowayout=0)
    [    1.680000] sunxi-mmc 1c0f000.mmc: No vqmmc regulator found
    [    1.730000] sunxi-mmc 1c0f000.mmc: base:0xe00b6000 irq:20
    [    1.760000] sunxi-codec 1c22c00.codec: Codec <-> 1c22c00.codec mapping ok
    [    1.770000] sunxi-mmc 1c0f000.mmc: smc 0 err, cmd 8, RTO !!
    [   17.600000]   #0: sunxi-codec
    # dmesg
    [    0.000000] Booting Linux on physical CPU 0x0
    [    0.000000] Linux version 4.2.0-rc1 (ubuntu@ip-172-31-37-115) (gcc version 4.9.2 20140904 (prerelease) (crosstool-NG linaro-1.13.1-4.9-2014.09 - Linaro GCC 4.9-2014.09) ) #1 SMP Fri Oct 2 23:23:30 UTC 2015
    [    0.000000] CPU: ARMv7 Processor [413fc082] revision 2 (ARMv7), cr=10c5387d
    [    0.000000] CPU: PIPT / VIPT nonaliasing data cache, VIPT aliasing instruction cache
    [    0.000000] Machine model: NextThing C.H.I.P.
    [    0.000000] Memory policy: Data cache writeback
    [    0.000000] On node 0 totalpages: 130666
    [    0.000000] free_area_init_node: node 0, pgdat c0761700, node_mem_map df9f9000
    [    0.000000]   Normal zone: 1020 pages used for memmap
    [    0.000000]   Normal zone: 0 pages reserved
    [    0.000000]   Normal zone: 130560 pages, LIFO batch:31
    [    0.000000]   HighMem zone: 106 pages, LIFO batch:0
    [    0.000000] CPU: All CPU(s) started in SVC mode.
    [    0.000000] PERCPU: Embedded 11 pages/cpu @df9d5000 s14464 r8192 d22400 u45056
    [    0.000000] pcpu-alloc: s14464 r8192 d22400 u45056 alloc=11*4096
    [    0.000000] pcpu-alloc: [0] 0 
    [    0.000000] Built 1 zonelists in Zone order, mobility grouping on.  Total pages: 129646
    [    0.000000] Kernel command line: root=ubi0:rootfs rootfstype=ubifs rw earlyprintk ubi.mtd=4
    [    0.000000] PID hash table entries: 2048 (order: 1, 8192 bytes)
    [    0.000000] Dentry cache hash table entries: 65536 (order: 6, 262144 bytes)
    [    0.000000] Inode-cache hash table entries: 32768 (order: 5, 131072 bytes)
    [    0.000000] Memory: 502252K/522664K available (5312K kernel code, 290K rwdata, 1700K rodata, 224K init, 8178K bss, 20412K reserved, 0K cma-reserved, 424K highmem)
    [    0.000000] Virtual kernel memory layout:
    [    0.000000]     vector  : 0xffff0000 - 0xffff1000   (   4 kB)
    [    0.000000]     fixmap  : 0xffc00000 - 0xfff00000   (3072 kB)
    [    0.000000]     vmalloc : 0xe0000000 - 0xff000000   ( 496 MB)
    [    0.000000]     lowmem  : 0xc0000000 - 0xdfe6a000   ( 510 MB)
    [    0.000000]     pkmap   : 0xbfe00000 - 0xc0000000   (   2 MB)
    [    0.000000]     modules : 0xbf000000 - 0xbfe00000   (  14 MB)
    [    0.000000]       .text : 0xc0008000 - 0xc06e14dc   (7014 kB)
    [    0.000000]       .init : 0xc06e2000 - 0xc071a000   ( 224 kB)
    [    0.000000]       .data : 0xc071a000 - 0xc0762860   ( 291 kB)
    [    0.000000]        .bss : 0xc0765000 - 0xc0f61ba8   (8179 kB)
    [    0.000000] SLUB: HWalign=64, Order=0-3, MinObjects=0, CPUs=1, Nodes=1
    [    0.000000] Running RCU self tests
    [    0.000000] Hierarchical RCU implementation.
    [    0.000000] 	RCU lockdep checking is enabled.
    [    0.000000] 	Build-time adjustment of leaf fanout to 32.
    [    0.000000] 	RCU restricting CPUs from NR_CPUS=4 to nr_cpu_ids=1.
    [    0.000000] RCU: Adjusting geometry for rcu_fanout_leaf=32, nr_cpu_ids=1
    [    0.000000] NR_IRQS:16 nr_irqs:16 16
    [    0.000000] clocksource: timer: mask: 0xffffffff max_cycles: 0xffffffff, max_idle_ns: 79635851949 ns
    [    0.000000] clocksource: timer: mask: 0xffffffff max_cycles: 0xffffffff, max_idle_ns: 6370868154 ns
    [    0.000000] sched_clock: 32 bits at 100 Hz, resolution 10000000ns, wraps every 21474836475000000ns
    [    0.000000] Console: colour dummy device 80x30
    [    0.000000] console [tty0] enabled
    [    0.000000] Lock dependency validator: Copyright (c) 2006 Red Hat, Inc., Ingo Molnar
    [    0.000000] ... MAX_LOCKDEP_SUBCLASSES:  8
    [    0.000000] ... MAX_LOCK_DEPTH:          48
    [    0.000000] ... MAX_LOCKDEP_KEYS:        8191
    [    0.000000] ... CLASSHASH_SIZE:          4096
    [    0.000000] ... MAX_LOCKDEP_ENTRIES:     32768
    [    0.000000] ... MAX_LOCKDEP_CHAINS:      65536
    [    0.000000] ... CHAINHASH_SIZE:          32768
    [    0.000000]  memory used by lock dependency info: 5167 kB
    [    0.000000]  per task-struct memory footprint: 1536 bytes
    [    0.070000] Calibrating delay loop... 1001.88 BogoMIPS (lpj=5009408)
    [    0.070000] pid_max: default: 32768 minimum: 301
    [    0.080000] Mount-cache hash table entries: 1024 (order: 0, 4096 bytes)
    [    0.080000] Mountpoint-cache hash table entries: 1024 (order: 0, 4096 bytes)
    [    0.080000] CPU: Testing write buffer coherency: ok
    [    0.080000] CPU0: thread -1, cpu 0, socket -1, mpidr 0
    [    0.080000] Setting up static identity map for 0x40008280 - 0x400082d8
    [    0.080000] Brought up 1 CPUs
    [    0.080000] SMP: Total of 1 processors activated (1001.88 BogoMIPS).
    [    0.080000] CPU: All CPU(s) started in SVC mode.
    [    0.080000] devtmpfs: initialized
    [    0.100000] VFP support v0.3: implementor 41 architecture 3 part 30 variant c rev 3
    [    0.100000] clocksource: jiffies: mask: 0xffffffff max_cycles: 0xffffffff, max_idle_ns: 19112604462750000 ns
    [    0.100000] pinctrl core: initialized pinctrl subsystem
    [    0.110000] NET: Registered protocol family 16
    [    0.110000] DMA: preallocated 256 KiB pool for atomic coherent allocations
    [    0.120000] hw-breakpoint: debug architecture 0x4 unsupported.
    [    0.140000] reg-fixed-voltage usb0_vbus: could not find pctldev for node /soc@01c00000/pinctrl@01c20800/chip_vbus_pin@0, deferring probe
    [    0.140000] reg-fixed-voltage wifi_reg_on: could not find pctldev for node /soc@01c00000/pinctrl@01c20800/chip_wifi_reg_on_pin@0, deferring probe
    [    0.140000] SCSI subsystem initialized
    [    0.140000] usbcore: registered new interface driver usbfs
    [    0.140000] usbcore: registered new interface driver hub
    [    0.140000] usbcore: registered new device driver usb
    [    0.140000] pps_core: LinuxPPS API ver. 1 registered
    [    0.140000] pps_core: Software ver. 5.3.6 - Copyright 2005-2007 Rodolfo Giometti <giometti@linux.it>
    [    0.140000] PTP clock support registered
    [    0.140000] Advanced Linux Sound Architecture Driver Initialized.
    [    0.140000] clocksource: Switched to clocksource timer
    [    0.150000] simple-framebuffer 5fe79000.framebuffer: framebuffer at 0x5fe79000, 0x178e00 bytes, mapped to 0xe0200000
    [    0.150000] simple-framebuffer 5fe79000.framebuffer: format=x8r8g8b8, mode=656x536x32, linelength=2880
    [    0.150000] Console: switching to colour frame buffer device 82x33
    [    0.150000] simple-framebuffer 5fe79000.framebuffer: fb0: simplefb registered!
    [    0.180000] NET: Registered protocol family 2
    [    0.180000] TCP established hash table entries: 4096 (order: 2, 16384 bytes)
    [    0.180000] TCP bind hash table entries: 4096 (order: 5, 147456 bytes)
    [    0.190000] TCP: Hash tables configured (established 4096 bind 4096)
    [    0.190000] UDP hash table entries: 256 (order: 2, 20480 bytes)
    [    0.200000] UDP-Lite hash table entries: 256 (order: 2, 20480 bytes)
    [    0.200000] NET: Registered protocol family 1
    [    0.210000] futex hash table entries: 256 (order: 2, 16384 bytes)
    [    0.240000] squashfs: version 4.0 (2009/01/31) Phillip Lougher
    [    0.260000] bounce: pool size: 64 pages
    [    0.260000] Block layer SCSI generic (bsg) driver version 0.4 loaded (major 250)
    [    0.270000] io scheduler noop registered
    [    0.270000] io scheduler deadline registered
    [    0.280000] io scheduler cfq registered (default)
    [    0.280000] sun4i-usb-phy 1c13400.phy: could not find pctldev for node /soc@01c00000/pinctrl@01c20800/chip_id_det_pin@0, deferring probe
    [    0.290000] sun5i-a13-pinctrl 1c20800.pinctrl: initialized sunXi PIO driver
    [    0.460000] Serial: 8250/16550 driver, 8 ports, IRQ sharing disabled
    [    0.500000] 1c28400.serial: ttyS0 at MMIO 0x1c28400 (irq = 27, base_baud = 1500000) is a U6_16550A
    [    1.120000] console [ttyS0] enabled
    [    1.150000] 1c28c00.serial: ttyS1 at MMIO 0x1c28c00 (irq = 28, base_baud = 1500000) is a U6_16550A
    [    1.170000] nand: device found, Manufacturer ID: 0xad, Chip ID: 0xde
    [    1.180000] nand: chip id data: 0xad, 0xde, 0x14, 0xa7, 0x42, 0x4a; 0xad, 0xde 
    [    1.190000] nand: Hynix H27QCG8T2E5R‐BCF 64G 3.3V 8-bit
    [    1.200000] nand: 8192 MiB, MLC, erase size: 4096 KiB, page size: 16384, OOB size: 1664, ECC strength 40 size 1024
    [    1.240000] Bad block table found at page 524032, version 0x01
    [    1.250000] Bad block table found at page 523776, version 0x01
    [    1.270000] nand_read_bbt: bad block at 0x0000c7800000
    [    1.270000] nand_read_bbt: bad block at 0x0000f9000000
    [    1.280000] nand_read_bbt: bad block at 0x00010c800000
    [    1.290000] nand_read_bbt: bad block at 0x000110c00000
    [    1.300000] nand_read_bbt: bad block at 0x00011c000000
    [    1.310000] nand_read_bbt: bad block at 0x000124800000
    [    1.320000] nand_read_bbt: bad block at 0x000157000000
    [    1.320000] nand_read_bbt: bad block at 0x000158c00000
    [    1.330000] nand_read_bbt: bad block at 0x000159400000
    [    1.340000] nand_read_bbt: bad block at 0x000199000000
    [    1.350000] nand_read_bbt: bad block at 0x0001cb800000
    [    1.360000] nand_read_bbt: bad block at 0x0001da800000
    [    1.400000] usbcore: registered new interface driver asix
    [    1.400000] usbcore: registered new interface driver ax88179_178a
    [    1.410000] usbcore: registered new interface driver cdc_ether
    [    1.420000] usbcore: registered new interface driver net1080
    [    1.430000] usbcore: registered new interface driver rndis_host
    [    1.440000] usbcore: registered new interface driver cdc_subset
    [    1.450000] usbcore: registered new interface driver zaurus
    [    1.450000] usbcore: registered new interface driver cdc_ncm
    [    1.460000] ehci_hcd: USB 2.0 'Enhanced' Host Controller (EHCI) Driver
    [    1.470000] ehci-platform: EHCI generic platform driver
    [    1.480000] ohci_hcd: USB 1.1 'Open' Host Controller (OHCI) Driver
    [    1.490000] ohci-platform: OHCI generic platform driver
    [    1.500000] usbcore: registered new interface driver usb-storage
    [    1.500000] udc-core: couldn't find an available UDC - added [g_serial] to list of pending drivers
    [    1.520000] mousedev: PS/2 mouse device common for all mice
    [    1.530000] i2c /dev entries driver
    [    1.540000] axp20x 0-0034: AXP20x variant AXP209 found
    [    1.550000] input: axp20x-pek as /devices/platform/soc@01c00000/1c2ac00.i2c/i2c-0/0-0034/axp20x-pek/input/input0
    [    1.580000] axp20x 0-0034: AXP20X driver loaded
    [    1.590000] pcf857x 2-0038: probed
    [    1.600000] sunxi-wdt 1c20c90.watchdog: Watchdog enabled (timeout=16 sec, nowayout=0)
    [    1.610000] vcc-3v3: supplied by ipsout
    [    1.620000] sunxi-mmc 1c0f000.mmc: No vqmmc regulator found
    [    1.670000] sunxi-mmc 1c0f000.mmc: base:0xe00b6000 irq:20
    [    1.670000] usbcore: registered new interface driver usbhid
    [    1.680000] usbhid: USB HID core driver
    [    1.700000] sunxi-codec 1c22c00.codec: Codec <-> 1c22c00.codec mapping ok
    [    1.710000] sunxi-mmc 1c0f000.mmc: smc 0 err, cmd 8, RTO !!
    [    1.730000] ip_tables: (C) 2000-2006 Netfilter Core Team
    [    1.740000] NET: Registered protocol family 10
    [    1.750000] mip6: Mobile IPv6
    [    1.750000] sit: IPv6 over IPv4 tunneling driver
    [    1.770000] NET: Registered protocol family 17
    [    1.770000] Registering SWP/SWPB emulation handler
    [    1.790000] vcc-5v0: supplied by ipsout
    [    1.800000] vbus-usb0: supplied by vcc-5v0
    [    1.810000] ehci-platform 1c14000.usb: EHCI Host Controller
    [    1.820000] ehci-platform 1c14000.usb: new USB bus registered, assigned bus number 1
    [    1.830000] ehci-platform 1c14000.usb: irq 22, io mem 0x01c14000
    [    1.850000] mmc0: new high speed SDIO card at address 0001
    [    1.860000] ehci-platform 1c14000.usb: USB 2.0 started, EHCI 1.00
    [    1.870000] hub 1-0:1.0: USB hub found
    [    1.880000] hub 1-0:1.0: 1 port detected
    [    1.890000] ohci-platform 1c14400.usb: Generic Platform OHCI controller
    [    1.900000] ohci-platform 1c14400.usb: new USB bus registered, assigned bus number 2
    [    1.920000] ohci-platform 1c14400.usb: irq 23, io mem 0x01c14400
    [    1.980000] hub 2-0:1.0: USB hub found
    [    1.990000] hub 2-0:1.0: 1 port detected
    [    2.000000] usb_phy_generic.0.auto supply vcc not found, using dummy regulator
    [    2.010000] musb-hdrc: ConfigData=0xde (UTMI-8, dyn FIFOs, bulk combine, bulk split, HB-ISO Rx, HB-ISO Tx, SoftConn)
    [    2.010000] musb-hdrc: MHDRC RTL version 0.0 
    [    2.010000] musb-hdrc: 11/11 max ep, 5184/8192 memory
    [    2.010000] musb-hdrc musb-hdrc.1.auto: MUSB HDRC host driver
    [    2.020000] musb-hdrc musb-hdrc.1.auto: new USB bus registered, assigned bus number 3
    [    2.040000] hub 3-0:1.0: USB hub found
    [    2.050000] hub 3-0:1.0: 1 port detected
    [    2.060000] g_serial gadget: Gadget Serial v2.4
    [    2.070000] g_serial gadget: g_serial ready
    [    2.080000] ubi0: attaching mtd4
    [    2.300000] random: nonblocking pool is initialized
    [    3.570000] g_serial gadget: high-speed config #2: CDC ACM config
    [   17.170000] ubi0: scanning is finished
    [   17.210000] ubi0: attached mtd4 (name "rootfs", size 4088 MiB)
    [   17.220000] ubi0: PEB size: 2097152 bytes (2048 KiB), LEB size: 2064384 bytes
    [   17.230000] ubi0: min./max. I/O unit sizes: 16384/16384, sub-page size 16384
    [   17.240000] ubi0: VID header offset: 16384 (aligned 16384), data offset: 32768
    [   17.250000] ubi0: good PEBs: 2028, bad PEBs: 16, corrupted PEBs: 0
    [   17.260000] ubi0: user volume: 1, internal volumes: 1, max. volumes count: 128
    [   17.270000] ubi0: max/mean erase counter: 1/0, WL threshold: 4096, image sequence number: 323437327
    [   17.290000] ubi0: available PEBs: 4, total reserved PEBs: 2024, PEBs reserved for bad PEB handling: 24
    [   17.300000] hctosys: unable to open rtc device (rtc0)
    [   17.330000] vbus-usb0: disabling
    [   17.330000] ALSA device list:
    [   17.340000]   #0: sunxi-codec
    [   17.350000] ubi0: background thread "ubi_bgt0d" started, PID 70
    [   17.380000] UBIFS (ubi0:0): background thread "ubifs_bgt0_0" started, PID 71
    [   18.390000] UBIFS (ubi0:0): UBIFS: mounted UBI device 0, volume 0, name "rootfs"
    [   18.400000] UBIFS (ubi0:0): LEB size: 2064384 bytes (2016 KiB), min./max. I/O unit sizes: 16384 bytes/16384 bytes
    [   18.420000] UBIFS (ubi0:0): FS size: 4099866624 bytes (3909 MiB, 1986 LEBs), journal size 18579457 bytes (17 MiB, 9 LEBs)
    [   18.430000] UBIFS (ubi0:0): reserved for root: 0 bytes (0 KiB)
    [   18.440000] UBIFS (ubi0:0): media format: w4/r0 (latest is w4/r0), UUID F140E5F3-B363-4BBF-B539-E2111DDBBF0A, small LPT model
    [   18.490000] VFS: Mounted root (ubifs filesystem) on device 0:14.
    [   18.530000] devtmpfs: mounted
    [   18.530000] Freeing unused kernel memory: 224K (c06e2000 - c071a000)
    [   21.190000] cfg80211: Calling CRDA to update world regulatory domain
    [   21.200000] cfg80211: World regulatory domain updated:
    [   21.210000] cfg80211:  DFS Master region: unset
    [   21.210000] cfg80211:   (start_freq - end_freq @ bandwidth), (max_antenna_gain, max_eirp), (dfs_cac_time)
    [   21.240000] cfg80211:   (2402000 KHz - 2472000 KHz @ 40000 KHz), (N/A, 2000 mBm), (N/A)
    [   21.250000] cfg80211:   (2457000 KHz - 2482000 KHz @ 40000 KHz), (N/A, 2000 mBm), (N/A)
    [   21.270000] cfg80211:   (2474000 KHz - 2494000 KHz @ 20000 KHz), (N/A, 2000 mBm), (N/A)
    [   21.280000] cfg80211:   (5170000 KHz - 5250000 KHz @ 80000 KHz, 160000 KHz AUTO), (N/A, 2000 mBm), (N/A)
    [   21.300000] cfg80211:   (5250000 KHz - 5330000 KHz @ 80000 KHz, 160000 KHz AUTO), (N/A, 2000 mBm), (0 s)
    [   21.320000] cfg80211:   (5490000 KHz - 5730000 KHz @ 160000 KHz), (N/A, 2000 mBm), (0 s)
    [   21.330000] cfg80211:   (5735000 KHz - 5835000 KHz @ 80000 KHz), (N/A, 2000 mBm), (N/A)
    [   21.350000] cfg80211:   (57240000 KHz - 63720000 KHz @ 2160000 KHz), (N/A, 0 mBm), (N/A)
    [   22.200000] RTL871X: module init start
    [   22.210000] RTL871X: rtl8723bs v4.3.16_13854.20150410_BTCOEX20150119-5844
    [   22.220000] RTL871X: build time: Oct  2 2015 23:23:51
    [   22.230000] RTL871X: rtl8723bs BT-Coex version = BTCOEX20150119-5844
    [   22.240000] cfg80211: Updating information on frequency 2412 MHz with regulatory rule:
    [   22.240000] cfg80211: 2402000 KHz - 2472000 KHz @ 40000 KHz), (N/A mBi, 2000 mBm)
    [   22.240000] cfg80211: Updating information on frequency 2417 MHz with regulatory rule:
    [   22.240000] cfg80211: 2402000 KHz - 2472000 KHz @ 40000 KHz), (N/A mBi, 2000 mBm)
    [   22.240000] cfg80211: Updating information on frequency 2422 MHz with regulatory rule:
    [   22.240000] cfg80211: 2402000 KHz - 2472000 KHz @ 40000 KHz), (N/A mBi, 2000 mBm)
    [   22.240000] cfg80211: Updating information on frequency 2427 MHz with regulatory rule:
    [   22.240000] cfg80211: 2402000 KHz - 2472000 KHz @ 40000 KHz), (N/A mBi, 2000 mBm)
    [   22.240000] cfg80211: Updating information on frequency 2432 MHz with regulatory rule:
    [   22.240000] cfg80211: 2402000 KHz - 2472000 KHz @ 40000 KHz), (N/A mBi, 2000 mBm)
    [   22.240000] cfg80211: Updating information on frequency 2437 MHz with regulatory rule:
    [   22.240000] cfg80211: 2402000 KHz - 2472000 KHz @ 40000 KHz), (N/A mBi, 2000 mBm)
    [   22.240000] cfg80211: Updating information on frequency 2442 MHz with regulatory rule:
    [   22.240000] cfg80211: 2402000 KHz - 2472000 KHz @ 40000 KHz), (N/A mBi, 2000 mBm)
    [   22.250000] cfg80211: Updating information on frequency 2447 MHz with regulatory rule:
    [   22.250000] cfg80211: 2402000 KHz - 2472000 KHz @ 40000 KHz), (N/A mBi, 2000 mBm)
    [   22.250000] cfg80211: Updating information on frequency 2452 MHz with regulatory rule:
    [   22.250000] cfg80211: 2402000 KHz - 2472000 KHz @ 40000 KHz), (N/A mBi, 2000 mBm)
    [   22.250000] cfg80211: Updating information on frequency 2457 MHz with regulatory rule:
    [   22.250000] cfg80211: 2402000 KHz - 2472000 KHz @ 40000 KHz), (N/A mBi, 2000 mBm)
    [   22.250000] cfg80211: Updating information on frequency 2462 MHz with regulatory rule:
    [   22.250000] cfg80211: 2402000 KHz - 2472000 KHz @ 40000 KHz), (N/A mBi, 2000 mBm)
    [   22.250000] cfg80211: Updating information on frequency 2467 MHz with regulatory rule:
    [   22.250000] cfg80211: 2457000 KHz - 2482000 KHz @ 40000 KHz), (N/A mBi, 2000 mBm)
    [   22.250000] cfg80211: Updating information on frequency 2472 MHz with regulatory rule:
    [   22.250000] cfg80211: 2457000 KHz - 2482000 KHz @ 40000 KHz), (N/A mBi, 2000 mBm)
    [   22.250000] cfg80211: Updating information on frequency 2484 MHz with regulatory rule:
    [   22.250000] cfg80211: 2474000 KHz - 2494000 KHz @ 20000 KHz), (N/A mBi, 2000 mBm)
    [   22.320000] 
    [   22.320000] =============================================
    [   22.320000] [ INFO: possible recursive locking detected ]
    [   22.320000] 4.2.0-rc1 #1 Tainted: G           O   
    [   22.320000] ---------------------------------------------
    [   22.320000] modprobe/87 is trying to acquire lock:
    [   22.320000]  (&(plock)->rlock){+.....}, at: [<bf06fe5c>] rtw_alloc_macid+0x78/0x2bc [8723bs]
    [   22.320000] 
    [   22.320000] but task is already holding lock:
    [   22.320000]  (&(plock)->rlock){+.....}, at: [<bf076544>] rtw_alloc_stainfo+0x28/0x190 [8723bs]
    [   22.320000] 
    [   22.320000] other info that might help us debug this:
    [   22.320000]  Possible unsafe locking scenario:
    [   22.320000] 
    [   22.320000]        CPU0
    [   22.320000]        ----
    [   22.320000]   lock(&(plock)->rlock);
    [   22.320000]   lock(&(plock)->rlock);
    [   22.320000] 
    [   22.320000]  *** DEADLOCK ***
    [   22.320000] 
    [   22.320000]  May be due to missing lock nesting notation
    [   22.320000] 
    [   22.320000] 3 locks held by modprobe/87:
    [   22.320000]  #0:  (&dev->mutex){......}, at: [<c02d4924>] __driver_attach+0x48/0x98
    [   22.320000]  #1:  (&dev->mutex){......}, at: [<c02d4934>] __driver_attach+0x58/0x98
    [   22.320000]  #2:  (&(plock)->rlock){+.....}, at: [<bf076544>] rtw_alloc_stainfo+0x28/0x190 [8723bs]
    [   22.320000] 
    [   22.320000] stack backtrace:
    [   22.320000] CPU: 0 PID: 87 Comm: modprobe Tainted: G           O    4.2.0-rc1 #1
    [   22.320000] Hardware name: Allwinner sun4i/sun5i Families
    [   22.320000] [<c0015aa8>] (unwind_backtrace) from [<c0012d04>] (show_stack+0x10/0x14)
    [   22.320000] [<c0012d04>] (show_stack) from [<c050df28>] (dump_stack+0x88/0x98)
    [   22.320000] [<c050df28>] (dump_stack) from [<c0065be8>] (__lock_acquire+0x1c7c/0x2080)
    [   22.320000] [<c0065be8>] (__lock_acquire) from [<c00668d4>] (lock_acquire+0x6c/0x8c)
    [   22.320000] [<c00668d4>] (lock_acquire) from [<c0513e0c>] (_raw_spin_lock_bh+0x40/0x50)
    [   22.320000] [<c0513e0c>] (_raw_spin_lock_bh) from [<bf06fe5c>] (rtw_alloc_macid+0x78/0x2bc [8723bs])
    [   22.320000] [<bf06fe5c>] (rtw_alloc_macid [8723bs]) from [<bf076698>] (rtw_alloc_stainfo+0x17c/0x190 [8723bs])
    [   22.320000] [<bf076698>] (rtw_alloc_stainfo [8723bs]) from [<bf076b7c>] (rtw_init_bcmc_stainfo+0x30/0x3c [8723bs])
    [   22.320000] [<bf076b7c>] (rtw_init_bcmc_stainfo [8723bs]) from [<bf089a70>] (rtw_init_drv_sw+0x128/0x168 [8723bs])
    [   22.320000] [<bf089a70>] (rtw_init_drv_sw [8723bs]) from [<bf08b4c0>] (rtw_sdio_if1_init+0x138/0x1d4 [8723bs])
    [   22.320000] [<bf08b4c0>] (rtw_sdio_if1_init [8723bs]) from [<bf08b5a0>] (rtw_drv_init+0x44/0xf8 [8723bs])
    [   22.320000] [<bf08b5a0>] (rtw_drv_init [8723bs]) from [<c039e9f0>] (sdio_bus_probe+0x100/0x118)
    [   22.320000] [<c039e9f0>] (sdio_bus_probe) from [<c02d4798>] (driver_probe_device+0x174/0x2b8)
    [   22.320000] [<c02d4798>] (driver_probe_device) from [<c02d4970>] (__driver_attach+0x94/0x98)
    [   22.320000] [<c02d4970>] (__driver_attach) from [<c02d2cec>] (bus_for_each_dev+0x68/0x9c)
    [   22.320000] [<c02d2cec>] (bus_for_each_dev) from [<c02d3f98>] (bus_add_driver+0x19c/0x214)
    [   22.320000] [<c02d3f98>] (bus_add_driver) from [<c02d5174>] (driver_register+0x78/0xf8)
    [   22.320000] [<c02d5174>] (driver_register) from [<bf189088>] (init_module+0x88/0xe0 [8723bs])
    [   22.320000] [<bf189088>] (init_module [8723bs]) from [<c0009750>] (do_one_initcall+0x8c/0x1d8)
    [   22.320000] [<c0009750>] (do_one_initcall) from [<c050d548>] (do_init_module+0x5c/0x1d0)
    [   22.320000] [<c050d548>] (do_init_module) from [<c009874c>] (load_module+0x18c0/0x1f44)
    [   22.320000] [<c009874c>] (load_module) from [<c0098ea0>] (SyS_init_module+0xd0/0x120)
    [   22.320000] [<c0098ea0>] (SyS_init_module) from [<c000f400>] (ret_fast_syscall+0x0/0x54)
    [   22.960000] cfg80211: Updating information on frequency 2412 MHz with regulatory rule:
    [   22.980000] cfg80211: 2402000 KHz - 2472000 KHz @ 40000 KHz), (N/A mBi, 2000 mBm)
    [   23.000000] cfg80211: Updating information on frequency 2417 MHz with regulatory rule:
    [   23.010000] cfg80211: 2402000 KHz - 2472000 KHz @ 40000 KHz), (N/A mBi, 2000 mBm)
    [   23.030000] cfg80211: Updating information on frequency 2422 MHz with regulatory rule:
    [   23.050000] cfg80211: 2402000 KHz - 2472000 KHz @ 40000 KHz), (N/A mBi, 2000 mBm)
    [   23.070000] cfg80211: Updating information on frequency 2427 MHz with regulatory rule:
    [   23.080000] cfg80211: 2402000 KHz - 2472000 KHz @ 40000 KHz), (N/A mBi, 2000 mBm)
    [   23.100000] cfg80211: Updating information on frequency 2432 MHz with regulatory rule:
    [   23.120000] cfg80211: 2402000 KHz - 2472000 KHz @ 40000 KHz), (N/A mBi, 2000 mBm)
    [   23.140000] cfg80211: Updating information on frequency 2437 MHz with regulatory rule:
    [   23.150000] cfg80211: 2402000 KHz - 2472000 KHz @ 40000 KHz), (N/A mBi, 2000 mBm)
    [   23.170000] cfg80211: Updating information on frequency 2442 MHz with regulatory rule:
    [   23.190000] cfg80211: 2402000 KHz - 2472000 KHz @ 40000 KHz), (N/A mBi, 2000 mBm)
    [   23.200000] cfg80211: Updating information on frequency 2447 MHz with regulatory rule:
    [   23.220000] cfg80211: 2402000 KHz - 2472000 KHz @ 40000 KHz), (N/A mBi, 2000 mBm)
    [   23.240000] cfg80211: Updating information on frequency 2452 MHz with regulatory rule:
    [   23.260000] cfg80211: 2402000 KHz - 2472000 KHz @ 40000 KHz), (N/A mBi, 2000 mBm)
    [   23.270000] cfg80211: Updating information on frequency 2457 MHz with regulatory rule:
    [   23.290000] cfg80211: 2402000 KHz - 2472000 KHz @ 40000 KHz), (N/A mBi, 2000 mBm)
    [   23.310000] cfg80211: Updating information on frequency 2462 MHz with regulatory rule:
    [   23.320000] cfg80211: 2402000 KHz - 2472000 KHz @ 40000 KHz), (N/A mBi, 2000 mBm)
    [   23.340000] cfg80211: Updating information on frequency 2467 MHz with regulatory rule:
    [   23.360000] cfg80211: 2457000 KHz - 2482000 KHz @ 40000 KHz), (N/A mBi, 2000 mBm)
    [   23.370000] cfg80211: Updating information on frequency 2472 MHz with regulatory rule:
    [   23.390000] cfg80211: 2457000 KHz - 2482000 KHz @ 40000 KHz), (N/A mBi, 2000 mBm)
    [   23.410000] cfg80211: Updating information on frequency 2484 MHz with regulatory rule:
    [   23.430000] cfg80211: 2474000 KHz - 2494000 KHz @ 20000 KHz), (N/A mBi, 2000 mBm)
    [   23.450000] RTL871X: rtw_ndev_init(wlan0)
    [   23.460000] RTL871X: rtw_ndev_init(wlan1)
    [   23.470000] RTL871X: module init ret=0
    [   34.570000] Bluetooth: Core ver 2.20
    [   34.570000] Bluetooth: Starting self testing
    [   34.630000] Bluetooth: ECDH test passed in 55193 usecs
    [   34.650000] Bluetooth: SMP test passed in 149 usecs
    [   34.650000] Bluetooth: Finished self testing
    [   34.650000] NET: Registered protocol family 31
    [   34.650000] Bluetooth: HCI device and connection manager initialized
    [   34.650000] Bluetooth: HCI socket layer initialized
    [   34.650000] Bluetooth: L2CAP socket layer initialized
    [   34.650000] Bluetooth: SCO socket layer initialized
    [   34.680000] Bluetooth: HCI UART driver ver 2.3
    [   34.680000] Bluetooth: HCI UART protocol H4 registered
    [   34.680000] Bluetooth: HCI UART protocol BCSP registered
    [   34.680000] Bluetooth: HCI UART protocol LL registered
    [   34.680000] Bluetooth: HCI UART protocol ATH3K registered
    [   34.680000] Bluetooth: HCI UART protocol Three-wire (H5) registered
    [   34.680000] Bluetooth: HCI UART protocol BCM registered
    [   35.160000] Bluetooth: BNEP (Ethernet Emulation) ver 1.3
    [   35.160000] Bluetooth: BNEP socket layer initialized
    [   81.280000] cfg80211: Verifying active interfaces after reg change

## Other Information

RTL8723BS_BT Version
https://github.com/lwfinger/rtl8723bs_bt.git
RTL8723BS MP Driver Version (Custom Git repository)  --->                                                
https://github.com/NextThingCo/RTL8723BS.git) URL of custom repository 


