# Enterprise Integration Patterns (EIP) | أنماط التكامل للمؤسسات

## Arabic Description | وصف بالعربية
قواعد هندسية متقدمة لتطبيق أنماط التكامل بين الأنظمة (EIP). تركز القواعد على إدارة الرسائل المعقدة، فك الارتباط بين الأنظمة (Decoupling)، واستخدام أنماط مثل Claim Check, Splitter, Aggregator لضمان تدفق بيانات موثوق وقابل للتوسع.

---

## Strict Rules | قواعد صارمة

### 1. Messaging Fundamentals
- **Asynchronous Decoupling**: Use message queues (Kafka, RabbitMQ) to decouple system components. NEVER allow a failure in a non-critical downstream system to block the upstream producer.
- **Message Headers**: Standardize message headers for metadata (TraceID, SourceSystem, Timestamp).

### 2. Complex Message Routing
- **Content-Based Router**: Implement routers that direct messages to different channels based on message content.
- **Splitter & Aggregator**: Use the Splitter pattern to break a large message into smaller ones for parallel processing, and an Aggregator to recombine the results.

### 3. Handling Large Payloads
- **Claim Check Pattern**: For large message payloads, store the data in an external store (e.g., S3) and pass only a reference (link/ID) in the message.
- **Payload Compression**: ALWAYS compress large JSON/XML payloads before sending them over the wire.

### 4. Reliability & Error Handling
- **Dead Letter Channel**: ALWAYS route failed messages to a specialized Dead Letter Queue (DLQ) for manual review or automated retry.
- **Transactional Messaging**: Use transactions to ensure that a message is only removed from the queue after it has been successfully processed.

### 5. Advanced Transformation
- **Message Translator**: Use a dedicated layer to translate between different data formats (e.g., XML to JSON, Legacy to Modern).
- **Canonical Data Model**: Use a standardized internal data model for all inter-system communication to avoid "N x M" mapping complexity.
