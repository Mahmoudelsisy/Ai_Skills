# Compliance, Privacy & Data Protection | الامتثال، الخصوصية وحماية البيانات

## Arabic Description | وصف بالعربية
قواعد صارمة لضمان امتثال البرمجيات للقوانين العالمية لحماية البيانات مثل GDPR و HIPAA. تهدف هذه القواعد إلى حماية خصوصية المستخدمين وتجنب المخاطر القانونية.

---

## Strict Rules | قواعد صارمة

### 1. Data Minimization
- **Collect Only what is Needed**: NEVER collect or store user data that is not essential for the application's function.
- **Retention Policy**: Implement automated data deletion policies for data that is no longer needed.

### 2. Privacy by Design
- **Default Privacy**: Ensure the most privacy-restrictive settings are the default for all users.
- **Anonymization**: Anonymize or pseudonymize sensitive data whenever possible, especially for analytics and testing.

### 3. Compliance Standards (GDPR/HIPAA)
- **User Consent**: Implement clear and explicit consent mechanisms for data collection.
- **Right to be Forgotten**: Provide users with a simple way to delete their entire account and all associated data.
- **Audit Logs**: Maintain detailed audit logs of who accessed sensitive data and when.

### 4. Data Security
- **Encryption**: All PII (Personally Identifiable Information) and PHI (Protected Health Information) MUST be encrypted both in transit and at rest.
- **Access Control**: Use RBAC (Role-Based Access Control) to limit data access to the minimum necessary personnel.

### 5. Third-Party Management
- **Vendor Assessment**: Review the privacy practices of any third-party services (SaaS, APIs) before integration.
- **Data Processing Agreements**: Ensure legal agreements are in place for any data shared with third parties.
