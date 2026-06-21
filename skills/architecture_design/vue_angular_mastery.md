# Enterprise Vue & Angular Mastery | احتراف إطاري عمل فيو وأنجولار للمؤسسات

## Arabic Description | وصف بالعربية
قواعد هندسية متقدمة لاحتراف إطاري عمل Vue 3 و Angular في المشاريع الضخمة. تركز القواعد على المعمارية النظيفة، تحسين الأداء في المتصفح، وإدارة الحالة (State) بكفاءة عالية.

---

## Strict Rules | قواعد صارمة

### 1. Vue 3 (Composition API)
- **Composition API**: Use the Composition API with `<script setup>` for all new components. Avoid the Options API in large projects.
- **State Management**: Use Pinia for global state. Strictly use "Store-to-Refs" and maintain small, modular stores.
- **Reactivity mastery**: Be careful with `shallowRef` and `shallowReactive` to optimize performance for large, nested objects.

### 2. Angular (Enterprise)
- **Signals & RxJS**: Transition to Angular Signals for reactive state where possible. Use RxJS strictly for asynchronous streams and event handling.
- **OnPush Change Detection**: Use `ChangeDetectionStrategy.OnPush` by default to minimize change detection cycles.
- **Strict Typing**: Enforce strict template type checking and `noImplicitAny` in `tsconfig.json`.

### 3. Frontend Architecture
- **Feature Modules**: Organize the application into lazy-loaded feature modules to improve initial load time.
- **Smart vs Dumb Components**: Separate components into "Smart" (handle logic/data) and "Dumb" (pure UI/presentation).

### 4. Performance & Rendering
- **Virtual Scrolling**: Use virtual scrolling for long lists (e.g., CDK Virtual Scroll in Angular).
- **Component Lifecycle**: Properly clean up subscriptions (RxJS `takeUntilDestroyed`) and event listeners to prevent memory leaks.

### 5. Testing & Tooling
- **Unit Testing**: Use Vitest (Vue) or Jasmine/Karma (Angular) for logic testing.
- **Storybook**: Develop UI components in isolation using Storybook for better reusability and documentation.
