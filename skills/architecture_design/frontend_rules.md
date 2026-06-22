# Enterprise Frontend Mastery & Decision Engine | احتراف الواجهات الأمامية ومحرك القرارات

## Arabic Description | وصف بالعربية
قواعد هندسية متقدمة لتطوير الواجهات الأمامية (Frontend). يتضمن هذا الملف محرك اتخاذ القرار لاختيار تقنيات الـ Rendering وإدارة الحالة، مع جداول مفاضلة وسيناريوهات فشل وتدقيق الأداء في بيئات الإنتاج.

---

## Decision Framework: Rendering Strategy
| Strategy | Pros | Cons | When to Use |
|---|---|---|---|
| SSG | Max performance, SEO | Build time scales with content | Documentation, Blogs, Static sites |
| SSR | SEO, dynamic data | Higher server load, TTFB | Dashboards, User-specific content |
| ISR | Performance + Dynamic | Complexity, eventual consistency | E-commerce, News portals |

---

## Strict Rules | قواعد صارمة

### 1. Performance & Interactivity
- **Web Workers**: Move heavy data processing or complex filtering tasks to Web Workers to ensure 60fps UI responsiveness.
- **Priority Hints**: Use `fetchpriority` and preload for LCP (Largest Contentful Paint) elements.

### 2. State & Architecture
- **Finite State Machines**: Use XState for complex UI flows (e.g., multi-step auth, complex forms) to prevent impossible states.
- **State Locality**: Prefer local state by default. Use global state managers only for data that is truly shared across disparate branches of the tree.

---

## Failure Scenarios: Frontend Issues
1. **Scenario**: Large JavaScript bundle causes slow load on mobile/low-end devices.
   - **Handling**: Implement aggressive code splitting. Audit with `bundle-analyzer`. Move non-critical features to dynamic imports.
2. **Scenario**: API is down or extremely slow.
   - **Handling**: UI MUST show appropriate loading/error states. Use `stale-while-revalidate` (SWR/React Query) to show cached data while updating.

---

## Production Checkpoints
- [ ] Is there an Error Boundary at the root and major feature levels?
- [ ] Are all images optimized and using responsive formats (WebP/AVIF)?
- [ ] Is the app fully navigable via Keyboard (a11y check)?
