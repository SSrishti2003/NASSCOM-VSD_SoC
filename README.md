# NASSDOM-VSD_SoC
ABOUT- This repository contains all the reports made for NASSCOM-VSD SoC Design Program including all 5 days.
<br><br>
# Table of Contents

- [DAY_1](#DAY_1)
- [DAY_2](#DAY_2)
- [DAY_3](#DAY_3)
- [DAY_4](#DAY_4)
- [DAY_5](#DAY_5)



## DAY_1<a name="DAY_1"></a>
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



## DAY_2<a name="DAY_2"></a>
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
BEFORE RUNNING FLOORPLAN, WE WILL DO CERTAIN THINGS.
<br>

![Screenshot 2024-03-16 232955](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/979d0e97-d34e-4a13-b378-a888aef1b7fb)

<br>
<br>WE will go to floorplan.tcl  and check the different parameters
<br>

![Screenshot 2024-03-16 233023](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/4c86bc8b-d769-4092-b152-eb81691bdf00)
![Screenshot 2024-03-16 233041](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/13a78499-1bfb-4b0c-8645-7c1cfdeaf13c)

<br>
<br>

Now let's go to config.tcl in picorv32a which has higher design priority than the previous one.  There were parameters missing in this so we used “gedit” command and edited it.
<br>

![Screenshot 2024-03-16 233058](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/d7b1703b-9361-4ab6-9475-6bd2f56632dd)
![Screenshot 2024-03-16 233107](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/2586a699-4d73-40ab-91fc-35a07ecccf04)
![Screenshot 2024-03-18 170635](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/b5cd6e53-6fa3-4727-ba17-e4cc6ec965fa)


<br>
<br>
1 micron= 1000 data base units<br>
<br>

![Screenshot 2024-03-18 172114](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/2633f324-3e82-443a-af34-cc9f9234eef7)

<br>
<br> <b>ON MAGIC: </b> commands to be given:<br>
run_floorplan
magic -T /home/vsduser/Desktop/work/tools/openlane_working_dir/pdks/sky130A/libs.tech/magic/sky130A.tech lef read ../../tmp/merged.lef def read picorv32a.floorplan.def &
<BR>
<BR>

![Screenshot 2024-03-18 181402](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/d2a9f665-4a31-4479-aa6b-35bb63cad980)
![Screenshot 2024-03-18 181413](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/ac4bdc1a-06f4-43e6-921e-1d880f8030dd)
![Screenshot 2024-03-18 181427](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/636759ac-addb-4472-90d8-8f7f950a2d87)
![Screenshot 2024-03-18 183425](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/b7d5a711-dc1e-4162-8c84-d609d471a4ce)

<br>
<br>
<H2><B> SKY130_D2_SK2 - Library Binding and Placement </B></H2>
<BR>1)<B>PLACEMENT AND NETLIST</B>
<BR>

![Screenshot 2024-03-18 183717](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/30306153-0689-4d31-ad5d-78a951a9235c)
![Screenshot 2024-03-18 183857](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/20805e93-86d1-45ef-8ad4-c29a6b6ba77e)

<BR>
<BR>
LIBRARY: It contains cells which can have different dimensions, various shapes of the cells, and timing info. Bigger cells have lesser resistance while the functionality is the same.
<br>

![Screenshot 2024-03-18 184531](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/89c9926c-4413-4e73-ae39-6821a35358e1)

<br><br><B>PLACEMENT OPTIMISTATION</B>
The next step is to take those shapes and place it onto the floorplan.
<br><BR>

![Screenshot 2024-03-18 184815](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/1cd33063-4f45-4548-bb50-2f8b880dbc81)
![Screenshot 2024-03-18 185146](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/31fb6b0e-516d-42d1-bd5f-d23914ee01f4)
![Screenshot 2024-03-18 185359](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/c2d33171-10d7-4e71-92d1-146f922b925d)
![Screenshot 2024-03-18 185852](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/17239f02-a56e-440f-b111-ff44d71335d7)
![Screenshot 2024-03-18 185948](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/c452590c-8da8-4753-803f-e6f49030e83a)

<br>

We use buffers or repeaters to retain signal intergrity. They reproduce the same signal they receive and send it again.
<br>
<B>LOGIC SYNTHESIS: </B> The first step to convert functionality into legal hardware is this. Th output of logic synthesis is the arrangement of gates that will represent original functionality.

<br>

![Screenshot 2024-03-18 191704](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/2e8a1aa7-574a-49fb-a37f-cce623226f20)
![Screenshot 2024-03-18 191941](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/fd36f9e3-d60f-44eb-aac5-9dba2f204c79)
![Screenshot 2024-03-18 192013](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/76a27762-a7b5-4438-9a6e-0b06966f676c)
![Screenshot 2024-03-18 192037](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/b8be417b-d9d1-4d00-9962-fa108c99aad5)
![Screenshot 2024-03-18 192056](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/2100adeb-7e8e-4182-8eaf-5dfb323b9aac)


<BR>
<BR>
<b>LAB</b>
1) <B>run_placement</B><br>
<br>

![Screenshot 2024-03-18 193102](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/44403cb1-e97a-4394-9aed-e7973b756f1b)
![Screenshot 2024-03-18 195524](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/1cbdc97e-b04d-4ea6-8355-1a2aa985d154)
![Screenshot 2024-03-18 200142](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/71a76a1e-00f6-4793-8495-612eb0291a6a)
![Screenshot 2024-03-18 200216](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/9b2815ac-f6b8-4911-927e-4a98aca70039)
![Screenshot 2024-03-18 200345](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/07809701-2c29-4183-ae9e-f2d124026bb6)

<br>

<b><h2>SKY130_D2_SK3 - Cell design and characterization flows</b></h2>
<br><b><h4>CELL DESIGN FLOW</b></h4>
<br>

![Screenshot 2024-03-18 205032](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/92545c6d-52c3-4cd7-be78-e549bbc6c538)
![Screenshot 2024-03-18 205551](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/61da931b-8e75-4070-bd48-be99f9448f50)
![Screenshot 2024-03-18 205807](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/6b9d01bf-d0ae-47bd-a5fe-d30c35224dd8)
![Screenshot 2024-03-18 205931](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/24df45b9-2a77-4f15-8d7c-ac43f3d56391)

<br>

![Screenshot 2024-03-18 212940](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/31df59d8-802b-4d79-bc5a-b1d921bbd22c)
![Screenshot 2024-03-18 214026](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/73d72adf-a873-4e17-9348-f937a82b54ac)
![Screenshot 2024-03-18 214232](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/0dc9da98-f994-45ef-a226-5963e2d80c19)
![Screenshot 2024-03-18 214306](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/0716db70-67d4-4799-b9ee-beaae89680c4)

<br>
<b><h2>SKY130_D2_SK4 - General timing characterization parameters</h2></b><br>
<br>

![Screenshot 2024-03-19 100908](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/38b6a831-cb91-446c-842e-a0b9fa6817bc)
![Screenshot 2024-03-19 101136](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/86d5739f-6f79-4408-8023-0910c6bd99e7)
![Screenshot 2024-03-19 101151](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/bf9acd60-91bc-44cc-b75a-c29a4777f72c)
![Screenshot 2024-03-19 101300](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/2e098220-d460-4b52-b089-2d823759d32a)
![Screenshot 2024-03-19 101309](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/0997bcc0-81e6-4bdd-b92c-69a64b9ea33d)
![Screenshot 2024-03-19 101959](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/816bc001-9f73-4389-ae9f-7805b7a18bd2)
![Screenshot 2024-03-19 102009](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/d6b459ed-5300-44fa-99fa-4c89babf46b1)
![Screenshot 2024-03-19 102017](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/f5a79eda-9cda-4b7f-8b1c-f0c7b20f0958)
![Screenshot 2024-03-19 102023](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/a3ba2696-69d7-4677-aa8e-93b295e6ab2c)

<br>
<b>PROPOGATION DELAY AND TRANSISTION TIME</b>
<BR>

![Screenshot 2024-03-19 102243](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/0bec77f3-b50d-4434-b310-607f4ecac268)
![Screenshot 2024-03-19 102431](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/15c548c8-2344-4516-9fd7-b6a75ca94b93)
![Screenshot 2024-03-19 102459](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/406d6bf6-b5ac-4e70-b7fd-07cde408812e)
![Screenshot 2024-03-19 102616](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/41eb026a-be3c-42b3-81ce-7c602806ba9e)
![Screenshot 2024-03-19 102652](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/ed6e4b5d-07d0-4965-aecc-1bc6890e249f)
![Screenshot 2024-03-19 102713](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/fe0b704e-98e6-4144-b771-77e0902371e7)
![Screenshot 2024-03-19 102719](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/b4b8849f-39e9-4adb-a59d-2b224b9bb4c2)
![Screenshot 2024-03-19 102820](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/39571e1a-2731-43d1-b0d4-47f3e6c37c81)

<BR>

## DAY_3<a name="DAY_3"></a>
<b><h1>Sky130 Day 3 - Design library cell using Magic Layout and ngspice characterization<b>/</h1>
<B><H2>SKY130_D3_SK1 - Labs for CMOS inverter ngspice simulations</B></H2>
<BR>
<B>Changing FP_IO MODE</B>
<BR>
<BR>

![Screenshot 2024-03-19 201332](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/dcc42c0d-d9ff-4d98-bad9-4d1bb23ffd8d)
![Screenshot 2024-03-19 201706](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/7af9fa09-7f02-4545-854a-bfe4999e8695)
![Screenshot 2024-03-19 201721](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/ffac32f5-da51-4e7f-94f3-37ee333d16d6)

<BR><BR>
<b>CLONE GIT FILE</b>
<BR><BR>

![Screenshot 2024-03-19 205231](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/61313bc7-a449-4651-90ab-62ea853474d7)
![Screenshot 2024-03-19 212001](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/c9a3b38c-a12d-4959-b2e0-9db9b8a79c20)
![Screenshot 2024-03-19 212359](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/bce504bf-f04a-4bca-89bb-d220054e38f3)
![Screenshot 2024-03-19 212418](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/8459cde3-a615-4c1c-a57f-a56351ca860b)

<BR><BR>
<B><H2> SKY130_D3_SK2 - Inception of Layout  CMOS fabrication process </B></H2>
<BR><BR>

![Screenshot 2024-03-20 210621](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/01a160e9-a3ad-4626-be7f-35f7c0eaf8dd)
![Screenshot 2024-03-21 222331](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/de62f391-be7c-489a-a681-7f71f9ec4a86)

![Screenshot 2024-03-20 205918](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/a37ec0a6-59bc-4a6a-8118-65582c8c3e7c)
![Screenshot 2024-03-20 210134](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/6d2e766b-55c4-49ef-93e2-34c9318ff9ca)
![Screenshot 2024-03-20 210329](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/eba13323-ba70-47cd-a73b-d79f642a423d)
![Screenshot 2024-03-20 210412](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/195c379b-aeca-499d-8f00-ae9008f86e71)
![Screenshot 2024-03-20 210506](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/86afa494-b423-4201-9c3e-480a8a0a2987)
![Screenshot 2024-03-20 210520](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/d26d9849-4987-4fbb-ba02-e44013042975)
![Screenshot 2024-03-20 212532](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/ae933ae6-e730-42c9-9125-d23de39e1dbc)

<BR>
<BR><BR>
<B><H2> SKY130_D3_SK3 - Sky130 Tech File Labs </B></H2>
<BR><BR>

![Screenshot 2024-03-20 211357](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/ec826bd7-fe71-4723-b99b-bff9b3e856a7)
![Screenshot 2024-03-20 211718](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/fb6ea6ef-3b23-4cd6-8752-a76385978bed)
![Screenshot 2024-03-20 212110](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/99094ab3-ecb1-4da9-91df-4c214f77b879)
![Screenshot 2024-03-20 212116](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/af59e4c2-2361-4ad3-981c-ad066e4c4cbd)
![Screenshot 2024-03-20 212352](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/701e395c-4785-44a9-843e-5597287bf00a)
![Screenshot 2024-03-20 212400](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/ca05d97e-936a-439a-9f36-4a333c3c09e0)
![Screenshot 2024-03-20 220121](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/12426b69-a53b-443a-b644-bf6a8ea1c399)
![Screenshot 2024-03-20 220121](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/df82ea2a-0785-41f2-bbe3-c10277aa2864)
![Screenshot 2024-03-20 221841](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/ca11049f-7a3d-4486-a161-1d282c575170)
![Screenshot 2024-03-20 223422](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/641f3071-32aa-4aba-87a4-afe1072dcea9)
![Screenshot 2024-03-20 224110](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/cd1d213a-1d83-4eb3-889e-c428d632967d)
![Screenshot 2024-03-20 224121](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/c00f4601-9ffb-4336-99cc-3e2e5321538f)

<br><br>
TO reduce spikes, new change in sky130_inv.spice file.<br>
<br>

![Screenshot 2024-03-20 224602](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/a3b9dc39-6125-453e-a5ac-4173ae552c59)
![Screenshot 2024-03-20 224633](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/6721e759-457a-4a7e-952f-948a522f3902)

<br>
<br>
RISE TIME CALCULATION<BR>

![Screenshot 2024-03-20 224902](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/8e88b7b5-a1c3-4ebf-be1e-a7ddcb9e685c)

<BR>20% VALUE<BR>

![Screenshot 2024-03-20 224910](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/075eadee-a0fb-432d-99e8-1bd5276b7d6a)

<BR>80% VALUE IS GIVEN<BR>

![Screenshot 2024-03-20 225043](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/44c3b4db-c20f-48c6-91bf-2747c7b3a639)
![Screenshot 2024-03-21 181956](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/8a55f1f6-9092-4f10-a576-5b80b61ce6db)

<BR> 80% X VALUE - 20% X VALUE= RISE TIME
2.24-2.18 = 0.06 ns
<br>
<br>
RISE DELAY
<BR>

![Screenshot 2024-03-21 182444](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/bf8a480f-114c-424f-888b-f5556ba28481)

<BR>
MAGIC WORKING 
<BR><BR>

![Screenshot 2024-03-21 195956](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/a975c235-30fc-4083-a9b6-6784aac15ee9)
![Screenshot 2024-03-21 200013](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/45e2cf45-b03c-49ab-afbc-0c9b0823a730)
![Screenshot 2024-03-21 200151](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/ae73342a-9711-4a26-97e3-71bb84cd617b)
![Screenshot 2024-03-21 200358](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/275ee93f-b569-4404-adac-d7ce29fa465c)
![Screenshot 2024-03-21 200430](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/13e11289-bd5b-4368-a92c-76a64bac70f8)
![Screenshot 2024-03-21 200532](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/227d449a-3933-447e-a5c9-aaca1cf612a2)
![Screenshot 2024-03-21 200541](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/5f823b24-f9f8-4e47-95e8-86f8d174fd58)
![Screenshot 2024-03-21 201130](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/3dd12227-ed94-4d62-91fb-dc794e738fe4)
![Screenshot 2024-03-21 201409](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/4a1fc63a-af0b-4134-a4a9-7564f0d34fa7)
![Screenshot 2024-03-21 202136](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/7cf961a9-ca09-42bb-95cd-da7449e7626d)
![Screenshot 2024-03-21 202611](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/2025a7bb-d886-49a1-a73d-2c18323f44b2)
![Screenshot 2024-03-21 204227](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/45056a54-8fdd-4131-ad34-9f65528e95ce)
![Screenshot 2024-03-21 204530](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/c6c9fd5e-6a82-4a5b-9cbe-d3d8a6302b6f)
![Screenshot 2024-03-21 204625](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/288096f5-1da6-49b0-9403-40e79cfdb872)
![Screenshot 2024-03-21 204902](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/14133a9b-d1ad-4204-a192-68d6f7bbfdd3)
![Screenshot 2024-03-21 205251](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/db8ed1f6-5b6f-4b41-aa89-1634e6d4205d)
![Screenshot 2024-03-21 205429](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/726bc0e3-5e89-4484-ab9f-866aa4b57d04)
![Screenshot 2024-03-21 205703](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/b34c880d-e580-470f-8b9e-7e9b674aa017)

<BR><BR>
## DAY_4<a name="DAY_4"></a>
<b><h1>Sky130 Day 4 - Pre-layout timing analysis and importance of good clock tree</b></h1>
<b><h2>SKY130_D4_SK1 - Timing modelling using delay tables</b></h2>
Now we will check the grids and track info according to thr labs.
<br>

![Screenshot 2024-03-22 154519](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/0213ae3a-34ad-492b-9837-e84b1cd8d461)
![Screenshot 2024-03-22 155337](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/e63f2ed4-68d6-4d5d-996b-3442bf7795ca)
![Screenshot 2024-03-22 155400](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/317f5dd6-1e64-43e9-9c5b-9996dbcee1fa)
![Screenshot 2024-03-22 155819](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/6c1e8b7e-8e2e-4bf9-9f77-54440fe27c18)
![Screenshot 2024-03-22 155851](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/5592ab74-ee68-42ae-83c2-925739332e25)
![Screenshot 2024-03-22 160010](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/9a5fa419-9d60-4490-bf36-f0351e24b46e)

<br><br><b> The width of the standard cell should be in the odd multiples of x direction pitch</b>
<br>

![Screenshot 2024-03-22 160934](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/a2cff06e-646a-4611-8d8c-56c3353024c2)
![Screenshot 2024-03-22 161145](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/0939f952-f96d-4119-9461-c28c82e32234)
![Screenshot 2024-03-22 161337](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/b66d3172-439f-4607-bbc4-2f32c2da4ad2)
![Screenshot 2024-03-22 161653](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/39df8906-9d9f-4327-964d-8630d99a27ea)

<Br>
<br>CREATING A LEF FILE IN MAGIC <BR>
<BR>

![Screenshot 2024-03-22 162329](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/0fdb4395-0fd1-4af0-a5a2-b13c47b7fae3)
![Screenshot 2024-03-22 162538](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/619d934d-f2d7-4a96-bc05-80e0db761a1b)
![Screenshot 2024-03-22 162646](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/617203b2-8364-4830-954b-e43d320c0fcd)
![Screenshot 2024-03-22 162735](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/1e6bc4a9-143e-41f2-911e-66e8d49a7e84)
![Screenshot 2024-03-22 162854](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/bc645ecb-8f5b-405b-afbe-76f5b72104d8)

<br>

![Screenshot 2024-03-22 164029](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/68006473-85c6-4de3-b4b6-aea8d615f079)
![Screenshot 2024-03-22 164038](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/b0e94bd9-6a55-4fd7-bb62-b678e67aad56)
![Screenshot 2024-03-22 164419](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/3822077e-f95a-4832-ae7f-b668c460e8c4)
![Screenshot 2024-03-22 165550](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/62448944-f790-4adb-9c1b-ce2b19f74878)
![Screenshot 2024-03-22 170044](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/8e8f76e0-e910-4c28-b5fc-c44d32e01b1a)
![Screenshot 2024-03-22 170427](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/ff2ec570-f14b-4041-9a7d-23e5d5eb4421)
![Screenshot 2024-03-22 172415](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/e240f293-05b8-4c7e-a711-b7bbe7ff9b39)
![Screenshot 2024-03-22 173151](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/0eb262ca-7c44-46f2-81cc-35ae2a9ec5cf)
![Screenshot 2024-03-22 173951](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/62c01f2e-c7df-4ef1-afcb-2e03fedaedf6)
![Screenshot 2024-03-22 174001](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/a821b529-6838-40ed-8c10-6d5dcdeb8fde)
![Screenshot 2024-03-22 183313](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/02bb608b-1c2c-4218-a11e-196cb33e338c)
![Screenshot 2024-03-22 183323](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/07f7cbee-e389-463e-99a3-208083b2998c)
![Screenshot 2024-03-22 183350](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/ddd2318a-a360-4820-b365-bbb91fb9f1fc)
![Screenshot 2024-03-22 183419](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/f065995d-7e9e-41da-916c-8dd1aae33335)
![Screenshot 2024-03-22 212249](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/5accf1c6-3855-4b68-8c6e-3678044904df)
![Screenshot 2024-03-22 212301](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/4bbca6fc-0b5b-4fcb-8c28-97d686bbd7c6)
![Screenshot 2024-03-22 212313](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/0dc314af-9678-4acd-a38f-490dc69286cc)
![Screenshot 2024-03-22 212328](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/9c64bf4e-76c1-48c0-9a1e-b58c2057390e)
![Screenshot 2024-03-22 215330](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/a1c0f95f-8189-4103-9244-b5dcf6bf25bd)
![Screenshot 2024-03-22 220440](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/acc8b92e-a4ce-4fe8-bac1-56cf81217a1d)
![Screenshot 2024-03-22 220620](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/5cc244f1-6404-4885-a883-5402d9b5620e)
![Screenshot 2024-03-22 220638](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/e688a461-aad3-491f-ad5e-f267f59e2953)
![Screenshot 2024-03-22 221042](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/502fcae6-3e04-4048-af35-de40bd475997)


<br>
<b><h2>SKY130_D4_SK2 - Timing analysis with ideal clocks using openSTA</h2></b>
<BR>

![Screenshot 2024-03-22 223654](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/bb1c1eff-d141-4ae3-b607-b37b72cd51f1)
![Screenshot 2024-03-22 223814](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/bd324763-8190-4e6b-acae-49d7b0efb7c7)
![Screenshot 2024-03-22 223922](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/494e4d16-8323-4489-924b-6cc0aefc2946)
![Screenshot 2024-03-22 223931](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/46789032-2478-43db-acb1-75cde58756e4)
![Screenshot 2024-03-22 225047](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/46c7732d-58ed-4ac0-8b41-832f0e741e9f)
![Screenshot 2024-03-22 225059](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/52fb217e-9cd1-4a4a-8efc-ae077d0d99c5)
![Screenshot 2024-03-22 230406](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/86de7491-5e47-4e5a-adf4-0b4aebe73245)
![Screenshot 2024-03-22 230453](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/03c0998b-b752-412d-b8b8-323fc908356c)
![Screenshot 2024-03-22 230506](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/9821a7c6-6a75-433f-9fec-d11d3d64b1d9)
![Screenshot 2024-03-22 230527](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/eb46e61f-b588-440b-92cd-185b64ff445b)

<BR>
<br><b><h2>SKY130_D4_SK3 - Clock tree synthesis TritonCTS and signal integrity</h2></b><br>
<Br>

![Screenshot 2024-03-23 142558](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/acdc24de-c6e9-4c47-9744-e242a5893a52)
![Screenshot 2024-03-23 143857](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/6bd1ca0f-9f56-4d2e-8e26-95c4433153cf)
![Screenshot 2024-03-23 144109](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/b9dc38b5-4867-43ab-a9b8-7af20d50afed)
![Screenshot 2024-03-23 145426](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/073d8bdd-e047-4c44-b52b-03e7bcbe5888)
![Screenshot 2024-03-23 151630](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/f9bd8eda-e2ad-4e3a-8351-874441a1bebd)
![Screenshot 2024-03-23 151651](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/3e817327-5ce8-44cf-aee9-8f1c594a0513)
![Screenshot 2024-03-23 152858](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/d00ae01e-d4c6-49cb-b80f-6ffd67e212f7)
![Screenshot 2024-03-23 153403](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/b0221b49-077a-42a4-907c-94656c6bc637)
![Screenshot 2024-03-23 153419](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/c28b367c-10a6-41a0-bea3-5eda56d02cc9)
![Screenshot 2024-03-23 153453](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/16fcefb5-cdd6-47d9-86c1-5cbde7e6701e)
![Screenshot 2024-03-23 154010](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/5bde9554-fd66-41de-ac7c-afabf081a5dc)
![Screenshot 2024-03-23 154147](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/031dffc1-6f5d-4ba2-a6dc-15dcc4f0670a)
![Screenshot 2024-03-23 154159](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/75843833-5161-41b8-86d2-50e52678114e)
![Screenshot 2024-03-23 154644](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/6befb3f8-14c0-4f90-8718-f0303b93ca11)

<Br>
<Br><b><h2>SKY130_D4_SK4 - Timing analysis with real clocks using openSTA</h2></b><br>
<br>

![Screenshot 2024-03-23 161352](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/e13e9623-7fb9-4acc-b5c3-f64ab9de7a6c)
![Screenshot 2024-03-23 161633](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/b43c082b-1d0f-4bd7-8d81-f96f247a8087)
![Screenshot 2024-03-23 161812](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/232a478e-14fb-4364-a3b6-adca758dc516)
![Screenshot 2024-03-23 161936](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/d0eeacd3-12fd-4f12-ae55-bee60fdf9342)
![Screenshot 2024-03-23 161954](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/3ac25ee8-d606-44f6-96af-0f2cdf5e02f9)
![Screenshot 2024-03-23 162317](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/dafbae11-e6c1-4f18-8ba3-e954b53cd64e)
![Screenshot 2024-03-23 162344](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/73662295-e3aa-48a0-8216-7a8f56db82d4)
![Screenshot 2024-03-23 162714](https://github.com/SSrishti2003/NASSDOM-VSD_SoC/assets/121450826/fe0b9e84-7964-437b-aba4-d836e9d00a27)

<br>

## DAY_5<a name="DAY_5"></a>
