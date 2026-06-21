# Enterprise React & Next.js Standards | معايير ريأكت ونيكست جيه إس للمشاريع الكبرى

## Arabic Description | وصف بالعربية
قواعد هندسية متقدمة لتطبيقات React و Next.js في بيئات العمل الحقيقية والأنظمة الضخمة. تغطي القواعد أنماط التصميم المتقدمة، تحسين الأداء على مستوى الـ Rendering، والتعامل مع البيانات الضخمة.

---

## Strict Rules | قواعد صارمة

### 1. Component Patterns & Performance
- **Compound Components**: Use the Compound Component pattern for complex UI widgets (e.g., Tabs, Selects) to allow flexible sub-component rendering.
- **Render Optimization**: Strictly prevent "Prop Drilling." Use Context for cross-cutting concerns, but wrap providers at the lowest possible level to minimize re-renders.
- **Slot Pattern**: Use `children` or explicit "slot" props for better component composition and to avoid large, complex prop interfaces.

### 2. Next.js App Router & Server Features
- **Streaming & Suspense**: Use `loading.tsx` and granular `<Suspense>` boundaries to stream UI segments. Data fetching MUST be moved as close to the leaf components as possible.
- **Server Actions**: Secure all Server Actions with middleware or library-based validation (e.g., `next-safe-action`). Implement CSRF protection and input validation (Zod).
- **Parallel & Intercepting Routes**: Utilize Next.js Parallel Routes for dashboard layouts and Intercepting Routes for modals to maintain URL state.

### 3. Advanced Data Management
- **Optimistic UI**: Implement optimistic updates for all mutation actions to provide an "instant" feel to the user.
- **Prefetching Strategy**: Use `Link` component prefetching and manual `router.prefetch()` for predicted user journeys.
- **Infinite Loading**: Use specialized hooks for large lists, ensuring virtualization (e.g., `react-window` or `virtuoso`) is used for more than 100 items.

### 4. Testing & Quality (Enterprise Standard)
- **Visual Regression**: Integrate visual regression testing (e.g., Chromatic) for the component library.
- **Integration over Unit**: Prioritize Integration tests (Testing Library) and E2E (Playwright) over testing individual component implementation details.
- **Hooks Testing**: Custom hooks MUST have 100% test coverage using `renderHook`.

### 5. Deployment & Production
- **Edge Runtime**: Use the Edge Runtime for global low-latency middleware and API routes where compatible.
- **Caching Headers**: Explicitly define `Cache-Control` headers for all static and dynamic assets to optimize CDN performance.
- **Strict TypeScript**: Never use `ts-ignore`. Use `satisfies` operator for better type inference with literal objects.
