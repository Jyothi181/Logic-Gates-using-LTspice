# Basic-Gates-using-LT-Spice
NAND Gate is one of the universal gate. A universal gate is a digital logic gate that can be used to implement any Boolean function without requiring other gates. This repository explains the implementation of NAND Gate in CMOS Logic using LT Spice Simulator. This shows the schematic of NAND Gate and plot the output waveform to verify the functionality.

# Table of Contents
Introduction
Objectives
Circuit Details
Working
Simulation Results

# INTRODUCTION
A logic gate is a device that performs logical operations on one or more binary inputs and produces a single binary output. The primary way of building logic gates uses diodes or transistors acting as electronic switches. Today, most logic gates are made from MOSFETs (metal–oxide–semiconductor field-effect transistors). Logic circuits include such devices as multiplexers, registers, arithmetic logic units (ALUs), computer memory and microprocessors which may contain more than 100 million logic gates. Basic gates, also known as elementary or fundamental gates, include the AND, OR and NOT gates. These gates operates on binary signals (0s and 1s) and provide the basis for all digit computations. Other gates such as XOR, XNOR, NAND and NOR can be derived from basic gates.

# OBJECTIVES
The main goal of this project are given below
1. To plot the schematics of logic gates, and circuits 
2. To plot the output waveform 
3. To verify the functionality

# PROJECT STRUCTURE
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

![image](https://github.com/user-attachments/assets/26c776f8-aa80-42a1-a93b-09903502a345)

![image](https://github.com/user-attachments/assets/9f8fca88-708e-4f45-8e0a-c03172b4fbdf)

![image](https://github.com/user-attachments/assets/bd57856a-a1a0-442e-8e61-975c2f24ce98)

# SIMULATION RESULTS

![image](https://github.com/user-attachments/assets/9c399522-1621-452f-b7f9-81a54d1d51c2)

![image](https://github.com/user-attachments/assets/ad43d981-ab06-4594-ac8c-0bf227bcce69)

![image](https://github.com/user-attachments/assets/f1db1ad2-8edb-4c54-a726-c0b860ae9479)

















