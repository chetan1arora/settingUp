#Approach
Writing some basic C functions to recognise the patterns in assembly
Using objdump for simple codes, later we will go for radare,etc.

Using 32 bit architecture for compilation
#objdump shows whole source how to find main

objdump ... | grep main get address

then
objdump ... --start-address=ADDR




1. Loops 
Normal pattern, not even inc and dec are used
compiler changes value such that i<5 changes to i<=4.


