# PocketCHIP

- [Troubleshooting](http://www.chip-community.org/index.php/Troubleshooting)
- [Emulators](https://bbs.nextthing.co/t/emulators-on-pocketchip-my-tests/5687)

```sh
chip@chip:~$ sudo apt-get install openssh-server
```

```sh
xe1gyq@jessie:~$ ssh chip@192.168.1.68
chip@192.168.1.68's password: 

The programs included with the Debian GNU/Linux system are free software;
the exact distribution terms for each program are described in the
individual files in /usr/share/doc/*/copyright.

Debian GNU/Linux comes with ABSOLUTELY NO WARRANTY, to the extent
permitted by applicable law.
Last login: Tue Jul 19 05:13:48 2016 from 192.168.1.70
chip@chip:~$ uname -a
Linux chip 4.3.0-ntc #1 SMP Wed May 11 21:57:30 UTC 2016 armv7l GNU/Linux
chip@chip:~$ 
```

```sh
chip@chip:~$ DISPLAY=:0.0 application
```

# Touchscreen Calibration

```sh
chip@chip:~$ DISPLAY=:0.0 xinput_calibrator
Calibrating EVDEV driver for "1c25000.rtp" id=6
	current calibration values (from XInput): min_x=3965, max_x=112 and min_y=3776, max_y=227

Doing dynamic recalibration:
	Setting calibration data: 3992, 182, 3694, 276
	--> Making the calibration permanent <--
  copy the snippet below into '/etc/X11/xorg.conf.d/99-calibration.conf' (/usr/share/X11/xorg.conf.d/ in some distro's)
Section "InputClass"
	Identifier	"calibration"
	MatchProduct	"1c25000.rtp"
	Option	"Calibration"	"3992 182 3694 276"
	Option	"SwapAxes"	"0"
EndSection
chip@chip:~$ 
```