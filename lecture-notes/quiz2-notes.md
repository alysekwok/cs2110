# lecture notes for quiz 2

## boolean logic
## digital logic
**decoders**

**multiplexers**

## k-maps
## state machines
### one-hot state machine
- called one-hot because there is always exactly one state bit "hot", or equal to 1, at any given moment
- an action will be taken every clock cycle
- you determine the changing light output based on the current state, NOT the next state
### binary encoded state machine
- called binary-encoded because we have encoded our state bits into a minimal binary representation
- used k-maps to reduce combinational circuitry
## LC-3 data path
### components of the LC-3
**the bus:** 16-bit wire on the datapath that transfers data between components. 
- only one piece of data can be on the bus at a time. 
- to ensure that onely one piece of data is on the bus at a time, there are tri-state buffer gates that allow data to be put on the bus only when the flag is set

**clock cycles:** LC-3 runs on clock cycles to prevent short circuit conflicts

**control signals:** 
- tri-state buffer signals
- register load signals
- MUX signals

**the microcontroller:**

**memory**

**PC**

**ALU**

**register file**
tracing instructions

