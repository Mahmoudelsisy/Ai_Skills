# Data Engineering & Database Management | هندسة البيانات وإدارة قواعد البيانات

## Arabic Description | وصف بالعربية
قواعد صارمة لإدارة البيانات، تصميم الجداول، وبناء أنابيب البيانات (Data Pipelines). تضمن هذه القواعد دقة البيانات، سرعتها، وسهولة الوصول إليها.

---

## Strict Rules | قواعد صارمة

### 1. Data Modeling
- **Normalization**: Use 3NF (Third Normal Form) for relational databases unless denormalization is required for performance.
- **Schema Design**: Always define clear schemas for NoSQL databases (e.g., using Mongoose for MongoDB) to maintain data integrity.

### 2. SQL Optimization
- **Query Performance**: NEVER use `SELECT *`. Always select specific columns.
- **Explain Plans**: Use `EXPLAIN` to analyze and optimize slow queries.
- **Transactions**: Use ACID transactions for operations that modify multiple related tables.

### 3. Data Pipelines (ETL/ELT)
- **Idempotency**: All data processing steps MUST be idempotent (running the same step twice should not duplicate data).
- **Failure Recovery**: Implement retries and dead-letter queues for failed pipeline stages.

### 4. Data Privacy & Security
- **PII Protection**: Mask or encrypt Personally Identifiable Information (PII) at all times.
- **Access Control**: Implement Row-Level Security (RLS) if the database supports it and is required by business logic.

### 5. Big Data & Warehousing
- **Partitioning**: Partition large tables by date or logical keys to improve query speed.
- **Compression**: Use columnar storage and compression for analytical workloads (OLAP).
