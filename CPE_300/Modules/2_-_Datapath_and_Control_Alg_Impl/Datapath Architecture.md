- Datapath
	- Responsible for transferring, storing and processing data, and thus includes registers or register file, ALU and morelogic for moving data to proper circuits using multiplexers.
- Control unit
	- Provides control signal to the Datapath to move data and select an operation to perform cycle-by-cycle.
	- Can be purely combinational circuit, a sequential circuit or can use memory for reading a pattern of control signals (microcoding).
- Decision about how the datapath modules **interface** (interconnect) has a critical effect on the performance and the cost of the design.
- A **single bus** (a **single port register file**) and **multi-bus** or point-to-point connection with a multi-port register file are examples the interconnect.
- Many simple microcontrollers are designed with a single bus architecture, while a general purpose microprocessors favor a 3-port register file.
- Please note that the architecture of the processor and the architecture of the system differ:
	- The processor can be designed based on a single(local) bus while the peripherals can be connected to the processor via a number of specialized buses.
# How to connect logic/registers to a shared BUS
- When various circuits output to <u>a shared bus</u>, **tri-state buffers are mandatory** to prevent 1 and 0 appearing at the same time on the line.
	- Logically, High and Low cannot be asserted at the same time on the same wire. What logic value is meant to be?
	- Electrically, it creates a **low resistance path from power supply to ground--with predictable results!**
### Connection to the bus: multiple registers or multiple circuits connect with Tri-state buffer (IRON LAW)
![[Iron_law.png]]
Only one of $G_i$ signals (enabling tri-state buffers) can be high during the bus cycle
- Transfers are possible
	- between any 2 registers $R[i]\leftarrow R[j]$
	- from one to many
	- from one to all
## Example of a single bus Datapath architecture:
- Since the bus allows one register transfer in a cycle, **registers Y and Z are added**.
- They are buffer registers
- The first operand is stored in Y register
- The $2^{nd}$ operand arrives to ALU, and the result of ALU is stored into Z register
- CAN use latches for registers