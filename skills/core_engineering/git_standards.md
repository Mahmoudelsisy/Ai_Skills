# Version Control with Git | إدارة النسخ باستخدام Git

## Arabic Description | وصف بالعربية
قواعد صارمة لاستخدام Git تضمن تاريخاً نظيفاً للشيفرة البرمجية، تعاوناً سهلاً بين المطورين، وعمليات دمج (Merge) آمنة.

---

## Strict Rules | قواعد صارمة

### 1. Commit Hygiene
- **Conventional Commits**: Use conventional commit messages (e.g., `feat:`, `fix:`, `docs:`, `style:`, `refactor:`, `test:`, `chore:`).
- **Atomic Commits**: Each commit MUST represent one single logical change.
- **Commit Body**: For complex changes, provide a detailed body in the commit message explaining the "why".

### 2. Branching Strategy
- **Descriptive Names**: Use descriptive branch names (e.g., `feature/login-system`, `bugfix/issue-123`).
- **Main Branch Protection**: NEVER push directly to the `main` or `master` branch. All changes must go through a Pull Request (PR).

### 3. Pull Requests (PRs)
- **Small PRs**: Keep PRs small and focused. Large PRs are harder to review and more prone to errors.
- **Review Requirements**: All PRs MUST be reviewed and approved by at least one other engineer before merging.
- **Clear Descriptions**: PRs must have a clear description of the changes and how to verify them.

### 4. Git Workflow
- **Rebase vs Merge**: Use `git rebase` to keep a linear history when updating your branch from the main branch.
- **No Large Files**: NEVER commit large binary files or secrets to the repository. Use `git-lfs` or `.gitignore`.

### 5. Repository Maintenance
- **Cleanup**: Delete branches after they have been merged.
- **Tags**: Use semantic versioning (SemVer) and Git tags for releases.
