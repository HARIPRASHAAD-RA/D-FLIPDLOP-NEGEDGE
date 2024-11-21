[# D-FLIPDLOP-NEGEDGE

# AIM:

To implement  D flipflop using verilog and validating their functionality using their functional tables

# SOFTWARE REQUIRED:

Quartus prime

# THEORY:

# D Flip-Flop:

D flip-flop operates with only positive clock transitions or negative clock transitions. Whereas, D latch operates with enable signal. That means, the output of D flip-flop is insensitive to the changes in the input, D except for active transition of the clock signal. The circuit diagram of D flip-flop is shown in the following figure.

![image](https://github.com/naavaneetha/D-FLIPDLOP-NEGEDGE/assets/154305477/48c81fe8-bc3f-40e7-95e2-519fc155ad51)

This circuit has single input D and two outputs Qtt & Qtt’. The operation of D flip-flop is similar to D Latch. But, this flip-flop affects the outputs only when positive transition of the clock signal is applied instead of active enable. The following table shows the state table of D flip-flop.

![image](https://github.com/naavaneetha/D-FLIPDLOP-NEGEDGE/assets/154305477/e5f3fda7-68ec-4a3a-a0a4-cf6f9cc4ab55)

Therefore, D flip-flop always Hold the information, which is available on data input, D of earlier positive transition of clock signal. From the above state table, we can directly write the next state equation as Qt+1t+1 = D

![image](https://github.com/naavaneetha/D-FLIPDLOP-NEGEDGE/assets/154305477/8592c0d8-2917-4142-91b9-d6c30dd891d2)

Next state of D flip-flop is always equal to data input, D for every positive transition of the clock signal. Hence, D flip-flops can be used in registers, shift registers and some of the counters.

# Procedure:
1. Define Module: Define a Verilog module for the D flip-flop with inputs (D, CLK) and outputs (Q, Q_bar).

2. Declare Inputs and Outputs: Declare input and output ports for the module.

3. Implement Flip-Flop Logic: Write Verilog code to implement the D flip-flop logic based on its functional table. Use a synchronous always @(posedge CLK) block to trigger the flip-flop on the positive edge of the clock signal.

4. Simulate Using Testbench: Write a Verilog testbench to simulate the behavior of the D flip-flop under different input conditions.

5. Apply Input Stimuli: In the testbench, apply various combinations of input stimuli (D, CLK) to cover all possible input states.

6. Verify Output Behavior: Verify that the output behavior of the D flip-flop matches the expected behavior defined by its functional table.

7. Check for Race Conditions: Ensure that there are no race conditions or undefined states in the design by analyzing the timing and sequence of input changes.

# PROGRAM:
```
Program for flipflops and verify its truth table in quartus using Verilog programming.
Developed by: HARIPRASHAAD RA
RegisterNumber: 212223040060
```
```
module Exp_08(D,clock,reset,Q);
input D,clock,reset;
output reg Q;
always @(negedge clock)
if(!reset)
	Q <= 0;
else
	Q <= D;
endmodule
```

# RTL LOGIC FOR FLIPFLOPS:

![327637340-9455081e-744a-4e51-88d8-344411dd2c75](https://github.com/amirthaviswanathan05/D-FLIPDLOP-NEGEDGE/assets/149035397/bf123208-45d5-4d3a-9e52-19d1285d259f)

# TIMING DIGRAMS FOR FLIP FLOPS:
![327637404-2a4e3fca-f6ce-49cf-a034-73760fa301b1](https://github.com/amirthaviswanathan05/D-FLIPDLOP-NEGEDGE/assets/149035397/37b16271-88e7-472f-90b9-f8a9175b5e58)


# RESULTS:
Thus the program to implement a D flipflop using verilog and validating their functionality using their functional tables.
](https://github.com/HARIPRASHAAD-RA/JKFLIPFLOP-USING-IF-ELSE/blob/main/README.md)
