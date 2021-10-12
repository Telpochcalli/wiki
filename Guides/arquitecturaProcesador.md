# Processor Architecture

## Central Procesing Unit:

The **Central Procesing Unit**, known as **CPU** for short acts as the computers brain, this is because the CPU is the electronic circuit inside the computer that is tasked with doing all the instructions the users asks. Like basic 
maths, logical comparisons and controling the input and output (I/O).

Below you can see a simplified diagram descriping what the CPU contains. You can see that the arithmetic logit unit (ALU) and the control unit (CU) are contained inside de CPU as well as the register bank which in this diagram is represented by the memory unit, all of which we will explain with detail later.

![image](https://computersciencewiki.org/images/1/1a/Cpu_diagram.png)

## Control Unit:

The control unit of the central processing unit regulates and integrates the operations of the computer. It selects and retrieves instructions from the memory bank and interprets them. It does this interpretation to know what information to give to the other parts of the CPU and to know when to activate the other functional elements of it.
  
All the input data is transferred form the memory bank to the arithmetic-logic unit, which we will cover in detail below, but in summary it is the unit for processing the information, which involves the four basic arithmetic functions (addition, subtraction, multiplication, and division), certain logic operations such as the comparing of data and the selection of the desired problem-solving procedure or a viable alternative based on predetermined decision criteria.

So you can say the control unit controls the flow of data within the system.

Furthermore, the control unit controls and monitors communications between the hardware attached to the computer. It controls the input and output of data, checks that signals have been delivered successfully, and makes sure that data goes to the correct place at the correct time.

The diagram below show how it works in a more visual way:

![image2](https://www.computerhope.com/jargon/m/machine-cycle.png)

## ALU

Like said before, in a computer, the **CPU** (Central Processing Unit) is the one in charge of interpretating and executing instructions. One of its various components is the **ALU** (Arithmetic Logic Unit). The ALU is the component in charge of performing logical operations. It receives two integer operands with which it performs the operation and returns the result of the operation. 

The ALU is represented by the following symbol:

![image](https://ati.ttu.ee/IAY0340/labs/Tutorials/SystemC/ALU/ALU.png)

The ALU is capable of performing these operations:

1.	Addition. Adds A and B with carry-in or carry-out sum at Y.
2.	Subtraction. Subtracts B from A or vice versa with the difference at Y and carry-in or carry-out.
3.	Increment. Where A or B is increased by one and Y represents the new value.
4.	Decrement. Where A or B is decreased by one and Y represents the new value.
5.	AND. The bitwise logic AND of A and B is represented by Y.
6.	OR. The bitwise logic OR of A and B is represented by Y.
7.	Exclusive-OR. The bitwise logic XOR of A and B is represented by Y.



## Register Bank:
Registers are used in computer systems as places to store a wide variety of data, such  as  addresses,  program  counters,  or  data  necessary  for  program  execution. In a simplified way,  a  register is  a  hardware  device  that  stores  binary  data.  Registers  arelocated on the processor so information can be accessed very quickly. 

Data  processing  on  a  computer  is  usually  done  on  fixed  size  binary  wordsthat are stored in registers. Therefore, most computers have registers of a certainsize.  Common  sizes  include  16,  32,  and  64  bits.  

Registers contain data, addresses, or control information.  Some  registers  are  specified  as  “special  purpose”  and  may  contain only  data,  only  addresses,  or  only  control  information.  Other  registers  are  more generic and may hold data, addresses, and control information at various times.Information is written to registers, read from registers, and transferred fromregister  to  register.  Registers  are  not  addressed  in  the  same  way  memory  is addressed. Registers are addressed and manipulated by the control unit itself. In  modern  computer  systems,  there  are  many  types  of  specialized  registers that:

- Store  information
- Shift  values
- Compare values
- Count
