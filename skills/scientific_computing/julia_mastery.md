# Scientific Computing & Julia Mastery | احتراف الحوسبة العلمية ولغة جوليا

## Arabic Description | وصف بالعربية
قواعد هندسية متقدمة للحوسبة العلمية وعالية الأداء (HPC) باستخدام لغة Julia. تركز القواعد على تحسين الأداء الحسابي، إدارة الذاكرة بكفاءة، وضمان الدقة الرياضية في النمذجة.

---

## Strict Rules | قواعد صارمة

### 1. Julia Performance (LLVM)
- **Type Stability**: Ensure all performance-critical functions are type-stable. Use `@code_warntype` to detect instabilities.
- **Avoid Global Variables**: NEVER use non-constant global variables in hot paths.
- **Pre-allocation**: Pre-allocate output arrays and use in-place functions (e.g., `f!(x)`) to avoid GC pressure.

### 2. Scientific Rigor & Accuracy
- **Floating Point Awareness**: Be mindful of precision issues (e.g., `Float64` vs `Float32`). Use `IntervalArithmetic.jl` for guaranteed bounds when required.
- **Unit Validation**: Use `Unitful.jl` to ensure dimensional consistency in physical simulations.

### 3. High Performance Computing (HPC)
- **Vectorization**: Use `@simd` and LoopVectorization.jl for optimal CPU usage.
- **Parallelism**: Use Julia's built-in `Threads` and `Distributed` modules correctly. Avoid race conditions using atomic operations or locks.
- **GPU Acceleration**: Leverage `CUDA.jl` or `AMDGPU.jl` for massive parallel processing.

### 4. Mathematical Modeling
- **Solver Selection**: Choose the appropriate solver from `DifferentialEquations.jl` based on stiffness and accuracy needs.
- **Linear Algebra**: Use optimized BLAS/LAPACK routines.

### 5. Packaging & Reproducibility
- **Project environments**: ALWAYS use `Project.toml` and `Manifest.toml` to ensure exact reproducible environments.
- **Docstrings**: Document mathematical formulas and assumptions clearly in docstrings.
