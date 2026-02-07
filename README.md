
# FIR Filter Architecture Comparison on FPGA (Vivado)

This project implements and compares three FIR filter architectures on Xilinx FPGA using Vivado:

• Direct Form  
• Symmetric Form  
• Transposed Form  

Each architecture is analyzed for:

- Maximum operating frequency (Fmax)
- Worst Negative Slack (WNS)
- LUT usage
- Flip-flop usage
- DSP block usage
- Power consumption

---

## 📁 Project Structure
direct_form/ → Direct FIR implementation + reports
fir_symmetric/ → Symmetric FIR implementation + reports
fir_transposed/ → Transposed FIR implementation + reports

Comparison_of_FIR_Filter_Architectures.xlsx → Final comparison table

---

## ⚙️ Tools Used

- Xilinx Vivado 2022.2  
- Verilog HDL  
- MATLAB (for coefficient generation)  
- Excel for result comparison  

---

## 📊 Performance Summary

| Architecture | Fmax (MHz) | LUTs | FFs | DSPs | Power (mW) |
|-------------|-----------|------|-----|------|-----------|
| Direct      | 20.2      | 9    | 513 | 32   | 92        |
| Symmetric   | 42.56     | 9    | 336 | 16   | 95        |
| Transposed  | 92.47     | 9    | 17  | 32   | 139       |

---

## 📈 Key Observations

- Transposed form achieves highest frequency due to pipelining  
- Symmetric form reduces DSP usage using coefficient symmetry  
- Direct form has highest register usage and lowest speed  

---

## 📌 Conclusion

This project demonstrates how FIR filter architecture selection strongly impacts:

✔ Speed  
✔ Resource utilization  
✔ Power consumption  

Transposed architecture is best for high-speed designs, while symmetric form is optimal for DSP efficiency.

---

## 👤 Author

Sanu P K  
FPGA & VLSI Design  


