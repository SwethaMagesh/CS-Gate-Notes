## Univ Gates: NAND and NOR
2 NAND GATES for AND 

3 NAND GATES for OR

Inputs : A and 1  NAND Output: A'

Inputs : A and 0  NOR  Output: A'

---
## Combinational circuits!
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
- Flipflop is also called as Bistable Multivibrator since it has two stable states either 0 or 1.
- NOR SR latch and Flipflop SR similar Truth table
- Edge and level trigger

### Registers 
- Usually D flipflops
- Shift Registers : SISO , PISO, SIPO, PIPO
- PISO alone - has F which decides load or previous input

### Counters
- Asynchronous - no univ clock == prev output as clock     
- Synchronous
- Decade counter, Up counter, down counter
- The one advantage of synchronous counter over asynchronous counter is, it can operate on higher frequency than asynchronous counter as it does not have cumulative delay because of same clock is given to each flip flop.
- Preset and Clear - 
    - Asynchronous inputs on a flip-flop have control over the outputs (Q and not-Q) regardless of clock input status.
    - These inputs are called the preset (PRE) and clear (CLR). The preset input drives the flip-flop to a set state while the clear input drives it to a reset state.
    - It is possible to drive the outputs of a J-K flip-flop to an invalid condition using the asynchronous inputs, because all feedback within the multivibrator circuit is overridden.
- Steps: 
  - Truth table for the Flipflop
  - Excitation Table 
  - State diagram
  - Truth table and KMap plus circuit

