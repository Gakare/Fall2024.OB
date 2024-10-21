- Single cycle and multi-cycle implementation
- Performance analysis

# Single Cycle MIPS design for a limited subset of instructions

## Design goals, 1st round
- Our design is limited to the following instructions:
	- Memory-reference instructions: <u>lw, sw</u>
	- arithmetic-logical instructions: <u>add, sub, and, or, addi</u>
	- control flow instructions: <u>beq</u>
- Then we will add ==j==
- Also, we will discuss and assign changes to incorporate <u>ori, jr, sll, sllv</u>
# Design Preliminaries
- Generic implementation:
	- Program Counter (PC) supplies the instruction address; fetch the instruction from memory;
		- Update the PC:
			- PC=PC+4
	- Decode the instruction (and read registers)
	- Execute the instruction: arithmetic/logic or memory access.
- All instructions use the ALU after reading the registers, even lw and sw for address calculation, or for comparison (subtraction).
# Single Cycle MIPS design, 1
- Instruction is fetched from the memory, decoded and executed in one cycle.
- Single cycle: no datapath resource can be used more than once per instruction, so some must be duplicated (e.g., adders)
- A single-cycle implementation dictates seperate instruction and data memories (caches)
	- Multiported memory is expensive
- RF has to have 3 ports (2 read and 1 write) to allow parallel read of two operands and writing to a destination.
# Design
- Design the datapath
- Identify control signals for the datapath.
	- Design the control unit
- Need to review the formats
# Decoding R instructions: two steps
- There are two parts of control unit
- One is called Main decoder outputs control signals for all parts of the datapath <u>based on the opcode</u>
- ALU decoder provides control signals to ALU for the operation type and needs the <u>funct field</u>.
![[Decoding R Instructions.png]]
# Control: Main decoder and ALU decoder
![[Main Decoder.png]]
- Based on the opcode, Main Decoder is able to differentiate lw, sw, beq and R type instructions (as a group) and produce control signals for the datapath except different ALU operation codes.
- lw, sw need from ALU add to calculate the memory address (base+offset)
- beq needs from ALU sub to calculate the difference between two registers and form the condition.
- R type instructions are not yet known and therefore decoded as a group as 10;
- 11 is not used; thus we pass to the second decoder, that is ALU decoder gets 1x
# ALU decoder
![[ALU Decoder.png]]
- ALU decoder checks Funct field to differentiate the arithmetic/logic
- Because there are add and subtract operation they need to be encoded.
- Also, to be encoded and, or, and slt.
- More than two bits needed now, and add and sub are decoded as 010 and 110.
- All other instructions for ALU are also encoded.
# MIPS Design Module (For This Class)
- Top
	- mips
		- controller
			- maindec
			- aludec
		- datapath
			- flopr
			- adder
			- sl2
			- adder
			- mux2 \#(32)
			- mux2 \#(32)
			- regfile
			- mux2 \#(5)
			- mux2 \#(32)
			- signext
			- mux2 \#(32)
			- alu
	- imem
	- dmem