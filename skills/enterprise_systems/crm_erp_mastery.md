# CRM & ERP Integration Mastery | احتراف الربط مع أنظمة CRM و ERP

## Arabic Description | وصف بالعربية
قواعد هندسية متقدمة لدمج وتوسيع الأنظمة المؤسسية الكبرى مثل Salesforce و SAP. تركز القواعد على دقة البيانات، أمن الربط (Integration Security)، والتعامل مع تدفقات العمل المعقدة (Workflows).

---

## Strict Rules | قواعد صارمة

### 1. Integration Security
- **OAuth & OIDC**: Use standard OAuth 2.0 flows for all integrations. NEVER store long-lived passwords or API keys in the integration layer.
- **Principle of Least Privilege**: Grant the integration user only the minimum permissions required for the specific integration task.

### 2. Data Integrity & Sync
- **Conflict Resolution**: Implement clear strategies for data conflicts (e.g., "Source of Truth" or "Last Write Wins").
- **Transactional Integrity**: Ensure multi-system updates are either completed everywhere or rolled back (using Sagas or Distributed Transactions).

### 3. Salesforce Mastery
- **Bulk API**: Use the Bulk API for large data transfers (>10,000 records). Avoid repetitive REST calls.
- **Apex Standards**: Follow Apex best practices (e.g., Bulkify triggers, avoid SOQL in loops).
- ** governor limits**: Strictly monitor and stay within Salesforce governor limits.

### 4. SAP & Middleware
- **BAPI/RFC Standards**: Use standard BAPIs for SAP integration. Avoid direct database access.
- **Event-Driven Integration**: Prefer event-based sync (e.g., via SAP Event Mesh) for real-time updates.

### 5. Monitoring & Error Handling
- **Dead Letter Queues**: Use DLQs for all failed integration messages.
- **Health Checks**: Implement automated health checks for all external enterprise endpoints.
