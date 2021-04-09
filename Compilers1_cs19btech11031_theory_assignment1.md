# Name-B AMOGH
# ROLL NO. - CS19BTECH11031
# Mini-Assignment#1: Compilers and their Options
             A formal definition for LLVM is that it is a collection of compiler and toolchain technologies(toolchain can be considered as a chain of multiple steps). GCC is an optimising compiler whose functionality is the same as that of LLVM, but the two are different in their own unique ways. LLVM has a modular architecture. It is divided into 3 parts: Front-end, LLVM optimiser(the middle part), back-end. On a high level LLVM does the following. It converts any program(for example .c file) to .ll file(.ll file is also the LLVM IR file) which is then converted to .asm files(assembly code). Whereas GCC can be compared to that of a huge blackbox (most of the time you do not know what happens in that black box).

## Various options in common compilers: GCC and LLVM. 
              There are various options available in both these compilers. A number of programming languages are supported by GCC. Currently not every language is supported by LLVM. GCC is considered to be more mature than LLVM. However in terms of performance LLVM is considerably better than GCC. Both have different forms of licensing based on their terms and conditions. The most important part of LLVM’s toolchain is the LLVM IR(intermediate representation). LLVM IR is generic, it is not specific to any architecture. LLVM IR optimises the code by removing redundancies (using techniques such as constant folding , function inlining,etc). GCC does not have these features. GCC has its own optimisations .

## Various front ends that GCC, LLVM support
               GCC compiler has frontends for languages such as C(gcc), C++(g++),Objective C, ADA(GNAT), FORTRAN, D, Go. There are other frontends for other languages but are not part of the main distribution of GCC. ADA, C, C++, D, Delphi, Haskell, Objective C, Haskell, Julia, Fortran, Swift, Rust are the languages supported by LLVM  front ends. Clang also is frontend in LLVM that supports C, C++, Objective-C. 

## Various back ends that GCC, LLVM support
               GCC and LLVM support various types of backends such as x86, ARM and many more. I cross compiled my program so the executables I got can be executed on x86, ARM32, ARM64 bit processors. My program calculates the factorial of a number and prints it on the console. I then calculated the size of each of the executable file(i.e x86, ARM32, ARM64 executables): here are the sizes of these files:
x86 executable size = 8.6 kB (8,560 bytes)
32 bit ARM executable size =8.1 kB (8,068 bytes)
64 bit ARM executable size =9.1 kB (9,120 bytes)
NOTE: I also used clang on x86 architecture where I got the size of the executable file to be 8.2 kB (8,224 bytes).
Size depends on various factors, it varies from architecture to architecture.

## Optimization levels of compilers
We use the -o commands to perform optimisation, There are various optimisation commands such as O0, O1, O2, O3,  Os, Oz, etc. While compiling my program(where I print out the factorial of a number) I applied these commands and then calculated the time for each compilation. Here are my results. 

### GCC compilation:
-O0    real    0m0.003s

-O1    real    0m0.003s

-O2    real    0m0.002s

-O3   real    0m0.002s

-Os   real    0m0.002s

-Oz   real    0m0.003s

### CLANG compilation:
-O0  real    0m0.001s

-O1    real    0m0.002s

-O2   real    0m0.002s

-O3   real    0m0.002s

-Os   real    0m0.002s

-Oz   real    0m0.002s

## Note: here the difference in time is very less since we used a basic factorial program. But in  general If we go for large code bases and compile them by applying these commands we will surely observe the difference.




