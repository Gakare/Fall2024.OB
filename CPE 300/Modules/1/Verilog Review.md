## Verilog Module
```verilog
module some(c, a, b,s); //name and ports
		output c; //data outputs
		input a, b; // data inputs
		input s; // data input

		assign c = s ? a : b; // (Terniary) data flow for modeling a combinational circuit
endmodule
```
## Data objects: nets and variables
* Net - a physical connection between structural entities (wire). It does not store any value.
	* <b>wire</b> is probably the most common net data type, although there are many other net data types such as <b>tri</b>, <b>wand</b> (AND on wires), <b>supply0</b>.
* A variable data type generally represents a piece of storage. <b>reg</b> generally used to model hardware registers can also represent combinatorial logic, like inside an <b>always@(*)</b> block). Other variable data types include <b>integer</b>, <b>time</b>, <b>real</b>, and <b>realtime</b>.
* Almost all Verilog data types are 4-state, which means they can take on 4 values: 0, 1, Z, X

## Wire elements
* Cannot store the value
* Cannot be used as the left-hand side of an = or <= sign in an always@ block.
* The only <font color="red">legal</font> type <font color="red">on the left-hand side</font> of an <font color="red">assign</font> statement.
* A stateless way of connecting two pieces in a Verilog-based design.
* Can only be used to model <font color="red">combinational logic</font>.
* By default, if not specified, in and out ports are wire type.
* Default initial value for a wire is "Z".

## Use Of Wire
```verilog
	wire A, B, C, D, E; // simple 1-bit wide wires
	wire [7:0] wide;    // 8-bit wide wire
...
	assign A = B & C;   // using a wire with an assignment
	always @(B or C)
		begin
			I = B | C;  // using wires on the RHS of an always@
			...
		end
	...
	mymodule mymodule_instance(. In (D), .Out(E)); // using a wire as the output of a module
```

## Register Type
* Used in combinational and sequential circuits.
* Only legal type on the left-hand side of an always@ block "=" or "<=".
* Only legal type on the left-hand side of an initial block "=" (used in Test Benches).
* Cannot be used on the left-hand side of an *assign* statement.
* Default value is "x"
* Similar to wires, but can be used to store information ('state') like registers, <font color="red">when used in conjunction with an always @(positive edge Clock)</font> blocks.
* <font color="red">Can be connected to the input port of a module instantiation.</font>
* *<font color="red">Cannot be connected to the output port of a module instantiation.</font>
* Can be used as outputs within an actual module declaration.
* <font color="red">Cannot be used as inputs</font> within an actual module declaration.

## Use Of Reg: Examples of Legal Usage
```verilog
wire A, B;      
reg I, J, K;    // simple 1-bit wide reg elements
reg[7:0] Wide;  // 8-bit wide reg element

always @(A or B) begin
	I = A | B;  // using a reg in an initial block
end

initial begin   // using a reg in an initial block
	J = 1'b1;
	#1          // delay
	j = 1'b0;
end
always @(posedge Clock) begin
	K <= I;    // Using a reg to create a pos-edge register
end
```

## Variable Data Types
* <b>integer</b> is typically a 32 bit 2's complement integer.
* <b>real-time</b> is of type <b>real</b> used for storing as a floating point value.
	* a 64 bit IEEE floating point number.
* <b>register</b>
* is driven in procedural block and initial block
* by default it is one bit unsigned value.
	* may have a modifier <b>signed</b>,
	* may have many bits by using the vector modifier \[most-significant bit : least-significant bit\].
* <b>time</b> is typically 64 bit unsigned value that is the simulation time
	* The <font color="red">system function $time</font> provides the simulation time.

## System-Verilog
* Has also 2-state variables: <font color="red">bit</font> and <font color="red">logic</font>
* Data types are called data objects: wire, register, wand
* *Bit*, *byte*, *short-int*, *int*, and *long-int* are the new System-Verilog two-state data objects.
* If the data type is not specified, then it is implicitly declared as <b>logic</b>.
```verilog
	var byte my_byte;    // byte is 2-state, so this is a variable
	var logic v;
	var logic [15:0] vw;
	var enum bit {clear, error} status; // variable of enumerated type
	var reg r;           // variable reg
```
* System-Verilog <b>logic</b> keyword standalone will declare a variable, but the rules have been rewritten such that you can pretty much use a variable everywhere in RTL (Register-Transfer Level) design.

## About Logic
* 'logic' and 'reg' can be used interchangeably.
* Multiple drivers can not be assigned to 'logic' data types i.e. values to a variable can not be assigned through two different places.
* Multiple-driver logic need to be implemented using net type e.ge 'wire', 'wand', and 'wor', which has the capability of resolving the multiple drivers.
* If we do not use not use the 'wire' to drive the muliple-driver logic, therefore 'wire' can also be replaced by 'logic'.

## Typedef and enum
* System-Verilog adds 'enum' and 'typedef', which can be used to define the '<b>user-defined (i.e. typedef) enumerated (i.e enum) type</b>'.
* '<b>typedef</b>' is similar to typedef in C. The 'typedef' is used to create the 'user-defined datatype'
```verilog
typedef logic [31:0] new_bus; // create a new data type 'new_bus' of size 32
new_bus data_bus, address_bus; // two variables of new data type 'new_bus'
```
* '<b>enum</b>' defines the 'abstract variable' which can have a specific set of values.
* If the type is not defined in 'enum' then the type will be set as 'integer' by default, which may use extra memory unnecessarily.
```verilog
// default type is integer i.e. new_word1 will have the size of 32 bit
enum {one, two, three} num_word1; // variable num_word1 can have only three types of values
num_word1 = one; // assign one to num_word1
// size of new_word2 is 2 bits
enum logic[1:0] {seven, eight, nine} new_word2
new_word2 = seven
```

