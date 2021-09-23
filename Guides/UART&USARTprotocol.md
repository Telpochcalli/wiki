# UART & USART Protocol

In this guide we will be extensively reviewing what is **UART** and **USART** and they work.

### What is UART?:

UART stands for Universal Asynchronous Receiver/Transmitter. And it is not a communication protocol like SPI and I2C, but a physical circuit in a microcontroller, or a stand-alone integrated circuit (IC). A UART’s main purpose is to transmit and receive serial data.

### UART Communication:

It occurs bewteen two UARTs. Where the transmitting UART converts parallel data from a controlling device like a CPU into serial form and then transmits it in serial to the receiving UART, which then converts the serial data back into parallel data. Only two wires are needed to transmit data between two UARTs. Data flows from the Tx pin of the transmitting UART to the Rx pin of the receiving UART as seen in the following image:

![image](https://www.circuitbasics.com/wp-content/uploads/2016/01/Introduction-to-UART-Basic-Connection-Diagram.png)

UARTs transmit data asynchronously, which means there is no clock signal to synchronize the output of bits from the transmitting UART to the sampling of bits by the receiving UART. Instead of a clock signal, the transmitting UART adds start and stop bits to the data packet being transferred. These bits define the beginning and end of the data packet so the receiving UART knows when to start and end the reading of the bits.

When the receiving UART detects a start bit, it starts to read the incoming bits at a specific frequency known as the *baud rate*. *Baud rate* is a measure of the speed of data transfer, expressed in bits per second (bps). Both UARTs must operate at about the same *baud rate*. The *baud rate* between the transmitting and receiving UARTs can only differ by about 10% before the timing of bits gets too far off.

Both UARTs must also must be configured to transmit and receive the same data packet structure.

### What is USART?:

A USART (Universal Synchronous/Asynchronous Receiver/Transmitter) is a microchip that facilitates communication through a computer's serial port using the [RS-232C protocol](https://circuitdigest.com/article/rs232-serial-communication-protocol-basics-specifications).

### USART Communication:

Like a UART, a USART provides the computer with the interface necessary for communication with modems and other serial devices. However, unlike a UART, a USART offers the option of Synchronous mode. In program-to-program communication, the Synchronous mode requires that each end of an exchange to respond in turns without initiating a new communication. Asynchronous operation means that a process operates independently of other processes.

### Synchronous and Asynchronous mode:

- #### Synchronous mode:

Synchronous operation uses a clock and data line.
thats why it requires both data and a clock.

In Synchronous mode, the data is transmitted at a fixed rate.

Synchronous data is normally transmitted in the form of blocks.

Synchronous mode allows for a higher DTR (data transfer rate)

- #### Asynchronous mode:

Asynchronous mode requires only data which means there is no separate clock accompanying the data for Asynchronous transmission.

In Asynchronous mode, the data does not have to be transmitted at a fixed rate.

Asynchronous data is normally transmitted one byte at a time.

Asynchronous mode has a lower DTR (data transfer rate) than Synchronous mode.

Since there is no clock signal in Asynchronous operation, one pin can be used for transmission and another pin can be used for reception. Both transmission and reception can occur at the same time, this is known as **full duplex operation**.

Transmission and reception can be independently enabled. However, when the serial port is enabled, the USART will control both pins and one cannot be used for general purpose I/O (input/output) when the other is being used for transmission or reception.

**The USART is most commonly used in the asynchronous mode.**
