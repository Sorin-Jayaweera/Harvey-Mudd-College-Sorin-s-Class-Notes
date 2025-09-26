
## Simple Combinational  logic
We usually use logic with
logic out, in;
assign out = ~ in; 

 The logic keyword can have *4* states - 0,1, X, Z.
 X means "don't know" - curse these whenever you see them, and check reset states
 Z means high impedance. 

### Operators
There is an or reduction operator - if any bits in a would be written as
|a;

We also have a ternary operator
assign out = s ? in1 : in2;
This is useful, because it is an idiom that describes a multiplexer - if else could be something different. 


## Complicated Combinational Logic
always_comb for complicated combinational logic.

The following block would not make a multiplexer, but would make a latch:
always_com begin
	if(s) out = in1;
end

Why? We don't specify what to do if s is false.



![[Pasted image 20250828135931.png]]

## Sequential Logic
We have memory. Don't forget to put a reset to put things into a known state.

We make sequential logic with
register, latches (dlatch, srlatch), flops (dff, jkflops, toggle flops, ...)

We usually only care about D latch, Dff, and sometimes SR latches.

SR latch:
![[Pasted image 20250828140854.png]]


D latch:
We switch between opaque and transparent states - transparent being writable.
![[Pasted image 20250828141127.png]]

Enable makes sure that it holds - S and R are 0 0 if enable is off.
If enable is on, then its either set (1) or reset(0). 

We could write a flop with
logic Q,D
always_ff@(posedge clk) begin
	Q <= D;
end

or extend it to be a register with
logic [3:0] Q,D
always_ff@(posedge clk) begin
	Q <= D;
end


### Implimenting a slowed clock
do a register that adds 1 each clock cycle,  




### Implimenting a flop
System verilog:
module dff(input logic d, input logic clk, output logic q);

always_ff@(posedge clk)
	D<= Q
endmodule

## Test Benches
Three parts:
Stimulus, Device Under Test, and a Check.

### Stimulus
initial block
din = 1'b1
dclock = 1'b1
clk = 1'b1
...
$finish

### DUT
In the middle of the stimulus,
instance 

dff dut( .d(din), .clk(clk), .out(out));
### Check
assert(out = 1'b1) else $error("Message")

The overall testbench for the dff.sv above:
dff_tb.sv
___________
module dff_tb;
	logic d,q,clk;
	dff dut(...);
	initial 
	{d,clk}= 2'b10;
	assert(out = 1'b1) $finish
end
	
	


