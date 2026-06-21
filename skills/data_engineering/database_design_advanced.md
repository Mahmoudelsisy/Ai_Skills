# Advanced Database Engineering & Design | هندسة وتصميم قواعد البيانات المتقدمة

## Arabic Description | وصف بالعربية
قواعد هندسية عميقة لتصميم وإدارة قواعد البيانات في المشاريع الضخمة. تغطي القواعد مبادئ ACID، استراتيجيات الـ Sharding والـ Replication، تحسين الاستعلامات (Query Optimization)، وإدارة التكرار (Caching).

---

## Strict Rules | قواعد صارمة

### 1. Relational Integrity & Transactions
- **ACID Compliance**: Ensure all business-critical transactions follow Atomicity, Consistency, Isolation, and Durability.
- **Normalization vs Denormalization**: Normalize for data integrity by default (3NF). Denormalize consciously for performance only in hot read paths.

### 2. Scalability & High Availability
- **Replication**: Use Primary-Replica architecture for read scaling. Use Synchronous replication for high consistency and Asynchronous for performance.
- **Sharding**: Implement horizontal sharding based on a logical shard key (e.g., `tenant_id` or `user_id`) when a single instance cannot handle the load.
- **Failover**: Implement automated failover mechanisms for primary database instances.

### 3. Query Optimization & Internals
- **Explain Plans**: Regularly audit slow queries using `EXPLAIN ANALYZE`. Fix "Full Table Scans" on large tables.
- **Index Selection**: Choose appropriate indexes (B-Tree, GIN, Hash). Avoid redundant indexes.
- **Partitioning**: Use table partitioning (e.g., by date) for large datasets to speed up queries and maintenance.

### 4. Advanced NoSQL Modeling
- **Key-Value & Document**: Use the correct NoSQL type for the use case. Master "Single Table Design" for performance in Key-Value stores.
- **CAP Theorem in Practice**: Choose the right database (e.g., Cassandra for Availability, MongoDB for Consistency) based on the application's needs.

### 5. Caching & Persistence
- **Redis Caching**: Use Redis for low-latency data access. Implement Cache Invalidation strategies (e.g., Cache-Aside, Write-Through).
- **Persistence Tuning**: Optimize database write performance by tuning WAL (Write Ahead Log) and checkpointing behavior.
