# As per the Update given for the next task "Should Use the RISC-V Core Verilog netlist and testbench for functional Simulation.
# Veriog code is being executed and the waveforms are generated using the gtkwave

# Aim: To verify the Functional Simulation:-
# Table of contents
- [1.RISC-V RV32I](#1-RISC-V-RV32I)
 - [2.BLOCK DIAGRAM OF RISC-V RV32I](#2-BLOCK-DIAGRAM-OF-RISC-V-RV32I)
 - [3.INSTRUCTION SET OF RISC-V RV32I](#3-INSTRUCTION-SET-OF-RISC-V-RV32I)
 - [4.FUNCTIONAL SIMULATION](#4-FUNCTIONAL-SIMULATION)
    - [4.1 About iverilog and gtkwave](#41-About-iverilog-and-gtkwave)
    - [4.2 Installing iverilog and gtkwave](#42-Installing-iverilog-and-gtkwave)
    - [4.3 The output waveform](#43-The-output-waveform)
  
   ## 1. RISC-V RV32I

This project provides an insight into the working of a few important instructions of the instruction set of a Single cycle Reduced Instruction Set Computer - Five(RISC-V) Instruction Set Architecture suitable for use across wide-spectrum of Applications from low-power embedded devices to high-performance Cloud-based Server processors. The base RISC-V is a 32-bit processor with 31 general-purpose registers, so all the instructions are 32-bit long. Some Applications where the RISC-V processors have begun to make some significant threads are in Artificial intelligence and machine learning, Embedded systems, ultra-low power processing systems, etc.

## 2. BLOCK DIAGRAM OF RISC-V RV32I

![WhatsApp Image 2024-03-04 at 6 55 53 AM](https://github.com/Lokeshwari2/lokeshwari/assets/161022299/97ffaef6-9cab-40d9-8d21-fb29314b396f)

## 3. INSTRUCTION SET OF RISC-V RV32I

![WhatsApp Image 2024-03-04 at 6 56 42 AM](https://github.com/Lokeshwari2/lokeshwari/assets/161022299/1b364438-a877-4e58-a092-04891beaaf56)

![WhatsApp Image 2024-03-04 at 7 29 23 AM](https://github.com/Lokeshwari2/lokeshwari/assets/161022299/b4e74a33-fe4a-4bfe-bbb6-8a4ca8f6f575)


## 4. FUNCTIONAL SIMULATION

### 4.1 About iverilog and gtkwave
- Icarus Verilog is an implementation of the Verilog hardware description language.
- GTKWave is a fully featured GTK+ v1. 2 based wave viewer for Unix and Win32 which reads Ver Structural Verilog Compiler generated AET files as well as standard Verilog VCD/EVCD files and allows their viewing.
  
### 4.2 Installing iverilog and gtkwave

- **For Ubuntu**

 Open your terminal and type the following to install iverilog and GTKWave
 ```
 $   sudo apt get update
 $   sudo apt get install iverilog gtkwave
 ```

![install![WhatsApp Image 2024-03-04 at 6 41 14 AM](https://github.com/Lokeshwari2/lokeshwari/assets/161022299/f99df23f-14f2-4a49-b92f-6b4d67472505)

- **To clone the repository and download the netlist files for simulation, enter the following commands in your terminal.**

 ```
 $ git clone https://github.com/Lokeshwari2/lokeshwari.git
 $ cd lokeshwari
```
![WhatsApp Image 2024-03-04 at 6 41 14 AM (3)](https://github.com/Lokeshwari2/lokeshwari/assets/161022299/83f4a65c-862e-4ef4-bfd3-5f989b589e30)

- **To simulate and run the Verilog code, enter the following commands in your terminal.**

```
$ iverilog -o hello hello.v hello_tb.v
$ ./hello
```
- **To see the output waveform in gtkwave, enter the following commands in your terminal.**

`$ gtkwave hello.vcd`
![WhatsApp Image 2024-03-04 at 6 41 14 AM (4)](https://github.com/Lokeshwari2/lokeshwari/assets/161022299/9403d167-8fd8-4c5c-91f0-cbf16f27f7d5)

![WhatsApp Image 2024-03-04 at 6 41 14 AM (7)](https://github.com/Lokeshwari2/lokeshwari/assets/161022299/dd42788f-3fab-49b9-90b7-742940c233e1)

### 4.3 The output waveform

 The output waveform showing the instructions performed in a 5-stage pipelined architecture.
 
 Instruction 1:add r6,r2,r1
 ![WhatsApp Image 2024-03-04 at 6 58 20 AM](https://github.com/Lokeshwari2/lokeshwari/assets/161022299/22c1fbe6-a1dc-4bcf-9bf5-50387f2204d8)

 Instruction 2:sub r7,r1,r2
 
![WhatsApp Image 2024-03-04 at 6 58 57 AM](https://github.com/Lokeshwari2/lokeshwari/assets/161022299/4a35445c-a6e0-4c68-92e1-20ddd99f35af)
 
Instruction 3:and r8,r1,r3
![WhatsApp Image 2024-03-04 at 6 59 44 AM](https://github.com/Lokeshwari2/lokeshwari/assets/161022299/889601c9-c63c-41ef-a73e-85a14af667f4)

Instruction 4:or r9,r2,r5

![WhatsApp Image 2024-03-04 at 7 30 18 AM](https://github.com/Lokeshwari2/lokeshwari/assets/161022299/e09d5f24-4359-4a75-9bbf-22245a804b41)

 Instruction 5:xor r10,r1,r4
![WhatsApp Image 2024-03-04 at 7 31 29 AM](https://github.com/Lokeshwari2/lokeshwari/assets/161022299/ca216b98-a968-412c-a46a-5323754273b5)

 Instruction 6:slt r11,r2,r4
![WhatsApp Image 2024-03-04 at 7 31 47 AM](https://github.com/Lokeshwari2/lokeshwari/assets/161022299/1598b215-fb1f-407f-b8ea-39804b154f33)

 Instruction 7:addi r12,r4,5
![WhatsApp Image 2024-03-04 at 7 32 24 AM](https://github.com/Lokeshwari2/lokeshwari/assets/161022299/bbbd8fc7-a51d-4af8-b397-5894c78f58ff)

 Instruction 8:sw r3,r1,2
![WhatsApp Image 2024-03-04 at 7 33 15 AM](https://github.com/Lokeshwari2/lokeshwari/assets/161022299/72a7c8ab-8130-43bc-a8e9-4ae43740ba02)

 Instruction 9:lw r13,r1,2
![WhatsApp Image 2024-03-04 at 7 34 02 AM](https://github.com/Lokeshwari2/lokeshwari/assets/161022299/063e036e-8c5b-4287-92b2-cf9e6a4fad20)

 Instruction 10:beq r0,r0,15

![WhatsApp Image 2024-03-04 at 7 36 19 AM](https://github.com/Lokeshwari2/lokeshwari/assets/161022299/2ffcf120-7e54-4f51-9a61-74145e0612f4)

 After branching, performing
 Instruction 11:add r14,r2,r2
![WhatsApp Image 2024-03-04 at 7 37 29 AM](https://github.com/Lokeshwari2/lokeshwari/assets/161022299/8ba8fc3c-6458-4b5e-9ac6-cdde71cac46b)

  Full 5-stage instruction pipeline and pc-increment description Waveform
 ![WhatsApp Image 2024-03-04 at 7 38 12 AM](https://github.com/Lokeshwari2/lokeshwari/assets/161022299/6ab12d7d-6e94-452d-8a83-cd47f36d2e9f)

![WhatsApp Image 2024-03-04 at 7 38 39 AM](https://github.com/Lokeshwari2/lokeshwari/assets/161022299/75d7425f-8156-461e-84fe-1a381373e6ca)

![WhatsApp Image 2024-03-04 at 8 41 16 AM](https://github.com/Lokeshwari2/lokeshwari/assets/161022299/34a4fffa-91ee-4c4d-ac78-cb5b8cf5e532)

