#Setting up qemu in user mode

In qemu kernel mode, the whole hw+kernel+sw is emulated.
In qemu user mode, only sw is emulated, the kernel will be native and will process the syscalls

Basically, it will be fast.

apt install qemu-user


#Cross Compiling ARM binary on my x86_64 CPU
Need gcc-arm-linux-gnueabihf package

apt install gcc-arm-linux-gnueabihf

making a file hello.c
Compiling...

arm-linux-gnueabihf-gcc hello.c -o helloArmStaticBinary -static

statically linked binary just add the library code to the binary,
it does not dynamically link the libraries
Dynamic binary size << Static binary size


#for study purpose, we are making both static and dynamic binaries

For static binary, there is no need of loader, so easy to execute the instructions

#Everything that we need for dynamic linked binaries

We can think of making soft links for the required ELF interpretor, but we have to do it for all the required libraries

Or

We can tell qemu where to look

... qemu-arm -L /usr/arm-linux-gnueabihf binary

Now the arm toolchain contains only basic libraries
What if we want some abstract library

Checking for dynamic libraries
... ldd binary

#Most Basic programs can be run including these libraries.

