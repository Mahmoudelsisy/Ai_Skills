# Software Lifecycle & Process Excellence | دورة حياة البرمجيات والتميز في العمليات

## Arabic Description | وصف بالعربية
قواعد صارمة لدورة حياة تطوير البرمجيات (SDLC) والعمليات الهندسية. تغطي القواعد جمع المتطلبات، مراحل التصميم والتنفيذ، الاختبارات الشاملة، وعمليات الصيانة المستمرة لضمان أعلى جودة ممكنة.

---

## Strict Rules | قواعد صارمة

### 1. Requirements & Discovery
- **Clear Definitions**: NEVER start development without a clear, written requirement (SRS).
- **Stakeholder Alignment**: Ensure technical design aligns with business goals before implementation.

### 2. Design & Architecture Phase
- **RFC/ADR Process**: Document major technical decisions and architectural changes using Request for Comments (RFC) or Architecture Decision Records (ADR).
- **Prototyping**: Build low-fidelity prototypes for risky or unproven technical concepts.

### 3. Implementation Standards
- **Standardized Environments**: Use Docker or Dev Containers to ensure consistent development environments for all team members.
- **Code Formatting**: Enforce automated formatting (Prettier, Gofmt, etc.) and Linting as a pre-commit hook.

### 4. Verification & QA (SDLC)
- **Test Matrix**: Ensure coverage for Unit, Integration, and End-to-End tests based on the criticality of the feature.
- **Security Audits**: Perform automated and manual security reviews before every major release.

### 5. Deployment & Maintenance
- **Post-deployment Verification**: Use automated health checks and smoke tests immediately after deployment.
- **Technical Debt Tracking**: Actively track technical debt and allocate at least 20% of sprint capacity to refactoring and maintenance.
- **Knowledge Transfer**: Document the internal workings of every major service to prevent "bus factor" risks.