## Continuous Assignments
* Wire can be driven in <font color="red">Continuous assignments model combinational logic.</font>
* Each time the expression changes on the right-hand side, the right-hand side is reevaluated, and the result is assigned to the net on the left-hand side.
![[Pasted image 20240827123740.png]]
* A continuous assignment drives a value into a net.
* Net data types connect structural components together.
* <font color="red">Continuous assignments model combinational logic.</font>
	* Each time the expression changes on the RHS, the RHS is re-evaluated, and the result is assigned to the net on the LHS.
* Continuous assignments provide models for combinational logic at a higher level of abstraction than at the *Gate-Level* logic.

## Procedural Assignments
* The procedural assignments can be used only within the structured procedures (<font color="red">always, initial, task, function</font>).
* Procedural assignment updates values of *reg, real, integer or time* variable.
* The left-hand side of an assignment should be one of the following:
	* Register
	* Bit-select of register
	* Part-select of <b>reg</b>, <b>integer</b>, or <b>time</b> data type
	* Memory word.
	* Concatenation of any of the above.

## Always Block
* <font color="red">always @ (*)</font> is sensitive to <u>all</u> the RHS statements.
* If anything in the RHS of the always block changes, that particular expression is evaluated and assigned.
* This is similar to assign statement, but this type of block is used to drive a reg datatype.
```verilog
module mux2(c, a, b, s);
output c
input a, b;
input s;
reg c;

always @(a, b, s) // starts evaluation of the LHS when a, b, and c change.
	if (s == 0)
		c =a;
	else
		c = b;

endmodule
```

## System Verilog: more of always
* always, <font color="red">always_comb</font>, <font color="red">always_ff</font>, <font color="red">always_latch</font>
* 'always_comb' - the block should be implemented using 'combinational logic'; and there is <font color="red">no need to define the sensitivity list</font> for this block, as it will be done by the software itself.
```verilog
module alway_comb_ex(input logic  a, b
					 output logic y, z);
	always_comb begin
		if (a > b) begin
			y = 1;
			z = 0;
		end
		else if (a < b) begin
			y = 0;
			z = 1;
		end
		else begin
			y = 1;
			z = 1;
		end
	end
endmodule
```

## always_latch
* Implied latches will be created
* No need in sensitivity list
```verilog
module always_latch_ex(input logic  a, b
					   output logic y, z);
	always_latch begin
		if (a > b) begin
			y = 1;
			z = 0;
		end
		else if (a < b) begin
			// y = 0; // missing output will create latch
			z = 1;
		end
		// else begin // missing 'else' block will create
			// y = 1;
			// z = 1;
		end
	end
endmodule
```

## always_ff
* Sensitivity list is required
```verilog
module always_ff_ex(input logic  clk, reset
					output logic y, z);
	always_ff @(posedge clk, posedge reset) begin
		if (reset) begin
			y <= 0;
			z <= 0;
		end
		else begin
			y <= 1;
			z <= 1;
		end
	end
endmodule
```

## Two types of procedural assignments
* Blocking and non-blocking.
* <font color="red">Blocking assignment</font> gets executed in the order statements are specified.
	* The "<font color="red">=</font>" is the symbol used for blocking assignment representation.
* <font color="red">Non-blocking assignment</font> doesn't not block the execution, and mainly used for concurrent data transfers.
	* The symbol (<=) is used for non-blocking assignment representation.

## Blocking and non-blocking: how it is synthesized (Quartus)
```verilog
module blocking (clk, a, c);
	input clk;
	input a;
	output c;
	wire clk;
	wire a;
	reg c;
	reg b;
	always @(posedge clk) begin
		b = a;
		c = b;
	end
endmodule
```
The resulting synthesization is:
![[Pasted image 20240827132446.png]]
```verilog
module nonblocking(clk, a, c);
	input clk;
	input a;
	output c;
	wire clk;
	wire a;
	reg c;
	reg b;
	always @(posedge clk) begin
		b <= a;
		c <= b;
	end
endmodule
```
The resulting synthesization is:
![[Pasted image 20240827132602.png]]

## Instantiation: connection by name and ordered connection.
* Modules can be instantiated from within other modules.
* When a module is instantiated, connection to the ports of the module must be specified.
* There are <font color="red">two ways to make port connections.</font>
* <font color="red">Connection by name</font>, in which variables connected to each of module inputs or outputs are specified in a set of parenthesis following the name of the ports. The order of connections is not significant.
* The second method is called <font color="red">ordered connection</font>. In this method the order of the ports must match the order appearing in the instantiated module.

## Instantiation, connection by name and order
```verilog
//by name
module top(data, clock, q_out);
input data, clock;
output q_out;
wire net_1;
delt inst_1(.d(data), .q(net_1),.clk(clock));   // As you can see
delt inst_2(.clk(clock), .d(net_1), .q(q_out)); // The order is not important
endmodule

module delt(clk, d, q);
input clk, d;
output reg q;
always @(posedge clk)
	q = d;
endmodule
```

```verilog
//by name
module top(data, clock, q_out);
input data, clock;
output q_out;
wire net_1;
delt inst_1(clock, data, net_1);   // As you can see
delt inst_2(clock, net_1, q_out); // The order is important
endmodule

module delt(clk, d, q);
input clk, d;
output reg q;
always @(posedge clk)
	q = d;
endmodule
```

## Not connected ports
![[Pasted image 20240827133707.png]]