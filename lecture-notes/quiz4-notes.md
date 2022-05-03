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
- variables stored here will only last the lifetime of a function call
**heap**
- where dynamically allocated memory will be
- live longer than the lifetime of a function call
**data**
- where global variables and static variables will be stored
**code**
- where executable code gets stored

## type qualifiers and storage class modifiers in C
**static:**
- defined on a function: not visible outside of the C file they are defined in
- defined inside a function on a local variable: variables do not lose their value between function calls, since they are NOT stored on the stack
- defined outside a funciton on a variable: variab;es are not visible outside of the C file they are defined in

**extern:** tells compiler that the variab;e is defined in another file (actual memory location allocated for the varaible is associated with another file)

**auto:** local variables that are always stored on the stack -- all variables are "automatically" declared auto unless explicitly declared otherwise

**const:** variable is constant

## structs
data type in C that contain multiple variables of different types. they are stored in one block in memory that is the struct

example struct:
`
struct myStruct { 
  int num; 
  char* letter; 
};
`

## typedef
keyword that allows you to create a new type that is an alias for an existing one

example: `typedef unsigned char BYTE; `

not BYTE can represent the type unsigned char
