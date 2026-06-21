# Expert Engineering Decision Making | اتخاذ القرارات الهندسية الخبيرة

## Arabic Description | وصف بالعربية
القواعد "السرية" التي تميز كبار المهندسين والتقنيين (Staff/Principal Engineers). تركز هذه القواعد على اتخاذ القرارات الصعبة تحت الضغط، التعامل مع مشاكل الإنتاج المعقدة، وفهم أن الهدف هو حل مشاكل الأعمال وليس فقط كتابة كود "مثالي".

---

## Strict Rules | قواعد صارمة

### 1. Decision Making Under Pressure
- **Stabilize First**: In a production crisis, the priority is to stabilize the system and minimize user impact. Deep RCA comes AFTER stability is achieved.
- **Decision Reversibility**: Distinguish between "Two-Way Door" (reversible) and "One-Way Door" (irreversible) decisions. Move fast on the former, and be cautious with the latter.

### 2. Best Solution vs Perfect Solution
- **Diminishing Returns**: Recognize when the effort to reach "100% perfection" exceeds the value it provides. Stop when the solution is robust, scalable, and meets business needs.
- **Avoid Hype-Driven Development**: Choose tools and patterns based on proven reliability and team fit, not just because they are currently trending in the industry.

### 3. Business-Code Alignment
- **Problem Ownership**: An engineer's job is to solve a business problem. Sometimes the "Best Solution" is a process change or a third-party tool, not writing new code.
- **ROI Mindset**: Evaluate every major technical initiative based on its expected Return on Investment (ROI) for the business.

### 4. Communication & Influence
- **Simplify Complexity**: Be able to explain complex technical issues to non-technical stakeholders in a way that relates to business risks and opportunities.
- **Consensus Building**: For major architectural changes, socializing the idea and building consensus early is as important as the technical design itself.

### 5. Managing Complexity
- **Simplicity as a Skill**: Strive to make the system as simple as possible. "Any fool can make something complex; it takes a genius to make it simple."
- **Legacy Empathy**: Understand the constraints and context under which legacy code was written before criticizing it.
