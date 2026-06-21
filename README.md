# AI Agent Skills Encyclopedia | موسوعة مهارات وكلاء الذكاء الاصطناعي

## English

### Overview
This repository contains a comprehensive collection of **Strict Rules** and **Expert Skills** for AI Agents used in modern IDEs (Cursor, Windsurf, Claude Code, Cline, etc.). These skills are designed to enforce high standards in software engineering, architecture, security, and business logic.

### How to Use
Depending on your tool, you can apply these skills in different ways:

#### 1. Cursor (.cursorrules)
Copy the content of the relevant `.md` files into your `.cursorrules` file in the root of your project. You can combine multiple skills by appending them.

#### 2. Windsurf (.windsurfrules)
Similar to Cursor, paste the rules into your `.windsurfrules` file.

#### 3. Cline / Claude Code / GitHub Copilot
You can copy the rules into the "Custom Instructions" or "System Prompt" settings of these extensions/tools.

#### 4. Project-Specific
You can keep a `docs/skills` folder in your project and instruct the agent to "Read and follow the rules in docs/skills/ before starting any task."

---

## العربية

### نظرة عامة
يحتوي هذا المستودع على مجموعة شاملة من **القواعد الصارمة** و **المهارات الخبيرة** لوكلاء الذكاء الاصطناعي المستخدمين في بيئات التطوير الحديثة (Cursor, Windsurf, Claude Code, Cline، إلخ). تم تصميم هذه المهارات لفرض معايير عالية في هندسة البرمجيات، المعمارية، الأمن، ومنطق الأعمال.

### كيفية الاستخدام
اعتماداً على الأداة التي تستخدمها، يمكنك تطبيق هذه المهارات بطرق مختلفة:

#### 1. برنامج Cursor (.cursorrules)
قم بنسخ محتوى ملفات الـ `.md` ذات الصلة إلى ملف `.cursorrules` في المجلد الرئيسي لمشروعك. يمكنك دمج عدة مهارات عن طريق إضافتها تباعاً.

#### 2. برنامج Windsurf (.windsurfrules)
مشابه لـ Cursor، قم بلصق القواعد في ملف `.windsurfrules`.

#### 3. Cline / Claude Code / GitHub Copilot
يمكنك نسخ القواعد في إعدادات "Custom Instructions" أو "System Prompt" الخاصة بهذه الإضافات أو الأدوات.

#### 4. مهارات خاصة بالمشروع
يمكنك الاحتفاظ بمجلد `docs/skills` في مشروعك وتوجيه الوكيل بـ "اقرأ واتبع القواعد الموجودة في docs/skills/ قبل البدء بأي مهمة."

---

## Directory Structure | هيكل المجلدات
- `skills/core`: General engineering principles | مبادئ الهندسة العامة
- `skills/languages`: Language-specific strict rules | قواعد صارمة لكل لغة برمجة
- `skills/security`: Security and vulnerability prevention | الأمن والوقاية من الثغرات
- `skills/architecture`: System design and patterns | تصميم الأنظمة والأنماط
- `skills/api`: API design and communication | تصميم الـ API والاتصالات
- `skills/devops`: CI/CD and infrastructure | العمليات والبنية التحتية
- `skills/business`: Requirements and project management | المتطلبات وإدارة المشاريع
- `skills/engineering`: General engineering practices | ممارسات هندسية عامة
- `skills/frontend`: Frontend best practices | أفضل ممارسات الواجهات الأمامية
- `skills/backend`: Backend best practices | أفضل ممارسات الأنظمة الخلفية
- `skills/ai_ml`: AI and Machine Learning practices | ممارسات الذكاء الاصطناعي
