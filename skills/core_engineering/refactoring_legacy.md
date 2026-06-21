# Refactoring & Legacy Code Management | إعادة الهيكلة وإدارة الكود القديم

## Arabic Description | وصف بالعربية
قواعد صارمة للتعامل مع الشيفرة البرمجية القديمة (Legacy Code) وإعادة هيكلتها (Refactoring) بأمان دون كسر الوظائف الحالية، مع التركيز على تحسين الجودة تدريجياً.

---

## Strict Rules | قواعد صارمة

### 1. Safety First
- **Test Baseline**: NEVER refactor code that doesn't have test coverage. Create tests first to establish a baseline.
- **Small Steps**: Refactor in small, incremental steps. Commit frequently.

### 2. Refactoring Patterns
- **Boy Scout Rule**: Always leave the code slightly cleaner than you found it.
- **Identify Smells**: Recognize and eliminate code smells (e.g., Long Methods, God Classes, Duplicated Code).
- **Safe Patterns**: Use established refactoring patterns (e.g., Extract Method, Rename Variable, Replace Conditional with Polymorphism).

### 3. Handling Legacy Systems
- **Strangler Fig Pattern**: Gradually replace legacy functionality with new code by wrapping it in an interceptor.
- **Characterization Tests**: Use characterization tests to document the *actual* behavior of the legacy code before changing it.

### 4. Technical Debt
- **Document Debt**: When you encounter technical debt that you cannot fix immediately, document it in a central tracking system.
- **Prioritization**: Prioritize refactoring areas that are frequently changed or have high bug density.

### 5. Quality Improvement
- **Continuous Improvement**: Integrate refactoring into the daily development workflow, not as a separate phase.
- **Code Reviews**: Specifically review refactoring changes for potential regressions in behavior.
