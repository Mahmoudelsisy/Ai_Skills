# Advanced Security Practices | الممارسات الأمنية المتقدمة

## Arabic Description | وصف بالعربية
قواعد أمان متقدمة تتجاوز القواعد الأساسية لتشمل حماية الأنظمة من هجمات XSS, CSRF, SQL Injection بشكل معمق، وتطبيق هندسة "الثقة الصفرية" (Zero Trust)، وإدارة الأسرار التقنية (Secrets Management) بشكل احترافي.

---

## Strict Rules | قواعد صارمة

### 1. Web Vulnerability Mitigation (Deep)
- **XSS Prevention**: Use Context-Aware Encoding. Never use `dangerouslySetInnerHTML` without rigorous sanitization. Set a strong `Content-Security-Policy` (CSP).
- **CSRF Protection**: ALWAYS use Anti-CSRF tokens for state-changing operations. Set `SameSite=Strict` for sensitive cookies.
- **SQL Injection**: Use parameterized queries or ORMs exclusively. NEVER build queries using string concatenation with user input.

### 2. Zero Trust Architecture
- **Verify Explicitly**: Never trust a request based on network location. ALWAYS verify the user, the device, and the request (e.g., using mTLS and OIDC).
- **Least Privilege**: Grant the minimum necessary access for the shortest duration possible. Use Role-Based Access Control (RBAC) and Attribute-Based Access Control (ABAC).

### 3. Identity & Authentication
- **Secure Hashing**: Use `bcrypt` or `Argon2` for password hashing with appropriate salt and cost factors.
- **Token Security**: Use signed, short-lived JWTs. Store them securely (HTTP-only, Secure cookies). Implement token revocation lists.

### 4. Advanced Secrets Management
- **No Secrets in Code**: Secrets MUST NEVER exist in version control, even encrypted.
- **Dynamic Secrets**: Use tools like HashiCorp Vault to generate dynamic, short-lived credentials for databases and services.
- **Secret Rotation**: Implement automated secret rotation for all production credentials.

### 5. Defensive Coding
- **Rate Limiting**: Implement rate limiting at the API gateway to prevent Brute Force and DoS attacks.
- **Input Sanitization**: Validate and sanitize ALL incoming data at the application boundary using strict schemas (e.g., JSON Schema, Zod).
