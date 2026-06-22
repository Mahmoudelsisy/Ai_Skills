# Load Testing & Quality Engineering Mastery | احتراف اختبارات الحمل وهندسة الجودة

## Arabic Description | وصف بالعربية
قواعد هندسية متقدمة لاختبار أداء الأنظمة تحت الضغط العالي (Load Testing) باستخدام أدوات مثل k6 و JMeter. تركز القواعد على تحديد نقاط الانهيار، قياس الـ Throughput، وضمان استقرار الأنظمة في ذروة الاستخدام.

---

## Strict Rules | قواعد صارمة

### 1. Load Test Design
- **Realistic Scenarios**: Use real production traffic patterns to design test scenarios. Include typical user journeys (e.g., browse, add to cart, checkout).
- **Environment Parity**: Run load tests in an environment that is as close to production as possible (staging/pre-prod).

### 2. Metrics & Benchmarking
- **Key Metrics**: ALWAYS measure Latency (P95/P99), Throughput (RPS), and Error Rate.
- **Resource Monitoring**: Monitor server resources (CPU, RAM, I/O, DB Connections) during the test to identify the specific bottleneck.

### 3. Tooling Standards (k6/JMeter)
- **k6 for Developers**: Prefer k6 for developer-centric load testing due to its JS-based scripting and easy CI/CD integration.
- **JMeter for Legacy/Complex**: Use JMeter for complex protocols or legacy systems where specialized plugins are required.

### 4. Continuous Performance Testing
- **CI/CD Integration**: Integrate performance smoke tests into the CI/CD pipeline to catch performance regressions early.
- **Thresholds**: Define strict pass/fail thresholds for performance metrics in every test.

### 5. Advanced Scenarios
- **Stress Testing**: Find the absolute breaking point of the system.
- **Soak Testing**: Run tests for extended periods (hours/days) to detect memory leaks and resource exhaustion over time.
