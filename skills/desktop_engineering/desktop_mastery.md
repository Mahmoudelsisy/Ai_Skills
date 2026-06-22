# Desktop Application Engineering Mastery | احتراف هندسة تطبيقات سطح المكتب

## Arabic Description | وصف بالعربية
قواعد هندسية متقدمة لتطوير تطبيقات سطح المكتب (Desktop) باستخدام أطر عمل مثل Electron و Tauri. تركز القواعد على الأداء، أمان العمليات (IPC)، التكامل مع نظام التشغيل، وتقليل استهلاك الموارد (RAM/CPU).

---

## Strict Rules | قواعد صارمة

### 1. Framework Selection & Performance
- **Tauri for Lean Apps**: Prefer Tauri for resource-efficient apps where a small binary size and low RAM usage are critical.
- **Electron Optimization**: For Electron, minimize the use of heavy dependencies. Use the `requestIdleCallback` for non-critical tasks.

### 2. Secure Process Communication (IPC)
- **Context Isolation**: ALWAYS enable `contextIsolation` in Electron. NEVER expose the full `remote` module to the renderer process.
- **Strict IPC Validation**: Validate all data sent between the Main and Renderer processes using strict schemas.

### 3. Native Integration
- **OS-specific Features**: Implement native menus, tray icons, and global shortcuts following the platform-specific UX guidelines (macOS, Windows, Linux).
- **File System Safety**: Use safe file dialogs. NEVER grant the app unrestricted access to the user's entire file system.

### 4. Build & Distribution
- **Code Signing**: All production binaries MUST be digitally signed to avoid OS security warnings.
- **Auto-updates**: Implement a secure auto-update mechanism (e.g., using Electron Updater or Tauri's built-in updater).

### 5. Resource Management
- **Memory Leaks**: Regularly audit the app for memory leaks in the renderer process.
- **Process Management**: Ensure that background processes are terminated properly when the app closes.
