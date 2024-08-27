## Latches and flip-flops
* Latches and flip-flops: state elemens that store one bit of state (0 or 1).
* Different types and implementations
	* Level-sensitive (latches)
		* Simple circuit, complex in control
	* Edge sensitive (flip-flops)
		* More complex and expensive circuit, but easy to control

## Latches SR
* SR Latch with active high or active low inputs
 ![[Pasted image 20240827134928.png]]
 * Operations is asynchronous (not controlled by Clock or a dedicated control input, such as Enable).

## Enabled, a.k.a Gated SR latch
![[Pasted image 20240827135320.png]]
<font color="red">E input is usually referred to as Clock</font> input, however it does not necessarily assume a periodic signal, but rather a level of the enable signal (high).

## A dataflow model for latch: logic operations
```verilog
// A gated RS latch
module part1(clk, r, s, q);
	input clk, r, s;
	output q;
	wire r_g, s_g, qa, qb; /*synthesis keep*/

	assign r_g = r & clk;
	assign s_g = s & clk;
	assign qa = ~(r_g | qb);
	assign qb = ~(s_g | qa);

	assign q = qa;
endmodule
```
![[Pasted image 20240827135744.png]]
The <b>assign</b> construct in Verilog is the continuous assignment statement in Verilog which is used in data flow modeling.
Used to model combinational logic and replaces the gate description of the circuit.