# Core Engineering Principles | مبادئ الهندسة الأساسية

## Arabic Description | وصف بالعربية
هذا الملف يحتوي على القواعد الأساسية والصارمة لهندسة البرمجيات. يركز على كتابة كود نظيف، قابل للصيانة، واتباع مبادئ SOLID و DRY. يجب على الوكيل الالتزام بهذه القواعد في كل سطر برمجى يكتبه.

---

## Strict Rules | قواعد صارمة

### 1. Clean Code & Readability
- **Self-Documenting Code**: Variable and function names MUST be descriptive. Avoid abbreviations like `str` or `fn` unless they are standard in the language.
- **Function Size**: Functions MUST NOT exceed 20 lines of code. If they do, refactor into smaller units.
- **Single Responsibility (SRP)**: Each function and class MUST have one, and only one, reason to change.
- **No Magic Numbers**: Use named constants instead of raw numbers or strings.

### 2. SOLID Principles
- **S**: Single Responsibility - One class/function per task.
- **O**: Open/Closed - Code should be open for extension but closed for modification.
- **L**: Liskov Substitution - Subtypes must be substitutable for their base types.
- **I**: Interface Segregation - Don't force clients to depend on methods they do not use.
- **D**: Dependency Inversion - Depend on abstractions, not concretions.

### 3. DRY (Don't Repeat Yourself) & KISS (Keep It Simple, Stupid)
- **Zero Duplication**: Never write the same logic twice. Abstract common logic into reusable helpers.
- **Avoid Over-Engineering**: Do not implement features that are not requested. Keep the solution as simple as possible.

### 4. Error Handling
- **No Silent Failures**: Always catch and handle errors. Provide meaningful error messages.
- **Fail Fast**: Check for edge cases and invalid inputs at the beginning of functions.

### 5. Documentation
- **Comments**: Only comment on *why* something is done, not *what* is being done (the code should explain the *what*).
- **Docstrings**: Every public function and class MUST have a docstring explaining its purpose, parameters, and return values.
