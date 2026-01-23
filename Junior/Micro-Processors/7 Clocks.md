
PLL: Phase Locked Loop

We take a reference clock and compare it with another with an xor. If they aren't aligned, then bursts in their misalignment will come out of the xor. If we use that to drive a controller to generate a clock signal at the pulse frequency, then clock divide and take that output back to the beginning xor thing - then the system will drive the divided clock to be the same frequency. This makes the non divided clock higher frequency then the reference!

![[Pasted image 20250918140054.png]]
Registers for:

PLL
System clock source

![[Pasted image 20250918142014.png]]

Base Address:
Address Offset: 0x0C
PLLON: 24
PLLRDY: 25
PLLPEN: 16 main pll48m1clk
PLLQEN: 20 main pllsaiclk
PLLREN: 24 main PLLclk 