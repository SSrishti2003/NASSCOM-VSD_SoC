# NASSDOM-VSD_SoC
ABOUT- This repository contains all the reports made for NASSCOM-VSD SoC Design Program including all 5 days.
<br><br>
<b><h1>TABLE OF CONTENTS</b></h1>
1)[DAY-1_NASSDOM _VSD-IAT](#DAY-1_NASSDOM _VSD-IAT)




## DAY-1_NASSDOM _VSD-IAT<a name="DAY-1_NASSDOM _VSD-IAT"></a>
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
<br>
<h1><b>SKY130_D1_SK3 - Get familiar to open-source EDA tools</b></h1>
<h2><b>SKY_LAB WORK</b></h2>
<br><br>
LETS FIRST TAKE A GLIMPS AT THE DIFFERENT DIRECTORIES.
<BR>
 
![Screenshot 2024-03-15 140411](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/19bb9dc1-1cb1-4e49-b63f-1810d8102cc3)

<BR>
Now open the openlane directory to work with the tool.<br>
The command used is <b> docker</b>.<br>
Then check the directories and use the command <b>open.tcl -interactive</b>, which is used for step by step process.
<br>

![Screenshot 2024-03-15 141829](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/1791fef6-4970-46f1-9895-553d4416004d)

<br>

Now as you can see the openlane has been incoked. The next command should be <b>package require openlane 0.9</b>,which imports all the packages which is required for the flow.
<br>
The next command is <b>prep -design picorv32a</b>. After that run the synthesis using <b>run_synthesis</b> command.
<br>
<br>

![Screenshot 2024-03-15 145728](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/db40f915-e3d2-4e11-8f1a-0f80f1d36fdb)

<br>
<br>
NOW lets find flop ratio which is <b> number of d flip flops/ total number of cells </b>= 1613/14876 =<b>0.1084</b><br>
<br>

![Screenshot 2024-03-15 145958](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/4664d053-7fdf-4ca3-b949-e55a8a14988b)
![Screenshot 2024-03-15 150010](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/bdc263ba-c3e1-49aa-8573-7e3431702386)

<br>
<br>




<h1><b>Sky130 Day 2 - Good floorplan vs bad floorplan and introduction to library cells</b></h1><br>
<h2><b> SKY130_D2_SK1 - Chip Floor planning considerations </b></h2>
<br>
<b> 1) </b>The first step of physical design overview flow is to define width and height. <br>
<br>

![Screenshot 2024-03-15 192255](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/97cccffa-d35a-4094-a5ae-0e17dacdd901)

<br>

To define the dimensions of the chip we need the dimensions of the logic gates. We have created an example netlist in this. Here we are not interested in the wires for now and just the dimensions of the standard cells.
<br>
![Screenshot 2024-03-15 192418](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/c2fb02e4-8b87-41c2-b4f7-9accd8d75442)
![Screenshot 2024-03-15 192734](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/de432f58-d671-48c1-8d39-60f6c29189ed)
![Screenshot 2024-03-15 194300](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/f756a056-d74f-4714-856e-b80d25ee493d)
![Screenshot 2024-03-15 194312](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/224c87b1-5a76-44e5-970b-d89d76124c12)

<br>
<br>
The netlist is placed perfectly inside the core which means that the core utilisation is 100%. utilisation= (area occupied by netlist)/ (total area of the core)<br>


<br>


![Screenshot 2024-03-15 232636](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/4b39de2a-e321-4b89-97fb-a95e389935e3)

<br>
If the aspect ratio is 1 it signifies the chip is square, otherwise it is rectangle. 
<BR><BR>
<B>2) DEFINE LOCATIONS OF PREPLACED CELLS</B>
<BR><BR>
For the combinational circuits, they can be divided into various blocks too. The advantage is if the respective circuit is replicated a lot of times in the circuit, then we can just clack box them.
<br>

![Screenshot 2024-03-16 194821](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/8110c6fe-1e01-4686-a475-67160e9e98a1)
![Screenshot 2024-03-16 195115](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/9424a02e-391a-456c-a037-f441208dd1a8)
![Screenshot 2024-03-16 195145](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/b5f7cf1d-9cd4-4657-9a90-009de99216ae)
![Screenshot 2024-03-16 195358](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/53df8b71-4b8e-46d0-96ae-f3f10b5c0659)

<br>
<br><br><br>
<b>3) SURROUND PREPLACED CELLS WITH DECOUPLING CAPACITORS</b><BR>
<br>

![Screenshot 2024-03-16 210829](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/ec815ab5-bd74-4746-b75b-eb4869047602)
![Screenshot 2024-03-16 211830](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/fbd41931-0909-4757-8df9-609b35b05ff4)

<br><br>
If we take any AND gate, and it switches from logic 0 to logic 1, there is an amount of current demand that it needs as there is a small capacitance sitting over there and whenever there is a switching from 0 to 1, the capacitance has to completely charge to logic 1 and that charge is sent from supply voltage.<br> When the supply voltage passes through the wire to the circuit, there is a drop in the wire.
<br>

![Screenshot 2024-03-16 211945](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/b79dd1a3-0e71-43f5-884e-1cfffc839fc9)

<br>
<br> Also, the vdd' should be within the noise margin range. If it doesnt then the logic 1 is unstable which is why there shouldnt be much gap between power supply and main circuit.<br>
<br>

![Screenshot 2024-03-16 212512](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/8bf2dc28-3915-4365-8234-0e1c2eae4b8d)

<br><br>
We can solve the above problem with the help of decoupling capacitor. The voltage across it is similar to power supply so whenever the circuit switches, it gets its voltage from capacitor.<br><br>
<br>

![Screenshot 2024-03-16 213024](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/a588530b-4bd2-4143-9880-5a112ca16eca)

<br><br>
Now lets consider the circuit as a <B>MACRO</B>  and it demands a current.
<br><br>
<b>4) POWER PLANNING </b>
<br><br>

![Screenshot 2024-03-16 215157](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/8ff971df-22e2-46c2-9375-aa614cdfccd0)
![Screenshot 2024-03-16 215229](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/1157ff72-40fb-4a35-82f2-748f04d4e9a1)
![Screenshot 2024-03-16 220716](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/01dab516-080b-4cd2-821b-beb539dfb0f6)
![Screenshot 2024-03-16 220831](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/e9b19374-a72d-4263-a5cb-dea074728ba9)

<br>
<br>
<br>
A ground bounce is when all the capacitors are discharging at the same time there will be a bump in ground line and if the size of the bump exceeds noise margin level, it might enter an undefined region and might go to either logic 1 or 0.<br><br>
Same happens with voltage supply. This can be avoided if each has their own power supply nearby.<br>
<br>

![Screenshot 2024-03-16 221504](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/b4007b34-4e74-43f0-af2f-e9d00aeb3276)
![Screenshot 2024-03-16 221651](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/f4df3ff7-c29e-46f8-80db-5da78b67a471)
![Screenshot 2024-03-16 221722](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/2f457246-7d5a-4d72-89c2-03b1a9ede80a)

<br>
<br>
  <b>5) PIN PLACEMENT </b><BR><BR>
  
![Screenshot 2024-03-16 222453](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/395ef5ac-3924-4a4e-8838-14528e06b911)
![Screenshot 2024-03-16 222612](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/e0b5afef-ce4f-412b-ab43-4245221c9823)

<br>
<H3><B>LAB WORK</B></H3>
