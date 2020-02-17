# Using radare2 for desassembling the binaries.
# Reading objdump assembly is hard.

# Crash course for radare 

Radare gives more informations like function signature.
Things it helped in:
Giving params some var names for both stack variables and function arguments


After using aaa, for analysis
: aaa
Use afl for getting all the funtions available in the binary
:afl 
and then we can go to any function 
:seek fcn
And to disassembly we use
: pdf


Writing new details when cracking new binaries