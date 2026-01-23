
Moore: Inputs change the state, state determines output
Mealy: Input determines state, input and state determine output


Designing a FSM:

EG a 1 cycle strobe
Lets keep it simple

![[Pasted image 20250904133955.png|300]]

If in is always high, it would be a half frequency clock.
We make a table

| S        | in  | NS       |
| -------- | --- | -------- |
| S IDLE   | 0   | S IDLE   |
|          | 1   | S STROBE |
| S Strobe | 0   | S IDLE   |
|          | 1   | S IDLE   |

Then we make state encodings to represent the state:
IDLE = 1'b0
Strobe = 1'b1

Then we make our output logic
assign strobe == SSTROBE

If we weren't in a Moore machine, then we would also have inputs in the table.


There is idiomatic verilog with magic pixie dust.

enum logic [bitwidth]{SIDLE,SSTROBE} cur_state, next_state;

an enum is a special variable that makes the state encoding only possible for those values.

Then we make the state logic:
``` verilog
always_ff@(posedge clk, reset)
	if(reset) currentstate <= SIDLE;
	else currentstate <= nextstate

// nextstate logic
always_comb
	case(cur_state)
		SIDLE: nextstate = in ? SSTROBE : SIDLE
		SSTROBE: nextstate = SIDLE
		
assign out = cur_state == SSTROBE
```



