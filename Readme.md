# ovsd package for OpenWrt

This is an OpenWrt feed repository for [ovsd](https://github.com/arkap/ovsd.git).
Ovsd is an external device handler for Open vSwitch to be used with the external device handler extension for netifd.


## Installation

Install this as a feed by adding the following line to `feeds.conf` in your OpenWrt source tree:
```
src-git ovsd https://github.com/arkap/package-ovsd.git
```
Next, run
```bash
scripts/feeds update ovsd
scripts/feeds install ovsd
```
from the same directory. There should now be a package `ovsd` selectable in `Network` when you run
`make menuconfig`.
