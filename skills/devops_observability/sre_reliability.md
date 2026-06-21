# Elite Site Reliability & Resilience | هندسة الموثوقية الفائقة والمرونة

## Arabic Description | وصف بالعربية
قواعد هندسية متقدمة من مستوى النخبة لضمان موثوقية الأنظمة (SRE). تغطي القواعد هندسة الفوضى (Chaos Engineering)، ميزانيات الأخطاء (Error Budgets)، وهندسة زمن الاستجابة (Latency Engineering) مع التركيز على P99 والتعامل مع حالات الفشل كحدث طبيعي.

---

## Strict Rules | قواعد صارمة

### 1. Advanced Reliability Concepts
- **Error Budgets as a Policy**: Use error budgets to determine the balance between velocity and reliability. If the budget is exhausted, freeze all non-security feature releases.
- **Chaos Engineering**: Regularly perform chaos experiments (fault injection) in staging and production to uncover hidden weaknesses.

### 2. Latency & Tail Engineering
- **P99 Focus**: Optimize for the 99th percentile (P99) latency, not just the average or median. Identify and fix "Tail Latency" causes.
- **Edge Performance**: Utilize Edge Computing and Global CDNs to minimize network latency for a global user base.

### 3. Operational Excellence (Elite)
- **Actionable Runbooks**: Maintain executable Runbooks and Playbooks for every high-fidelity alert.
- **Alert Fatigue Management**: Strictly eliminate alerts that don't require immediate human action. Every alert MUST be a symptom of a user-facing problem.

### 4. Incident & Crisis Management
- **RCA (Root Cause Analysis)**: Perform deep RCA for every production incident. Look for structural and process failures, not just human errors.
- **Blame-Free Postmortems**: Focus on learning and system improvement. Postmortems MUST be published and searchable for the entire team.

### 5. On-Call Efficiency
- **Automation of Toil**: Any manual operation performed more than twice MUST be considered "Toil" and prioritized for automation.
- **On-Call Handover**: Maintain a strict handover process between on-call shifts to ensure no information is lost.
