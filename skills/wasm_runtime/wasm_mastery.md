# WebAssembly (WASM) & Runtime Mastery | احتراف ويب أسمبلي وبيئات التشغيل

## Arabic Description | وصف بالعربية
قواعد هندسية متقدمة لتطوير تطبيقات WebAssembly (WASM) باستخدام لغات مثل Rust و C++. تركز القواعد على تحسين الأداء الحسابي، تقليل حجم الملفات، والتعامل الآمن والسريع بين WASM وبيئة المتصفح (Host).

---

## Strict Rules | قواعد صارمة

### 1. Language Selection & Compilation
- **Rust/C++ to WASM**: Use Rust (wasm-bindgen) or C++ (Emscripten) for high-performance modules. Prefer Rust for better safety and modern tooling.
- **Optimization Levels**: ALWAYS compile with high optimization levels (e.g., `-O3` or `-Oz`) for production to minimize binary size.

### 2. Performance & Memory
- **Manual Memory Management**: Manage WASM linear memory efficiently. Use tools like `wasm-opt` to further optimize the compiled binary.
- **Zero-Copy Data Transfer**: Minimize data copying between JavaScript and WASM using `SharedArrayBuffer` or directly accessing WASM linear memory.

### 3. Size Optimization
- **Strip Debug Info**: ALWAYS strip debug symbols from production WASM binaries to reduce size.
- **Dynamic Imports**: Load WASM modules dynamically to avoid blocking the initial page load.

### 4. Host-Guest Communication
- **Standardized Interfaces**: Use WebIDL or standard bindgen patterns for consistent communication between the host (JS) and guest (WASM).
- **Security Sandbox**: Respect the WASM sandbox. NEVER expose sensitive host functions to the WASM module unless strictly required.

### 5. Advanced Runtime Usage
- **WASI**: Use WebAssembly System Interface (WASI) for non-browser WASM runtimes (e.g., Edge Computing, Serverless).
- **SIMD in WASM**: Leverage WASM SIMD instructions for heavy mathematical and media processing tasks where supported.
