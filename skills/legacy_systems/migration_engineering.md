# Migration Engineering & Legacy Transformation | هندسة الترحيل وتحويل الأنظمة القديمة

## Arabic Description | وصف بالعربية
قواعد هندسية متقدمة لعمليات ترحيل الأنظمة (Migration) الكبرى، مثل التحول من Monolith إلى Microservices أو الترحيل بين قواعد البيانات. تركز القواعد على استراتيجيات الترحيل بدون توقف (Zero Downtime)، نمط Strangler Fig، وسلامة البيانات.

---

## Strict Rules | قواعد صارمة

### 1. Zero-Downtime Migration Patterns
- **Dual Writing**: When migrating data stores, ALWAYS implement dual writing (writing to both old and new stores) to ensure consistency before the final cutover.
- **Canary Migration**: Migrate traffic incrementally. Start with 1% of users or non-critical features and monitor health metrics closely.

### 2. Strangler Fig Strategy
- **Facade Injection**: Use an API Gateway or Reverse Proxy as a facade to intercept requests and route them to either the legacy system or the new microservice.
- **Incremental Extraction**: Extract logical domains one by one based on business priority and technical complexity.

### 3. Data Integrity & Parity
- **Shadow Mirroring**: Run production read requests against both systems and compare results in the background. Fail the migration if parity is not 100%.
- **Reverse ETL**: Implement tools to sync data back from the new system to the legacy system if some legacy components still require the old data format.

### 4. Rollback Readiness
- **Instant Rollback**: Every migration step MUST have an automated and tested rollback plan.
- **Feature Flags**: Use feature flags to enable/disable the new system instantly without redeploying code.

### 5. Decision Framework: Migration Approach
- **Trade-off Analysis**:
| Choice | Pros | Cons | When to Use |
|---|---|---|---|
| Big Bang | Faster (if successful), simple | Extremely high risk, massive downtime | Small, non-critical systems only |
| Strangler Fig | Low risk, continuous value | High complexity, longer duration | All enterprise mission-critical systems |
