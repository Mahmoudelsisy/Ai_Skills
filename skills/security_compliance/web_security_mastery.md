# Advanced Web Security & Identity Mastery | احتراف أمن الويب والهوية المتقدم

## Arabic Description | وصف بالعربية
قواعد هندسية متقدمة لتأمين تطبيقات الويب وإدارة الهوية. تركز القواعد على بروتوكولات OAuth2/OIDC، تقنيات المصادقة الحديثة (Passkeys)، سياسات أمن المحتوى (CSP)، وحماية التطبيقات من الهجمات المتقدمة في المتصفح.

---

## Strict Rules | قواعد صارمة

### 1. Modern Authentication & Passkeys
- **WebAuthn**: Prioritize WebAuthn (Passkeys) for secure, phishing-resistant authentication.
- **MFA Enforcement**: ALWAYS require Multi-Factor Authentication (MFA) for administrative and high-risk operations.

### 2. OAuth2 & OpenID Connect (OIDC)
- **Grant Types**: Use `Authorization Code Flow` with `PKCE` for both single-page and mobile applications. NEVER use the `Implicit Flow`.
- **Token Security**: Store tokens in HTTP-only, Secure, and SameSite cookies where possible. If stored in memory, ensure they are cleared on logout and tab closure.

### 3. Content Security Policy (CSP)
- **Strict CSP**: Implement a strict, nonce-based or hash-based CSP. Strictly disallow `'unsafe-inline'` and `'unsafe-eval'`.
- **Reporting**: Use `report-to` or `report-uri` to monitor CSP violations in production.

### 4. Cross-Origin Security
- **Isolation**: Enable Cross-Origin Isolation (`COOP` and `COEP` headers) to use powerful browser features like `SharedArrayBuffer` safely.
- **CORS Management**: Maintain a strict whitelist of allowed origins. NEVER use `Access-Control-Allow-Origin: *` for authenticated endpoints.

### 5. Client-Side Protection
- **XSS Mitigation**: Use Trusted Types API to prevent DOM-based XSS vulnerabilities.
- **Subresource Integrity (SRI)**: ALWAYS use SRI hashes when loading third-party scripts from CDNs.
