CMSIS: Hardware abstraction layer

If you want to use interrupts

< x >_IRIQHANDLER is automatically handled as an interrupt


```
main:
stuff

EXTIO_IRQHANDLER
	if (GPIOA->OPR)
		capture TIM16-> CNT
	else
		dT = TIM16->CNT - captured
```

