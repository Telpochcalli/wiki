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

### How UARTs transmit data:

The UART that is going to transmit data receives the data from a data bus. (The data bus is used to send data to the UART by another device like a CPU, memory, or microcontroller). 

UART transmitted data is organized into packets. Each packet contains 1 start bit, 5 to 9 data bits (depending on the UART), an optional parity bit, and 1 or 2 stop bits.

![imagen](https://www.engineersgarage.com/wp-content/uploads/2019/07/UART-Data-Format.jpg)

Knowing that, the transmission follow these steps:

1. Data is transferred from the data bus to the transmitting UART in parallel form.
2. The transmitting UART that gets the parallel data from the data bus, adds a start bit, a parity bit, and a stop bit, creating the data packet. 
3. The data packet is output serially, bit by bit at the Tx pin. 
4. The receiving UART reads the data packet bit by bit at its Rx pin. 
5. The receiving UART then converts the data back into parallel form and removes the start bit, parity bit, and stop bits. 
6. Finally, the receiving UART transfers the data packet in parallel to the data bus on the receiving end like illustrated in this diagram:

![imagen](https://www.circuitbasics.com/wp-content/uploads/2016/01/Introduction-to-UART-Data-Transmission-Diagram.png)

#### Start Bit:

The UART data transmission line is normally held at a high voltage level when it’s not transmitting data. To start the transfer of data, the transmitting UART pulls the transmission line from high to low for one clock cycle. When the receiving UART detects the high to low voltage transition, it begins reading the bits in the data frame at the frequency of the baud rate.

#### Data Frame:

The data frame contains the actual data being transferred. It can be anything bewteen 5 and 8 bits long if a parity bit is used. If no parity bit is used, the data frame can be 9 bits long. In most cases, the data is sent with the least significant bit first.

#### Parity:

Parity describes the evenness or oddness of a number. The parity bit is a way for the receiving UART to tell if any data has changed during transmission. Bits can be changed by electromagnetic radiation, mismatched *baud rates*, or long distance data transfers. After the receiving UART reads the data frame, it counts the number of bits with a value of 1 and checks if the total is an even or odd number. If the parity bit is a 0 (even parity), the bits with a value of 1 in the data frame should total to an even number. If the parity bit is a 1 (odd parity), the bits with a value of 1 in the data frame should total to an odd number. 

When the parity bit matches the data, the UART knows that the transmission was free of errors. But if the parity bit is a 0, and the total is odd; or the parity bit is a 1, and the total is even, the UART knows that bits in the data frame have changed.

#### Stop Bits:

To signal the end of the data packet, the sending UART drives the data transmission line from a low voltage to a high voltage for at least two bit durations.

### Advantages and Disadvantages of UARTs:

- Advantages:

Only uses two wires.

No clock signal is necessary.

Has a parity bit to allow for error checking.

The structure of the data packet can be changed as long as both sides are set up for it.

Well documented and widely used method.

- Disadvantages:

The size of the data frame is limited to a maximum of 9 bits.

Doesn’t support multiple slave or multiple master systems.

The *baud rates* of each UART must be within 10% of each other.

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

If you want more detailed information on how to use a USART in Asynchronous mode check [this link](http://ww1.microchip.com/downloads/en/devicedoc/usart.pdf).

### Final Conclusions:

As we can see the first major difference between a USART and a UART is the way in which the serial data may be clocked. A UART generates its data clock internally to the microcontroller and synchronizes that clock with the data stream by using the start bit transition. A USART, on the other hand, can be set up to run in synchronous mode. In this mode the sending USART will generate a clock that the receiving one can recover from the data stream without knowing the *baud rate* ahead of time.

The second major difference between a USART and a UART is the number of protocols the microchip can support. A UART is simple and only offers a few options from its base format, such as number of stop bits and even or odd parity. A USART is more complex and can generate data in a form corresponding to many different standard protocols such as IrDA, LIN, Smart Card, Driver Enable for RS-485 interfaces, and Modbus, to name a few. A USART also has the same asynchronous capabilities as a UART, that is, a USART can generate the same type of serial data.