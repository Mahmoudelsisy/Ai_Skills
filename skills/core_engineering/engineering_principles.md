# Core Software Engineering Mastery | احتراف هندسة البرمجيات الأساسية

## Arabic Description | وصف بالعربية
القواعد الجوهرية التي تشكل الفرق بين "المبرمج" و "المهندس". تغطي هذه القواعد مبادئ Clean Code، الـ SOLID بكل تفاصيلها، والمبادئ الذهبية للبساطة (KISS, DRY, YAGNI, SoC).

---

## Strict Rules | قواعد صارمة

### 1. Advanced Clean Code (Naming & Structure)
- **Contextual Naming**: Names MUST be descriptive but avoid redundancy (e.g., `user.id`, not `user.userId`).
- **Function Purity**: Functions MUST be small, have no side effects where possible, and strictly follow the "Do One Thing" principle.
- **Vertical Formatting**: Keep related code close together vertically. Variables should be declared close to their first use.

### 2. SOLID Principles (Deep Integration)
- **S (SRP)**: Each module/class MUST have a single reason to change. Separate business logic from data access and UI.
- **O (OCP)**: Design for extension using interfaces or abstract classes. Avoid modifying existing, tested code for new features.
- **L (LSP)**: Subclasses MUST be completely substitutable for their base classes without breaking the system.
- **I (ISP)**: Create small, specific interfaces. Clients should not be forced to depend on methods they do not use.
- **D (DIP)**: Depend on abstractions, not concretions. Use Dependency Injection (DI) strictly.

### 3. Golden Simplicity Principles
- **DRY (Don't Repeat Yourself)**: Eliminate logical duplication. Every piece of knowledge must have a single, unambiguous representation.
- **KISS (Keep It Simple, Stupid)**: Avoid over-engineering. The simplest solution that works is usually the best.
- **YAGNI (You Aren’t Gonna Need It)**: NEVER implement functionality until it is actually needed.
- **SoC (Separation of Concerns)**: Divide the system into distinct sections, each addressing a separate concern (e.g., layers, modules).

### 4. Advanced Code Quality & Anti-patterns
- **Identify Code Smells**: Actively refactor "God Classes," "Long Methods," "Spaghetti Code," and "Dead Code."
- **No Magic Numbers**: Use well-named constants or enums for all literal values.
- **Coupling & Cohesion**: Aim for Low Coupling (minimal dependencies between modules) and High Cohesion (related logic grouped together).

### 5. Professional Refactoring
- **Atomic Refactoring**: Refactor in small steps. Use automated tools where possible.
- **Characterization Tests**: Write tests for existing behavior before refactoring legacy code.
