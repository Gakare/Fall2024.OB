# ARM Architecture
- Developed in the 1980's by Advanced RISC Machines - now called ARM Holdings
	- ARM is a Reduced Instruction Set Computer (RISC)
- Nearly 10 billion ARM processors sold/year
- Almost all cell phones and tablets have multiple ARM processors
- Over 75% of humans use products with an ARM processor
- Used in servers, cameras, robots, cars, pinball machines, etc.
# ARM Register Set: 16 of 32-bit registers
ARM is a "32-bit achitecture"
![[Arm Registers.png]]
- A user-mode program can see 15 of 32-bit general purpose registers
	- (R0-R14)
	- program counter (PC)
	- CPSR
- R(uppercase) before number
-  Example "R0" or "register zero" or "register R0"
- Text (user code starts at 0x00008000 and $sp at 0xBEFFFAE8)
# Program Status Registers (PSRs) (here it is for Cortex ARMv7)
![[Cortex ARMv7.png]]
# Processor Modes
![[Processor Modes.png]]
# ARM processor modes (Thumb, Thumb-2 and ARM mode)
- In an ARM processor, a "Thumb" instruction refers to a reduced instruction set encoding that allows the processor to execute code more efficiently in terms of code size and memory usage. **Thumbs instructions are 16 bits long**, compared to the regular ARM instructions that are 32 bits long.
	- Arm instructions - 32 bits long
	- Thumb instructions - 16 bits long
- An extension to the ARM architecture to enable more efficient code execution in memory-constrained environments. It provides a subset of the ARM instruction set, allowing developers to write code that takes up less space while still maintaining reasonable performance.
- The code size can be **reduced by approximately 30-40%** compared to the equivalent ARM instructions. This reduction in code sizes can be particularly advantageous in embedded systems and mobile devices where memory resources may be limited.
- Once in Thumb mode, the processor can execute Thumb instructions until it encounters a branch instruction that transfers control to an ARM instruction. At that point, the processor switches back to ARM mode.
- Newer ARM architectures, such as ARMv7 and ARMv8, introduced the **Thumb-2** instruction set, which ==combines both Thumb and ARM instructions==. Thumb-2 allows the processor to seamlessly switch between Thumb and ARM instruction sets, providing a wider range of instructions while still maintaining code density benefits.
# Thumb state and ARM state
- Except in the most speed-critical of embedded devices, the cost of memory is much more critical than the execution speed of the processor. To reduce memory requirements and, thereby, cost, Advanced RISC Machines (ARM) created the Thumb instruction set as an option for their RISC processor cores. The most well-known chip that includes the Thumb instruction set is the ARM7TDMI. The "T" in the core's full name specifies Thumb.
- Every Thumb instruction could instead be executed via the equivalent 32-bit ARM instruction.
- However, not all ARM instructions are available in the Thumb subset;
	- For example, there's no way to access status or coprocessor registers.
- Also, some functions that can be accomplished in a single ARM instruction can only be simulated with a sequence of Thumb instructions.
# Thumb registers
- In the 16-bit Thumb state, it is a slightly different set of registers.
- In the ARM state, 17 registers are visible in user mode. One additional register -- a saved copy of Current Program Status Register (**CPSR**) that's called **SPSR** (Saved Program Status Register) -- is for exception mode only.
- 12 registers accessible in Thumb state are exactly the same physical 32-bit registers accessible in ARM state. Thus data can be passed between software running in the ARM state and software running in the Thumb state via registers R0 through R7.
- The Thumb state has unique stack mnemonics (PUSH, POP) that don't exist in the ARM state. These instruction assume the existence of a stack pointer, for which **R13** is used. They translate into load and store instructions in the ARM state.
- The **CPSR** register holds the processor mode (user or exception flag), interrupt mask bits, condition codes, and Thumb status bit (T=1 for Thumb state).
- Although other bits in the CPSR may be modified in software, it's dangerous to write to **T** directly; the results of an improper state changes are unpredictable.
![[Arm & Thumb Regs.png]]
# Features
- Load-store architecture
- 32-bit instructions
- Byte-addressable memory
	- 32-bit word = 4 bytes, so word address increments by 4
	- Memory load and store for a word, byte and a half-word.
- 3-address instructions
- Conditional execution of every instruction
- Load/store multiple registers at once
- Possible to combine shift and ALU operations in a single instruction
- 3 instruction classes: data processing, data movement, flow control
- Formats
![[Formats.png]]