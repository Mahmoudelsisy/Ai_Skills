# Enterprise Ruby & PHP Mastery | احتراف لغتي روبي وبي إتش بي للمؤسسات

## Arabic Description | وصف بالعربية
قواعد هندسية متقدمة لاحتراف لغتي Ruby و PHP باستخدام أطر العمل الأكثر شهرة (Ruby on Rails, Laravel) في بيئات المؤسسات الكبرى. تركز القواعد على الأداء العالي، الأمان البرمجي، وقابلية التوسع.

---

## Strict Rules | قواعد صارمة

### 1. Ruby on Rails (Enterprise)
- **Database Optimization**: ALWAYS avoid N+1 queries using `includes` or `joins`. Use `select` to only fetch required columns.
- **Service Objects**: Move complex business logic out of models and controllers into specialized Service Objects or Interaction objects.
- **Background Jobs**: Offload all non-UI tasks to Sidekiq or Shoryuken. Use idempotency for job retries.

### 2. PHP & Laravel (Professional)
- **Type Safety**: Use strict types (`declare(strict_types=1);`). ALWAYS type hint properties, parameters, and return values.
- **Eloquent Optimization**: Use `chunk` or `lazy` for processing large datasets. Use API Resources for consistent response formatting.
- **Middleware & Policies**: Enforce authorization strictly using Policies and Gates. Never perform authorization checks inside controllers.

### 3. Dependency & Security
- **Security Audits**: Regularly run `bundle audit` (Ruby) and `composer audit` (PHP).
- **Environment Isolation**: Use Dotenv strictly. Never hardcode configurations.

### 4. High Performance
- **Caching**: Implement intelligent caching using Redis/Memcached. Use Russian Doll Caching in Rails for view performance.
- **OpCache**: Ensure OpCache is enabled and tuned for PHP in production.

### 5. Testing & Quality
- **RSpec/PHPUnit**: Maintain 80%+ test coverage. Use Factories and Mocks to isolate tests.
- **Linting**: Enforce RuboCop (Ruby) and Pint/PHPCS (PHP) in the CI/CD pipeline.
