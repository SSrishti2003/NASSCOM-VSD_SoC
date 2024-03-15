# NASSDOM-VSD_SoC
ABOUT- This repository contains all the reports made for NASSCOM-VSD SoC Design Program including all 5 days.
<br>
DAY 1 NASSDOM _VSD-IAT
<b><h1>SKY130_D1_SK1: How to talk to Computers</b></h1>
<b><h2>SKY_L1 - Introduction to QFN-48 Package, chip, pads, core, die and IPs</b></h2>
<br>
![Screenshot 2024-03-14 170431](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/be91649f-8e02-4403-910a-c1373e9cbd92)
<br>
             [ARDUINO UNO BOARD]


The highlighted chip is what we are going to study for now. The diagram below is the block diagram of the board above, with the centre chip or processor highlighted.

![Screenshot 2024-03-14 170546](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/d780c082-594b-424e-8797-0dbea24c9d83)



                                          [BLOCK DIAGRAM OF BOARD]

Now if we try to open and look inside that IC, the below figure is what it will look like. From now on we will call this a package. There are different types of packages and all look different. The pin location of this package is driven by the arduino board it is embedded on.
![Screenshot 2024-03-14 180546](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/523dc8f2-12a5-4840-9f58-bab750141fc9)

                                                                   [PACKAGE]

The chip is sitting at the centre of the package and it is connected to the pins using bond wires. The signals from the outside world are sent to the chip using these wires.
<br>
![Screenshot 2024-03-14 180905](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/536f07e7-76e9-42c0-b3ca-09061f1bb66a)
<br>
                                          [CONNECTION BETWEEN CHIP AND PINS]

Now if you look into the chip and study its important components one of which is pads, which are something through which we send the signal inside the chip and vice versa.
Then comes the core of the chip where our digital logic sits like our gates like OR, AND NOR.  And die is the size of the entire chip, which is getting manufactured on silicon paper.
<br>
![Screenshot 2024-03-14 181639](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/2fdc96cc-3906-4421-8aef-daeedba53f71)
<br>



                                                                  [CHIP]
FOUNDRY:  All performance, all devices are dependent on it. It is a big factory where chips get manufactured.<br>
IP: Intellectual Property and it needs intelligence to build the blocks.<br>
MACROS: Pure digital logic.
<br>
![Screenshot 2024-03-14 182737](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/f3f5b12a-1131-4fe8-b81c-63d7a03638a9)
<br>
        [ FOUNDRY IPS AND MACROS INSIDE A CHIP]

<b><h2>SKY_L2 - Introduction to RISC-V</b></h2>
<br>
![Screenshot 2024-03-14 184429](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/e2b6a615-7c1a-4849-8430-6a74c428bc26)

<br>

RISC-V is the language of the computer. If we want the C program to run on the particular layout, we need to pass the information to the hardware in particular terms. The C program is compiled and converted into machine language.
One more interface is needed to be present between RISC-V architecture and layout and that is the hardware description language. RISC-V specifications need to be implemented using some RTL.

<b><h2>SKY_L3 - From Software Applications to Hardware</b></h2>

<br>

![Screenshot 2024-03-14 191056](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/4a8b2e4f-7115-4f0e-8320-84c8ecab0d97)

<br>

Application Software enters into system software which converts the program into binary language.<br>
Major components of system software are OS, COMPILER and ASSEMBLER. Job of an OS is to take the app and convert it into a respective assembly language program so that it is understood by the hardware.<br>
The output of the OS is small functions in C,C++ JAVA language which using their respective compiler are converted into instructions. The syntax of the instructions depends on the type of hardware.<br>
The work of the assembler is to convert instructions into binary language. Then this binary code is fed to the hardware which performs the specific function.<br>

ex:
<br>
![Screenshot 2024-03-14 191312](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/937ff16c-da95-41be-9960-2f47a3547a96)
![Screenshot 2024-03-14 191350](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/3c327ec4-ea42-45bb-beca-372999754972)
<br>
<br>

![Screenshot 2024-03-14 202606](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/19dff9f6-4efb-4678-80de-304afa70f699)
<br>
Start from the instruction set, get specification of the instruction set, write a hardware description language of the instruction, synthesise it into the gate level, then the gate level is converted into its respective layout using RTL to GDS.


<b><h1>SKY130_D1_SK2 - SoC design and OpenLANE</b></h1>
<b><h2>SKY_L1 - Introduction to all components of open-source digital asic design</b></h2>

Designing Digital Application Specific Integrated circuits( AISC)
<br>

![Screenshot 2024-03-14 212308](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/cb8c0300-eb7a-4551-ae12-669b58d8829e)

<br>

                                             [REQUIREMENTS FOR ASIC]

