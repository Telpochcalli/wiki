# Upload code ARM Tool Chain

Sorry bro, we still haven't figure this out 😔.


## Concepts:

1. Cross-compilation: The process of compiling desgined for a differernt platform that the one that is coded in.
   1. Build system: Where code is written and built. 
   2. Host system: Where code is executed

* You can virtualize systems on the host Platform, a known tool to do so is [Qemu](https://www.qemu.org/).
  * *file.dtb* is a "devicetree file. It's readen by the Linux Kernel and contains information about a system's hardware. 
* Files withhout extentions are binaries. (In Unix systems). 

## Universal Requirements:

* [ARM gcc tool chain](https://developer.arm.com/tools-and-software/open-source-software/developer-tools/gnu-toolchain/gnu-rm). This includes a compiler, debugger and libraries to develop to an ARM platform. 
* CMake. Tool to ease compiling process. 
* Free tools to burn (upload) the code onto the board:
    * STLINK: https://github.com/stlink-org/stlink
    * Install on Windows: https://github.com/stlink-org/stlink/blob/develop/doc/compiling.md#Windows
    * Install on Ubuntu:

    sudo add-apt-repository ppa:team-gcc-arm-embedded/ppa

    sudo apt update

* OpenOCD: http://openocd.org/getting-openocd/ 
    * Necesary to debug


https://askubuntu.com/questions/637113/unable-to-locate-package-lib32bz2-1-0


### Linux:
1. GDB 
2. 
### Windows: