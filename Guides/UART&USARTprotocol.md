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

Like a UART, a USART provides the computer with the interface necessary for communication with modems and other serial devices. However, unlike a UART, a USART offers the option of synchronous mode. In program-to-program communication, the synchronous mode requires that each end of an exchange respond in turn without initiating a new communication. Asynchronous operation means that a process operates independently of other processes.

Practical differences between synchronous mode (which is possible only with a USART) and asynchronous mode (which is possible with either a UART or a USART) can be outlined as follows:

Synchronous mode requires both data and a clock. Asynchronous mode requires only data.
In synchronous mode, the data is transmitted at a fixed rate. In asynchronous mode, the data does not have to be transmitted at a fixed rate.
Synchronous data is normally transmitted in the form of blocks, while asynchronous data is normally transmitted one byte at a time.
Synchronous mode allows for a higher DTR (data transfer rate) than asynchronous mode does, if all other factors are held constant.



