# Embedded Systems & C/C++ Professional Standards | معايير الأنظمة المدمجة ولغة C/C++

## Arabic Description | وصف بالعربية
قواعد صارمة لتطوير الأنظمة المدمجة (Embedded Systems) والبرمجة منخفضة المستوى باستخدام C و C++. تركز هذه القواعد على إدارة الذاكرة اليدوية، كفاءة الموارد، والتعامل المباشر مع الأجهزة (Hardware).

---

## Strict Rules | قواعد صارمة

### 1. Resource Constraints
- **Minimal Footprint**: Optimize code for minimum RAM and Flash usage. Avoid large libraries.
- **No Dynamic Allocation**: In critical embedded systems, NEVER use `malloc()` or `new` after initialization. Use static allocation.

### 2. Memory Safety (C/C++)
- **Pointer Safety**: Always initialize pointers to `NULL` or `nullptr`. Perform null checks before dereferencing.
- **RAII**: In C++, use Resource Acquisition Is Initialization (RAII) for managing resources (smart pointers, file handles).
- **Buffer Overflow**: Use safe string and buffer functions (e.g., `strncpy`, `snprintf`). Never use `gets()`.

### 3. Hardware Interfacing
- **Volatile Keyword**: Use the `volatile` keyword for variables modified by hardware or ISRs (Interrupt Service Routines).
- **Atomic Operations**: Ensure shared data between ISRs and the main loop is accessed atomically.

### 4. Real-Time Performance
- **Deterministic Code**: Avoid algorithms with unpredictable execution times in real-time tasks.
- **ISR Optimization**: Keep Interrupt Service Routines as short as possible. Never call blocking functions inside an ISR.

### 5. Standards Compliance
- **MISRA C**: Follow MISRA C guidelines where safety and reliability are paramount.
- **C++ Standards**: Use modern C++ standards (C++17/20/23) features when available for safer and more expressive code.
