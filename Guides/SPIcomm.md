# SPI Communcation

## But, what is SPI?:

SPI stands for Serial Peripheral Interface 
and it's a synchronous **(with an internal clock)** serial communication **(sending data one bit at a time, sequentially, over a communication channel or computer bus)** interface specification, which means it's a standard that your interface has to comply with if it wants to be called so. It is primarily used for short-distance communication, in embedded systems. 

![image](https://upload.wikimedia.org/wikipedia/commons/thumb/e/ed/SPI_single_slave.svg/350px-SPI_single_slave.svg.png)

Developed by Motorola in the 1980s, SPI boasts both simple implementation and high-speed data transfer capability. For these reasons, we can see SPI at use in a wide variety of applications, from sensors to camera lens control, communications, and data storage on SD cards. SPI communication takes place in a **master/slave** configuration, where a single master can choose between one or more slave devices.

![image2](https://upload.wikimedia.org/wikipedia/commons/thumb/f/fc/SPI_three_slaves.svg/300px-SPI_three_slaves.svg.png)

SPI devices communicate in full duplex 
A full-duplex (FDX) system allows communication in both directions, and, unlike half-duplex, allows this to happen simultaneously.

mode using a master-slave architecture usually with a single master (though some Atmel devices support changing roles on the fly depending on an external (SS) pin). The master (controller) device originates the frame for reading and writing. Multiple slave-devices may be supported through selection with individual chip select (CS), sometimes called slave select (SS) lines.

Sometimes SPI is called a four-wire serial bus, contrasting with three-, two-, and one-wire serial buses. The SPI may be accurately described as a synchronous serial interface,[1] but it is different from the Synchronous Serial Interface (SSI) protocol, which is also a four-wire synchronous serial communication protocol. The SSI protocol employs differential signaling and provides only a single simplex communication channel. For any given transaction SPI is one master and multi slave communication.



