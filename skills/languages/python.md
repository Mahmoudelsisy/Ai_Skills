# Python Professional Standards | معايير بايثون الاحترافية

## Arabic Description | وصف بالعربية
هذا الملف يحدد القواعد الصارمة لكتابة كود بايثون احترافي. يركز على النوعية (Type Hinting)، التنسيق القياسي (PEP 8)، وكفاءة الأداء.

---

## Strict Rules | قواعد صارمة

### 1. Type Hinting
- **Mandatory Typing**: ALL function signatures MUST have type hints for parameters and return values.
- **No `Any`**: Avoid using `Any` unless absolutely necessary. Use `Union`, `Optional`, or generics.

### 2. Standards (PEP 8)
- **Compliance**: Follow PEP 8 strictly (indentation, spacing, naming conventions).
- **Naming**: Use `snake_case` for functions/variables and `PascalCase` for classes.

### 3. Asynchronous Programming
- **Async/Await**: Use `asyncio` for I/O bound tasks. Avoid blocking calls in async functions.

### 4. Dependency Management
- **Explicit Imports**: Avoid `from module import *`. Be explicit.
- **Virtual Environments**: Always use `venv` or `poetry`.

### 5. Testing
- **Pytest**: Use `pytest` for testing. Aim for 80%+ coverage.
