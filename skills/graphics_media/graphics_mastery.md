# Graphics & Media Engineering Mastery | احتراف هندسة الرسوميات والوسائط

## Arabic Description | وصف بالعربية
قواعد هندسية متقدمة لتطوير محركات الرسوميات، التعامل مع معالجات الرسوم (GPU)، وكتابة الـ Shaders. تركز القواعد على الرياضيات ثلاثية الأبعاد المعقدة، تحسين الأداء الرسومي، ومعالجة الوسائط المتعددة.

---

## Strict Rules | قواعد صارمة

### 1. GPU Programming & Shaders
- **Shader Optimization**: Minimize branching in shaders (GLSL/HLSL). Use bitwise operations and vectorization where possible.
- **Compute Shaders**: Leverage Compute Shaders for non-graphics parallel tasks (e.g., physics simulation, data processing).

### 2. 3D Math & Geometry
- **Matrix Mastery**: Use Quaternions for rotations to avoid Gimbal Lock. Optimize matrix multiplications in the vertex shader.
- **Precision Management**: Be mindful of floating-point precision in large-scale scenes. Use camera-relative rendering for distant objects.

### 3. Rendering Pipelines
- **Vulkan/DirectX 12**: Manage memory and synchronization manually for high-performance low-level APIs. Use pipeline state objects (PSO) efficiently.
- **Ray Tracing**: Implement efficient Bounding Volume Hierarchies (BVH) for real-time ray tracing.

### 4. Media Processing (Video/Audio)
- **Codec Mastery**: Choose appropriate codecs (H.264, H.265, AV1) based on bitrate and quality requirements. Use hardware-accelerated encoding/decoding.
- **Buffer Management**: Implement zero-copy media pipelines to minimize CPU overhead.

### 5. Performance & Profiling (Graphics)
- **Frame Debugging**: Use tools like RenderDoc or NVIDIA Nsight to identify draw call bottlenecks and GPU stalls.
- **Memory Bandwidth**: Optimize texture sampling and vertex buffer layouts to minimize GPU memory bandwidth usage.
