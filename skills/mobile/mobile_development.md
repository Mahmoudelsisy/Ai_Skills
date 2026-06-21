# Mobile Application Development | تطوير تطبيقات الجوال

## Arabic Description | وصف بالعربية
قواعد صارمة لتطوير تطبيقات جوال احترافية (Native أو Cross-platform) تضمن الأداء العالي، توفير البطارية، وتجربة مستخدم سلسة.

---

## Strict Rules | قواعد صارمة

### 1. User Experience & UI
- **Platform Guidelines**: Follow iOS Human Interface Guidelines and Android Material Design principles.
- **Offline First**: Design applications to handle offline states gracefully (e.g., caching, local databases).
- **Responsive Layouts**: UI MUST adapt to different screen sizes and orientations.

### 2. Performance & Efficiency
- **Memory Management**: Avoid memory leaks, especially when handling large lists or images.
- **Battery Life**: Minimize background processes and excessive network polling.
- **Startup Time**: Optimize app startup time by lazy loading non-critical modules.

### 3. Cross-Platform Frameworks (React Native / Flutter)
- **Bridge Optimization**: Minimize bridge traffic in React Native. Use native modules only when necessary.
- **Widget Efficiency**: In Flutter, keep builds efficient by minimizing the scope of `setState`.

### 4. App Security
- **Secure Storage**: Use Keychain (iOS) and EncryptedSharedPreferences (Android) for sensitive data.
- **Certificate Pinning**: Implement SSL pinning for critical API communications.

### 5. Deployment & Updates
- **Versioning**: Follow semantic versioning for app releases.
- **Feature Flags**: Use feature flags to enable/disable features without requiring a full app store update.
