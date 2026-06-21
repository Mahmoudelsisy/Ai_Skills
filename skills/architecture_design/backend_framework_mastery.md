# Enterprise Backend Framework Mastery | احتراف أطر عمل الأنظمة الخلفية

## Arabic Description | وصف بالعربية
قواعد هندسية متقدمة لاحتراف أشهر أطر عمل الأنظمة الخلفية (NestJS, FastAPI, Go Gin/Echo). تركز هذه القواعد على المعمارية النظيفة، الأداء العالي، وكفاءة التطوير في بيئات المؤسسات الكبرى.

---

## Strict Rules | قواعد صارمة

### 1. NestJS (TypeScript)
- **Dependency Injection**: Use constructor-based DI strictly. Group related logic into feature-based Modules.
- **Interceptors & Decorators**: Use Interceptors for cross-cutting concerns (logging, response transformation) and custom Decorators for reusable logic (e.g., `@CurrentUser`).
- **Validation**: Use `class-validator` with `ValidationPipe` (whitelist: true, forbidNonWhitelisted: true).

### 2. FastAPI (Python)
- **Asynchronous Paths**: Use `async def` for I/O bound operations. Use background tasks for non-blocking processes.
- **Dependency Overriding**: Leverage FastAPI's dependency injection system for testing and reusable logic.
- **Pydantic Models**: Use Pydantic v2 strictly for request/response schemas. Enforce strict type checking in models.

### 3. Go Gin & Echo
- **Middleware Chain**: Keep the middleware chain lean. Handle errors at the middleware level where possible (e.g., recovery, logging).
- **Context Handling**: NEVER ignore the `gin.Context` or `echo.Context`. Propagate deadlines and cancellations correctly.
- **Structuring**: Follow a domain-driven structure (e.g., cmd, internal, pkg). Avoid flat folder structures for large projects.

### 4. Framework Agnostic Patterns
- **Exception Filters**: Implement centralized global error handling for all frameworks to ensure consistent API error responses.
- **Configuration**: Use environment-specific schema-validated configurations (e.g., NestJS ConfigService, Pydantic Settings).
- **Graceful Shutdown**: Implement listeners for `SIGTERM` and `SIGINT` to close database connections and finish active requests before exiting.

### 5. Documentation & Contracts
- **Swagger/OpenAPI**: Enable and configure Swagger UI for all frameworks. Document every endpoint, parameter, and status code.
- **DTO Isolation**: Use Data Transfer Objects (DTOs) for API boundaries; never expose internal database entities directly.
