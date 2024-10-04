# Static RAM cell (6-transistor): Operation
- Transistors arrangement gives stable logic state
- State 1
	- $C_1$ high, $C_2$ low
	- $T_1$ $T_4$ off, $T_2$ $T_3$ on
- State 0
	- $C_2$ high, $C_1$ low
	- $T_2$ $T_3$ off, $T_1$ $T_4$ on
- Address line transistors $T_5$ $T_6$ are switches
- Write: Apply value to B & complement to B
- Read: value is on line B
![[Transistors Static RAM.png]]
# Demux (aka 1-to-8 decoder)
- Need DEMUX to write to a specific column and MUX to read from a specific column in a tiled design of a chip
- Data input is given to a selected output (selection bits S0 and S1)
![[Demux black box.png]]
![[DMUX.png]]