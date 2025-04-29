# LogisimALU
Wow look at all this documentation about the ALU.


INPUT PINS
A0-A7 Used for the 1st 8-bit binary number.
B0-B7 Used for the 2nd 8-bit binary number.
S0-S3 Used to select the output from the ALU.
SUB Used to select if you want to add or subtract.
CLOCK Used as the clock for the ALU.

OUTPUT PINS
Z0-Z7 Used to output the result from the ALU as a 8-bit binary number.
COUT - Used to idicate if the ALU has had an overflow of output bits

VALID INPUTS FOR ALU SELECTION ON S0-S3 PINS
000 = NOT
010 = AND
100 = OR
110 = XOR
001 = ADD/SUBTRACT
011 = MULTIPLY
101 = DIVIDE

VALID INPUTS FOR ADD/SUBTRACT SELECTION ON SUB PIN
0 = ADD
1 = SUBTRACT


NOT
Takes 1 8-bit binary number from pins A0-A7 and outputs the NOT of it on pins Z0-Z7

AND
Takes 2 8-bit binary numbers from pins A0-A7 and B0-B7 and ouputs the AND of the 2 numbers on pins Z0-Z7 


DIVIDE
Takes 1 8-bit binary number from pins A0-A7 and 1 4-bit binary number  from pins B0-B3 and outputs the division of the 2 numbers on pins Z0-Z3 for result and pins Z4-Z7 for remainder.
