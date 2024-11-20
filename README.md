# Logic Gates using LTspice

This repository explains the implementation of Logic Gates in CMOS Logic using LTspice Simulator. This shows the schematics of Logic Gates and plot the output waveform to verify the functionality.

# Table of Contents
- # Table of Contents
- [Introduction](#Introduction)
- [Objectives](#Objectives)
- [Project Structure](#Project-Structure)
- [Circuit Details](#Circuit-Details)
- [LTspice Simulation](#LTspice-Simulation)
     - [Terms Description](#Terms-Description)
     - [Schematics](#Schematics)
       - [Steps to draw schematics](#Steps-to-draw-schematics)
       - [Schematic of AND Gate](#Schematic-of-AND-Gate)
       - [Schematic of OR Gate](#Schematic-of-OR-Gate)
       - [Schematic of NOT Gate](#Schematic-of-NOT-Gate)
       - [Schematic of NAND Gate](#Schematic-of-NAND-Gate)
       - [Schematic of NOR Gate](#Schematic-of-NOR-Gate)
- [Simulation Results](#Simulation-Results)
     - [How to simulate](#How-to-simulate)
     - [Results](#Results)

# Introduction
**Logic Gate:** A logic gate is a device that performs logical operations on one or more binary inputs and produces a single binary output. The primary way of building logic gates uses diodes or transistors acting as electronic switches. Today, most logic gates are made from MOSFETs (metal–oxide–semiconductor field-effect transistors). Logic circuits include such devices as multiplexers, registers, arithmetic logic units (ALUs), computer memory and microprocessors which may contain more than 100 million logic gates.

**Logic Gates** - Basic Gates and Universal Gates

**Basic Gates:** Basic gates, also known as elementary or fundamental gates, include the AND, OR and NOT gates. These gates operates on binary signals (0s and 1s) and provide the basis for all digit computations. Other gates such as XOR, XNOR, NAND and NOR can be derived from basic gates.

**Universal Gates:** A universal gate is a digital logic gate that can be used to implement any Boolean function without requiring other gates. NAND and NOR Gates are universal gates.

**CMOS:** Complementary metal–oxide–semiconductor (CMOS) is a type of MOSFET that uses complementary and symmetrical pairs of p-type and n-type MOSFETs for logic functions. Input is applied at the common gate of PMOS and NMOS transistors.Output is taken from the PMOS and NMOS drain. CMOS technology is used for constructing integrated circuit (IC) chips, including microprocessors, microcontrollers, memory chips and other digital logic circuits. Two important characteristics of CMOS devices are high noise immunity and low static power consumption.

**PMOS:** The PMOS transistor is a p-channel device. It conducts current when a negative voltage (logic low) is applied to its gate terminal with respect to the source terminal. In CMOS, PMOS acts as pull up network in which the source is connected to VDD. When logic low(0) is applied is CMOS, the PMOS transistor turns on and connects the VDD to output which makes the output to logic high(1).

**NMOS:** The NMOS transistor is an n-channel device. It conducts current when a positive voltage (logic high) is applied to its gate terminal with respect to the source terminal. In CMOS, MMOS acts as pull down network in which the source is connected to ground. When logic high(1) is applied is CMOS, the NMOS transistor turns on and connects the output to ground which makes the output to logic low(0).

# Objectives
The main goal of this project are given below
1. To plot the schematics of logic gates, and circuits 
2. To plot the output waveform 
3. To verify the functionality

# Project Structure
- **Tool :** LTspice
- **Technology :** C5N technology

**LTspice Simulation Files**: Files with .asc extension represents LTspice simulation files for each logic gate.

- **AND.asc :** LTspice simulation file for the AND gate.
- **OR.asc :** LTspice simulation file for the OR gate.
- **NOT.asc :** LTspice simulation file for the NOT gate.
- **NAND.asc :** LTspice simulation file for the NAND gate.
- **NOR.asc :** LTspice simulation file for the NOR gate.

# Circuit Details

1. The output of AND gate produces 1 if and only if all the input states are 1 else it produces 0. The logic symbol and truth table of 2-input AND gate is shown below.

![image](https://github.com/Jyothi181/Pictures/blob/main/Picture1.png)      ![image](https://github.com/Jyothi181/Pictures/blob/main/Picture2.png)
                                                                                                                                                                                                           
**Figure 1: Logic Symbol, Truth table and Logic Circuit of AND gate**

2. The output of OR gate produces 1 if one or more input states are 1 else it produces 0. The logic symbol and truth table of 2-input OR gate is shown below.

![image](https://github.com/Jyothi181/Pictures/blob/main/Picture3.png)  ![image](https://github.com/Jyothi181/Pictures/blob/main/Picture4.png)

**Figure 2: Logic Symbol, Truth table and Logic Circuit of OR gate**

3. The NOT gate is a digital logic device whose output is always the complement of its input. The NOT gate can be implemented in CMOS logic by connecting PMOS to VDD which acts as Pull Up Network (PUN) and NMOS is connected to ground which acts as Pull Down Network (PDN). The logic symbol, truth table and CMOS implementation of NOT gate is shown below.

![image](https://github.com/Jyothi181/Pictures/blob/main/Picture5.png)    ![image](https://github.com/Jyothi181/Pictures/blob/main/Picture6.png)

**Figure 3: Logic Symbol, Truth table and Logic Circuit of NOT gate**

4. The output of NAND gate produces 1 if any one of the input state is 0 else it produces 0. The logic symbol and truth table of 2-input NAND gate is shown below. 


![image](https://github.com/Jyothi181/Pictures/blob/main/Picture7.png)   ![image](https://github.com/Jyothi181/Pictures/blob/main/Picture8.png)

***Figure 4: Logic Symbol, Truth table and Logic Circuit of NAND gate***

5. The output of NOR gate produces 1 if and only if all the input states are 0 else it produces 0. The logic symbol and truth table of 2-input NOR gate is shown below. 

![image](https://github.com/Jyothi181/Pictures/blob/main/Picture9.png)  ![image](https://github.com/Jyothi181/Pictures/blob/main/Picture10.png)

***Figure 5: Logic Symbol, Truth table and Logic Circuit of NOR gate***

# LTspice Simulation

LTspice captures schematics of different circuits and shows the results of simulation by using waveform viewer. Circuit simulation analysis provides the transient, AC and DC analysis.  

- Tool = LT spice Simulator
- Technology = C5N technology file
- Logic Gates = AND, OR, NOT, NAND and NOR
- VA = `PULSE(0 5 0 1n 1n 5u 10u)`
- VB = `PULSE(0 5 0 1n 1n 10u 20u)`
- V1 = 5v
- Spice Directive = `.include D:\NIELIT\ENGR3426\ENGR3426\engr3426.sub`
- Transient = `.tran 100u`
- PMOS -> Length = 0.6u, Width = 7.2u
- NMOS -> Length = 0.6u, Width = 3.6u
- PMOS = Pull Up Network (PUN)
- NMOS = Pull Down Network (PDN)


## Terms Description

- **Inputs:** The inputs are VA and VB. VA is applied to one of the PMOS and one of the NMOS. Likewise, VB is applied to one of the PMOS and one of the NMOS.
- **Output:** The output Vout is based on the functionality of logic gates.

- **PULSE(0 5 1n 1n 5u 10u)** is a syntax used to define a pulse waveform for a voltage source VA
- **PULSE(0 5 1n 1n 10u 20u)** is a syntax used to define a pulse waveform for a voltage source VB

- **Initial Value (Vintial):** 0[V] This is the voltage level of the source before the pulse begins.

- **Pulse Value (Von):** 5[V] This is the voltage level during the ON period of the pulse.

- **Delay Time (Tdelay):** 0[s] This is the delay time from input voltage to output voltage. In this case, there is no delay.

- **Rise Time (Trise):** 1n[s] This is the time taken for the pulse to change from the Initial Value to the Pulse Value.

- **Fall Time (Tfall):** 1n[s] This is the time taken for the pulse to change from the Pulse Value back to the Initial Value.

- **On Time (Ton):** 5u for VA and 10u for VB This is the time for which the pulse on for some period of time

- **Time period (Tperiod):** 10us for VA and 20us for VB This is the total time for one complete cycle of the pulse waveform.

- **Number of Cycles (Ncycles):** 10 This specifies how many cycles of the pulse waveform should be generated.

- **Spice Directive:** This contains text directly passes to the netlist which is placed on the schematic. The text may be single line or block or lines.
- **Transient Analysis:** This analyzes the changes in voltage and current over time when an input signal is applied. To apply tansient analysis `.tran` is used as a keyword. 

So, with the given inputs, the voltage source will start at 0V, then immediately rise to 5V. It will remain at 5V upto 5us for VA and 10us for VB, then drop back down to 0V. The total period for one complete cycle of this waveform is 10us for VA and 20us for VB. This cycle will repeat 10 times.

## Schematics

### Steps to draw schematics

1. To create a new schematic -> `File - New Schematic (Ctrl+N)`
2. Place the transistors using the option `Component (P)` in the toolbar.
3. Place the voltage sources and ground from the toolbar and set the values as mentioned above.
4. Label all the components by using left click on each component.
5. Make connections by using the option `Wire (W)` in the toolbar.
6. Include the technology library using spice directive.
7. Give the length and width of NMOS and PMOS transistors by selecting the respective transistors.


![image](https://github.com/Jyothi181/Pictures/blob/main/Picture11.png) ![image](https://github.com/Jyothi181/Pictures/blob/main/Picture12.png)


***Figure 6: Length and Width of transistors***

8. To verify the transient analysis -> Click on Voltage sources and give the specific values as mentioned above in the Terms Description.


![image](https://github.com/Jyothi181/Pictures/blob/main/Picture13.png)

***Figure 7: Transient Analysis values***


### Schematic of AND Gate

- M1,M2 and M6 are PMOS transistors
- M3,M4 and M5 are NMOS transistors
- VA and VB are input voltages
- V1 is voltage source
- Vout is output voltage
- PUN : Two C5NPMOS are connected in parallel
- PDN : Two C5NNMOS are connected in series
- The AND gate can be obtained by connecting output of NAND gate to an inverter.

![image](https://github.com/Jyothi181/Pictures/blob/main/Picture14.png)

***Figure 8: LTspice Schematic of AND Gate***

### Schematic of OR Gate
- M1,M2 and M6 are PMOS transistors
- M3,M4 and M5 are NMOS transistors
- VA and VB are input voltages
- V3 is voltage source
- Vout is output voltage
- PUN : Two C5NPMOS are connected in series
- PDN : Two C5NNMOS are connected in parallel
- The OR gate can be obtained by connecting the output of NOR gate to an inverter.

![image](https://github.com/Jyothi181/Pictures/blob/main/Picture15.png)

***Figure 9: LTspice Schematic of OR Gate***

### Schematic of NOT Gate

- M1 is PMOS transistor
- M2 is NMOS transistor
- Vin is input voltage
- VDD is voltage source
- Vout is output voltage
- PUN : C5NPMOS
- PDN : C5NNMOS

![image](https://github.com/Jyothi181/Pictures/blob/main/Picture16.png)

***Figure 10: LTspice Schematic of NOT Gate***

### Schematic of NAND Gate
- M3 and M4 are PMOS transistors
- M1 and M2 are NMOS transistors
- VA and VB are input voltages
- VDD is voltage source
- Vout is output voltage
- PUN : Two C5NPMOS are connected in parallel
- PDN : Two C5NNMOS are connected in series

![image](https://github.com/Jyothi181/Pictures/blob/main/Picture17.png)

***Figure 11: LTspice Schematic of NAND gate***

### Schematic of NOR Gate
- M1 and M2 are PMOS transistors
- M3 and M4 are NMOS transistors
- VA and VB are input voltages
- VDD is voltage source
- Vout is output voltage
- PUN : Two C5NPMOS are connected in series
- PDN : Two C5NNMOS are connected in parallel

![image](https://github.com/Jyothi181/Pictures/blob/main/Picture18.png)

***Figure 12: LTspice Schematic of NOR gate***

# Simulation Results

## How to simulate

- Once the schematic is done, click on `Run/Pause(Alt+R)` to run the schematic.
- Select the `Add Plot Pane Above` option by left click on the waveform viewer window. Add 3 panes for 2 inputs and 1 output.
- To plot the graphs, click on the specific pane and each input and output nodes.

## Results

The pulse rises from 0 to 5v. Depending on the pulse width and period settings, the pulse will repeat at regular intervals. The generated output is based on the applied inputs VA, VB and the logic functionality. The graphs VA - V(n002), VB - V(n003), Vout - V(vout) represent the inputs and output respectively with different colours. The simulation results verifies the functionality of circuits. 

![image](https://github.com/Jyothi181/Pictures/blob/main/Picture19.png)

***Figure 13: Simulated waveform of AND Gate***

![image](https://github.com/Jyothi181/Pictures/blob/main/Picture20.png)

***Figure 14: Simulated waveform of OR Gate***

![image](https://github.com/Jyothi181/Pictures/blob/main/Picture21.png)

***Figure 15: Simulated waveform of NOT Gate***

![image](https://github.com/Jyothi181/Pictures/blob/main/Picture22.png)

***Figure 16: Simulated waveform of NAND gate***

![image](https://github.com/Jyothi181/Pictures/blob/main/Picture23.png)


***Figure 17: Simulated waveform of NOR gate***

