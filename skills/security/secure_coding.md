# Secure Coding & DevSecOps | البرمجة الآمنة والأمن البرمجي

## Arabic Description | وصف بالعربية
هذا الملف يحتوي على قواعد صارمة لمنع الثغرات الأمنية في الكود، وحماية البيانات الحساسة، واتباع معايير OWASP.

---

## Strict Rules | قواعد صارمة

### 1. Input Validation & Sanitization
- **Trust No One**: All input from users, APIs, or files MUST be validated and sanitized.
- **SQL Injection**: Never concatenate strings to build queries. Use parameterized queries or ORMs.
- **XSS Prevention**: Escape all data before rendering it in the UI.

### 2. Secret Management
- **No Hardcoding**: NEVER hardcode API keys, passwords, or secrets. Use environment variables or secret managers.
- **Git Safety**: Use `.gitignore` to prevent committing sensitive files.

### 3. Authentication & Authorization
- **Principle of Least Privilege**: Grant only the minimum permissions necessary.
- **Secure Sessions**: Use secure, HTTP-only cookies and strong JWT tokens.

### 4. Dependency Security
- **Audit**: Regularly run security audits on dependencies (e.g., `npm audit`, `pip-audit`).
- **Update**: Keep all libraries updated to their latest secure versions.

### 5. Logging & Monitoring
- **No Sensitive Data in Logs**: Never log passwords, PII, or tokens.
- **Audit Trails**: Log critical actions for security auditing.
