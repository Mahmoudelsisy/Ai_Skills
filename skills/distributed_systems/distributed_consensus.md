# Distributed Consensus & Coordination | التوافق الموزع والتنسيق

## Arabic Description | وصف بالعربية
قواعد هندسية متقدمة لضمان التوافق (Consensus) في الأنظمة الموزعة. تركز القواعد على فهم خوارزميات Raft و Paxos، وإدارة الحالة المشتركة، والتعامل مع مشكلات الانتخاب (Leader Election) في البيئات الموزعة الضخمة.

---

## Strict Rules | قواعد صارمة

### 1. Consensus Algorithm Adherence
- **Raft/Paxos Implementation**: Use well-proven libraries for consensus (e.g., Etcd, Consul) rather than building custom implementations unless for research.
- **Quorum Management**: ALWAYS ensure a quorum (N/2 + 1) is maintained for all state changes.

### 2. Leader Election
- **Term Management**: Properly handle term numbers and election timeouts to prevent "Split Brain" scenarios.
- **Failover Speed**: Optimize leader election timeouts to balance between system availability and stability.

### 3. Log Replication & Safety
- **Log Matching**: Ensure logs are replicated in the correct order to all followers.
- **Commit Safety**: A log entry is only considered "Committed" after it has been replicated to a majority of nodes.

### 4. Distributed State Machines
- **Determinism**: The state machine MUST be strictly deterministic. Given the same inputs in the same order, it must produce the exact same state.
- **Snapshots**: Implement log compaction and snapshotting to prevent logs from growing indefinitely.

### 5. Membership Changes
- **Dynamic Membership**: Handle adding or removing nodes from the cluster without downtime using joint consensus patterns.
