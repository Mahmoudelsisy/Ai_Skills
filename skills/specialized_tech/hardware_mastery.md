# Advanced Hardware Engineering (FPGA/ASIC) | احتراف هندسة العتاد المتقدمة

## Arabic Description | وصف بالعربية
قواعد هندسية متقدمة لتصميم العتاد باستخدام FPGA و ASIC. تركز القواعد على تحسين تصميم الـ RTL، واستخدام تقنيات HLS (High-Level Synthesis)، وتحقيق الـ Timing Closure في التصميمات المعقدة.

---

## Strict Rules | قواعد صارمة

### 1. Advanced RTL Design
- **Pipeline Stages**: ALWAYS optimize long combinational paths by adding pipeline registers to increase the maximum clock frequency (Fmax).
- **Resource Usage**: Monitor and optimize the usage of LUTs, Flip-Flops, BRAMs, and DSP slices. Avoid unnecessary resource bloat.

### 2. High-Level Synthesis (HLS) Mastery
- **Pragma Usage**: Use HLS pragmas (e.g., `#pragma HLS pipeline`, `#pragma HLS unroll`) correctly to guide the tool towards optimal hardware generation.
- **Interface Synthesis**: Define appropriate interface protocols (e.g., AXI4-Stream, AXI4-Lite) for IP blocks.

### 3. Timing Closure & Constraints
- **Multi-Clock Domains**: Implement robust Clock Domain Crossing (CDC) circuits (e.g., dual-clock FIFOs, synchronizers). Use specialized CDC analysis tools.
- **Constraint Management**: Provide comprehensive SDC/XDC files. Define all clocks, input/output delays, and false paths accurately.

### 4. Verification & UVM
- **Universal Verification Methodology (UVM)**: Use UVM for complex testbenches to ensure reusable and coverage-driven verification.
- **Code Coverage**: Track statement, branch, and toggle coverage. Aim for 100% coverage on critical control logic.

### 5. Hardware/Software Co-design
- **AXI Interconnect**: Optimize data movement between the processor (PS) and programmable logic (PL) using AXI interconnects and DMA controllers.
- **Register Map Standards**: Maintain an accurate, version-controlled register map for software-hardware communication.
