# Data-processing (DP) Instruction Format
- Operands:
	- **Rn**: First source register
	- **Src2**: Second source - register or immediate
	- **Rd**: Destination register
- Control fields:
	- **cond**: specifies conditional execution
	- **op**: opcode (00 for data processing)
	- **funct**: the function/operation to perform
![[Data-Processing Format.png]]
# Data-processing Control Fields
- op = $00_2$ for data-processing (DP) instructions
- funct is composed of cmd, *I*-bit, and *S*-bit
	- cmd: specifies the specific data-processing instruction. For example
		- *cmd* = $0100_2$ for ADD
		- *cmd* = $0010_2$ for SUB
	- *I*-bit
		- *I* = 0: Src2 is register
		- *I* = 1: Src2 is an immediate
	- *S*-bit: 1 if sets condition flags
		- *S* = 0: SUB R0, R5, R7
		- *S* = 1: ADDS R8, R2, R4 or CMP R3, #10
![[funct spec.png]]
# Data-processing Src2 Variations
- Src2 can be:
	- Immediate
	- Register
	- Register-Shifted register
![[Src2.png]]
# Immediate Src2
- Immediate encoded as:
	- imm8: 8-bit unsinged immediate
	- rot: 4-bit rotation value
- 32-bit constant is: imm8 ROR (rot $\times$ 2)
	- Example: imm8 = abcdefh
![[ROR.png]]
![[rot.png]]
- See how **two bits** are rotated because it is 32-bits.
![[imm src2.png]]
# DP Instruction with Immediate Src2
- Example: ADD R0, R1, \#42
- op = $00_2$ (0) for data-processing instructions
- cmd = $0100_2$ (4) for ADD
- Src2 is an immediate so *I* = 1
- Rd = 0, Rn = 1
- imm8 = 42, rot = 0
![[imm instr ex.png]]
![[Mnemonic.png]]
# DP Instruction with Immediate Src2
- Example: SUB R2, R3, \#0xFF0
- cond = $1110_2$ (14) for uncoditional execution
- op = $00_2$ (0) for data-processing instructions
- cmd = $0010_2$ (2) for SUB
- Src2 is an immediate so *I* = 1
- Rd = 2, Rn = 3
- imm8 = 0xFF
- imm8 must be rotated right by 28 to produce 0xFF0. (rotate 14x2)
- S = 0 (no condition is to set)
![[imm src2 ex 2.png]]
# DP Instruction with Src2 - Register
- Rm: the second source operand
- shamt5: the amount $r_m$ is shifted
- sh: 2 bits for 4 types of shift (i.e., >>, <<, >>>, ROR)
First, consider unshifted versions of Rm (shamt5 = 0, sh = 0)
![[src2 - register.png]]