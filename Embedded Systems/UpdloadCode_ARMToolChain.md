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

1. [ARM gcc tool chain](https://developer.arm.com/tools-and-software/open-source-software/developer-tools/gnu-toolchain/gnu-rm). This includes a compiler, debugger and libraries to develop to an ARM platform. 
2. CMake. Tool to ease compiling process. 


### Linux:
1. GDB 
2. 
### Windows: