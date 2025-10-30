SKILL ASSIGNMENT-1

PROGRAM:
14.Write an assembly language program in 8051 to reverse the elements of an array and store the reversed array in another memory location.

APPARATUS REQUIRED:

LAPTOP WITH KEIL SOFTWARE

PROGRAM:
```
ORG 0000H
	
START:
    MOV R0, #30H       ; Source array start address
    MOV R1, #44H       ; Destination array end address
    MOV R2, #05H       ; Number of elements in array

REVERSE_LOOP:
    MOV A, @R0          ; Get element from source
    MOV @R1, A          ; Store element in reversed location
    INC R0              ; Next source address
    DEC R1              ; Previous destination address
    DJNZ R2, REVERSE_LOOP  ; Repeat for all elements

HERE: SJMP HERE          ; Stop program (infinite loop)

END
```
OUTPUT:

![WhatsApp Image 2025-10-29 at 19 49 57_304441fc](https://github.com/user-attachments/assets/827bae94-d396-4fa3-a622-bbf18c95b0a6)
![WhatsApp Image 2025-10-29 at 19 49 41_7dd902a5](https://github.com/user-attachments/assets/5ba8b854-1a95-42c2-956b-df78fec2caa8)

RESULT:

THUS  reverse the elements of an array and store the reversed array in another memory location.
