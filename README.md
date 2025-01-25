# VHDL Counter Rollover Bug

This repository demonstrates a common, subtle bug in VHDL counter implementations: incorrect rollover behavior.  The `buggy_counter` entity implements a counter that resets to 0 when it reaches its maximum value.  This might be the intended behavior, or it might not. The solution shows alternative approaches.

## Bug Description

The `buggy_counter` design uses a simple `if-else` structure for incrementing and resetting the counter.  While functional, it is not as robust as it could be. A more flexible and robust implementation would allow a user to change the rollover behavior to suit their needs.

## Solution

The `bugSolution.vhdl` file provides a more robust counter that demonstrates the correct use of modulo operation for seamless rollover handling.

## How to reproduce

1.  Simulate the `bug.vhdl` file to observe the counter's behavior. Observe the behavior at the rollover point (count 15).
2.  Compare that behavior to the correct implementation in `bugSolution.vhdl`
3. Observe how the solution file gracefully handles the rollover situation.
