# Clock Period
# Cycle (register transfer)
- Read from the register occurs at the beginning of the cycle
- Write takes place at the end of the cycle meaning the beginning of the next cycle.
- Shortly after the edge, the updated value is available for reading in the next cycle.
- $R[3]\leftarrow R[1]+R[2]$
![[Clock_Cycle.png]]

- Combine all delays associated with buffers, bus propagation and combinational logic (maximum among all transfers) into one CL delay, which will indicate the longest propagation delay through the datapath.

- Same registers can be on the both ends
	- Example: R1=R1+R2
# Calculation of Clock Period
- Depends on the **maximum**T delay from register R1 to R2
- The input to register R2 must be stable at least $t_{setup}$ before clock edge

**Clock to Q delay: $t_{pcq}$** = time after clock edge that the output $Q$ is guaranteed to be stable (i.e., to stop changing)
**Critical (Long) Path through CL is** the propagation delay $t_{pd}$

**Clock cycle** $T_c\ge t_{pcq}+t_{pd}+t_{setup}$

if clock is set, then your design of the datapath, that is propagation delay through the combinational logic (datapath) must meet the condition

$t_{pd}\le T_c-(t_{pcq}+t_{setup})$

![[calc_of_clock.png]]

# Practical aspect: Clock skew
- If Clock arrives to different registers at different times (due to the travel distance difference), then the **Clock Skew** is to be taken into account
- **Clock Skew is the arrival time** difference between two clock edges.
- Conditions change the following:
	- $T_c\ge t_{pcq}+t_{pd}+t_{setup}+t_{skew}$
	- $t_{pd}\le T_c-(t_{pcq}+t_{setup}+t_{skew})$
![[clk.png]]

# Hold Time Constraint
- Depends on the **minimum** delay from register R1 through the combinational logic to R2
- The input to register R2 must be stable for at least $t_{hold}$ after the clock edge.

$t_{ccq}+t_{cd}>t_{hold}$
$t_{cd}>t_{hold}-t_{ccq}$

**Contamination delay for Q1**: $t_{ccq}$ is the time after clock edge when Q might be unstable (i.e., start changing)
The CL delay, $t_{cd}$, is the minimum time from when an input to CL changes until the output starts to change its value

$t_{ccq}+t_{cd}>t_{hold}+t_{skew}$
$t_{cd}>t_{hold}+t_{skew}-t_{ccq}$