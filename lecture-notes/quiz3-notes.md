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
