
When bringing up a new $\mu C$, we need to get some hardware right.

## Hardware checklist
- Power supply, decoupling capacitance
- Clock or crystal connections
- Programmer interface
- External memory?

## Software checklist
* Where is memory?
* How to turn on the clock
	* have to boot before any commands will be executed
* Architecture considerations? (Probably none)
* How to turn on an LED (blinky).


There are usually loads of resources,
Lectures

Reference manuals: Peripherals and special function registers (i.e. connected to external pins to drive GPIO)

Datasheets: Block diagram, pins, electrical information

Programmers manuals: Architecture, Instruction set, Memory Map


c:
Volatile - can change, don't use cached value
const - read only
static - in a function, doesn't depend on the instance - any time its called, it will update for every other call.
extern - global
void - no return type



## C syntax

``` c

char * str = (char * ) 0x200000100;
str[13] = "a";

```


