# CPU
## Program description
To use this program, you need to write code to a file asm.txt, in this case, the code must be written using a specific syntax:
1) CRT (create) is a command that should be written at the beginning of the program code, it creates a stack for the processor;  
2) IN - command to enter a number from the keyboard (the number is put on the processor stack);  
3) - PUSH 0 - puts the number 0 on the processor stack;  
   - PUSH ax - puts a number from the ax register on the processor stack;  
   - PUSH [1] - puts a number from RAM at address 1 on the processor stack;  
   - PUSH [ax] - puts a number from RAM to the address ax;  
4) ADD - adds two numbers from the processor stack and puts the result back;  
5) SUB - subtraction;  
6) MUL - multiplication;  
7) DIV - division;  
8) OUT - takes an element from the processor stack and displays it on the screen;  
9) HLT is a command that is written at the end of the program, it clears the memory that the processor stack occupied;  
10) POP - command is an analog of PUSH, which takes an element from the processor stack and puts it in a register or RAM;  
11) :label - label;  
12) JMP label - switch to label label;  
13) JA label - switch to label label if the penultimate number in the processor stack is greater than the last one;  
14) JAE label (>=);  
15) JB label (<);  
16) JBE label (<=);  
17) JE label (==);  
18) JNE label (!=);  
19) CALL nameFunction - the command switches to the nameFunction label, and the execution of the function code begins;  
20) RET is a command that is written inside a function that starts with the nameFunction label and returns the execution of the program to the command following the CALL nameFunction command;  
21) SQRT is a square root command that takes the last number from the processor stack and returns the result of the operation in its place;
22) DRAW - command to draw the contents of RAM;  
23) MOVE - movement command (experimental command that needs improvement);  
24) P_CDOT - is a command that displays the character '*';  
25) P_SPACE - a command that displays the symbol ' ';  
26) NEW_LINE - a command that moves the cursor to a new line.  
  
Assembler/main.cpp - a file that converts code from a file asm.txt in binary code and writes it to a file code.txt.  
  
CPU/main.cpp - a file that executes code from a file code.txt and displays the result of the program on the screen.  
  
Disassembler/main.cpp - a file that converts binary code from a code file.txt into the program text and writes it to a file asm.txt (the code of this program is proposed to be written to the reader as a training task).  
## Using the program
You can only call the execution of a file CPU/main.cpp , since programs are called inside this program Assembler/main.cpp and Disassembler/main.cpp using the system() function, which is done for the convenience of the user.  
### Additional information
libs/ is a folder with header files *.h that are used inside programs.  
testPrograms is a folder with examples of programs written using the syntax described above.
