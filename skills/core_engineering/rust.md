# Enterprise Rust Mastery | احتراف لغة رست للمشاريع الكبرى

## Arabic Description | وصف بالعربية
قواعد هندسية متقدمة لاحتراف لغة Rust في بناء أنظمة آمنة وفائقة الأداء. تغطي القواعد أنماط الأمان المتقدمة، تحسين الأداء على مستوى الذاكرة، والتعامل مع الـ Unsafe code بحذر شديد.

---

## Strict Rules | قواعد صارمة

### 1. Advanced Ownership & Memory
- **Smart Pointers Mastery**: Use `Arc`, `Rc`, `Box`, and `RefCell` correctly based on the ownership needs. Prefer `Arc<Mutex<T>>` for shared mutable state across threads.
- **Pinning**: Use `Pin` for self-referential structs or manual Future implementations.
- **Memory Layout**: Use `#[repr(C)]` or `#[repr(packed)]` when interfacing with hardware or FFI.

### 2. High-Performance Async (Tokio/Futrues)
- **Zero-cost Futures**: Understand how futures are polled. Avoid long-running synchronous work in async functions. Use `spawn_blocking` for CPU-heavy tasks.
- **Concurrency primitives**: Prefer specialized sync primitives from `tokio::sync` for async code over standard library ones.

### 3. Safety & Unsafe
- **No Unsafe by Default**: `unsafe` code is strictly forbidden unless there is no safe alternative and it's thoroughly documented with `# Safety` comments.
- **Boundary Checks**: Use `get()` and `get_mut()` for safe slice access instead of raw indexing where failure is possible.

### 4. Advanced Abstractions & Generics
- **Trait Objects vs Generics**: Use Generics (Static Dispatch) by default for performance. Use Trait Objects (Dynamic Dispatch) only when heterogeneous collections are needed.
- **Associated Types & GATs**: Master Generic Associated Types (GATs) for building complex, flexible abstractions.

### 5. Tooling & Ecosystem
- **Cargo Workspaces**: Use workspaces for large projects with multiple packages.
- **Performance Profiling**: Use `cargo-flamegraph` and `perf` to identify hot spots.
- **CI/CD Hygiene**: Enforce `cargo deny` to check for security vulnerabilities and unapproved licenses in dependencies.
