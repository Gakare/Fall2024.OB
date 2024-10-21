Microprocessor without Interlocked Pipelined Stages

# Instruction Set \[Architecture\]
- Computer has to operate these intructions
- Computer design and performance depend on the choice of the instruction set.
- ==Instructions expressed in a native machine language are called Assembly.==
- Assembly is specific to machine, as it is tailored for a specific architecture
	- MC68000, PIC, MIPS, etc

# Instruction Set and Machines
- Operations (number and type)
- Addressing modes (register, memory, constants)
- Length of data and instructinos (8-bit, 16-bit, 32-bit, 64-bit)
- Number of operands in instructions
- Format of the instructions: number of fields, lengths of fields
- Number of register in the Register file
- Types of architecture: <b>RISC, CISC, VLIW</b>.
# Dynamic-Static Interface (DSI)
![[DSI.png]]
# Possible placements of DSI
![[Placement Of DSI.png]]
- DEL - Directly executable language (program written in a high level language can be directly executed);
- CISC - Complex Instruction Set Computer (DSI is placed at the traditional assembly language or macrocode level);
- RISC - Reduced Instruction Set Computer (more optimization by compiler);
- VLIW - Very Large Instruction Word processor (RISC-type instructions are packed together);
![[Levels Of Representation.png]]
# Memory Addressing Modes
- Data can be in Memory
- Data (operands) can be given in the form of constants
- Data can be placed in Register
- Large memory needs a lots of bits for addressing
	- Use base + *displacement*
	- Keep the base value in a register
	- Use a constant within instructions for displacement
	- Can use PC as a base
- CPU must form an effective address (EA) of memory location
- Some addresses may be known at compiler time, e.g. global variables
- Other may not be known until run time, e.g. pointers
# Instruction Classes - 1
- Data movement instructions
	- Move data from a memory location or register to another memory location or register.
	- ==Load== - <u>Source</u> is ==Memory== and <u>destination</u> is ==Register==
	- ==Store== - <u>Source</u> is ==Register== and <u>destination</u> is ==Memory==
# Instruction Classes - 2
- Arithmetic and logic (ALU) instructions
	- Add, Sub, Shift, OR, AND, NOT, etc.
		- MUL, DIV, XOR, NEG, ...
# Instruction Classes - 3
- Branch instructions (control flow instructions)
	- Any instruction that alters the normal flow of control from executing the next instruction sequence
	- br Loc1 - unconditional branch, a.k.a. ==jump==
	- brz Loc2 - conditional branch

# RISC (MIPS, SPARC) Architectures
- Usually Load/Store architecture.
	- Only 2 types of instruction are allowed to access memory <u>Load</u> and <u>Store</u>. Arithmetic is done on registers only.
- $<120$ instructions; MIPS has 111 instructions ; some are pseudo-instructions.
- Fewer data types support: integer, double, byte.
- Fewer addressing modes (direct, base +displacement, PC - relative, register indirect)
- Simple hardware control unit (without microcode memory).
- Large number of register 32 - 128.
# Characteristics of RISC
- *Large number of registers*: the RISC generally have a larger number of registers to limit frequent interactions with memory which is behind and thus affects the overall performance drop.
- *Uniform instruction length*: all instructions have the same length (usually, 32 bits).
	- Some microprocessors contain instructions as small as a byte and as large as 16 bytes.
- Fewer instruction formats
- Encoding the different fields in the instruction as uniformly as possible.
	- To simplify instruction decoding.
- Few addressing modes
- Load/Store architecture
# MIPS is RISC
- The first RISC projects came from IBM, Stanford, and UC Berkeley in the late 70s and early 80s.
- The IBM 801, Stanford MIPS, and Berkeley RISC 1 and 2 were all designed with a similar philosophy which become known as RISC.
- MIPS Technologies, Inc., Founded in 1984.
# MIPS Architecture
- Hardvard architecture: seperate instruction and data (cache) memory.
- 3-port register file (two for reading and one for writing)
	- There are 32 general-purpose registers in the RF.
		- Each register is 32 bits wide.
- Load-store machine
	- Arithmetuc runs on register operands.
	- Special instructions (load and store) move operands between memory and registers.
- Fixed size instructions, 32 bits.
- Small number of instruction formats, 3 instruction formats (R, I, J)
	- Opcode (fixed size) always the first 6 bits.
- Limited number of addressing modes
- Limited number of instructions.
# MIPS-32 Instructions
- 21 arithmetic instructions (+, -, \*, /, %)
- 8 logic instructions (\&, |, ~)
- 8 bit manipulation instructions
- 12 comparison instructions (>, <, =, >=, <=, $\neg$)
- 25 branch/jump instructions
- 15 load instructions
- 10 store instructions
- 8 move instructions
- 4 miscellaneous instructions
- About 111 instructions

# Stored Program
- Instructions are first stored in Memory and then fetched to CPU to be executed.
- The insructions of the current instruction is kept in a 32-bit register.
	- Program Counter (PC).
![[Stored Program.png]]
# MIPS Registers
- 32 general-purpose 32-bit registers; numbers are preceded by \$ symbol
- 2 ways for addressing:
	- Using register number : \$0 through \$32
	- Using equivalent names: \$t1, \$sp, \$ra
- Special registers Lo and Hi used to store result of multiplication and division
	- not directly addressable; contents accessed with special instruction mfhi ("move from Hi") and mflo ("move from Lo")
	- Hi is used to store the upper part of the multiplication result and the remainder of the division result.
	- Lo is used to store the lower part of the multiplication result and the quotient of the division result.
# Data Registers:
- \$0 always holds the constant value 0.
- 18 register for data
- The *saved* registers, \$s0-\$s7, used to hold variables
- The *temporary* registers, \$t0-\$t9, used to hold intermediate values during a larger computation; used for function calls
# MIPS Registers
![[Register BD.png]]
![[Register Table.png]]
# MIPS Memory
- Memory is byte addressable
- MIPS can be Big Endian or Little Endian
![[endian.png]]
- MIPS instructions are placed aligned by a word: 4 bytes.
	- Alignment restriction - the memory address of a word must be on natural word boundaries
	- a multiple of 4 in MIPS-32
![[Memory.png]]
# Memory Allocation In Mips
- Stack grows from high memory to low memory.
- Text is the code (instruction) space.
- Reserved space for Operating System (OS).
![[Memory Example.png]]
# MIPS-32 ISA Instruction Categories
- Arithmetic/Logic/Bit operations
- Load/Store
- Jump and Branch
- Floating Point
	- By so-called co-processor1, which is not a different processor, but another ALU, called floating point unit
- Memory Management
- Special, like NOP
# MIPS-32 ISA Instruction Formats
![[Instruction Formats.png]]
- op (operation code) 6-bits opcode that specifies the operation
- rs (source register) 5-bits register file address of the first source operand
- rt (target register) 5-bits register file address of the second source operand
- rd (destination register) 5-bits register file address of the result's destination
- shamt 5-bits shift amount (for shift instruction)
- funct 6-bits function code augmenting/extending the opcode
- immediate (constant value) directly placed into the instruction
- jump target - address of the instruction in the memory to fetch
# Instruction Examples
## Operations
![[Operations.png]]
## Conditionals And Jumps
![[Conds.png]]