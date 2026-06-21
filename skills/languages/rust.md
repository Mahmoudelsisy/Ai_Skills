# Rust Professional Standards | معايير لغة رست الاحترافية

## Arabic Description | وصف بالعربية
قواعد صارمة للغة Rust تضمن الأمان الذاكري (Memory Safety)، الأداء العالي، واستخدام أنماط البرمجة الصحيحة للغة.

---

## Strict Rules | قواعد صارمة

### 1. Ownership & Borrowing
- **Borrow Checker**: Write code that satisfies the borrow checker without excessive use of `.clone()`.
- **Lifetimes**: Use explicit lifetimes only when necessary; prefer lifetime elision where possible.

### 2. Error Handling
- **No `panic!`**: Avoid `panic!`, `unwrap()`, and `expect()` in production code. Use `Result` and `Option`.
- **Custom Errors**: Use crates like `thiserror` or `anyhow` for structured error handling.

### 3. Concurrency
- **Send & Sync**: Ensure types correctly implement `Send` and `Sync` for thread safety.
- **Rayon/Tokio**: Use `Tokio` for async I/O and `Rayon` for parallel CPU tasks.

### 4. Macros & Generics
- **Simplicity**: Avoid complex macros if functions or generics can achieve the same result.
- **Zero-cost Abstractions**: Leverage Rust's zero-cost abstractions to keep performance at the C/C++ level.

### 5. Tooling
- **Clippy**: Code MUST pass all `cargo clippy` checks.
- **Fmt**: Code MUST be formatted with `cargo fmt`.
