## Basic
Manually writing everything:

module 7seg_tb;
	logic [3:0] s;
	logic [6:0] seg;
7seg dut(s,seg)

initial begin
	s = 4'b0000; #1; assert(seg == 0000001) else $error("fail message")
	...
	...
	$finish
end

Note: You can use for loops in testbenches.

## Advanced
There should be a stimulus module, a DUT module, and a check module. Nothing from stimulus goes to check. 

UVM (rough "language" for verification)
LEC (compare with a perfect system)
formal proofs


## Keypad
tranif1 principle

We have primitive gates, such as and a1(z,x,y,...)

tranif1 t1(left, right, control). If the control value is one, left and right are connected. This can be used to look at the keypad. 




## Coverage



## Modularity

## Stimulation / assert

## Advanced

## Tricky Inputs
