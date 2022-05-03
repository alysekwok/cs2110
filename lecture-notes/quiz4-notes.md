# lecture content for quiz 4

## C programming
**loops**
- while
- do while
- for

**conditionals**
- if/else
- switch

**compilation:** C source and header files -> preprocessed code -> compiled code -> binary code -> linked executable

**header files:** contain function declarations and global variables to be shared between several source files -- keeps all the global data in one file. 

**preprocessed code:** C processor performs text-level substitution in C source files and header files before they reach the compiler. handles four major tasks:
- #include (file inclusion i.e. header files)
- conditional compilation
- #define (macro expansion)
- code line identification

## memory regions in C
**stack**
- what we used with the LC-3 calling convention
- where local variables to a function
