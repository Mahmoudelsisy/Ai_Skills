# TypeScript & JavaScript Standards | معايير تيب سكريبت وجافا سكريبت

## Arabic Description | وصف بالعربية
قواعد صارمة لتطوير تطبيقات TypeScript و JavaScript حديثة، مع التركيز على الأمان البرمجي، دقة الأنواع، وأفضل الممارسات.

---

## Strict Rules | قواعد صارمة

### 1. TypeScript Strict Mode
- **Strict Mode**: `strict: true` MUST be enabled in `tsconfig.json`.
- **No `any`**: Use of `any` is strictly forbidden. Use `unknown` if the type is truly unknown.

### 2. Functional Programming
- **Immutability**: Use `const` by default. Avoid `let` and never use `var`.
- **Pure Functions**: Prefer pure functions that do not mutate state.

### 3. Modern Syntax
- **ES6+**: Use arrow functions, destructuring, and spread operators where appropriate.
- **Async/Await**: Use `async/await` instead of raw Promises where possible.

### 4. Code Quality
- **ESLint/Prettier**: All code must pass ESLint rules and be formatted by Prettier.
- **Interfaces vs Types**: Use `interface` for public APIs and `type` for internal definitions/unions.
