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

## the stack

### reserved registers

**R7** - holds the current reserve address

**R6** - holds the stack pointer, aka top of the stack
- when more data gets pushed on, R6 gets decremented
- when data gets popped off, R6 gets incremented

**R5** - holds the frame pointer
- 'anchor' of the stack frame -- never changes throughout a function's execution
- basically a constant point that we can always reference (in comparision to the stack pointer, which is constantly moving depending on what is being pushed/popped off the stack)
