# FIR Filter Architecture Comparison on FPGA (Vivado)

This project implements and compares three FIR filter architectures:

- Direct Form
- Symmetric Form
- Transposed Form

Implemented in Verilog and synthesized on Xilinx FPGA using Vivado 2022.2.

## Architectures Compared

✔ Direct Form FIR  
✔ Symmetric FIR (multiplier optimized)  
✔ Transposed FIR (high speed pipelined)

## Metrics Analyzed

- Maximum Frequency (Fmax)
- Worst Negative Slack (WNS)
- LUT utilization
- Flip-Flop utilization
- DSP block usage
- Power consumption

## Tools Used

- Xilinx Vivado 2022.2
- Verilog HDL
- MATLAB (for coefficient generation)

## Key Results

| Architecture | Fmax (MHz) | LUTs | FFs | DSPs | Power (mW) |
|-------------|-----------|------|-----|------|-----------|
| Direct | 20.2 | 9 | 513 | 32 | 92 |
| Symmetric | 42.56 | 9 | 336 | 16 | 95 |
| Transposed | 92.47 | 9 | 17 | 32 | 139 |

## Conclusion

- Transposed form achieves highest speed
- Symmetric form minimizes DSP usage
- Direct form has lowest power consumption

This demonstrates architectural tradeoffs in FPGA DSP design.
