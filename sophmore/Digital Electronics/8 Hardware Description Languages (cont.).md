
## Verilog

### Delays

We have a unit of 'ticks', which we can have delayed logic through the circuit.
We can do, for example
assign #1 {ab,bb,cb} = ~{a,b,c}; will assign the result after one tick instead of immediatly. 

### Sequential Logic
We could have synchronous reset:
![[Pasted image 20250213132617.png|300]]

or asynchronous reset:
![[Pasted image 20250213132600.png|300]]

We could enable a value to be passed:
![[Pasted image 20250213132933.png|300]]

or have a value that changes any time  that the clock is high.
![[Pasted image 20250213132958.png|300]]

We have a nice structure always_comb where any time any of the inputs change, it will reevaluate:
![[Pasted image 20250213133239.png|300]]
We have a great example:
![[Pasted image 20250213133623.png|300]]

We can also ignore some parts of our input:
![[Pasted image 20250213133748.png|300]]

### Blocking and Nonblocking

In sequential logic areas, <= is a non blocking assignment. These happen at the same time. If we care about a value from the previous input, then we would make it blocking, by assigning with the sign =.

However, what if we wrote something like:

always_comb begin
	a<=b&c;
	d<=a&w;
	e<=d|p;
end
If we update b, then a will change. The others will evaluate with the old a. Then, those values will update, and the always_comb will update them. Then the others will change again. This will keep going until we have the answer, but it takes 3 cycles to simulate. We could do this in just one. Using equals, then we wait for each step and update the rest. 

We now have some rules:
Synchronous sequential logic should use always_ff @(posedge clk) and non-blocking assignments, so that our flip-flops will work.

Simple combinational logic should use continuous statements, 
assign y = a&b

More complicated combinational logic, use =.

In an always block, use gets (<=) and you will be safe. 

### FSMs

![[20250213_140549.jpg|600]]

I stopped taking live notes here:

![[20250213_135734.jpg|200]]



### Parameterized Modules
We can make modules that automatically have a parameter as one value, but which can be overwritten.
![[Pasted image 20250213144736.png|300]]
### Test Benches

Big overview notes: Check that the number of bits in your test vector matches the number of bits for your input file, and also set that bit length at the end for terminating the test vector file when it becomes nulls.

Generate the clock signal
![[Pasted image 20250213144819.png]]
Read your testvector file:
![[Pasted image 20250213144833.png]]
Set your input values and the expected outputs
![[Pasted image 20250213144847.png]]
Check your outputs:
![[Pasted image 20250213144904.png]]