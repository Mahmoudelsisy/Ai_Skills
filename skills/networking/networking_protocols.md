# Computer Networking & Protocols | شبكات الحاسب والبروتوكولات

## Arabic Description | وصف بالعربية
قواعد صارمة لبرمجة الشبكات والتعامل مع البروتوكولات المختلفة. تضمن هذه القواعد كفاءة الاتصال، الأمان، وقدرة الأنظمة الموزعة على التواصل بسلاسة.

---

## Strict Rules | قواعد صارمة

### 1. Protocol Usage
- **Appropriate Choice**: Choose the right protocol for the task (e.g., gRPC for high-performance internal communication, WebSockets for real-time bi-directional data, REST for public APIs).
- **HTTP/3 & HTTP/2**: Prefer modern HTTP versions for better performance (multiplexing, header compression).

### 2. Network Programming
- **Timeouts**: ALWAYS set connection and read/write timeouts for all network calls to avoid hanging processes.
- **Retries & Backoff**: Implement exponential backoff for retrying failed network requests.

### 3. Reliability & Performance
- **Connection Pooling**: Use connection pools to reuse established connections and reduce latency.
- **Serialization**: Use efficient serialization formats (e.g., Protobuf, MessagePack) for high-throughput systems instead of bulky JSON.

### 4. Security
- **TLS/SSL**: All network communication MUST be encrypted using modern TLS (1.2 or 1.3).
- **Certificate Verification**: Always verify server certificates. NEVER disable SSL verification in production code.

### 5. Troubleshooting & Observability
- **Logging**: Log network errors with sufficient context (destination, protocol, error code).
- **Metrics**: Track network-level metrics like RTT (Round Trip Time), packet loss, and connection errors.