PDK: Process Design Kit. These are the collection of files used to model for the fabrication process for the EDA tools used in IC design. It contains :<br>
Process Design rules- LVS, DRC, PEX<br>
Device Models<br>
Digital Standard cell Libraries<br>
<br>
![Screenshot 2024-03-14 214112](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/ce9ce495-c023-483a-aafd-19e99237afca)
![Screenshot 2024-03-14 214333](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/6078d34c-66b9-4d9a-af46-2868ba2da42c)

<br>


<b><h2>SKY_L2 - Simplified RTL2GDS flow</h2></b>
<br>
![Screenshot 2024-03-14 214421](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/60c21c84-3a26-4575-ae8b-1416c85bc8f8)
<br>

The first major step in the ASIC flow is the synthesis where RTL is converted into circuit components from standard cell library(SCL). Standard calls have a regular layout. 
<br>
![Screenshot 2024-03-14 215216](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/e849dc54-bf1e-4484-9a18-39a0c41765fe)

<br>
FLOOR AND POWER PLANNING
i)CHIP-FLOORPLANNING- chip die is partitioned between different components.
<br>

![Screenshot 2024-03-14 215444](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/575ef65d-6dec-4c29-8657-545e33fbe34a)

<br>
ii)MACRO PLANNING- define macro dimensions and pic locations. In this step, the rows are not undefined

iii) POWER PLANNING- the power network is constructed. The chip is powered by multiple VDD and GND pins. Parallel strips are used to reduce resistance and to address electro migration problems. Electromigration occurs when the current density in the wires exceeds the specified limits for a given process. It uses upper metal layers which are thicker.
POWER PLANNING
<br>

![Screenshot 2024-03-14 215847](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/7c8a7211-fe8d-4c16-8367-e25b307df371)

<br>
PLACEMENT
Typically done in 2 steps: Global and Detailed
<br>

![Screenshot 2024-03-14 220537](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/ee9967b9-1354-4b8b-b687-60cc8a83d3a5)


<br>
CTS
<br>

![Screenshot 2024-03-14 220614](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/9440a0f2-83c4-48c5-9b65-bdfd3f2a7df9)

<br>
ROUTING: Implement the interconnect using available metal layers. For each metal layer, the pdk defines the thickness, the pitch and defines the tracks the minimum width. The SKYWATER PDK defines 6 routing layers
<br>

![Screenshot 2024-03-14 220714](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/e46e2d47-4190-4e17-95bd-3ad24a30a355)

<br>
<h2><b>SKY_L3,4 - Introduction to OpenLANE </h2></b>
<br>

![Screenshot 2024-03-15 101937](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/3e073c07-e53a-4750-b54d-98ea51fa1ad5)

<br>
ASIC DESIGN FLOW has a number of steps which starts with design RTL and ends with GDSII format.
<br>
1) SYNTHESIS:
RTL is fed to YOSYS, which translates it into a logic circuit. <br>
SYNTH EXPLORATION decides design delay and area. 
<br>

![Screenshot 2024-03-15 103319](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/779b0277-094d-4e33-a9fe-6dfcf0eb1a1b)


<br>
<br>
DESIGN EXPLORATION<br>
<br>

![Screenshot 2024-03-15 104007](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/00a28ea3-c2b9-421d-8cfd-c5cb929a87c6)

<br>
OPEN LANE REGRESSION TESTING<br>
70 of them and this generates reports which shows design method and number of violations and then these results are comapred to best known results.
<br>

![Screenshot 2024-03-15 104036](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/e4a72912-d824-40a3-98c0-3b3e35b32eee)

<br>
DESIGN FOR TEST<BR>
<BR>

![Screenshot 2024-03-15 104226](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/bec22cd6-b244-41af-b6db-8766430c896a)

<BR>
<BR>

LOGIC EQUIVALENCE CHECK

<BR>

![Screenshot 2024-03-15 104708](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/3c12f4d8-5295-49ab-a416-a2a7c85ed038)
![Screenshot 2024-03-15 104726](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/c3f63861-6d27-4b62-9dd1-a17b97b24ae2)

<BR>

DURING the PHYSICAL implementation there is a special step which is <b> FAKE ANTENNA DIODE INSERTION SCRIPT</B>, which is required to adderss the antennas rules violation.
<br>
<br>

![Screenshot 2024-03-15 105137](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/d44ca223-5be1-4aa9-af5d-7403d2dc1a92)<br>
![Screenshot 2024-03-15 105251](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/79bad89a-5ba9-4e9d-a187-ffef999cb370)<br>
![Screenshot 2024-03-15 105639](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/2d9558a1-2124-40ea-8017-9b7f9908336f)<br>
![Screenshot 2024-03-15 105719](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/ecefb0b4-6c81-4c91-aa3d-912866327e7d)<br>
![Screenshot 2024-03-15 105726](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/975e0720-646f-44a7-b3cc-2d58d4816d6c)<br>


<br>

