# Enterprise Go Mastery | احتراف لغة جو للمشاريع الكبرى

## Arabic Description | وصف بالعربية
قواعد هندسية متقدمة لاحتراف لغة Go في بناء أنظمة موزعة وعالية الأداء. تغطي القواعد إدارة الـ Goroutines المتقدمة، تحسين الأداء على مستوى الذاكرة، والتعامل مع الـ Garbage Collector.

---

## Strict Rules | قواعد صارمة

### 1. Advanced Concurrency (Goroutines & Channels)
- **Structured Concurrency**: ALWAYS use `context.Context` for cancellation, timeouts, and metadata propagation across goroutines.
- **Worker Pools**: Use worker pool patterns to limit the number of concurrent goroutines and prevent resource exhaustion.
- **Select Statement Mastery**: Use `select` with `default` for non-blocking channel operations. Use timers for timeouts.

### 2. High-Performance Memory Management
- **Zero Allocation Policy**: In performance-critical paths, minimize allocations. Use `sync.Pool` to reuse objects.
- **Escape Analysis**: Understand and monitor escape analysis. Avoid pointers for small objects to keep them on the stack.
- **Buffer Reuse**: Use `bytes.Buffer` or `strings.Builder` for efficient string manipulation.

### 3. Engineering Practices for Scale
- **Interface Segregation**: Keep interfaces small and specific. "The bigger the interface, the weaker the abstraction."
- **Internal/External Packaging**: Use the `internal` directory to hide implementation details from other modules.
- **Error Handling (Professional)**: Use custom error types for domain-specific errors. Wrap errors with `%w` but only at the boundaries.

### 4. System & Runtime Optimization
- **GC Tuning**: Monitor and tune GC behavior (e.g., `GOGC`, `GOMEMLIMIT`) based on the application's memory profile.
- **Profiling (pprof)**: Regularly use `net/http/pprof` for CPU, Memory, and Block profiling in production.
- **Compiler Inlining**: Write code that is easy for the compiler to inline in hot paths.

### 5. Testing & Verification
- **Table-Driven Tests**: ALL unit tests MUST use the table-driven test pattern for comprehensive coverage of cases.
- **Race Detection**: ALWAYS run tests with the `-race` flag in CI/CD.
- **Benchmarking**: Write benchmarks for performance-critical functions to prevent regressions.
