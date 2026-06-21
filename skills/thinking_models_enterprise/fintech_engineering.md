# Fintech Engineering & Financial Systems | هندسة التقنيات المالية والأنظمة المالية

## Arabic Description | وصف بالعربية
قواعد صارمة لتطوير الأنظمة المالية (Fintech). تركز هذه القواعد على سلامة المعاملات (Transaction Integrity)، الامتثال للوائح المالية، والأمان الفائق لمنع الاحتيال وحماية الأصول.

---

## Strict Rules | قواعد صارمة

### 1. Transaction Integrity & ACID
- **Atomic Transactions**: All financial operations MUST be atomic. Either the entire transaction succeeds, or it is rolled back completely.
- **Idempotency**: All payment and transfer APIs MUST be idempotent to prevent double-charging or duplicate transfers.
- **Precision**: Never use floating-point numbers for currency. Use specialized decimal types or represent values in the smallest unit (e.g., cents).

### 2. Security & Fraud Prevention
- **PCI-DSS Compliance**: Follow PCI-DSS standards for handling credit card data. Never store raw CVV or magnetic stripe data.
- **Audit Trails**: Maintain an immutable, detailed log of every financial transaction and sensitive configuration change.
- **KYC/AML**: Implement robust Know Your Customer (KYC) and Anti-Money Laundering (AML) checks in the workflow.

### 3. Reliability & Reconciliation
- **Automated Reconciliation**: Implement daily automated reconciliation between internal ledgers and external bank/gateway statements.
- **Error Handling**: Use structured error codes for financial failures to allow for specific recovery actions.

### 4. High-Performance Trading (If applicable)
- **Low Latency**: Optimize critical paths for minimal latency. Use efficient data structures and zero-copy techniques.
- **Determinism**: Ensure processing times are consistent and deterministic.

### 5. Regulatory Compliance
- **Data Residency**: Adhere to local data residency laws for financial data.
- **Reporting**: Automate the generation of required regulatory and financial reports.
