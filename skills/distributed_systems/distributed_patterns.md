# Advanced Distributed Systems & Mastery | احتراف الأنظمة الموزعة المتقدمة

## Arabic Description | وصف بالعربية
قواعد هندسية من مستوى النخبة للأنظمة الموزعة. يركز هذا الملف على حل المشاكل الحقيقية (Real-world problems) مثل Clock Drift و Network Partitions، مع جداول مفاضلة شاملة وأطر لاتخاذ القرار وسيناريوهات الفشل المعقدة.

---

## Decision Framework: Consistency Model
| Model | Pros | Cons | When to Use |
|---|---|---|---|
| Strong Consistency | No data anomalies, simple logic | High latency, low availability | Financial transactions, critical metadata |
| Eventual Consistency | High availability, low latency | Stale reads, complex conflict resolution | Social media feeds, analytics, profiles |
| Causal Consistency | Better user experience (monotonic) | Performance overhead for tracking | Chat apps, comment threads |

---

## Strict Rules | قواعد صارمة

### 1. Resilience & Reliability
- **Transactional Outbox**: ALWAYS use the Outbox pattern when a database update MUST trigger an external event. Never use dual-writes without an atomic boundary.
- **Idempotency Everywhere**: EVERY distributed API and message consumer MUST be idempotent. Support `Idempotency-Key` or unique event IDs.

### 2. Time & Ordering
- **Clock Drift**: NEVER trust system time for ordering events across different servers. Use Logical Clocks (Lamport) or Hybrid Logical Clocks (HLC).
- **Consensus**: Use established consensus algorithms (Raft/Paxos) via tools like Etcd or Consul for critical shared state.

### 3. Traffic Control
- **Load Shedding**: Implement adaptive load shedding at the entry point. Reject non-critical traffic when system health (CPU/Memory/Latency) is degraded.
- **Backpressure**: Propagate pressure signals upstream. If a consumer is slow, the producer MUST slow down or buffer limitedly.

---

## Failure Scenarios: Real-World Issues
1. **Scenario**: Network Partition between two data centers (Split Brain).
   - **Handling**: Quorum-based writes MUST fail if a majority is not reached. Read-only mode for the minority partition.
2. **Scenario**: Consumer group lag in Kafka increases significantly.
   - **Handling**: Automated alerts MUST trigger. Scale consumer count if CPU permits; otherwise, identify and fix the processing bottleneck (e.g., slow DB query).

---

## Production Checkpoints
- [ ] Is every distributed transaction wrapped in a Saga or compensated correctly?
- [ ] Are all external calls protected by a Circuit Breaker with a tested fallback?
- [ ] Do we have visibility into end-to-end trace IDs across all services?
