SKILL ASSIGNMENT-2

PROGRAM:
Write an assembly language program in 8051 to generate a 10 ms delay using Timer 1 in Mode 1 and toggle an LED connected to Port 1.0 continuously.

APPARATUS REQUIRED:

LAPTOP WITH KEIL SOFTWARE

PROGRAM:
```
ORG 0000H

MAIN:	
    MOV TMOD, #10H        ; Set Timer1 in Mode1 (16-bit timer)
    CLR P1.0              ; Initialize LED to OFF

HERE:	
    ACALL DELAY_10MS      ; Call delay subroutine
    CPL P1.0              ; Toggle LED (Complement bit P1.0)
    SJMP HERE             ; Repeat forever

;----------------------------------------------------------
; Subroutine: DELAY_10MS
; Generates approximately 10 ms delay using Timer1
;----------------------------------------------------------
DELAY_10MS:
    MOV TH1, #0xDC        ; Load high byte
    MOV TL1, #0x00        ; Load low byte (for 10 ms @ 11.0592 MHz)
    SETB TR1              ; Start Timer1

WAIT1:	
    JNB TF1, WAIT1        ; Wait for Timer1 overflow flag
    CLR TR1               ; Stop Timer1
    CLR TF1               ; Clear overflow flag
    RET                   ; Return to main program

END
```
OUTPUT:
![WhatsApp Image 2025-10-28 at 20 38 33_cdbb3606](https://github.com/user-attachments/assets/a5522758-7c12-4a56-ad5c-88a8c0591854)

![WhatsApp Image 2025-10-28 at 20 39 11_8e03bb05](https://github.com/user-attachments/assets/aeb2d057-2bcb-4c3a-a0db-00857b460630)

![WhatsApp Image 2025-10-28 at 20 39 43_60bb5ffa](https://github.com/user-attachments/assets/2d3347f4-d385-462f-9d7a-119df55f17f4)






RESULT:
Thus the assembly language program in 8051 to generate a 50 ms delay using Timer 0 in Mode 2 (8-bit auto-reload mode) and blink an LED connected to Port 3.0 is successfully completed.
