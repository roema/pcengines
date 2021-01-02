# PC Engines - NanoBSD

Build a nanoBSD for PC Engines APU boards.

It is a really stable system with very little power consumption. During the last 10 years I realized various projects like VoIP with Kamailio or Asterisk.

During a stress test Asterisk could handle 180 calls in a freeBSD jail with an apu1d board at the same time.

```
cd /usr/src/tools/tools/nanobsd/
```
```
Usage: nanobsd.sh [-bfhiKknqvwX] [-c config_file]
	-b	suppress builds (both kernel and world)
	-c	specify config file
	-f	suppress code slice extraction
	-h	print this help summary page
	-i	suppress disk image build
	-K	suppress installkernel
	-k	suppress buildkernel
	-n	add -DNO_CLEAN to buildworld, buildkernel, etc
	-q	make output more quiet
	-v	make output more verbose
	-w	suppress buildworld
	-X	make native-xtools
```

At the first call, the nanobsd script must be started as follows. The files MINI and KERNEL must be in the same directory.

```
sh nanobsd.sh -c MINI
```
This can take some time because buildworld and buildkernel are running.


If you want to create a new image after a change, you can call up nanobsd with the -b switch.

```
sh nanobsd.sh -b -c MINI
```

The finished image can be found at

```
cd /usr/obj/nanobsd.APUJ
```
