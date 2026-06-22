# Modern CSS & Styling Mastery | احتراف لغة CSS الحديثة والتنسيق

## Arabic Description | وصف بالعربية
قواعد هندسية متقدمة لتنسيق واجهات الويب باستخدام تقنيات CSS الحديثة. تركز القواعد على استخدام Container Queries، CSS Layers، رموز التصميم (Design Tokens)، وتحسين أداء الحركات (Animations) لضمان تجربة مستخدم سلسة واحترافية.

---

## Strict Rules | قواعد صارمة

### 1. Modern Layout & Responsiveness
- **Container Queries**: ALWAYS prefer Container Queries over Viewport Media Queries for reusable components. Design components to adapt based on their parent container's size.
- **Flexbox & Grid**: Use CSS Grid for overall page layouts and Flexbox for 1D alignments. Avoid absolute positioning for core layout structures.

### 2. Advanced CSS Architecture
- **Cascade Layers (@layer)**: Use `@layer` to explicitly manage the cascade and prevent specificity wars between base styles, components, and third-party libraries.
- **Logical Properties**: Use Logical Properties (`margin-inline`, `inset-block`) instead of physical properties to support multi-language (LTR/RTL) layouts natively.

### 3. Design Tokens & Theming
- **CSS Variables (Custom Properties)**: Use CSS variables for all design tokens (colors, spacing, typography). NEVER hardcode hex codes or pixel values in components.
- **Theming**: Implement Dark/Light modes using `prefers-color-scheme` and CSS variable overrides.

### 4. Animation Performance
- **GPU Acceleration**: Only animate `transform` and `opacity` to ensure 60fps animations. Avoid animating layout-triggering properties like `width`, `height`, or `top`.
- **Will-change**: Use `will-change` sparingly only for complex animations to hint the browser about upcoming changes.

### 5. Maintainability & Standards
- **Nesting**: Use native CSS nesting (or Sass/PostCSS) to group related styles, but limit nesting depth to 3 levels to maintain readability.
- **Accessibility**: Ensure all interactive states (`:focus-visible`, `:hover`) are clearly defined and meet contrast requirements.
