# Expert API Engineering & Decision System | هندسة الـ API ونظام اتخاذ القرار

## Arabic Description | وصف بالعربية
قواعد هندسية متقدمة لتصميم الـ APIs. يتضمن هذا الملف نظام اتخاذ القرار لتطوير العقود البرمجية، مع جداول مفاضلة شاملة وسيناريوهات فشل وكيفية التعامل مع تطور النظام دون كسر التوافقية.

---

## Decision Framework: API Versioning
| Strategy | Pros | Cons | When to Use |
|---|---|---|---|
| URL Versioning | Explicit, easy to cache | Breaking changes require new URLs | Most public APIs |
| Header Versioning | Cleaner URLs, flexible | Harder to test in browser | Enterprise internal APIs |
| Content Negotiation | Most standard compliant | Highly complex for clients | Versioning media types only |

---

## Strict Rules | قواعد صارمة

### 1. Contract & Stability
- **Schema-First**: Define API contracts using OpenAPI/AsyncAPI before implementation.
- **Strict Backward Compatibility**: NEVER remove a field or change a type in a non-major version.
- **Sunset Policy**: Use `Sunset` headers to notify clients of upcoming deprecations.

### 2. Integration Resilience
- **Idempotency Keys**: MANDATORY for all state-changing operations (POST/PATCH/PUT).
- **Webhooks Reliability**: Use a reliable message queue for outgoing webhooks with exponential backoff retries.

---

## Failure Scenarios: API Issues
1. **Scenario**: A client sends a massive request payload that exhausts server memory.
   - **Handling**: Implement strict request body size limits at the gateway level. Use streaming parsers where possible.
2. **Scenario**: An API version is deprecated, but a high-value client hasn't migrated.
   - **Handling**: Use "Shadow Mirroring" to monitor usage. Implement "Virtual Sunset" (artificial errors for small % of traffic) to force attention before final cutoff.

---

## Production Checkpoints
- [ ] Is there a machine-readable schema (OpenAPI) available?
- [ ] Are rate limits configured based on client priority/tiers?
- [ ] Is HMAC signature verification enabled for all Webhooks?
