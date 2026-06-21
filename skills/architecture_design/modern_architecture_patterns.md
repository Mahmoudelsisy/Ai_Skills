# Modern Architectural Patterns (Hexagonal & Onion) | الأنماط المعمارية الحديثة

## Arabic Description | وصف بالعربية
قواعد صارمة لتطبيق الأنماط المعمارية الحديثة مثل Hexagonal Architecture (Ports and Adapters) و Onion Architecture. تضمن هذه القواعد فصل كامل للمنطق البرمجي (Domain) عن التفاصيل التقنية الخارجية.

---

## Strict Rules | قواعد صارمة

### 1. Hexagonal Architecture (Ports & Adapters)
- **The Core (Domain)**: The Domain logic MUST be isolated at the center. It MUST NOT have any dependencies on external frameworks or databases.
- **Ports (Interfaces)**: Define Ports as interfaces that the Domain uses to interact with the outside world (Output Ports) or that the outside world uses to interact with the Domain (Input Ports).
- **Adapters (Implementation)**: Implement Adapters to translate between the Domain's ports and external technologies (e.g., SQL Database Adapter, REST API Adapter).

### 2. Onion Architecture
- **Inward Dependencies**: Dependencies MUST only point inwards. Outer layers (Infrastructure, UI) depend on inner layers (Application, Domain), but never the reverse.
- **Independence**: The Domain and Application layers MUST be testable without any external infrastructure.

### 3. Repository Pattern & Unit of Work
- **Repository Pattern**: Abstract data access logic behind repositories. The Domain only interacts with repository interfaces.
- **Unit of Work**: Group multiple database operations into a single transaction to ensure consistency and atomicity.

### 4. Modular Monolith vs Microservices
- **Modular Monolith**: For complex projects starting out, prefer a Modular Monolith with strictly enforced boundaries before moving to Microservices.
- **Service Boundaries**: Use DDD Bounded Contexts to define service boundaries. Avoid "Anemic Domain Models."

### 5. Integration Patterns
- **Anti-Corruption Layer (ACL)**: Implement an ACL when integrating with legacy or external systems to prevent their models from leaking into your domain.
- **BFF (Backend for Frontend)**: Use the BFF pattern to tailor API responses for specific frontend types (Mobile, Web).
