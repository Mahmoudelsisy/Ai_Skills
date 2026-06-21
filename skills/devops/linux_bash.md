# Linux, Bash & Shell Scripting | لينكس وبرمجة الشل

## Arabic Description | وصف بالعربية
قواعد صارمة للتعامل مع أنظمة لينكس وكتابة سكربتات Bash احترافية. تركز هذه القواعد على الأمان، قابلية القراءة، وإدارة النظام بكفاءة.

---

## Strict Rules | قواعد صارمة

### 1. Bash Scripting Safety
- **Strict Mode**: Every script MUST start with `set -euo pipefail` to catch errors and undefined variables.
- **Quoting**: ALWAYS quote variables (e.g., `"$VAR"`) to prevent word splitting and globbing issues.
- **Shebang**: Use a proper shebang (e.g., `#!/usr/bin/env bash`).

### 2. Scripting Best Practices
- **Functionality**: Use functions to modularize logic. Avoid giant scripts with global state.
- **Comments**: Document the purpose and usage of the script at the top.
- **Error Handling**: Use `trap` for cleanup on script exit or error.

### 3. System Administration
- **Permissions**: Follow the principle of least privilege. Never use `sudo` unless absolutely necessary.
- **Automation**: Prefer idempotent tools (like Ansible) for complex system configurations, but use shell scripts for simple tasks.
- **Log Management**: Redirect output to logs properly (`stdout` and `stderr`). Use `logger` for system logs.

### 4. Command Line Usage
- **Pipe Safety**: Be mindful of long pipe chains. Break them down if they become unreadable.
- **Aliases**: Avoid using aliases in scripts; use full command names for clarity and portability.

### 5. File Management
- **Temp Files**: Use `mktemp` for creating temporary files securely.
- **Path Handling**: Use absolute paths in scripts when possible, or define a base directory variable.
