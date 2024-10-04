# Memory System
- ROM
- RAM
	- SRAM, DRAM
- Verilog modules for on-board memories

# What is ahead
- Microprocessor design
	- Implements various instructions (code)
- Instructions and data are stored in Memories.
	- Memories are on the CPU chip and off-chip.
	- Memory are of different physical types.
![[Von Neumann Arch.png]]

# Memory types and hierarchy
![[Memory Hierarchy.png]]
- L1 Data and Instruction caches (separate) - 32KB or 64KB per core
- L2 cache - 256KB or 512KB (could be per core or shared up to 2 cores)
- L3 cache - May vary from 8MB to 32MB

# Memory Types
- RAM: Random Access Memory - memory arry with individual bit access.
	- Refers to memory with both Read and Write capabilities.
- ROM: Read Only Memory
	- No capabilities for "online" memory Write operations
	- Write typically requires high voltages
	- Erasing of information can be done by UV light.
# SRAM: Static RAM
- Static: holds data as long as power is applied
- Volatile: can not hold data if power is removed
- Three operation states: hold, write, read
- Basic 6T (6 transistor) SRAM Cell
	- Bi-stable (cross-coupled) INVs for storage
	- Access transistors MAL & MAR (Memory Access Left and Right)
	- Word line, WL, control access
	- WL = 0 (hold) = 1 (read/write)
![[SRAM.png]]

# DRAM: Dynamic Random Access Memory
- 1T DRAM Cell
	- Single access transistor; storage capacitor, C
	- Control input: word line (WL); data I/O: bit line (bi)
	- Dynamic: Must be refreshed periodically
	- Volatile: Loses data when power is removed
 ![[DRAM.png]]

# DRAM to SRAM Comparison
## Dram
- DRAM cell is smaller & less expensive **per bit**.
- DRAM requires more peripheral circuitry.
- DRAM memory is made large because it is off-chip and because it is less expensive. Also, because the whole memory architecture is heirarchical.
## SRAM
- SRAM cell is faster.
- SRAM cell is more expensive (6T).

# Logic Components of Memory
- Memory Array
	- *N* address bits and *M* data bits:
	- $2^N$ rows $M$ columns
	- *Depths*: number of rows (number of words)
	- *Width*: number of columns (size of word)
	- *Array Size*: depth $\times$ width = $2^N\times M$
- Decoder
	- Convert the address to a line selection in the array
- MUXes and DEMUXes for chip design
![[Logic Components of Memory.png]]
# A CMOS ROM Chip
When a line is selected, G=High and Line access=Ground. Outputs 1.
![[CMOS.png]]
- CS - Chip Select

# ROM Verilog module: Depth = 8; Width = 8
``` verilog
module my_Rom(address, data, read_en)
	input [2:0] address; // Depth of address will be 8
	output [7:0] data; // Width of data is 8
	input read_en;

	reg [7:0] data;

	always @(read_en or address) begin
		case (address)
		0: data = 10; 
		1: data = 55;
		2: data = 244;
		3: data = 0;
		4: data = 1;
		5: data = 8'hff;
		6: data = 8'h11;
		7: data = 8'h1;
		endcase
	end
endmodule
```

