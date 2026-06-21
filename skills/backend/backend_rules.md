# Backend Engineering & System Architecture | هندسة الأنظمة الخلفية ومعمارية الأنظمة

## Arabic Description | وصف بالعربية
قواعد صارمة لتطوير أنظمة خلفية قوية، قابلة للتطوير، وعالية الأداء. تغطي معالجة البيانات، الاتصال بقواعد البيانات، وإدارة الموارد.

---

## Strict Rules | قواعد صارمة

### 1. Database Best Practices
- **Indexing**: Always ensure appropriate indexing for frequently queried columns.
- **Connections**: Use connection pooling; never open/close connections for every request.
- **Migrations**: All database schema changes MUST be versioned using migration scripts.

### 2. Resource Management
- **Memory Usage**: Be mindful of memory leaks, especially in long-running processes.
- **File I/O**: Always close file handles and streams. Use buffered I/O for large files.

### 3. Concurrency & Parallelism
- **Race Conditions**: Use proper locking mechanisms or atomic operations to prevent race conditions.
- **Background Jobs**: Offload heavy or long-running tasks to background workers (e.g., Celery, BullMQ).

### 4. API & Integration
- **Idempotency**: Ensure that critical POST/PUT operations are idempotent.
- **Contract First**: Define API contracts before starting implementation.

### 5. Performance Optimization
- **Profiling**: Regularly profile the application to identify bottlenecks.
- **Caching**: Use multi-level caching (In-memory, Distributed) strategically.
