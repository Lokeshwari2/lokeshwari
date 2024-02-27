 # lokeshwari
 # learn various types of RISC-V instructions
<p align="justify">RISC-V instructions are encoded using a fixed-length 32-bit format, which simplifies decoding and execution. The instruction formats are categorized into six types: R, I, S, B, U, and J. Each format serves a specific purpose and has a unique encoding structure:</p>

<details>
<summary><b>R-type instructions:
</b></summary>
<br>
<p align="justify">Used for register-to-register operations, such as arithmetic and logical operations. They include three register operands: two source registers and one destination register. Eg:- add (Add 2 registers and store results in another)</p>
  </details>
<details>
<summary><b>I-type instructions:
</b></summary>
<br>
<p align="justify">Used for immediate operations, such as arithmetic and logical operations with an immediate value. They include two register operands and a 12-bit immediate value. Eg:- li (Load immediate value)</p>
  </details>
<details>
<summary><b>S-type instructions:
</b></summary>
<br>
<p align="justify">Used for store operations, which store data from a register to memory. They include two register operands and a 12-bit immediate value for the memory address offset. Eg:- sw (store the value in register)</p>
  </details>
<details>
<summary><b>B-type instructions:
</b></summary>
<br>
<p align="justify">Used for conditional branch operations, which transfer control to a different instruction based on a condition. They include two register operands and a 12-bit immediate value for the branch target address. Eg:- beq (compare and label)</p>
  </details>
<details>
<summary><b>U-type instructions:
</b></summary>
<br>
<p align="justify">Used for operations with a 20-bit immediate value, such as loading a 20-bit constant into a register or setting the upper 20 bits of a register. Eg:- lui (load upper immediate value)</p>
  </details>
<details>
<summary><b>J-type instructions:
</b></summary>
<br>
<p align="justify">Used for unconditional jump operations, which transfer control to a different instruction unconditionally. They include one register operand and a 20-bit immediate value for the jump target address. Eg:- J (jump)</p>
</details>

# Base Instructions Format

<p align="justify">In RISC-V, the base instruction format is a 32-bit instruction word divided into several fields. The basic format consists of opcode, rd (destination register), funct3 (function 3), rs1 (source register 1), imm (immediate value), and funct7 (function 7). This design allows for a wide range of instructions while maintaining simplicity and flexibility, which are key principles of the RISC-V architecture.</p>

<details>
<summary><b>Instruction code format </b></summary>
	<br>
![WhatsApp Image 2024-02-24 at 1 20 51 AM](https://github.com/Lokeshwari2/lokeshwari/assets/161022299/6fb9cb76-b57f-40b2-a0a7-6a2ff09f7450)

 +  add r6, r2, r1 	= R type instruction
+ sub r7, r1, r2	= R type instruction
+ and r8, r1, r3	= R type instruction
 + or r9, r2, r5	= R type instruction
+ xor r10, r1, r4	= R type instruction
+ slt r11, r2, r4	= R type instruction
+ addi r12, r4, 5	= I type instruction
+ sw r3, r1, 2		= S type instruction
+ lw r13, r1, 2		= I type instruction
+ beq r0, r0, 15	= B type instruction
+ bne r0, r1, 20	= B type instruction

</details>

# RISC-V REGISTER FILE: 
 <p align="justify">The RISC-V register file is a key component of the RISC-V architecture, providing a set of storage locations for holding data during the execution of instructions. The register file is organized into a set of integer registers and floating-point registers, depending on the extensions implemented in the processor. Registers play a crucial role in the RISC-V architecture, as they enable fast access to data and help improve the performance and efficiency of the processor.</p>
