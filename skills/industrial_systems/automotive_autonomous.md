# Automotive & Autonomous Software Mastery | احتراف برمجيات السيارات والقيادة الذاتية

## Arabic Description | وصف بالعربية
قواعد هندسية متقدمة لتطوير برمجيات السيارات (Automotive) والأنظمة ذاتية القيادة. تركز القواعد على معايير السلامة الوظيفية (ISO 26262)، معمارية AUTOSAR، ودمج بيانات الحساسات (Sensor Fusion).

---

## Strict Rules | قواعد صارمة

### 1. Functional Safety (ISO 26262)
- **ASIL Levels**: Clearly define the ASIL (Automotive Safety Integrity Level) for each software component. Apply rigorous testing based on the ASIL level.
- **Fault Detection**: Implement hardware and software watchdogs and heartbeats to detect failures in real-time.

### 2. AUTOSAR Architecture
- **Layered Structure**: Follow the AUTOSAR classic or adaptive platform layers strictly. Decouple application software from hardware-specific drivers.
- **RTE Usage**: Use the Runtime Environment (RTE) for all inter-component communication to ensure standardized data exchange.

### 3. Autonomous Driving (AD) & Sensor Fusion
- **Latency Budget**: Critical perception and control loops MUST meet sub-50ms end-to-end latency.
- **Redundancy in Perception**: Use multiple sensor types (LiDAR, Radar, Camera) and ensure the sensor fusion algorithm handles sensor failure or occlusion gracefully.
- **Path Planning Reliability**: Path planning algorithms MUST always result in a safe state, even if the optimal path is unavailable.

### 4. Communication Protocols (Automotive)
- **CAN/LIN/FlexRay**: Use appropriate bitrates and priority levels for CAN bus messages. Implement cyclic redundancy checks (CRC) for data integrity.
- **Automotive Ethernet**: Use Automotive Ethernet (100Base-T1/1000Base-T1) for high-bandwidth data like camera feeds and point clouds.

### 5. Testing & Validation (V-Model)
- **V-Model Adherence**: Follow the V-model lifecycle strictly, from requirements to unit testing, integration testing, and HIL (Hardware-in-the-Loop) simulation.
- **MISRA C/C++**: Code MUST strictly adhere to MISRA C:2012 or MISRA C++:2023 guidelines for automotive safety.
