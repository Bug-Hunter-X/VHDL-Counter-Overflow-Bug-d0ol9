# VHDL Counter with Overflow Bug

This repository demonstrates a common error in VHDL code: an unchecked counter that overflows.

The `counter.vhdl` file contains a simple counter that increments on each rising edge of the clock. The `counter_fixed.vhdl` file shows the correct implementation.

## Bug Description
The original `counter.vhdl` design does not check for overflow before incrementing the counter. This can lead to unpredictable behavior if the counter reaches its maximum value (15 in this case). The counter simply wraps around to 0.

## Solution
The solution involves adding a check for the maximum counter value before incrementing. If the counter reaches 15, it stops incrementing, preventing the overflow.

## How to Reproduce
1. Compile and simulate both VHDL files (counter.vhdl and counter_fixed.vhdl).
2. Observe the behavior of the counter in both versions when the maximum count is reached.
