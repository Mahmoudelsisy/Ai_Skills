# Legacy Modernization & Systems Archaeology | تحديث الأنظمة القديمة وعلم آثار الأنظمة

## Arabic Description | وصف بالعربية
قواعد هندسية متقدمة لتحديث الأنظمة القديمة (Legacy Systems) وترحيلها من بيئات المينفريم (Mainframe) إلى السحاب (Cloud). تركز القواعد على فهم الأنظمة القديمة (COBOL, JCL)، استراتيجيات الترحيل التدريجي، وضمان سلامة البيانات خلال التحول.

---

## Strict Rules | قواعد صارمة

### 1. Systems Archaeology
- **Document Before Change**: Thoroughly document the *actual* current behavior of the legacy system, especially undocumented "features" and bug-dependencies.
- **Data Mapping**: Create a rigorous field-by-friend mapping between legacy data stores (e.g., VSAM, DB2 on Mainframe) and modern target databases.

### 2. Migration Strategies
- **Strangler Fig Pattern**: ALWAYS prefer the Strangler Fig pattern for gradual migration. Never attempt a "Big Bang" migration for critical enterprise systems.
- **Dual Writing**: Implement dual-write patterns to keep legacy and modern systems in sync during the transition period.

### 3. Legacy Tech Awareness
- **Mainframe Concepts**: Understand EBCDIC vs ASCII encoding differences during data migration.
- **Fixed-Width Handling**: Be meticulous when parsing fixed-width files and COBOL Copybooks.

### 4. Risk Mitigation & Testing
- **Shadow Mirroring**: Run production traffic through both legacy and modern systems and compare outputs for 100% parity before switching over.
- **Reverse Engineering Tests**: Write automated integration tests that use the legacy system as the "Source of Truth" to verify the new system's correctness.

### 5. Cultural & Process Management
- **Legacy Empathy**: Respect the constraints of the original developers. Focus on technical goals, not criticizing historical choices.
- **Knowledge Preservation**: Actively interview subject matter experts (SMEs) of the legacy system to capture institutional knowledge.
