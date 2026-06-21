# Localization & Cultural Engineering Mastery | احتراف التوطين والهندسة الثقافية

## Arabic Description | وصف بالعربية
قواعد هندسية متقدمة لتوطين البرمجيات (Localization) وتكييفها ثقافياً لتناسب الأسواق العالمية. تركز القواعد على دعم اللغات التي تكتب من اليمين إلى اليسار (RTL)، إدارة الوقت والعملات عالمياً، وتصميم واجهات مستخدم تحترم التنوع الثقافي.

---

## Strict Rules | قواعد صارمة

### 1. Advanced Localization (L10n)
- **Externalize All Strings**: NEVER hardcode user-facing text. Use resource files (e.g., JSON, YAML, XLIFF).
- **Pluralization & Gender**: Use advanced localization libraries that support complex pluralization rules and gender-aware translations (e.g., ICU message format).

### 2. RTL Support Mastery
- **Logical Properties**: Use CSS Logical Properties (e.g., `margin-inline-start`, `padding-inline-end`) instead of physical properties (`margin-left`, `padding-right`) to support RTL automatically.
- **Directional Mirroring**: Ensure icons and layouts are appropriately mirrored in RTL mode, except for universal icons (e.g., play buttons, clocks).

### 3. Global Time & Data
- **UTC Everywhere**: ALWAYS store and process time in UTC. Only convert to local time at the presentation layer using the user's IANA timezone ID.
- **Date & Number Formatting**: Use the `Intl` API for locale-aware formatting of dates, numbers, and currencies. NEVER manually format these strings.

### 4. Cultural UI/UX Adaptation
- **Color Meanings**: Be aware of cultural differences in color symbolism. Provide theme overrides for specific markets if necessary.
- **Form Design**: Adapt address and name fields to fit different cultural standards (e.g., varying lengths, name orders).

### 5. Encoding & Fonts
- **UTF-8 Mastery**: Ensure the entire pipeline (Database, API, Frontend) is strictly UTF-8 compliant to prevent character corruption.
- **Font Fallbacks**: Provide appropriate font stacks for different scripts (Arabic, CJK, Cyrillic) to ensure readability and performance.
