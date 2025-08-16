
We have multiple ways of interfacing with chips to handle peripherals, but most of them are based off of the same ARM core.

I.e, take the arduino nano (a super cheap microprocessor) that has a DAC (digital to analog) and ADC (analog to digital) + I2C and SPI and GPIO pins.

We interface with the core via a bus, i.e. a 32 bit bus. Typically it goes through a matrix

![[Pasted image 20250429132802.png]]
