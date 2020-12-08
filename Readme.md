# ovsd package for OpenWRT

This is an OpenWrt feed repository for [ovsd](https://gitlab.inet.tu-berlin.de/SDWN/ovsd).
Ovsd is an external device handler for Open vSwitch to be used with the external device handler extension for netifd.


## Installation

Install this as a feed by adding the following line to `feeds.conf` in your OpenWRT source tree:
```
src-git ovsd https://gitlab.hhi.fraunhofer.de/wn-ina/ovsd.git
```
Next, run
```bash
scripts/feeds update ovsd
scripts/feeds install ovsd
```
from the same directory. There should now be a package `ovsd` selectable in `Network` when you run
`make menuconfig`.
