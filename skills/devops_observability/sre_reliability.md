# Site Reliability Engineering (SRE) | هندسة موثوقية المواقع

## Arabic Description | وصف بالعربية
قواعد صارمة لهندسة موثوقية الأنظمة (SRE) تضمن أن الأنظمة البرمجية تعمل بكفاءة عالية وتوافر مستمر، مع التركيز على القياس، الأتمتة، وإدارة الحوادث.

---

## Strict Rules | قواعد صارمة

### 1. Measurement (SLI/SLO)
- **Define Indicators (SLI)**: Clearly define Service Level Indicators (e.g., latency, error rate, availability).
- **Set Objectives (SLO)**: Establish target values for SLIs that reflect user satisfaction.
- **Error Budgets**: Use error budgets to balance the speed of innovation with the stability of the system.

### 2. Incident Management
- **On-Call Standards**: Follow a structured on-call rotation with clear escalation paths.
- **Blame-Free Post-mortems**: Conduct post-mortems after every major incident to identify root causes and prevent recurrence without blaming individuals.

### 3. Automation & Toil
- **Eliminate Toil**: Actively automate repetitive, manual tasks (toil).
- **Self-Healing**: Implement self-healing mechanisms (e.g., automated restarts, circuit breakers).

### 4. Change Management
- **Canary Deployments**: Use canary releases to test changes on a small percentage of users before a full rollout.
- **Rollback Strategy**: Every change MUST have a tested and automated rollback plan.

### 5. Monitoring & Alerting
- **Actionable Alerts**: Only alert on issues that require human intervention. Avoid "alert fatigue."
- **Symptoms over Causes**: Prioritize alerting on user-facing symptoms (e.g., "500 errors are up") rather than internal causes (e.g., "CPU is at 90%").
