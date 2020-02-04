https://maxkersten.nl/binary-analysis-course/assembly-basics/crash-course/
#Crash course in x86 assembly

Common instructions

#Compare Instruction
cmp eax,ebx

cmp var1,var2

flags register is changed

#Jump Instruction

jmp 0x00565

#Move Instruction

mov dest, src

mov dest,[src] // src is a memory address

#Add and Subtract Instruction

add v1, v2 => v1 = v1 + v2

sub v1, v2 => v1 = v1 - v2

#Increment & Decrement operator

inc var
dec var2

#Push and pop instruction

push var or eax

pop ebx // Pop the value into the register

#Call Instruction

For calling a function

All instructions are passed onto stack before calling the function

On x86_64 some initial params are passed using registers(SMaRT)

# Return Instruction

ret is used which changes eip to address

We can also provide param to ret instruction the number of bytes to remove from stack.

# Load Effective address

Used when to do trick calculations 
lea ebx, [eax+ecx+3543] // No register is changed in this addition operation

Now Mov and ebx is different

Above instruction is same as

MOV ebx, eax+ecx+3543 // But we cant do complex calculations like this.

So basically LEA do complex calculations and store the final memory address into ebx.

& We know how much we need pointers in real-life


AND/XOR Bitwise Operations

AND src, dest => src = src&dest
XOR src, dest => src = src^dest

TEST op

test a,b => a&b, then check for flag being set to zero (used before jump)


#Important task, Recognising patterns in Assembly

