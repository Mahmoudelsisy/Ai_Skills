# Go (Golang) Professional Standards | معايير لغة جو الاحترافية

## Arabic Description | وصف بالعربية
قواعد لغة Go الصارمة التي تركز على البساطة، الأداء العالي، ومعالجة الأخطاء بشكل صحيح وفقاً لنمط Go الفلسفي.

---

## Strict Rules | قواعد صارمة

### 1. Error Handling
- **Explicit Checks**: Check every error explicitly. No ignoring errors with `_`.
- **Error Wrapping**: Use `%w` to wrap errors with context.

### 2. Concurrency
- **Goroutines**: Only use goroutines when necessary. Ensure they have a way to exit (avoid leaks).
- **Channels**: Use channels for communication; avoid shared memory where possible.

### 3. Formatting & Style
- **Gofmt**: All code MUST be formatted with `gofmt`.
- **Naming**: Use short, meaningful names. Avoid `snake_case` in favor of `camelCase`.

### 4. Performance
- **Pointers**: Use pointers only when mutation is needed or for large structs to avoid copying.
- **Pre-allocation**: Pre-allocate slices with `make([]T, 0, cap)` when capacity is known.
