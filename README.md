Arithmetic-operation-using-8086
8086 Assembly Language Programs for Arithmetic Operations
AIM
To write and execute Assembly Language Programs to perform arithmetic operations for the 8086 microprocessor.

APPARATUS REQUIRED
Personal Computer with MASM Software
1. ADDITION
Algorithm
Initialize memory location in HL register.
Store 1st data.
Increment HL to enter 2nd data.
Move 2nd number to accumulator.
Decrement HL.
Add value in memory with accumulator.
Store result.
Stop.
FLOW CHART
image
Program
CODE SEGMENT
ASSUME CS:CODE, DS:CODE
ORG 1000H
MOV CL,00H
MOV AX,1234H
MOV BX,1234H
ADD AX,BX
JNC L1
INC CL
L1:MOV SI,1200H
MOV [SI],AX
MOV [SI+2],CL
MOV AH,4CH
INT 21H
CODE ENDS
END
Output Table
MEMORY LOCATION (INPUT)	MEMORY LOCATION (OUTPUT)
1200🔢 01 12	
| 1200 |

Manual Calculations
2+6=8
OUTPUT IMAGE FROM MASM SOFTWARE
Screenshot 2026-10-15 103322(1)
2. SUBTRACTION
Algorithm
Initialize memory and store 1st data.
Increment to get 2nd data.
Move 2nd data to accumulator.
Subtract memory content.
Store result.
FLOWCHART
image
Program
CODE SEGMENT
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV SI,2000H
MOV CL,00H
MOV AX,[SI]
MOV BX,[SI+02H]
SUB AX,BX
JNC L1
INC CL
L1:
MOV [SI+04H],AX
MOV [SI+06H],CL
MOV AH,4CH
INT 21H
CODE ENDS
END
Output Table
MEMORY LOCATION (INPUT)	MEMORY LOCATION (OUTPUT)
Manual Calculations
6-2=4
OUTPUT SCREEN FROM MASM SOFTWARE
Screenshot 2026-10-15 103953(1)
3. MULTIPLICATION
Algorithm
Initialize memory and store operands.
Move operands to registers.
Multiply.
Store result.
##FLOWCHART

image
Program
CODE SEGMENT
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV SI,2000H
MOV DX,0000H
MOV AX,[SI]
MOV BX,[SI+02H]
MUL BX
MOV [SI+04H],AX
MOV [SI+06H],DX
MOV AH,4CH
INT 21H
CODE ENDS
END
Output Table
MEMORY LOCATION (INPUT)	MEMORY LOCATION (OUTPUT)
Manual Calculations
2*6=12
OUTPUT SCREEN FROM MASM SOFTWARE
Screenshot 2026-10-15 104611(1)
4. DIVISION
Algorithm
Load memory location of operands.

Perform division.

Store result.

FLOWCHART
image
Program
CODE SEGMENT
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV SI,2000H
MOV DX,0000H
MOV AX,[SI]
MOV BX,[SI+02H]
DIV BX
MOV [SI+04H],AX
MOV [SI+06H],DX
MOV AH,4CH
INT 21H
CODE ENDS
END
Output Table
MEMORY LOCATION (INPUT)	MEMORY LOCATION (OUTPUT)
Manual Calculations
6/2=3
OUTPUT FROM MASM SOFTWARE
Screenshot 2026-10-15 104900(1)
RESULT
Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.
