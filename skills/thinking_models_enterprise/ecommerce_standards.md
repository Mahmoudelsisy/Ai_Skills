# E-commerce & Digital Commerce | التجارة الإلكترونية والرقمية

## Arabic Description | وصف بالعربية
قواعد صارمة لبناء منصات تجارة إلكترونية قوية وقابلة للتوسع. تغطي هذه القواعد عمليات الدفع، إدارة المخزون، وتحسين تجربة الشراء لزيادة التحويل (Conversion).

---

## Strict Rules | قواعد صارمة

### 1. Checkout & Payments
- **Secure Integration**: Use secure, hosted payment fields (e.g., Stripe Elements) to minimize PCI scope.
- **Fail-Safe Checkout**: Ensure the checkout process can handle intermittent failures without losing the user's cart or order data.
- **Idempotent Payments**: Payment processing MUST be idempotent to avoid multiple charges for the same order.

### 2. Inventory Management
- **Real-time Updates**: Sync inventory in real-time across all channels to prevent overselling.
- **Race Condition Prevention**: Use database-level locking or distributed locks when updating inventory counts during high-traffic events.

### 3. Catalog & Search
- **Indexing**: Optimize product search using specialized engines like Elasticsearch or Algolia.
- **SEO for E-commerce**: Every product page MUST have proper schema markup (Product, Offer, Review).

### 4. Scalability & Performance
- **Caching**: Aggressively cache product catalogs and static pages, but ensure price and availability are always accurate.
- **High Traffic Handling**: Design the system to handle flash sales and major traffic spikes (e.g., Black Friday).

### 5. Customer Experience
- **Mobile First**: The entire shopping experience MUST be optimized for mobile devices.
- **Fast Loading**: Optimize page load times to reduce bounce rates and improve conversion.
