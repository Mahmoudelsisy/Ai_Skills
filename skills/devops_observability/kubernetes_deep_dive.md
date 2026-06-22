# Kubernetes (K8s) Deep Dive Mastery | الغوص العميق في كوبيرنيتيس

## Arabic Description | وصف بالعربية
قواعد هندسية متقدمة للغوص في أعماق Kubernetes. تركز القواعد على فهم آلية الجدولة (Scheduling)، نماذج الشبكات (CNI)، استخدام Service Mesh (Istio)، وإدارة أحمال العمل ذات الحالة (Stateful) وتوسيع النظام بشكل تلقائي ومتقدم.

---

## Strict Rules | قواعد صارمة

### 1. Scheduler Internals & Resource Control
- **Advanced Scheduling**: Use `nodeAffinity`, `taints`, and `tolerations` to control pod placement strictly. Implement `topologySpreadConstraints` for high availability across zones.
- **VPA & HPA**: Use Horizontal Pod Autoscaler (HPA) for scaling instances and Vertical Pod Autoscaler (VPA) for optimizing resource requests/limits over time.

### 2. Networking & CNI
- **CNI Selection**: Choose the right CNI (e.g., Cilium for eBPF-based security, Calico for robust network policies) based on organization needs.
- **Network Policies**: Implement strict default-deny network policies for all namespaces. Only allow explicit required communication.

### 3. Service Mesh (Istio / Linkerd)
- **Traffic Management**: Use the Service Mesh for Canary releases, circuit breaking, and traffic mirroring.
- **mTLS & Security**: Enforce mutual TLS (mTLS) for all inter-pod communication to ensure zero-trust security.

### 4. Stateful Workloads
- **StatefulSets & PVs**: Use `StatefulSets` for databases. Ensure `volumeClaimTemplates` are configured for persistent, high-performance storage.
- **Operator Pattern**: Use K8s Operators for managing complex stateful applications (e.g., automated DB backups, failover).

### 5. Production Reliability (K8s)
- **Admission Controllers**: Use Validating and Mutating Admission Webhooks (e.g., Kyverno, OPA Gatekeeper) to enforce best practices at deployment time.
- **Cluster Autoscaling**: Configure the Cluster Autoscaler or Karpenter to manage underlying node capacity efficiently based on pod requirements.
