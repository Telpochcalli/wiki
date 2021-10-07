# What is a protocol?

## Introduction to protocols:

When you connect a microcontroller to a sensor, display, or other module, do you ever stop and think about how this is posible, how the two devices are able to understand each other?

Well, communication between electronic devices can be compared in a way to human communication, because in both each part needs to speak the same language. In electronics, these languages are called communication protocols.

Here, we will introduce the basics of protocols to then pass on to some of the most common protocols: Serial Peripheral Interface (SPI), Inter-Integrated Circuit (I2C), Universal Asynchronous Receiver/Transmitter (UART) and Universal Synchronous/Asynchronous Receiver/Transmitter (USART).

![image](https://www.mbtechworks.com/hardware/imgs/uart-spi-i2c.png)

These are quite a bit slower than protocols that may sound more familiar to you like USB, ethernet, Bluetooth, and WiFi, but they’re a lot simpler and use less hardware and system resources. These protocols are ideal for communication between microcontrollers and between microcontrollers and sensors where large amounts of high speed data don’t need to be transferred.

Summarizing:

A **Protocol** is a set of rules and regulations. 
**Communication** is the exchange of information from one system to another system with a medium.
And a **Communication Protocol** is a set of rules and regulations that allow two electronic devices to connect to exchange the data with one and another.

## Inter and Intra System Protocols:

Inter-system protocols are used to achieve communication between two different devices. Like between a computer and a microcontroller kit, this communication is done through an inter bus system.

Intra system protocols are used when we want to communicate two devices within the circuit board. Using intra system protocols circuit complexity and power consumption wil be decreased and it will ensure a secure environment to access data.

## Serial vs. Parallel Communication:

Electronic devices talk to each other by sending bits of data through wires physically connected between devices. A bit is like a letter in a word, except instead of the 26 letters (in the English alphabet), a bit is binary and can only be a 1 or 0 (for more information  visit our [binary guide](https://github.com/Telpochcalli/wiki/blob/Guides/Guides/binary.md) where we cover this in depth). Bits are transferred from one device to another by quick changes in voltage. In a system operating at 5 V, a 0 bit is communicated as a short pulse of 0 V, and a 1 bit is communicated by a short pulse of 5 V.

The bits of data can be transmitted either in parallel or serial form.
In parallel communication, the bits of data are sent all at the same time, each through a separate wire. The following diagram shows the parallel transmission of the letter “C” in binary (01000011):

![imagen1](https://www.circuitbasics.com/wp-content/uploads/2016/01/Introduction-to-SPI-Parallel-Transmission-of-One-Byte-3-300x191.png)

In serial communication, the bits are sent one by one through a single wire. The following diagram shows the serial transmission of the letter “C” in binary (01000011):

![imagen2](https://www.circuitbasics.com/wp-content/uploads/2016/01/Introduction-to-SPI-Serial-Transmission-of-the-Letter-C-300x92.png)