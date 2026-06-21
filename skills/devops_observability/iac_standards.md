# Infrastructure as Code (IaC) | البنية التحتية كشيفرة برمجية

## Arabic Description | وصف بالعربية
قواعد صارمة لإدارة البنية التحتية باستخدام أدوات مثل Terraform و Ansible. تضمن هذه القواعد أن تكون البيئات التقنية قابلة لإعادة الإنتاج (Reproducible)، آمنة، وسهلة الإدارة.

---

## Strict Rules | قواعد صارمة

### 1. Terraform Best Practices
- **Remote State**: ALWAYS use a remote backend with state locking (e.g., S3 with DynamoDB) to prevent state corruption.
- **Modularity**: Organize code into reusable modules. Avoid large, monolithic `main.tf` files.
- **Plan Verification**: Always review the output of `terraform plan` before applying changes in production.

### 2. Ansible Standards
- **Idempotency**: All playbooks MUST be idempotent. Running them multiple times should not change the system state after the first run.
- **Variables**: Use `group_vars` and `host_vars` for configuration. Never hardcode values in tasks.
- **Role-Based**: Organize tasks into roles for better reuse and maintainability.

### 3. Security in IaC
- **Secret Management**: Never store secrets in plain text. Use Ansible Vault or integration with Secret Managers (AWS Secrets Manager, HashiCorp Vault).
- **Least Privilege**: Grant the IaC execution identity only the minimum permissions required to create/modify resources.

### 4. Version Control & CI/CD
- **Code Reviews**: Every infrastructure change MUST be reviewed through a Pull Request.
- **Automated Linting**: Use tools like `tflint` or `ansible-lint` to enforce coding standards.

### 5. State Management & Drift
- **No Manual Changes**: Avoid making changes via the cloud console. Use IaC for everything to prevent "configuration drift."
- **Drift Detection**: Regularly run plans or use automated tools to detect if the actual state matches the defined code.
