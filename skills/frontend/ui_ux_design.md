# Sophisticated UI/UX & Design Systems | تصميم الواجهات وتجربة المستخدم المتقدمة

## Arabic Description | وصف بالعربية
قواعد تصميم متقدمة لبناء أنظمة تصميم (Design Systems) وتجارب مستخدم عالمية. تغطي القواعد استخدام رموز التصميم (Design Tokens)، علم نفس تجربة المستخدم، الحركات الدقيقة (Micro-interactions)، وإدارة التركيز المتقدمة لسهولة الوصول.

---

## Strict Rules | قواعد صارمة

### 1. Design System & Tokens
- **Design Tokens**: Use a token-based system for colors, spacing, typography, and elevation. Avoid hardcoded values in design and code to ensure multi-theme support (Dark/Light).
- **Component Lifecycle**: Every component MUST go through "Design -> Review -> Documentation -> Implementation" phases.
- **Storybook First**: All UI components MUST be developed in isolation using Storybook before being integrated into the application.

### 2. UX Psychology & Patterns
- **Hick's Law**: Simplify choices for the user. Break down complex forms into multi-step processes.
- **Fitts's Law**: Make interactive elements (buttons, inputs) large enough and easy to reach, especially on mobile.
- **Peak-End Rule**: Pay special attention to the most intense points of a user journey and the final interaction (e.g., success animations).

### 3. Motion & Micro-interactions
- **Purposeful Animation**: Every animation MUST serve a purpose (e.g., guiding attention, providing feedback). Avoid distracting or purely decorative motion.
- **Performance**: Use CSS transforms and opacity for animations. Ensure they run at 60fps. Respect `prefers-reduced-motion` settings.

### 4. Advanced Accessibility (a11y)
- **Focus Management**: Strictly manage focus during UI transitions (e.g., returning focus to the trigger after a modal closes).
- **Complex Widget a11y**: Use appropriate ARIA roles and states (e.g., `aria-expanded`, `aria-controls`) for complex widgets like accordions, tabs, and comboboxes.
- **Inclusive Language**: Design for a global audience by using gender-neutral and culturally sensitive language and imagery.

### 5. Design Verification
- **A/B Testing**: For critical flows, use A/B testing to validate design hypotheses against real user data.
- **Usability Audits**: Regularly conduct usability audits with diverse user groups, including those with disabilities.
- **Responsive Proofing**: Test designs across a wide range of devices, from low-end mobile to high-resolution ultrawide monitors.
