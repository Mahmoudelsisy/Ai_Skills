# Enterprise Backend & Distributed Systems | الأنظمة الخلفية والموزعة للمؤسسات الكبرى

## Arabic Description | وصف بالعربية
قواعد هندسية متقدمة لتطوير أنظمة خلفية موزعة ومعقدة. تركز هذه القواعد على مبادئ DDD، الموثوقية العالية، المراقبة العميقة (Observability)، وأنماط التصميم التي تضمن استمرارية العمل في الأنظمة الضخمة.

---

## Strict Rules | قواعد صارمة

### 1. Domain-Driven Design (DDD)
- **Ubiquitous Language**: Use the same terminology in code as defined by domain experts.
- **Bounded Contexts**: Strictly define boundaries between different business domains. Communication between contexts MUST go through well-defined APIs or events.
- **Aggregates**: Group related entities and value objects into aggregates to ensure data consistency and transactional boundaries.

### 2. Distributed Systems & Microservices
- **Database per Service**: In microservices, every service MUST own its data. Direct database access between services is strictly forbidden.
- **Saga Pattern**: Use Sagas (Choreography or Orchestration) to manage distributed transactions across multiple services.
- **Service Mesh**: For complex service topologies, utilize a Service Mesh (e.g., Istio, Linkerd) for traffic management, mTLS, and observability.

### 3. Resilience & Fault Tolerance
- **Resilience Patterns**: Implement **Bulkheads** to isolate failures, **Circuit Breakers** to prevent cascading failures, and **Sidecars** for cross-cutting concerns (logging, proxying).
- **Graceful Degradation**: Design services to provide limited functionality if a dependency is down (e.g., return cached data or defaults).
- **Chaos Engineering**: Regularly test system resilience by injecting failures in a controlled environment (e.g., using Chaos Mesh).

### 4. Observability & Tracing
- **OpenTelemetry**: Instrument all services with OpenTelemetry. Propagate trace IDs across all service boundaries.
- **Structured Logging**: All logs MUST be structured (JSON) and include context (RequestID, UserID, SpanID).
- **SLIs/SLOs**: Monitor services based on defined Service Level Objectives. Use "Golden Signals" (Latency, Traffic, Errors, Saturation).

### 5. High-Performance Execution
- **Zero-Downtime Migrations**: Implement "Expand and Contract" pattern for database schema changes to allow rolling updates.
- **Non-blocking I/O**: Use asynchronous, non-blocking I/O for high-concurrency workloads (e.g., Go routines, Node.js Event Loop, Java Virtual Threads).
- **Caching Tiers**: Implement a multi-tier caching strategy (L1: Local memory, L2: Distributed cache like Redis, L3: CDN/Edge).
