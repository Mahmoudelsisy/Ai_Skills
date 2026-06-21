# Professional DevSecOps & Secure Coding | الأمن البرمجي المتقدم وعمليات الأمان

## Arabic Description | وصف بالعربية
قواعد أمان متقدمة تدمج الأمان في صلب عملية التطوير (Shift-left security). تغطي القواعد أمان سلاسل التوريد البرمجية (Supply Chain Security)، نمذجة التهديدات المتقدمة، وإدارة الـ SBOM.

---

## Strict Rules | قواعد صارمة

### 1. Shift-left Security & SAST/DAST
- **Integrated Scanning**: Security scans (SAST, Secret Detection) MUST run on every commit. Build pipelines MUST fail if high/critical vulnerabilities are detected.
- **DAST in Staging**: Run Dynamic Application Security Testing (DAST) on the staging environment before every production release.

### 2. Software Supply Chain Security
- **SBOM (Software Bill of Materials)**: Generate and maintain a current SBOM for all production software to track and manage component vulnerabilities.
- **Dependency Pinning**: ALWAYS pin dependencies to specific versions or hashes. Avoid "floating" versions in production.
- **Provenance Verification**: Verify the integrity and provenance of third-party packages using digital signatures.

### 3. Advanced Threat Modeling
- **Component-Level Modeling**: Perform threat modeling (e.g., using PASTA or STRIDE) at the design phase for every new microservice or major feature.
- **Attack Path Analysis**: Identify and mitigate potential attack paths that could lead to unauthorized data access or system compromise.

### 4. Infrastructure & Runtime Security
- **Hardened Images**: Use distroless or minimal images for production. Remove all shells and unnecessary utilities.
- **Immutable Infrastructure**: Production environments MUST be immutable. No manual configuration changes or direct SSH access allowed.
- **Runtime Protection**: Implement runtime security monitoring (e.g., Falco) to detect suspicious system calls or process behavior in containers.

### 5. Secure Data & Identity
- **Secrets Encryption**: Secrets MUST be encrypted at rest and in transit. Use specialized tools like HashiCorp Vault with dynamic secret generation.
- **mTLS Everywhere**: Implement mutual TLS for all internal service-to-service communication to ensure both encryption and authentication.
- **Zero Trust**: Validate every request as if it originated from an untrusted network, regardless of its location in the internal architecture.
