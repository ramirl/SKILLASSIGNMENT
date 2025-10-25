SKILL ASSIGNMENT-1

PROGRAM:

Write an assembly language program in 8051 to find the factorial of a given  number and store the result in memory.

APPARATUS REQUIRED:

LAPTOP WITH KEIL SOFTWARE

PROGRAM:
```
ORG 0000H

MOV A, #01H    
MOV R1, #05H   

FACT_LOOP:
    MOV B, R1
    MUL AB      
    DJNZ R1, FACT_LOOP
MOV 30H, A      
MOV 31H, B
END
```
OUTPUT:

![WhatsApp Image 2025-10-25 at 08 59 46_a743e8a6](https://github.com/user-attachments/assets/ab69f471-1946-4eb4-9523-2f3cf9ac73f5)

RESULT:

THUS THE PROGRAM TO FIND THE FACTORIAL OF THE GIVEN NUMBER IS EXECUTED.
