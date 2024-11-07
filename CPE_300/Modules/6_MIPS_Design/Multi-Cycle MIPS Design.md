# Single Cycle Disadvantages (0:00)
- The clock cycle must be timed to accomodate the slowest instruction
	- Especially problematic for more complex instructions like floating point multiply
	- May be wasteful of area since some functional units (e.g., adders) must be duplicated because they can not be shared during a clock cycle.
	![[Single Cycle Disadvantage.png]]
This gives us a question on if we can improve this design in order to not waste valuable cycle resource.
# Multicycle Design Approach (2:15)
- Split the instruction execution into steps.
- Number of cycles is the design decision.
- Due to the simplicity of instruction set, there will be
	1. Instruction Fetch
	2. Instruction Decode and RF read
	3. ALU (for address calculation, compare registers, arithmetic/logic)
	4. Memory load and store (void for arithmetic/logic and branches)
	5. Write the result to RF (arithmetic or load)
- Need buffers between cycles as the
# Multicycle design: promises (8:22)
- Higher clock speed due to the cycle split.
- Simpler instructions run faster.
- Can reuse expensive hardware on multiple cycles, so the cycle can benefit.
![[Multicycle Processor Design.png]]
- Buffer registers are introduced between cycles.
# Multi-Cycle Mips (Performance Analysis)
![[Performance.png]]
![[Performance Cont.png]]