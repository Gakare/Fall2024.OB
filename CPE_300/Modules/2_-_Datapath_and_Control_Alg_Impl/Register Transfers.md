# Things that will get covered:
- Register transfers
- Datapath architectures
- Register files and the architecturee
- Delays, machine cycle, Clock.
- General Datapath

# Register Transfers
## Behavioral model of 4-bit D register (4-bit memory)
```verilog
module reg4(CLK, D, Q);
	input CLK;
	input [3:0] D;
	output [3:0] Q;
	reg [3:0] Q
	always @(posedge CLK) begin
		Q = D;
	end
endmodule
```

Data transfer
- Either copying data
	- $R_x\leftarrow R_y$
- Or storing modified data into on-board memory
	- $R_x\leftarrow R_y+R_x$
	- $R_x\leftarrow R_y+R_z$
- Each of the above statements are implemented in one cycle (Clock period).
# Gated Register Transfers
![[GRT.png]]
- A $\leftarrow$ C, and B $\leftarrow$ C can occur together
- But not A $\leftarrow$ C and A $\leftarrow$ D, or B $\leftarrow D$ and A $\leftarrow$ C
- $G_c$, $G_D$, $S_A$, $S_B$ are control signals

# Multiplexed Register Transfer
![[MRT.png]]
- The difference is that there is one control signal, G
	- Control unit is simplified
# Example of transfers through the CL
![[Comb_With_Mux.png]]
- Combinational circuit implements functions (F1(C,D) and F2(C,D)).
- Possible transfers are:
	- $A\leftarrow F1(C,D)$
	- $A\leftarrow F2(C,D)$
# How to connect logic/registers to a shared BUS
- When various circuits output to a shared bus, **tri-state buffers are mandatory** to prevent 1 and 0 appear at the same time on the bus line
	- Logically, High and Low cannot be asserted at the same time on the same wire
	- Electrically, it creates a <u>low resistance path from power supply to ground - with predictable results!</u>

# Buffer
```verilog
module tristate_buff(output_x, input_x, enable);
	input input_x;
	input enable;
	output output_x;

	assign output_x = enable?input_x:'bz;
endmodule
```

![[Tri_Buff.png]]
# Registers can transfer to the BUS and can get Data from the Bus:
Only one out of n enable signals $G_i$ can be high in any bus cycles
- Transfers are possible
	- between any 2 registers $R[i]\leftarrow R[j]$
	- from one to many
	- from one to all

# Single-bus architecture
- All circuits are connected through a single pathway- BUS
- Electronic circuit that carries data and control signals through the wires
- Circuits 1, 3 and 4 connect to the bus through tri-state buffers
![[Single_Bus_Arch.png]]