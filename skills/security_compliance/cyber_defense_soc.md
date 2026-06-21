# Cyber Defense & SOC Mastery | احتراف الدفاع السيبراني وعمليات الأمن

## Arabic Description | وصف بالعربية
قواعد هندسية متقدمة للدفاع عن الأنظمة وإدارة مراكز العمليات الأمنية (SOC). تركز القواعد على كشف التهديدات، الاستجابة للحوادث، وتحصين البنية التحتية ضد الهجمات المتطورة.

---

## Strict Rules | قواعد صارمة

### 1. Detection & SIEM Standards
- **Log Aggregation**: Centralize all logs (CloudTrail, Syslog, Web Server) into a SIEM (e.g., Splunk, ELK, Sentinel).
- **Correlation Rules**: Create high-fidelity detection rules based on the MITRE ATT&CK framework.
- **Noise Reduction**: Continuously tune alerts to minimize false positives and focus on critical threats.

### 2. Incident Response (IR)
- **Playbook Execution**: Implement automated or semi-automated playbooks for common incidents (e.g., compromised credentials, malware detected).
- **Containment First**: Prioritize isolation and containment of the affected systems to prevent lateral movement.
- **Evidence Preservation**: Follow forensic standards for preserving evidence during and after an incident.

### 3. Infrastructure Hardening
- **OS Hardening**: Disable unnecessary services and protocols. Use CIS Benchmarks for baseline configurations.
- **Container Security**: Implement runtime security (e.g., Sysdig, Falco) to detect anomalous container behavior.
- **VPC Flow Logs**: Enable and monitor VPC flow logs to identify suspicious network traffic.

### 4. Threat Hunting
- **Proactive Hunting**: Regularly search for indicators of compromise (IoCs) that may have bypassed automated detections.
- **Intelligence Integration**: Integrate internal detections with external threat intelligence feeds (STIX/TAXII).

### 5. Vulnerability & Patch Management
- **Risk-Based Patching**: Prioritize patching based on exploitability (EPSS) and business criticality of the asset.
- **Continuous Scanning**: Run weekly or daily vulnerability scans on all production endpoints.
