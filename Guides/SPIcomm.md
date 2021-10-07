# SPI Communcation

## But, what is SPI?:

SPI stands for Serial Peripheral Interface 
and it's a synchronous **(with an internal clock)** serial communication **(sending data one bit at a time, sequentially, over a communication channel or computer bus)** interface specification, which means it's a standard that your interface has to comply with if it wants to be called so. It is primarily used for short-distance communication, in embedded systems. 

![image](https://upload.wikimedia.org/wikipedia/commons/thumb/e/ed/SPI_single_slave.svg/350px-SPI_single_slave.svg.png)

Sometimes SPI is called a four-wire serial bus, in contrast to three-, two-, and one-wire serial buses. The SPI may be accurately described as a synchronous serial interface, but it is different from the **Synchronous Serial Interface (SSI) protocol**, which is also a four-wire synchronous serial communication protocol. The SSI protocol employs differential signaling and provides only a single simplex communication channel. For any given transaction SPI is one master and multi slave communication.

Developed by Motorola in the 1980s, SPI boasts both simple implementation and high-speed data transfer capability. For these reasons, we can see SPI at use in a wide variety of applications, from sensors to camera lens control, communications, and data storage on SD cards.

## SPI Communication:

SPI communication takes place in a **master/slave** configuration, where a single master can choose between one or more slave devices. And where both master and slave can transmit data at the same time.

![image2](https://upload.wikimedia.org/wikipedia/commons/thumb/f/fc/SPI_three_slaves.svg/300px-SPI_three_slaves.svg.png)

SPI devices also communicate in full duplex.
A full-duplex system allows communication in both directions, and, unlike half-duplex, allows this to happen simultaneously.

4-wire SPI devices have four signals:
- SCLK: Serial Clock (output from master)
- MOSI: Master Out Slave In (data output from master)
- MISO: Master In Slave Out (data output from slave)
- CS /SS: Chip/Slave Select (often active low, output from master to indicate that data is being sent)

![image3](https://www.circuitbasics.com/wp-content/uploads/2016/01/Introduction-to-SPI-Master-and-Slave.png)


The clock signal synchronizes the output of data bits from the master to the sampling of bits by the slave. One bit of data is transferred in each clock cycle, so the speed of data transfer is determined by the frequency of the clock signal. SPI communication is always initiated by the master since the master configures and generates the clock signal.

Any communication protocol where devices share a clock signal is known as synchronous. Because of this SPI is a synchronous communication protocol. 

The clock signal in SPI can be modified using the properties of clock polarity and clock phase. These two properties work together to define when the bits are output and when they are sampled. Clock polarity can be set by the master to allow for bits to be output and sampled on either the rising or falling edge of the clock cycle. Clock phase can be set for output and sampling to occur on either the first edge or second edge of the clock cycle, regardless of whether it is rising or falling.

Since the master has multiple slaves, it can choose which slave it wants to communicate with by setting the slave’s CS/SS line to a low voltage level, because the slave select line is always kept at a high voltage level. Multiple CS/SS pins may be available on the master, which allows for multiple slaves to be wired in parallel. If only one CS/SS pin is present, multiple slaves can be wired to the master by daisy-chaining (wiring scheme in which multiple devices are wired together in sequence or in a ring).

There are two ways to connect multiple slaves to the master. If the master has multiple slave select pins, the slaves can be wired in parallel like this:

![image4](https://www.circuitbasics.com/wp-content/uploads/2016/01/Introduction-to-SPI-Multiple-Slave-Configuration-Separate-Slave-Select-293x300.png)

And if only one slave select pin is available, the slaves can be daisy-chained like this:

![image5](https://www.circuitbasics.com/wp-content/uploads/2016/01/Introduction-to-SPI-Multiple-Slave-Configuration-Daisy-Chained-295x300.png)

## Steps of the Communication:

To begin SPI communication, the master must send the clock signal and select the slave by enabling the CS signal. Like we said chip select is an active high signal; hence, the master must send a low signal to select the slave. Both master and slave can send data at the same time via the MOSI and MISO lines respectively. 

- Steps:

1. The master outputs the clock signal.

![image](https://www.circuitbasics.com/wp-content/uploads/2016/01/Introduction-to-SPI-Data-Transmission-Diagram-Clock-Signal-768x198.png)

2. The master switches the SS/CS pin to a low voltage state, which activates the slave.

![image2](https://www.circuitbasics.com/wp-content/uploads/2016/01/Introduction-to-SPI-Data-Transmission-Diagram-Slave-Select-Activation-768x198.png)

3. The master sends the data one bit at a time to the slave along the MOSI line. The slave reads the bits as they are received.

![image3](https://www.circuitbasics.com/wp-content/uploads/2016/01/Introduction-to-SPI-Data-Transmission-Diagram-Master-to-Slave-Data-Transfer-768x198.png)

4. If a response is needed, the slave returns data one bit at a time to the master along the MISO line. The master reads the bits as they are received.

![image4](https://www.circuitbasics.com/wp-content/uploads/2016/01/Introduction-to-SPI-Data-Transmission-Diagram-Slave-to-Master-Data-Transfer-768x198.png)

## Advantages and Disadvantages:

**Advantages**
- No start and stop bits, so the data can be streamed continuously without interruption.

- No complicated slave addressing system like I2C.

- Higher data transfer rate than I2C.

- Separate MISO and MOSI lines, so data can be sent and received at the same time.

**DisadvantagesS**

- Uses four wires (I2C and UARTs use two).

-No acknowledgement that the data has been successfully received (I2C has this).

- No form of error checking like the parity bit in UART
Only allows for a single master.

## References:

Most of the information and images where taken from [here](https://www.circuitbasics.com/basics-of-the-spi-communication-protocol/).





