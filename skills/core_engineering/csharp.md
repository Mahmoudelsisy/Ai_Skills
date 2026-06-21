# C# & .NET Professional Standards | معايير سي شارب ودوت نت الاحترافية

## Arabic Description | وصف بالعربية
قواعد صارمة لتطوير تطبيقات .NET حديثة، تركز على الأداء، أمن الشيفرة البرمجية، وأفضل ممارسات Microsoft.

---

## Strict Rules | قواعد صارمة

### 1. Modern C# Syntax
- **File-scoped Namespaces**: Use file-scoped namespaces for cleaner code.
- **Pattern Matching**: Utilize modern pattern matching features for concise logic.

### 2. ASP.NET Core
- **Middleware**: Keep the middleware pipeline lean.
- **Dependency Injection**: Use the built-in DI container strictly.

### 3. Asynchronous Programming
- **Async All the Way**: Use `async`/`await` throughout the entire call stack. NEVER use `.Result` or `.Wait()`.
- **Task.WhenAll**: Use `Task.WhenAll` for parallel asynchronous tasks.

### 4. Performance
- **Span & Memory**: Use `Span<T>` and `Memory<T>` for high-performance memory management without allocations.
- **Entity Framework**: Use `AsNoTracking()` for read-only queries to improve performance.

### 5. Security
- **Data Protection**: Use the .NET Data Protection API for sensitive data.
- **Authentication**: Use IdentityServer or built-in ASP.NET Core Identity for secure auth.
