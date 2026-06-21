# Docker & Kubernetes (Orchestration) | دوكر وكوبيرنيتيس (الأتمتة)

## Arabic Description | وصف بالعربية
قواعد صارمة لإدارة الحاويات (Containers) وأتمتتها باستخدام Kubernetes. تضمن هذه القواعد الأمان، خفة الوزن، والقدرة على التوسع (Scalability) في بيئات الإنتاج.

---

## Strict Rules | قواعد صارمة

### 1. Docker Best Practices
- **Multi-stage Builds**: ALWAYS use multi-stage builds to keep production images small and secure.
- **No Root User**: Run applications inside the container as a non-root user.
- **Layers Optimization**: Minimize the number of layers by combining `RUN` commands. Use `.dockerignore`.

### 2. Kubernetes Fundamentals
- **Declarative YAML**: All K8s resources MUST be managed via declarative YAML files, never via `kubectl run`.
- **Labels & Selectors**: Use consistent labels for all resources to facilitate management and monitoring.

### 3. Resource Management
- **Requests & Limits**: Every container MUST have CPU and Memory requests and limits defined.
- **Liveness & Readiness**: Define proper liveness and readiness probes for all deployments to ensure traffic only goes to healthy pods.

### 4. Security in K8s
- **Secrets Management**: Use K8s Secrets (or better, an external Vault) for sensitive data. Never store secrets in ConfigMaps or Environment variables in YAML.
- **Network Policies**: Implement Network Policies to restrict traffic between pods (Principle of Least Privilege).

### 5. Config & State
- **ConfigMaps**: Use ConfigMaps for application configurations that are not sensitive.
- **Stateless Apps**: Prefer stateless deployments. For stateful apps, use `StatefulSets` and persistent volumes carefully.
