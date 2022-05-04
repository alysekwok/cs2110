# lecture notes for quiz 3
## execution cycle
**fetch:** we retrieve an instruction from memory and get it into the machine
- since PC holds the address of the next instruction, we should put it in the MAR
- in order to ensure that the PC retains this property, we need to increment it
- one the PC walue is in the MAR we can load the MDR with the memory contents at that address
- not that we have the instruction in the MDR we can put it in the IR and move on to the decode portion

**decode:** once the instruction is in the IR, the FS< takes over and uses the instruction and the logic of the FSM in order to control the datapath and execute the instruction

**execute:** now that the FSM has decoded the instruction, it will assert the signals on the datapath in order to move data around and execute the instruction

## pseudo-ops and memory layout
- .orig: tells the assembler to put this block of code at the desired address (e.x: `.orig x3000` will put a block of code at address x3000)
- .stringz "string here": will put a string of characters in memory followed by NULL (which is a single ASCII character with the value 0
- .blkw n: a pseudo-op that will allocate the next nlocations of memory for a specified label
- .fill value: pseudo-op that will put that value in that memory location
- .end: pseudo-op that denotes the end of an address block. matches with an .orig

## assembly instructions
**BR:** useful for loops and conditionals

**LD:** basic load operation. loads data at a certain memory address into the designated register

**LDR:** load operation that takes the memory address from a register, adds it to an offset, and restrieves the data at the subsequent offset + address memory address, and loads it into the designated register

**LEA:** aka load effective address. will load the memory address into a designated register. useful for printing strings, because you can load the address of the starting character into R0 via LEAS and then call PUTS

**ST:** basic storing operation. stores a particular value at a certain memory address

**STR:** similar to the basic ST but the memory address is calculated by adding a base address to a value located in a register

**NOTE:** LD, LDI, and LDR all do the same thing (as in they find an address in memory and copy the value in that address to a destination register (aka a READ from memory)). they only differ in the way that they calculate the address to read from (LD: PC-relative; LDI: indirect; LDR: base+offset)

in the same respect, all of the storing instructions (ST, STI, STR) take a value from a source register, and copy that valueinto a certain address in memory (aka a WRTIE to memory). they only differ in the way they calculate that address. 

## the stack

### reserved registers

**R7** - holds the current reserve address

**R6** - holds the stack pointer, aka top of the stack
- when more data gets pushed on, R6 gets decremented
- when data gets popped off, R6 gets incremented

**R5** - holds the frame pointer
- 'anchor' of the stack frame -- never changes throughout a function's execution
- basically a constant point that we can always reference (in comparision to the stack pointer, which is constantly moving depending on what is being pushed/popped off the stack)
