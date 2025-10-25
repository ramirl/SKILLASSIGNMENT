SKILL ASSIGNMENT-2

PROGRAM:
Write an assembly language program in 8051 to generate a 50 ms delay using Timer 0 in Mode 2 (8-bit auto-reload mode) and blink an LED connected to Port 3.0.

APPARATUS REQUIRED:

LAPTOP WITH KEIL SOFTWARE

PROGRAM:
```
ORG 0H         

MOV P3, #00H    

MOV TMOD, #02H  
MOV TH0, #56H
MOV TL0, #56H   

SETB TR0        

MAIN:
    MOV R2, #250   

WAIT_OVERFLOW:
    JNB TF0, $     
    CLR TF0        
    DJNZ R2, WAIT_OVERFLOW 

    CPL P3.0       
    SJMP MAIN      

END
```
OUTPUT:

![WhatsApp Image 2025-10-25 at 10 15 58_a73af6f9](https://github.com/user-attachments/assets/281aeb78-22ae-4d3f-b080-a2a773245796)

![WhatsApp Image 2025-10-25 at 10 16 06_584e37bc](https://github.com/user-attachments/assets/102cd50a-4273-4a3c-bffc-0017e119e718)

RESULT:

THUS THE PROGRAM TO FIND THE FACTORIAL OF THE GIVEN NUMBER IS EXECUTED.
