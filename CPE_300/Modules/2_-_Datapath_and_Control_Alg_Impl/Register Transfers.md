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