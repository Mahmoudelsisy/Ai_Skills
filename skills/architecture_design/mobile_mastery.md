# Native Mobile Mastery (Swift & Kotlin) | احتراف تطوير تطبيقات الجوال الأصلية

## Arabic Description | وصف بالعربية
قواعد هندسية متقدمة لتطوير تطبيقات الجوال باستخدام اللغات الأصلية (Native) مثل Swift لنظام iOS و Kotlin لنظام Android. تركز القواعد على المعماريات الحديثة (MVVM/MVI)، إدارة الذاكرة، وكفاءة الأداء.

---

## Strict Rules | قواعد صارمة

### 1. iOS Development (Swift)
- **Architecture**: Use MVVM with Combine or SwiftUI with Observation. For complex apps, consider The Composable Architecture (TCA).
- **Memory Management**: Avoid Strong Reference Cycles by using `[weak self]` in closures.
- **SwiftUI Performance**: Minimize the use of `AnyView`. Use `@ViewBuilder` and keep view bodies small and efficient.

### 2. Android Development (Kotlin)
- **Architecture**: Follow the official "Guide to App Architecture" using MVVM or MVI. Use Jetpack Compose for UI.
- **Coroutines & Flow**: Use Kotlin Coroutines for asynchronous work. Use `StateFlow` and `SharedFlow` for reactive data streams.
- **Dependency Injection**: Use Hilt (Dagger) or Koin for DI to ensure testability and modularity.

### 3. Native UI & UX Mastery
- **Accessibility**: Support Dynamic Type (Text Scaling) and VoiceOver/TalkBack for all UI components.
- **Design Consistency**: Follow Apple's Human Interface Guidelines (HIG) and Android's Material Design 3 strictly.
- **Local Persistence**: Use Room (Android) or SwiftData/CoreData (iOS) with migrations for offline-first capabilities.

### 4. Networking & API (Mobile)
- **Error Handling**: Implement generic error wrappers for API calls. Handle network loss gracefully with local caching.
- **Security**: Use Certificate Pinning and Biometric Authentication where required. NEVER store secrets in the app binary.

### 5. Build & CI/CD (Mobile)
- **Fastlane**: Automate beta releases and App Store/Play Store submissions using Fastlane.
- **Modularization**: Break large apps into feature modules to improve build times and separation of concerns.
