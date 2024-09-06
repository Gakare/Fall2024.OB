# Datapath Architectures and the Register Files

# An example of a single bus DP: registers and ALU
- Since the bus allows one register transfer in a cycle, registers Y and Z are added.
- They are buffer registers
- The first operand is stored in Y register
- The $2^{nd}$ operand arrives to ALU, and the result of ALU is stored into Z register
- Can use latches for registers
- Assume ALU performs only addition and subtraction

# Register transfers (expressed in RTL) and <u>control words</u>
<u>Abstract transfer (what to do)</u>
- $R[1]\leftarrow R[0]+R[1]$;

<u>Concrete transfers (how to do on the DP)</u>
Cycle 1: $Y\leftarrow R[0]$;
Cycle 2: $Z\leftarrow R[1]+Y$;
Cycle 3: $R[1]\leftarrow Z$;

<u>Control Words (what signals by CU and when (cycle #))</u>
Cycle 1: $R[0]$out, Yin; //Other signals are 0
Cycle 2: $R[1]out, Zin; S = 0 (meaning add); // others = 0
Cycle 3: Zout, R[1]in; //others = 0

# Register file: RF
- When we want to store several numbers in a digital circuit, we use several registers.
- There are times when we want to treat these registers as a unit, similar to addressing locations of memory by having an array of registers.
- This array of registers is known as a **register file (RF)**.
- Having an RF has a benefit of reducing the total number of control signals for register transfers.
- In a register file, all control signals for allowing input or output to the individual registers can be connected in common, but the selection of a specific register can be made (using a decoder).

## An examle of a single-bus datapath with the RF
- 32 registers
- 32-bit registers
 ![[single_bus_DP_RF.png]]
# RF for a single bus architecture
RF has a **single port** to access a register either for reading one operand, or for writing the result.

**A decoder selects a register for read or write**
$r_x$ is a 5-bit register identifier, that is the register number to be accessed.

Wtih this provision, only one gate signal $R_{in}$ is required.
Likewise, only one Enable signal for tri-state buffers is sufficient.
This is considerable saving in terms of the CU complexity
- Instead of 64 control signals for 32 registers, we only need 2.

# 3-bus architecture (or point-to-point connection)
![[3_bus_arch.png]]
- RF has two read ports and one write port (3 decoders)
- Two registers can output to Bus A and to Bus B and the result can be rewritten to a register in the same cycle: $R_x\leftarrow R_y+R_z$
- Add numbers that are in $R[1]$ and $R[2]$ and write the result into $R[3]$

<u>Abstract transfer (what to do)</u>
- $R[3]\leftarrow R[1]+R[2]$

<u>Concrete transfers (how to do on the DP)</u>
- Cycle 1: $R[3]\leftarrow R[1]+R[2]$;

Control words:
**Need to know how the RF is designed:**
# Control signlas to operate the RF
- Address lines are used to specify which register in the RF is to be accessed.
- A typical RF has one writing port
- WE - enables decoding of the write port decoder.
- W$A_1$ and W$A_0$ are two bits of the register identifier for writing into (through in port)
- RAE and RBE are enable signals for decoding register identifiers for reading to ports A and B.
- RB$A_1$, RB$A_0$ are two bits of the register identifier for reading to port B.
- RA$A_1$, RA$A_0$ are two bits of the register identifier for reading to part A.
# IC of the RF (four eight-bit registers)
- Note the large number of pins.
- Check also the total number of control signals required.
	- Large number of control signals will increase the complexity of the Control unit (cost).
- But <u>can improve the performance</u>: the wall clock time.