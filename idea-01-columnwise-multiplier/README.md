# Columnwise Popcount Multiplier

## Overview

This idea focuses on a hardware method for multiplying two 16-bit integers without using the usual shift-and-add or tree-based approaches. Instead, it calculates the final result by counting how many basic operations contribute to each output bit.

## Key Points

- For each output bit position, we count how many bit-wise AND operations contribute to that position.
- This count is then used to determine the correct value and carry for each column.
- Only one register is needed to hold A, and partial products are not stored.
- The design is fully combinational and may be suitable for resource-limited systems like microcontrollers or FPGAs.

## Goals

- Reduce hardware resource usage such as registers and adders.
- Provide a simple and fast structure for small to medium-sized multiplication tasks.
- Explore how well this method performs compared to Wallace tree and Booth multipliers.

## Questions

- What is the delay and area compared to existing techniques?
- Can the method be extended to 32-bit or 64-bit multiplication?
- How can we efficiently implement the counting and carry propagation logic?

## Next Steps

- Formalize the logic design on paper.
- Create a Verilog simulation.
- Compare test results with existing multiplier architectures.
