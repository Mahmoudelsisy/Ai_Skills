# Advanced Cybersecurity & Pentesting | الأمن السيبراني المتقدم واختبار الاختراق

## Arabic Description | وصف بالعربية
قواعد صارمة للأمن السيبراني تغطي اختبار الاختراق، النمذجة الأمنية للتهديدات (Threat Modeling)، والدفاع عن الأنظمة. تهدف هذه القواعد إلى بناء أنظمة محصنة ضد الهجمات المتقدمة.

---

## Strict Rules | قواعد صارمة

### 1. Threat Modeling
- **STRIDE Analysis**: Perform STRIDE (Spoofing, Tampering, Repudiation, Information Disclosure, Denial of Service, Elevation of Privilege) analysis on every new feature.
- **Attack Surface Minimization**: Always disable unnecessary services, ports, and protocols.

### 2. Vulnerability Assessment
- **Automated Scanning**: Integrate DAST (Dynamic Application Security Testing) and SAST (Static Application Security Testing) into the CI/CD pipeline.
- **Dependency Auditing**: Use tools like `Snyk` or `OWASP Dependency-Check` to find and patch vulnerabilities in libraries.

### 3. Offensive Security (Pentesting)
- **Reconnaissance Rules**: Follow ethical boundaries. Never perform scans or tests on systems without explicit authorization.
- **Payload Safety**: Use non-destructive payloads when testing for vulnerabilities in production-like environments.

### 4. Defensive Security (Hardening)
- **Zero Trust Architecture**: Never trust a request based on its origin (internal or external). Always verify.
- **WAF Configuration**: Implement and tune Web Application Firewalls (WAF) to block common attack patterns.
- **Encryption**: Use TLS 1.3 for all data in transit and AES-256 for data at rest.

### 5. Incident Response
- **Logging for Forensics**: Ensure logs are immutable and contain enough detail (timestamp, user ID, IP, action) for forensic analysis.
- **Alerting**: Set up real-time alerts for suspicious activities (e.g., multiple failed login attempts, unauthorized API access).
