# Research Unix Verion 7

This is the result of following the gunkies.org wiki.

Everything is ready. I did it so you dont have to. I have installed Research Unix Verion 7 and **NOTHIG** else. So you have a pure system.

From here you can do what you want. I Would suggest to copy/backup the file `rp06-0.disk`, if you mess things up, you can easily revert.

----

What else you need: Nothing really (if you're using a 64bit linux distro), i even included the pdp11 emulator. But you should be using your Distros `simh` package, which should be having the latest version.

----

### Contents:

- File `pdp11`: Its from [archlinux](https://archlinux.org/packages/community/x86_64/simh/) repo, `simh` version 3.11.1-2. Use this if your distro doesnt have the `simh` package, or if it wont work with this project. This is a x86_64 binary. [SimH Github Repo](https://github.com/simh/simh/)
- File `rp06-0.disk` is the "disk" of the system. Thats where the system is installed. make a copy of it for backup.
- Files `nboot.ini` and `tapei.ini` are configs for the SimH emulator.
- Directory `www.tuhs.org/`: i literaly `wget --no-parent -r https://www.tuhs.org/Archive/Distributions/Research/Keith_Bostic_v7/`. So you have everything you need if you want to do it yourself.
- Directory `docs/`:
	- File `Installing_v7_on_SIMH__gunkies.org__.html` is all you need to follow. Is a readable form, i link to the original, and original archive.
	- File `research-unix-7-pdp11-45.pdf` is recommended from the gunkies wiki page. If you want to customize/tailor the system, follow this pdf.

----

### How to:

FIRST: Uncompress the disk image `unxz rp06-0.disk.xz`. I had to compress the disk image. Github limit it 100Mb.

Read the gunkies.org wiki [official wiki-site](https://gunkies.org/wiki/Installing_v7_on_SIMH) or [readable archive locally](docs/Installing_v7_on_SIMH__gunkies.org__.html), section "Normal Boot", part "And let's boot up!". But Here is a **very short** tutorial, to **just** start it:

>type `./pdp11 nboot.ini` and it will start
>
>wait to prompt, then type `boot`
>
>wait to prompt, then type `hp(0,0)unix`
