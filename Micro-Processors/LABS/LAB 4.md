
## Driving Pin with Frequency
PLL

![[Pasted image 20250927165705.png]]
## Configuring SYS clock frequency

Don't use PLL

## Waiting for note duration:


SysTick Timer (STK) prog manual 4.5

SysTick counts down from value stored in register and then reads the value again and counts down. 

![[Pasted image 20250927155222.png]]


For waiting,

time = 1000ms;
sysclk = 80Mhz.

systic_load = count;
while(STK_VAL != 0){

}