# Software Architecture & System Design | معمارية البرمجيات وتصميم الأنظمة

## Arabic Description | وصف بالعربية
قواعد معمارية البرمجيات لضمان بناء أنظمة قابلة للتوسع (Scalable) وقوية (Robust). تغطي الأنماط الشائعة وتقسيم المكونات.

---

## Strict Rules | قواعد صارمة

### 1. Modularity & Separation of Concerns
- **Domain Logic**: Business logic MUST be separated from framework/infrastructure code.
- **Layers**: Follow a layered architecture (e.g., Presentation, Application, Domain, Infrastructure).

### 2. Design Patterns
- **Standard Patterns**: Use established design patterns (Factory, Singleton, Observer, Strategy) only when appropriate.
- **Avoid Anti-patterns**: Avoid God Objects, Spaghetti Code, and Golden Hammer.

### 3. Scalability
- **Statelessness**: Prefer stateless services to allow horizontal scaling.
- **Caching**: Implement caching strategies (Redis, Memcached) for frequently accessed data.

### 4. Microservices (If applicable)
- **Independence**: Each service must have its own database and be deployable independently.
- **Communication**: Use asynchronous messaging (RabbitMQ, Kafka) for inter-service communication where possible.

### 5. Resiliency
- **Circuit Breakers**: Use circuit breakers for external service calls.
- **Retries**: Implement exponential backoff for transient failures.
