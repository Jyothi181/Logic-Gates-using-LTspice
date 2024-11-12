# Basic-Gates-using-LT-Spice

This repository explains the implementation of Basic Gates in CMOS Logic using LT Spice Simulator. This shows the schematic of Basic Gates and plot the output waveform to verify the functionality.

# Table of Contents
Introduction
Objectives
Circuit Details
Working
Simulation Results

# INTRODUCTION
A logic gate is a device that performs logical operations on one or more binary inputs and produces a single binary output. The primary way of building logic gates uses diodes or transistors acting as electronic switches. Today, most logic gates are made from MOSFETs (metal–oxide–semiconductor field-effect transistors). Logic circuits include such devices as multiplexers, registers, arithmetic logic units (ALUs), computer memory and microprocessors which may contain more than 100 million logic gates. Basic gates, also known as elementary or fundamental gates, include the AND, OR and NOT gates. These gates operates on binary signals (0s and 1s) and provide the basis for all digit computations. Other gates such as XOR, XNOR, NAND and NOR can be derived from basic gates.

Complementary metal–oxide–semiconductor (CMOS) is a type of MOSFET that uses complementary and symmetrical pairs of p-type and n-type MOSFETs for logic functions. Input is applied at the common gate of PMOS and NMOS transistors.Output is taken from the PMOS and NMOS drain. CMOS technology is used for constructing integrated circuit (IC) chips, including microprocessors, microcontrollers, memory chips and other digital logic circuits. Two important characteristics of CMOS devices are high noise immunity and low static power consumption.

PMOS: The PMOS transistor is a p-channel device. It conducts current when a negative voltage (logic low) is applied to its gate terminal with respect to the source terminal. In CMOS, PMOS acts as pull up network in which the source is connected to VDD. When logic low(0) is applied is CMOS, the PMOS transistor turns on and connects the VDD to output which makes the output to logic high(1).

NMOS: The NMOS transistor is an n-channel device. It conducts current when a positive voltage (logic high) is applied to its gate terminal with respect to the source terminal. In CMOS, MMOS acts as pull down network in which the source is connected to ground. When logic high(1) is applied is CMOS, the NMOS transistor turns on and connects the output to ground which makes the output to logic low(0).

## OBJECTIVES
The main goal of this project are given below
1. To plot the schematics of logic gates, and circuits 
2. To plot the output waveform 
3. To verify the functionality

## PROJECT STRUCTURE
Tool : LTspice
Technology : C5N technology

# CIRCUIT DETAILS

The output of AND gate produces 1 if and only if all the input states are 1 else it produces 0. The logic symbol and truth table of 2-input AND gate is shown below.

![image](https://github.com/user-attachments/assets/e58eb1ee-58d5-4565-8813-a40ad05e960b)  ![image](https://github.com/user-attachments/assets/516544f5-eda3-4d6c-8f04-072f829f78d4)



The output of OR gate produces 1 if one or more input states are 1 else it produces 0. The logic symbol and truth table of 2-input OR gate is shown below.

![image](https://github.com/user-attachments/assets/f43f1257-c6c0-4bfb-9b90-ab726dcbd6de)   ![image](https://github.com/user-attachments/assets/211df32d-a96f-4dee-9df7-3786fb3eb088)


The NOT gate is a digital logic device whose output is always the complement of its input. The NOT gate can be implemented in CMOS logic by connecting PMOS to VDD which acts as Pull Up Network (PUN) and NMOS is connected to ground which acts as Pull Down Network (PDN). The logic symbol, truth table and CMOS implementation of NOT gate is shown below.

![image](https://github.com/user-attachments/assets/75f98793-2abf-4971-a744-4f0d1233621f)  ![image](https://github.com/user-attachments/assets/d683b441-be50-40d2-867f-ef4d74c39289)

# LTSPICE SIMULATION

Tool = LT spice Simulator
Technology = C5N technology file
Logic Gates = AND, OR, NOT, NAND, NOR 
VA = PULSE(0 5 0 1n 1n 5u 10u)
VB = PULSE(0 5 0 1n 1n 10u 20u)
V1 = 5v
Spice Directive = .include D:\NIELIT\ENGR3426\ENGR3426\engr3426.sub
Transient = .tran 100u

Inputs: The inputs are VA and VB. VA is applied to one of the PMOS and one of the NMOS. Likewise, VB is applied to one of the PMOS and one of the NMOS.

Output: The output Vout is based on the functionality of logic gates.

PULSE(0 5 1n 1n 5u 10u) is a syntax used to define a pulse waveform for a voltage source VA
PULSE(0 5 1n 1n 5u 20u) is a syntax used to define a pulse waveform for a voltage source VB

Initial Value (Vintial): 0[V]
This is the voltage level of the source before the pulse begins.

Pulse Value (Von): 5[V]
This is the voltage level during the ON period of the pulse.


Delay Time (Tdelay): 0[s] 
This is the delay time from input voltage to output voltage. In this case, there is no delay.

Rise Time (Trise): 1n[s] 
This is the time taken for the pulse to change from the Initial Value to the Pulse Value.

Fall Time (Tfall): 1n[s] 
This is the time taken for the pulse to change from the Pulse Value back to the Initial Value.
On Time (Ton): 5u for VA and 10u for VB
This is the time for which the pulse on for some period of time
Period (Tperiod): 10us for VA and 20us for VB
This is the total time for one complete cycle of the pulse waveform.

Number of Cycles (Ncycles): 10 
This specifies how many cycles of the pulse waveform should be generated.

Spice Directive: This contains text directly passes to the netlist which is placed on the schematic. The text may be single line or block or lines.

Transient: This analyzes the changes in voltage and current over time when an input signal is applied.

So, with the given inputs, the voltage source will start at 0V, then immediately rise to 5V. It will remain at 5V upto 5us for VA and 10us for VB, then drop back down to 0V. The total period for one complete cycle of this waveform is 10us for VA and 20us for VB. This cycle will repeat 10 times.

![image](https://github.com/user-attachments/assets/26c776f8-aa80-42a1-a93b-09903502a345)

![image](https://github.com/user-attachments/assets/9f8fca88-708e-4f45-8e0a-c03172b4fbdf)

![image](https://github.com/user-attachments/assets/bd57856a-a1a0-442e-8e61-975c2f24ce98)

# SIMULATION RESULTS

The pulse rise from 0 to 5v. Depending on the pulse width and period settings, the pulse will repeat at regular intervals. The generated output is based on the applied inputs VA, VB and the logic functionality. The graphs VA - V(n002), VB - V(n002), Vout - V(vout) represent the inputs and output respectively with different colours. The simulation results verifies the functionality of the circuits.  

![image](https://github.com/user-attachments/assets/9c399522-1621-452f-b7f9-81a54d1d51c2)

![image](https://github.com/user-attachments/assets/ad43d981-ab06-4594-ac8c-0bf227bcce69)

![image](https://github.com/user-attachments/assets/f1db1ad2-8edb-4c54-a726-c0b860ae9479)

















