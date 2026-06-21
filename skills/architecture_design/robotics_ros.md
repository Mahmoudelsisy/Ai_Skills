# Robotics Engineering & ROS | هندسة الروبوتات ونظام تشغيل الروبوت

## Arabic Description | وصف بالعربية
قواعد صارمة لهندسة الروبوتات وتطوير البرمجيات باستخدام نظام تشغيل الروبوت (ROS). تضمن هذه القواعد استقرار الأنظمة الميكانيكية-الإلكترونية، كفاءة معالجة الحساسات، والتحكم الدقيق.

---

## Strict Rules | قواعد صارمة

### 1. ROS Best Practices (ROS 1/2)
- **Node Modularity**: Each ROS node MUST perform one single task. Avoid "Monolithic" nodes.
- **Message Types**: Use standard ROS messages whenever possible. Create custom messages only when absolutely necessary.
- **Launch Files**: Use launch files for complex system startups. Never start multiple nodes manually.

### 2. Sensor Integration & Processing
- **Data Filtering**: ALWAYS apply filtering (e.g., Kalman Filter, Moving Average) to noisy sensor data before use in control loops.
- **Frequency Management**: Ensure sensor data is published at appropriate frequencies. Avoid overloading the network with high-frequency raw data.

### 3. Control & Actuation
- **Safety Limits**: Implement software-level safety limits for all actuators (e.g., maximum velocity, torque limits).
- **Watchdogs**: Use watchdog timers to detect and handle node failures or communication loss.

### 4. Real-Time & Performance
- **Zero-Copy**: In ROS 2, leverage zero-copy transport for large data (like point clouds or images) between nodes on the same host.
- **Threading**: Be careful with multi-threading. Use thread-safe subscribers and publishers.

### 5. Simulation & Testing
- **Simulation First**: ALWAYS test algorithms in simulation (Gazebo, Webots) before deploying to physical hardware.
- **Unit Testing**: Write unit tests for independent algorithms (e.g., path planning, perception) without requiring a full ROS environment.
