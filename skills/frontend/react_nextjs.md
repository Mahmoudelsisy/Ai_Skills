# React & Next.js Professional Standards | معايير ريأكت ونيكست جيه إس الاحترافية

## Arabic Description | وصف بالعربية
قواعد صارمة لتطوير تطبيقات ويب حديثة باستخدام React و Next.js. تركز هذه القواعد على تحسين الأداء (Rendering), إدارة الحالة (State), وخصائص Next.js الحديثة (App Router, SSR).

---

## Strict Rules | قواعد صارمة

### 1. Component Architecture
- **Functional Components**: Use functional components with Hooks strictly. No Class components.
- **Atomic Design**: Structure components into atoms, molecules, and organisms for maximum reusability.
- **Composition**: Prefer component composition over deep prop drilling.

### 2. State Management
- **Local vs Global**: Keep state as local as possible. Use `useContext` or lightweight libraries (Zustand, Jotai) only when needed.
- **Immutability**: NEVER mutate state or props directly. Use `useState` or `useReducer`.

### 3. Next.js App Router (Modern)
- **Server Components**: Use React Server Components (RSC) by default. Only use `'use client'` when interactivity is required.
- **Data Fetching**: Use `fetch` with appropriate caching and revalidation strategies. Use Server Actions for data mutations.

### 4. Performance Optimization
- **Memoization**: Use `useMemo` and `useCallback` judiciously to avoid unnecessary re-renders.
- **Image Optimization**: Always use the `next/image` component for automatic image optimization.
- **Code Splitting**: Leverage dynamic imports for large components or libraries.

### 5. Styling
- **CSS-in-JS or Tailwind**: Use a consistent styling approach (Tailwind CSS is preferred for performance).
- **Responsive Design**: Ensure all components are responsive and mobile-friendly by default.
