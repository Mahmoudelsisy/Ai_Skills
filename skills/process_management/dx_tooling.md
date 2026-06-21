# Developer Experience (DX) & Engineering Tooling | تجربة المطور والأدوات الهندسية

## Arabic Description | وصف بالعربية
قواعد صارمة لتحسين تجربة المطورين (DX) وبناء أدوات هندسية داخلية قوية. تركز القواعد على بناء واجهات سطر الأوامر (CLIs)، أتمتة بيئات التطوير المحلية، وتقليل العبء المعرفي للمطورين.

---

## Strict Rules | قواعد صارمة

### 1. CLI Design Standards
- **Clarity**: Every CLI command MUST have a descriptive `--help` and intuitive error messages.
- **Consistent Output**: Support `--json` output for all commands to facilitate scripting and automation.
- **Idempotency**: All management/setup scripts MUST be idempotent.

### 2. Local Development Loop
- **Speed**: The local feedback loop (build, test, reload) MUST be optimized to under 5 seconds for common tasks.
- **Containerized Dev**: Use `devcontainer.json` or Docker Compose to ensure a "One-command setup" for new developers.

### 3. Internal Developer Platforms (IDP)
- **Self-Service**: Build tooling that allows developers to provision resources (DBs, Buckets, Environments) without manual ticket requests.
- **Guardrails**: Implement "Golden Paths" that are secure and compliant by default.

### 4. Documentation & Discovery
- **Searchable Docs**: Maintain a centralized, searchable portal for technical documentation and RFCs.
- **Automated API Discovery**: Use tools like Backstage or custom portals to track service ownership and API schemas.

### 5. Automation & Code Generation
- **Scaffolding**: Provide CLI tools or templates for generating new services/modules following organization standards.
- **Automated Housekeeping**: Use bots or scripts to automate routine tasks (e.g., dependency updates, stale branch cleanup).
