# Frontend Engineering Standards | معايير هندسة الواجهات الأمامية

## Arabic Description | وصف بالعربية
قواعد صارمة لتطوير واجهات مستخدم احترافية، سريعة، وسهلة الوصول (Accessible)، مع التركيز على تجربة المستخدم وجودة الكود.

---

## Strict Rules | قواعد صارمة

### 1. Accessibility (a11y)
- **Semantic HTML**: Use proper HTML tags (`<main>`, `<nav>`, `<button>`, etc.). No `<div>` for everything.
- **ARIA Labels**: Use ARIA labels when semantic HTML is not enough.
- **Contrast**: Ensure text-to-background contrast meets WCAG standards.

### 2. Performance
- **Asset Optimization**: Optimize images and use lazy loading.
- **Bundle Size**: Monitor and minimize JavaScript bundle sizes.
- **Core Web Vitals**: Aim for high scores in LCP, FID, and CLS.

### 3. State Management
- **Local vs Global**: Use local state by default. Only use global state (Redux, Context, etc.) when truly necessary.
- **Immutability**: Never mutate state directly.

### 4. Responsive Design
- **Mobile First**: Design for mobile first, then scale up.
- **Flex/Grid**: Use Flexbox and CSS Grid for layouts. Avoid absolute positioning for layout.

### 5. UI/UX Consistency
- **Design System**: Follow the project's design system/component library strictly.
- **Consistency**: Maintain consistent spacing, typography, and color usage.
