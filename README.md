BeagleBone Black-Xenomai
========================

For a full set of instructions on how to use this material, please see <a href="http://yapatel.org/xenomai_bbb.html">Xenomai on BBB Guide</a>!

Robert Nelson's notes:

This just a simple set of scripts to rebuild a known working kernel for ARM devices..

Script Bugs: "bugs@rcn-ee.com"

Dependencies: GCC ARM Cross ToolChain

Linaro:
http://www.linaro.org/downloads/

Angstrom:
http://www.angstrom-distribution.org/simplified-development-setup

Dependencies: Linux Kernel Source

This git repo contains just scripts/patches to build a specific kernel for these
ARM devices. It doesn't any of the mainline kernel source, so it must clone a
local tree for use.

By default this script will clone the linux-stable tree, to ${HOME}/linux-src:
git://git.kernel.org/pub/scm/linux/kernel/git/stable/linux-stable.git

If you've already cloned torvalds tree and would like to save some hard drive
space, just modify the LINUX_GIT variable in system.sh to point to your current
git clone.

Build Kernel Image:

./build_kernel.sh

Optional: Build Debian Package:

./build_deb.sh

Install Kernel Image to SD card: (requires MMC set in system.sh)

./tools/install_kernel.sh

Development/Hacking:

first run (to setup baseline tree): ./build_kernel.sh then modify files under KERNEL directory then run (to rebuild with your changes): ./tools/rebuild.sh


[![Bitdeli Badge](https://d2weczhvl823v0.cloudfront.net/yapatel/beagleboneblack-xenomai/trend.png)](https://bitdeli.com/free "Bitdeli Badge")

