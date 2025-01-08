# Segmentation Fault in Assembly due to Incorrect Pointer Arithmetic

This repository demonstrates a common assembly language error: accessing memory outside the program's allocated space.  The error results from an incorrect calculation of a memory address using pointer arithmetic.

## Bug Description
The `bug.asm` file contains an assembly instruction that uses `ebx`, `esi`, and an offset to calculate a memory address.  Under certain conditions, this calculation produces an address outside the valid memory range, leading to a segmentation fault (or access violation) when the program attempts to read or write to that address.

## Solution
The `bugSolution.asm` file provides a corrected version of the code.  The solution involves careful checks to ensure the calculated address falls within the program's allowed memory boundaries before accessing it.  Error handling mechanisms might also be implemented to gracefully handle invalid addresses.