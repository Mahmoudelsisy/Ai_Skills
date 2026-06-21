# Game Development & Engineering | تطوير وهندسة الألعاب

## Arabic Description | وصف بالعربية
قواعد صارمة لتطوير الألعاب باستخدام محركات مثل Unity و Unreal Engine. تركز هذه القواعد على تحسين الأداء (Optimization)، إدارة الذاكرة، وبناء أنظمة ألعاب قابلة للتوسع.

---

## Strict Rules | قواعد صارمة

### 1. Performance Optimization
- **Draw Calls**: Minimize draw calls through batching and using atlases.
- **Object Pooling**: NEVER instantiate/destroy objects frequently during gameplay. Use object pooling.
- **LOD (Level of Detail)**: Implement LOD for all complex 3D models to save GPU resources.

### 2. Game Architecture
- **Component-Based**: Use Entity-Component-System (ECS) or clear component patterns. Avoid deep inheritance.
- **Decoupling**: Separate game logic from rendering and input handling.

### 3. Memory Management
- **Asset Loading**: Use asynchronous loading for assets to avoid frame drops.
- **Garbage Collection**: Minimize allocations in `Update()` loops to avoid GC spikes.

### 4. Engine Specifics (Unity/Unreal)
- **Unity**: Use ScriptableObjects for data-driven design. Prefer `ComputeShaders` for heavy parallel tasks.
- **Unreal**: Use C++ for performance-critical systems and Blueprints for high-level logic/prototyping.

### 5. Multiplayer & Networking
- **Lag Compensation**: Implement client-side prediction and server-side reconciliation.
- **Bandwidth**: Only sync essential data. Use delta compression for network packets.
