# Notes
Aqui tenemos todas las notas de como se puede programar, tecnicamente un Manuel para el desarrollo de Embedded Systems en Robomaster.
Este contiene PDF's y ReadMes para establecer los detalles de cada parte y su integración en el sistema. Además, funciona como back-up de información que puede no estar dispobible en un futuro. 

**El cotenido debe estar en inglés.**

## Links utiles

Esos links son referencias a otras documentaciones para poder hacer cosas mas chidas y mejor.

1. Official RM GitHub: https://github.com/RoboMaster
1. Offial RM forum: https://bbs.robomaster.com/portal.php

1. STM32 Website: https://www.st.com/content/st_com/en.html
1. Keil IDE: https://www.keil.com/

1. RobotRTS (EN): 
    * https://robomaster.github.io/RoboRTS-Tutorial/#/en/sdk_docs/architecture
    * https://github.com/RoboMaster/RoboRTS-Firmware/blob/icra2021/doc/en/readme.md
    * https://github.com/RoboMaster/RoboRTS-Firmware/blob/icra2021/doc/en/protocol.md
1. Ejemplos de como programar algunas cosas: https://github.com/RoboMaster/Development-Board-C-Examples (los programas si estan chidos, pero el resto como que ni idea de que esta pasando)

1. Docs de como desarroyar par RM: https://robomaster-dev.readthedocs.io/en/latest/
1. Descargar el Python dev env y las cosas: https://robomaster-dev.readthedocs.io/en/latest/python_sdk/installs.html (no por nada, pero Linux y MacOS es millones de veces mas facil, quiza quieran usar o Linux o Mac o WSL)

1. Battery use information under the name "Intelligent Flight Battery Guidelines": https://cdn-hz.robomaster.com/documents/935c504aecb741521451469256431010.pdf

1. Team iRM Guide: https://github.com/illini-robomaster/iRM_Embedded_2020
1. Team iRM tutorials: https://github.com/illini-robomaster/iRM_Embedded_2018/tree/master/tutorials
1. RTOS info: https://www.keil.com/pack/doc/CMSIS/RTOS/html/group__CMSIS__RTOS.html
    * CMIS RTOS and Free RTOS are different dependencies 
1. Guide to crack Keil: https://www.cnblogs.com/sasasatori/p/11599883.html
1. RT-thread: https://www.rt-thread.org/document/site/tutorial/nano/nano-port-cube/an0041-nano-port-cube/ (No es necesario, es un ejemplo de desarrollo)
1. Got many resources from this blog: https://blog.csdn.net/qq_35739721/article/details/105357480
1. J-Link manuals: https://www.segger.com/downloads/jlink/
1. BSP lib: https://github.com/illini-robomaster/iRM_Embedded_Libraries/tree/master/BSP

## Reglas:

- Estamos creando un folder por cada tema.
- Se pueden crear subfolders para subtemas.
- Cualquier cosa pregunten a @JorgePerC.

En general, se divide en los siguientes areas
- Embedded Systems
    - Control de acuadores.
        - Datasheets
        - Manuales
        - Librerías
        - Documentación propia y tips.
    - Implementación sensores
        - Datasheets
        - Librerías
        - Documentación propia y tips.
- Communication
    - Protocols
        - Set up guides

Cada uno puede tener lo que sea.



## Dentro de cada documento:

Intenten seguir este lineamiento:

`Nombre del comando` - *Descripcion basica* Ejemplo de como se usa y cosas extra

Todo esto es para poder buscar todo de forma mas rapida, es un doc en markdown, y, para tener ejemplos el formato tiene que ser NOMBREDELEJEMPLO_example.cpp con referencia en un markdown

Gracias UwU. 🐉

## "Useless" Documentation:
1. RM Training Guidelines Repo:
    https://github.com/RoboMaster/robomaster_training_guidelines
    It contains administrative information about how to get started with a RM team, no actual code. Refers to sites and topics to learn for the robot's development. 
    Must be build by Sphinx (Python). Written in **Chinese**  

## Vocabulary and other stuff:
https://www.youtube.com/watch?v=rXGE4tEj5IM


**.bin files** Binary files. 
**.dll files** _insert_ files. 
**.pdb files** _files_ files. 
**.xml files** _insert_ files. 
**.xaml files** _insert_ files. 
**.ioc files** According to: https://file.org/extension/ioc, specify the which app can use the different files. 
**.bat files** batch file. Contains executable commands for Windows' Console.  https://www.computerhope.com/jargon/b/batchfil.htm. 
**CMOS** 
**RTOS:** Real Time Operating Systems
**G++** Tool to compile C/C++ programs
**Gdb** Tool to debug C/C++ programs
