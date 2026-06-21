# AR/VR, Spatial Computing & Metaverse | الواقع المعزز والافتراضي والحوسبة المكانية

## Arabic Description | وصف بالعربية
قواعد صارمة لتطوير تجارب غامرة (Immersive Experiences) باستخدام تقنيات الواقع المعزز (AR) والافتراضي (VR). تركز هذه القواعد على الأداء العالي (High FPS)، تقليل دوار الحركة (Motion Sickness)، والتفاعل المكاني الصحيح.

---

## Strict Rules | قواعد صارمة

### 1. Performance & Framerate
- **Maintain Target FPS**: Ensure a consistent framerate (typically 72, 90, or 120 FPS) to prevent motion sickness.
- **Draw Call Optimization**: Minimize draw calls through batching and using simple shaders.

### 2. User Comfort & Safety
- **Motion Sickness Prevention**: Avoid sudden accelerations or rotations of the camera. Use teleportation or vignetting for locomotion.
- **Safety Boundaries**: Respect the user's physical safety boundaries (Guardian/Chaperone systems).

### 3. Spatial Interaction
- **Hand Tracking**: Implement intuitive and responsive hand tracking interactions. Provide visual/haptic feedback for every touch.
- **Spatial Audio**: Use 3D spatial audio to enhance immersion and guide the user's attention.

### 4. Rendering & Assets
- **LOD (Level of Detail)**: Use aggressive LOD strategies for 3D assets.
- **Occlusion Culling**: Implement occlusion culling to only render what the user can actually see.

### 5. Multi-user & Metaverse
- **Avatar Synchronization**: Optimize networking for low-latency avatar and object synchronization in multi-user environments.
- **Interoperability**: Use open standards (e.g., OpenXR, glTF) to ensure experiences work across different hardware.
