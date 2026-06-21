# Business Logic & Project Management | منطق الأعمال وإدارة المشاريع

## Arabic Description | وصف بالعربية
قواعد لضمان توافق الكود مع متطلبات الأعمال، وإدارة المشروع بطريقة منظمة تضمن تحقيق الأهداف التقنية والتجارية.

---

## Strict Rules | قواعد صارمة

### 1. Requirement Alignment
- **Feature Focus**: Every line of code MUST contribute to a documented business requirement.
- **Scope Creep**: Do not implement "nice-to-have" features unless they are officially part of the sprint/task.

### 2. Documentation & Communication
- **Changelogs**: Maintain a `CHANGELOG.md` following the "Keep a Changelog" standard.
- **Commit Messages**: Use Conventional Commits (e.g., `feat:`, `fix:`, `docs:`, `chore:`).

### 3. Task Management
- **Atomic Commits**: Each commit should represent a single, logical change.
- **PR Descriptions**: Pull requests MUST have a clear description of changes, why they were made, and how to test them.

### 4. Technical Debt
- **Tracking**: Document technical debt when it is incurred.
- **Refactoring**: Allocate time in each cycle for refactoring and paying down technical debt.

### 5. Quality Assurance
- **User Acceptance**: Test features against the original business acceptance criteria.
- **Edge Cases**: Business logic must handle edge cases like missing data or invalid states gracefully.
