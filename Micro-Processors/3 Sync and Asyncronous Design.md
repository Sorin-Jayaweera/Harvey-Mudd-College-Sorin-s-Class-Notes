If we only have one resource, we use time multiplexers to select what processes are using that resource at any given time.
![[Pasted image 20250902134647.png]]

we are limited by current to supply from the FPGA, so we use PNP transistors
![[Pasted image 20250902134616.png]]

## Fancy flip flops
design a flip flop with a reset with a schematic and verilog.

![[Pasted image 20250902140015.png]]
![[Pasted image 20250902140048.png]]



How would we make an asynchronous reset?

Lets start with how latches really look:
![[Pasted image 20250902141420.png]]

We can change this to include the reset for the state and the immediate output
![[Pasted image 20250902141519.png]]

To do this is only a 1 word change in verilog.
Change
	always@(posedge clk)
to be
	always@(posedge clk, reset)


What if we don't want to update a flop?

We'll use an enable.

![[Pasted image 20250902142506.png]]

always_ff@(posedge clk,reset) begin
	if(reset) q <= 1'b0
	 else if(enable) q<= d;
	 else(q)<=q; 

end

or, more idiomatically
else:
 q<= enable? d,q;

What is not synchronous?
- user inputs
- clock skew
- divided clocks/ subsampling (propagation delays)
- plesiochrony (different clocks, i.e. two chips that are separate)
- 