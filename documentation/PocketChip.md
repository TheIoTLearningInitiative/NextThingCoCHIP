# PocketCHIP

- [Information Resources](https://bbs.nextthing.co/t/information-resources/3382)
- [Troubleshooting](http://www.chip-community.org/index.php/Troubleshooting)
- [Emulators](https://bbs.nextthing.co/t/emulators-on-pocketchip-my-tests/5687)
- [C.H.I.P. Projects to Start With](https://www.hackster.io/glowascii/c-h-i-p-projects-to-start-with-7a8485?ref=part&ref_id=16248&offset=7)
- [AlexCHIP](https://github.com/sammachin/AlexaCHIP)

```sh
chip@chip:~$ sudo apt-get install openssh-server
```

# Connecting Through SSH

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

# Application Launching Through SSH

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

```sh
chip@chip:~$ sudo nano /etc/X11/xorg.conf

We trust you have received the usual lecture from the local System
Administrator. It usually boils down to these three things:

    #1) Respect the privacy of others.
    #2) Think before you type.
    #3) With great power comes great responsibility.

[sudo] password for chip: 
```

## Screenshot

```sh
chip@chip:~$ sudo apt-get install gnome-screenshot             
Reading package lists... Done
Building dependency tree       
Reading state information... Done
The following NEW packages will be installed:
  gnome-screenshot
...
Setting up gnome-screenshot (3.14.0-1) ...
chip@chip:~$ 
```

```sh
chip@chip:~$ gnome-screenshot --display=:0

(gnome-screenshot:19483): Gtk-WARNING **: Locale not supported by C library.
	Using the fallback 'C' locale.

(gnome-screenshot:19483): GLib-GIO-CRITICAL **: g_dbus_connection_call_sync_internal: assertion 'G_IS_DBUS_CONNECTION (connection)' failed
** Message: Unable to use GNOME Shell's builtin screenshot interface, resorting to fallback X11.

(gnome-screenshot:19483): GLib-GObject-CRITICAL **: g_object_unref: assertion 'G_IS_OBJECT (object)' failed
chip@chip:~$ 
```

# Gaming Doom

```sh
chip@chip:~$ sudo apt-get install prboom
chip@chip:~$ sudo apt-get install doom-wad-shareware
```