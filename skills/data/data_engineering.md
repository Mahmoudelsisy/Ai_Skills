# High-Scale Database Engineering | هندسة قواعد البيانات للأنظمة الضخمة

## Arabic Description | وصف بالعربية
قواعد هندسية متقدمة لإدارة قواعد البيانات في الأنظمة العملاقة. تغطي القواعد التحسينات على مستوى المحرك (Database Internals)، أنواع الفهارس المتقدمة، نمذجة NoSQL للمشاريع الكبرى، واستراتيجيات ترحيل البيانات بدون توقف (Zero-downtime migrations).

---

## Strict Rules | قواعد صارمة

### 1. Advanced SQL & Relational Mastery
- **Indexing Strategy**: Use specific index types (B-Tree, GIN, GiST, BRIN) based on the query pattern. Avoid over-indexing as it degrades write performance.
- **Window Functions**: Use Window Functions (`OVER`, `PARTITION BY`) for complex analytical queries instead of inefficient self-joins.
- **CTE Usage**: Use Common Table Expressions (CTEs) for readability, but be mindful of "materialization" overhead in older database versions.

### 2. NoSQL Modeling at Scale
- **Single Table Design**: In DynamoDB/Key-Value stores, prioritize Single Table Design to minimize round-trips and leverage GSIs (Global Secondary Indexes) effectively.
- **Denormalization for Reads**: In high-scale NoSQL, denormalize data to match the "Read Query" pattern, ensuring data consistency is handled at the application layer or via background jobs.

### 3. High Availability & Scalability
- **Sharding & Partitioning**: Implement application-level or database-native sharding (e.g., Citus for Postgres) for datasets exceeding several terabytes.
- **Read Replicas**: Separate Read/Write traffic. Use a load balancer to distribute read queries across multiple read replicas.
- **Connection Multiplexing**: Use tools like `PgBouncer` to manage thousands of concurrent connections efficiently.

### 4. Zero-Downtime Operations
- **Migrations**: Database schema changes MUST follow the **Expand/Contract** pattern: 1. Add new column, 2. Dual write, 3. Backfill data, 4. Update reads to new column, 5. Stop writing to old column, 6. Remove old column.
- **Lock Management**: Avoid operations that lock large tables (e.g., adding a column with a default value in older versions). Use specialized tools like `gh-ost` or `pt-online-schema-change`.

### 5. Performance & Internals
- **Vacuum & Maintenance**: Understand and tune database-specific maintenance (e.g., Autovacuum in Postgres, Compaction in Cassandra).
- **Execution Plan Analysis**: Regularly audit slow queries. Look beyond just indexes; check for "Seq Scans," "Temp Sorts," and "Nested Loops."
- **Pool Sizing**: Optimize connection pool sizes based on database CPU cores and I/O capacity to prevent "Connection Bloat."
