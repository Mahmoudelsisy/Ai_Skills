# AWS Well-Architected & Enterprise Cloud | احتراف السحاب وإطار العمل الجيد من AWS

## Arabic Description | وصف بالعربية
قواعد هندسية متقدمة لاحتراف السحاب باستخدام إطار عمل "AWS Well-Architected". تركز القواعد على الموثوقية (Reliability)، التميز التشغيلي، استراتيجيات الحسابات المتعددة (Multi-account)، والتعامل مع الكوارث (DR).

---

## Strict Rules | قواعد صارمة

### 1. Multi-Account Strategy
- **Control Tower & Organizations**: Use AWS Organizations with Control Tower to manage multiple accounts. Enforce Service Control Policies (SCPs) for centralized guardrails.
- **Isolation**: Separate workloads into dedicated accounts (Dev, Staging, Prod, Security, Shared Services) to minimize the blast radius of errors or compromises.

### 2. Networking (VPC Mastery)
- **VPC Peering vs Transit Gateway**: Use Transit Gateway for complex hub-and-spoke networking. Prefer PrivateLink for secure, private service consumption.
- **Subnet Strategy**: Strictly use private subnets for all internal services. Use NAT Gateways (or better, NAT instances for cost) for egress traffic only.

### 3. Reliability & Disaster Recovery (DR)
- **RTO/RPO Targets**: Define and strictly adhere to Recovery Time Objective (RTO) and Recovery Point Objective (RPO) based on business criticality.
- **DR Strategies**: Implement appropriate DR patterns: Backup & Restore, Pilot Light, Warm Standby, or Multi-site (Active-Active).

### 4. Advanced IAM Patterns
- **Identity Federation**: Use OIDC or SAML for federating identity with external providers. Avoid creating long-lived IAM Users.
- **Permission Boundaries**: Use IAM Permission Boundaries to limit the maximum permissions a developer or role can have.

### 5. Cost & Operational Excellence
- **Compute Optimizer**: Regularly review and apply recommendations from AWS Compute Optimizer.
- **Infrastructure Lifecycle**: Use AWS Config and CloudTrail to maintain a complete history of resource changes and ensure continuous compliance.
