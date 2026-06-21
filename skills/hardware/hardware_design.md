# Hardware Design (Verilog/VHDL) | تصميم الأجهزة والدوائر الإلكترونية

## Arabic Description | وصف بالعربية
قواعد صارمة لتصميم الأجهزة باستخدام لغات وصف الأجهزة (HDL) مثل Verilog و VHDL. تركز هذه القواعد على تصميم دوائر منطقية (RTL) صحيحة، قابلة للتوليد (Synthesizable)، ومختبرة بعناية.

---

## Strict Rules | قواعد صارمة

### 1. Synthesizable Code
- **Hardware Mindset**: Write code that represents actual physical logic gates and flip-flops. Avoid non-synthesizable constructs in RTL.
- **Synchronous Design**: Use a single clock and a single reset for the entire module unless multi-clock domains are strictly necessary.

### 2. RTL Best Practices
- **Blocking vs Non-Blocking**: In Verilog, use non-blocking assignments (`<=`) for sequential logic and blocking assignments (`=`) for combinational logic.
- **FSM Design**: Use a structured approach for Finite State Machines (e.g., two-process or three-process style).

### 3. Verification & Simulation
- **Testbenches**: Every module MUST have a corresponding testbench that covers all edge cases.
- **Assertions**: Use SystemVerilog Assertions (SVA) to verify design properties during simulation.

### 4. Timing & Constraints
- **Setup & Hold**: Ensure design meets setup and hold time requirements.
- **SDC Constraints**: Provide a proper Synopsys Design Constraints (SDC) file for synthesis and implementation.

### 5. Code Quality
- **Naming Conventions**: Use consistent naming for signals (e.g., `_clk`, `_rst_n`, `_en`).
- **Parameterization**: Use parameters or generics to make modules reusable across different designs.
