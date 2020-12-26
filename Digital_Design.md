## Univ Gates: NAND and NOR
2 NAND GATES for AND 

3 NAND GATES for OR

Inputs : A and 1  NAND Output: A'

Inputs : A and 0  NOR  Output: A'

---
## Combinational circuits
### Decoder
- n x 2 pow n 

### Encoder
- 2 pow n x n
- Priority Encoder (Takes the highest significant bit )
- Valid bit

### Multiplexer 
- INPUTS: 2 power n 
- SELECTION : n 
- OUTPUT: 1 
- Selection lines selects which input is output

### Demux 
Opposite to mux

---
## Sequential circuits
- Outputs depend on present input
- Latch - no clock
- Flipflop - SR , D , JK , T
- NOR SR latch and Flipflop SR similar Truth table
- Edge and level trigger

### Registers 
- Usually D flipflops
- Shift Registers : SISO , PISO, SIPO, PIPO
- PISO alone - has F which decides load or previous input

### Counters
- Asynchronous
- Synchronous
- Preset and Clear - 
- Steps: 
  - Truth table for the Flipflop
  - Excitation Table 
  - State diagram
  - Truth table and KMap plus circuit
