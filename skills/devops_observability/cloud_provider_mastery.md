# Cloud Provider Mastery (AWS, GCP, Azure) | احتراف مزودي الخدمات السحابية

## Arabic Description | وصف بالعربية
قواعد هندسية متقدمة لاحتراف مزودي الخدمات السحابية الثلاثة الكبار (AWS, GCP, Azure). تركز القواعد على اختيار الخدمة الصحيحة، تحسين التكلفة، وإدارة الموارد بأمان واحترافية.

---

## Strict Rules | قواعد صارمة

### 1. Amazon Web Services (AWS)
- **IAM Best Practices**: Use IAM Roles for EC2/Lambda; never use IAM User Access Keys in code. Enforce MFA for all console users.
- **Compute Selection**: Prefer Lambda for event-driven, Fargate for containerized, and Spot Instances for non-critical interruptible workloads to save costs.
- **Networking**: Use VPC Endpoints for S3/DynamoDB to keep traffic within the AWS network.

### 2. Google Cloud Platform (GCP)
- **Project Structure**: Organize resources using Folders and Projects for clear billing and permission isolation.
- **GKE Standards**: Use Autopilot mode for GKE unless fine-grained control over nodes is strictly required. Implement Workload Identity for pod-to-GCP-service auth.
- **BigQuery Efficiency**: Use partitioned and clustered tables. Avoid `SELECT *` to minimize query costs.

### 3. Microsoft Azure
- **Resource Groups**: Logically group all resources for a specific application or environment. Use Tags for cost tracking.
- **Managed Identities**: Use Azure Managed Identities for secure authentication between Azure services (e.g., App Service to Key Vault).
- **Service Plans**: Monitor and scale App Service Plans based on memory and CPU pressure. Use Elastic Premium for Functions.

### 4. Cross-Cloud Governance
- **Tagging Policy**: Implement a mandatory tagging policy for all resources (Owner, Environment, CostCenter).
- **Cost Guardrails**: Set up billing alerts and budgets at the account/subscription level.
- **Region Selection**: Choose regions based on compliance (Data Residency) and latency to the end user.

### 5. Cloud Security (Mastery)
- **Encryption**: Enable Default Encryption for all storage (S3/GCS/Blob). Use customer-managed keys (KMS/Cloud KMS/Key Vault) for highly sensitive data.
- **VPC Hardening**: Implement Network Security Groups (NSG) or Firewall rules to block all traffic by default (Deny All).
