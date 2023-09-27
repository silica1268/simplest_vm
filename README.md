# simplest_vm
A Turing-complete virtual machine with only one instruction. To write a program for this virtual machine, simply change the content of its memory.

The VM is composed of an instruction pointer and an array of addresses, which is its memory. With this VM, every value is an address and an address can be manipulated.

The VM reads 4 consecutive addresses at a time, which are: input 1 value, input 2 value, output address and next instruction pointer address.

At each iteration, the VM will:
1. Read the address at the address in the instruction pointer, which is the first input.
2. Read the address at the address in the instruction pointer + 1, which is the second input.
3. Compute the output by simply adding the 2 input addresses.
4. Write the output to the address in the instruction pointer + 2.
5. Set the instruction pointer to the address at the address in the instruction pointer + 3.

\* This description alone may be confusing to understand. Reading the code might help.

That's it! The VM runs until the program is stopped and theoretically it can emulate any other program.
