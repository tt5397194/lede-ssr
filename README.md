# LEDE with SSR

copy from  https://github.com/coolsnowwolf/lede 09c550f R7.4.3


Usage:

In Ubuntu 16.04 LTS x64

```shell
sudo apt-get update
sudo apt-get install build-essential asciidoc binutils bzip2 gawk gettext git libncurses5-dev libz-dev patch unzip zlib1g-dev lib32gcc1 libc6-dev-i386 subversion flex uglifyjs git-core gcc-multilib p7zip p7zip-full msmtp libssl-dev texinfo libglib2.0-dev

git clone https://github.com/tt5397194/lede-ssr.git
cd lede-ssr
./scripts/feeds update -a
./scripts/feeds install -a
make menuconfig

# If you want to download the files needed for compilation in advance 
# git clone https://github.com/tt5397194/dl.git 
make -j8

```



========================================================================

This is the buildsystem for the OpenWrt Linux distribution.

Please use "make menuconfig" to choose your preferred
<br>
configuration for the toolchain and firmware.

You need to have installed gcc, binutils, bzip2, flex, python, perl, make,
<br>
find, grep, diff, unzip, gawk, getopt, subversion, libz-dev and libc headers.

Run "./scripts/feeds update -a" to get all the latest package definitions
<br>
defined in feeds.conf / feeds.conf.default respectively
<br>
and "./scripts/feeds install -a" to install symlinks of all of them into
<br>
package/feeds/.

Use "make menuconfig" to configure your image.

Simply running "make" will build your firmware.
<br>
It will download all sources, build the cross-compile toolchain, 
<br>
the kernel and all choosen applications.

To build your own firmware you need to have access to a Linux, BSD or MacOSX system
<br>
(case-sensitive filesystem required). Cygwin will not be supported because of
<br>
the lack of case sensitiveness in the file system.

Sunshine!
<br>
　　Your LEDE Community
<br>
　　http://www.lede-project.org

