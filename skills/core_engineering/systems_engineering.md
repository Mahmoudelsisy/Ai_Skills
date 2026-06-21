# Systems Programming (OS, Kernels & Compilers) | برمجة الأنظمة (أنظمة التشغيل، النواة، والمترجمات)

## Arabic Description | وصف بالعربية
قواعد صارمة لبرمجة الأنظمة منخفضة المستوى، بما في ذلك تطوير أنظمة التشغيل (OS)، النواة (Kernel)، والمترجمات (Compilers). تركز هذه القواعد على إدارة الذاكرة اليدوية الدقيقة، تحسين الأداء على مستوى المعالج، والتعامل المباشر مع عتاد الحاسوب.

---

## Strict Rules | قواعد صارمة

### 1. Low-Level Memory Management
- **Manual Control**: ALWAYS have full control over memory layout. Avoid abstractions that hide allocation costs.
- **Cache Locality**: Design data structures to maximize cache hits (Data-Oriented Design).
- **Alignment**: Ensure data structures are properly aligned for the target architecture.

### 2. Kernel & Driver Development
- **No Blocking in Kernel**: Never call blocking functions or perform long operations in interrupt context or critical kernel paths.
- **Concurrency**: Use appropriate locking primitives (spinlocks, mutexes) correctly to prevent deadlocks and race conditions in the kernel.

### 3. Compiler & Toolchain Engineering
- **Intermediate Representation (IR)**: Design efficient and expressive IRs for compilers.
- **Optimization Passes**: Implement optimizations that balance compile time with execution performance (e.g., constant folding, dead code elimination).

### 4. Hardware Interaction
- **Instruction Set Architecture (ISA)**: Be deeply familiar with the target ISA (x86, ARM, RISC-V) and use assembly only when necessary for performance or hardware access.
- **Memory Barriers**: Use memory barriers/fences correctly in multi-core systems to ensure proper ordering of operations.

### 5. Debugging & Verification
- **Static Analysis**: Use advanced static analysis tools to detect memory leaks, undefined behavior, and potential security vulnerabilities.
- **Low-Level Debugging**: Be proficient with debuggers like GDB/LLDB and hardware-level debugging tools (JTAG).
