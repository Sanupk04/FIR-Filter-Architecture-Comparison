FIR Filter Architecture Comparison on FPGA (Vivado)
📌 Project Objective

The objective of this project is to design, implement, and compare three different FIR (Finite Impulse Response) filter architectures on Xilinx FPGA using Verilog HDL and Vivado.

The architectures implemented are:

Direct Form FIR Filter

Symmetric (Folded) FIR Filter

Transposed FIR Filter

The comparison focuses on:

Maximum operating frequency (Fmax)

Worst Negative Slack (WNS)

FPGA resource utilization (LUTs, Flip-Flops, DSP blocks)

Power consumption

This project demonstrates how different hardware architectures affect performance, area, and power in digital signal processing systems.

📖 Introduction

FIR filters are extensively used in digital signal processing applications such as communication systems, audio processing, biomedical devices, and signal conditioning due to their inherent stability and linear phase properties.

Although FIR filters perform the same mathematical convolution operation, their hardware realization can vary significantly depending on the chosen architecture. These differences influence:

Processing speed

Hardware resource usage

Power efficiency

In this project, three popular FIR filter architectures were designed in Verilog HDL and implemented on a Xilinx FPGA using Vivado 2022.2:

✔ Direct Form

A straightforward implementation using delay registers, multipliers, and adders.

✔ Symmetric Form

Utilizes coefficient symmetry to reduce the number of multipliers and DSP resources.

✔ Transposed Form

Rearranges computation into a pipelined structure to achieve higher operating frequency.

All designs were implemented on the same FPGA device with identical timing constraints for fair comparison.

🛠 Tools and Software Used

Verilog HDL – RTL design

Xilinx Vivado 2022.2 – Synthesis, implementation, timing & power analysis

Simulation tools (Vivado/GTKWave) – Functional verification

MATLAB – FIR coefficient generation (if applicable)

Microsoft Excel – Result comparison

📁 Project Structure
Fir_filter_architectures/
│
├── direct_form/
│   ├── fir_direct.v
│   ├── tb_fir_direct.v
│   ├── constraints.xdc
│   ├── timing report
│   ├── utilization report
│   └── power report
│
├── fir_symmetric/
│   ├── fir_symmetric.v
│   ├── tb_fir_symmetric.v
│   ├── constraints.xdc
│   ├── timing report
│   ├── utilization report
│   └── power report
│
├── fir_transposed/
│   ├── fir_transposed.v
│   ├── tb_fir_transposed.v
│   ├── constraints.xdc
│   ├── timing report
│   ├── utilization report
│   └── power report
│
└── Comparison_of_FIR_Filter_Architectures.xlsx

⚙ Methodology

Designed FIR filters in three architectures using Verilog HDL

Verified functionality with testbenches

Applied identical timing constraints in Vivado

Performed:

Synthesis

Implementation

Timing analysis

Power estimation

Resource utilization

Extracted performance metrics from Vivado reports

Compiled results into a comparison table

📊 Performance Comparison
Architecture	Fmax (MHz)	WNS (ns)	LUTs	FFs	DSPs	Power (mW)
Direct Form	20.2	0.499	9	513	32	92
Symmetric Form	42.56	0.506	9	336	16	95
Transposed Form	92.47	0.188	9	17	32	139
📈 Key Observations

Transposed architecture achieves the highest speed due to pipelined data flow

Symmetric form significantly reduces DSP usage by exploiting coefficient symmetry

Direct form is simplest but consumes the most registers and has lowest speed

Higher performance comes at the cost of increased power consumption

✅ Conclusion

This project demonstrates that FIR filter architecture selection plays a crucial role in:

System speed

Hardware resource utilization

Power efficiency

For high-speed DSP systems, transposed FIR is preferred.
For area-optimized designs, symmetric FIR is most efficient.
Direct form is suitable for simplicity and educational purposes.

🔮 Future Work

Fixed-point precision optimization

Comparison with Vivado FIR IP core

Testing different filter lengths

FPGA board implementation

Low-power architectural exploration

👨‍💻 Author

Sanu P K
B.Tech – Electronics and Communication Engineering
FPGA & Verilog HDL Project
Vivado 2022.2

⭐ If you like this project, feel free to star the repository!
