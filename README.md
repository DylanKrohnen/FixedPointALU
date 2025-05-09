# Fixed Point ALU
## Setup Instructions
- Install the latest version of Logisim Evolution: https://github.com/logisim-evolution/logisim-evolution
- Download the ALU file: `FixedPointALU.circ`
- Open `FixedPointALU.circ` in Logisim Evolution.

## Operation Codes
- AND = 000
- OR = 010
- XOR = 100
- NOT = 110
- ADD = 001
- SUB = 011
- MUL = 101
- DIV = 111
  
## Pin Diagram
![Image](https://github.com/user-attachments/assets/8bf06ee5-03ee-4c2f-b951-f682424d2907)<br/>
**Input Pins**
- A0-A7 = 1st 8-bit, 2s compliment binary number.
- B0-B7 = 2nd 8-bit, 2s compliment binary number.
- C0-C2 = Control pins to select operation.
  
**Output Pins**
  - Y0-Y7 = ALU result.
  - OVERFLOW = Triggers if an overflow error has occurred.

## ALU Functions
**AND**\
Inputs = A0-A7, B0-B7\
Output = Y0-Y7\
Function = Outputs a value of 1 (true) for Y[i] if both A[i] and B[i] are 1 otherwise it outputs a value of 0 (false).

**OR**\
Inputs = A0-A7, B0-B7\
Output = Y0-Y7\
Function = Outputs a value of 1 (true) for Y[i] if either or both A[i] and B[i] are 1 otherwise it outputs a value of 0 (false).

**XOR**\
Inputs = A0-A7, B0-B7\
Output = Y0-Y7\
Function = Outputs a value of 1 (true) for Y[i] if either A[i] or B[i] are 1 otherwise it outputs a value of 0 (false).

**NOT**\
Input = A0-A7\
Output = Y0-Y7\
Function = Outputs a value of 1 (true) for Y[i] if A[i] is 0 otherwise it outputs a value of 0 (false).

**ADD**\
Inputs = A0-A7, B0-B7\
Outputs = Y0-Y7, OVERFLOW\
Function = Adds together 2 8-bit, 2s compliment, binary numbers and outputs the result as an 8-bit, 2s compliment, binary number. If the result is not between -128 and 127 then the overflow error is triggered and the result is truncated to the first 8 bits.

**SUB**\
Inputs = A0-A7, B0-B7\
Outputs = Y0-Y7, OVERFLOW\
Function = Subtracts 2 8-bit, 2s compliment, binary numbers and outputs the result as an 8-bit, 2s compliment, binary number. If the result is not between -128 and 127 then the overflow error is triggered and the result is truncated to the first 8 bits.

**MUL**\
Inputs = A0-A7, B0-B7\
Outputs = Y0-Y7, OVERFLOW\
Function = Multiplies 2 8-bit, 2s compliment, binary numbers and outputs the result as an 8-bit, 2s compliment, binary number. If the result is not between -128 and 127 then the overflow error is triggered and the result is truncated to the first 8 bits.

**DIV**\
Inputs = A0-A7, B0-B7\
Outputs = Y0-Y7, OVERFLOW\
Function = PLACEHOLDER
