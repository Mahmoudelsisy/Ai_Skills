# Java & Spring Boot Professional Standards | معايير جافا وسبرينج بوت الاحترافية

## Arabic Description | وصف بالعربية
قواعد صارمة لتطوير تطبيقات جافا احترافية، مع التركيز على بيئة Spring Boot، إدارة الذاكرة، والأنماط المعمارية للمؤسسات.

---

## Strict Rules | قواعد صارمة

### 1. Java Fundamentals
- **Stream API**: Use Streams and Lambdas for cleaner collection processing, but avoid them if performance is critical in tight loops.
- **Optional**: Use `Optional` to avoid `NullPointerException`, but do not use it as a method parameter.

### 2. Spring Boot Practices
- **Dependency Injection**: Use constructor injection instead of `@Autowired` on fields.
- **Profiles**: Use Spring Profiles (`dev`, `prod`, `test`) to manage environment-specific configurations.

### 3. Concurrency
- **CompletableFuture**: Use `CompletableFuture` or Project Loom (Virtual Threads) for asynchronous tasks.
- **Thread Safety**: Always use thread-safe collections (e.g., `ConcurrentHashMap`) in multi-threaded environments.

### 4. Persistence (JPA/Hibernate)
- **Lazy Loading**: Be careful with `FetchType.EAGER` to avoid N+1 query problems.
- **DTOs**: Always return DTOs (Data Transfer Objects) instead of Entities from your controllers.

### 5. Build & Quality
- **Maven/Gradle**: Use a consistent build tool.
- **Checkstyle/Sonar**: Code MUST pass static analysis checks for security and quality.
