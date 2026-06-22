# Platform Engineering Mastery | احتراف هندسة المنصات

## Arabic Description | وصف بالعربية
قواعد هندسية متقدمة لبناء منصات تطوير داخلية (Internal Developer Platforms - IDP) تهدف إلى تقليل العبء المعرفي للمطورين وتوفير "مسارات ذهبية" (Golden Paths) مؤتمتة وآمنة لتوفير البنية التحتية والخدمات.

---

## Strict Rules | قواعد صارمة

### 1. Internal Developer Platform (IDP)
- **Self-Service Infrastructure**: Developers MUST be able to provision standard resources (DBs, Buckets, Environments) via a portal or CLI without manual IT intervention.
- **Backstage Integration**: Use a centralized portal (e.g., Backstage) for service discovery, documentation, and ownership tracking.

### 2. Golden Paths (The Paved Road)
- **Standardized Templates**: Provide production-ready, security-hardened templates for new services. Deviating from the Golden Path MUST require a manual architecture review.
- **Reduced Cognitive Load**: Abstract complex K8s/Cloud configurations into simple, high-level abstractions (e.g., using Crossplane or specialized CRDs).

### 3. Platform APIs & Tooling
- **Infrastructure as a Product**: Treat the platform as a product. Gather feedback from "customers" (developers) and iterate based on usage data.
- **Consistent Tooling**: Ensure all internal CLIs and scripts follow consistent UX and output formats.

### 4. Governance & Guardrails
- **Automated Compliance**: Implement guardrails (e.g., OPA/Rego) that prevent the creation of non-compliant resources from the start.
- **Resource Limits**: Enforce strict quotas and limits to prevent one team from exhausting platform-wide resources.

### 5. Decision Framework: Platform vs Product
- **Choice**: Build a generic system vs. a specialized platform.
- **Trade-off**:
| Choice | Pros | Cons | When to Use |
|---|---|---|---|
| generic system | Flexible, low initial cost | High developer cognitive load | Early startups, small teams |
| IDP/Platform | High consistency, low MTTR | High initial investment | Scale-ups, Enterprise, 50+ devs |
