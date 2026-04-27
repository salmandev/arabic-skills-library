# مكتبة المهارات العربية

> أول مجموعة مجتمعية من ملفات SKILL.md لوكلاء الذكاء الاصطناعي الناطقين بالعربية

[![الترخيص: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![نرحب بالمساهمات](https://img.shields.io/badge/contributions-welcome-brightgreen.svg)](CONTRIBUTING.md)

---

## 📖 نظرة عامة

**مكتبة المهارات العربية** هي أول مجموعة مفتوحة المصدر من ملفات SKILL.md المصممة خصيصاً للمطورين الناطقين بالعربية الذين يبنون وكلاء الذكاء الاصطناعي. تحتوي هذه المستودع على:

- تعليمات عربية أصيلة (Native Arabic instructions)
- قوالب ثنائية اللغة (Bilingual templates)
- مهارات امتثال خاصة بمنطقة الشرق الأوسط (MENA-specific compliance skills)
- قوالب Prompt متوافقة مع RTL (RTL-aware prompt templates)
- لهجات عربية متنوعة (MSA, خليجي, شامي, مصري)

---

## 🎯 لماذا هذا مهم؟

### الفجوة بالأرقام

| الإحصائية | الرقم |
|-----------|-------|
| الناطقون بالعربية | ٤٢٢ مليون ناطق أصلي |
| تغطية SKILL.md العربية | أقل من ٣٪ من السجلات العامة |
| مهارات الامتثال MENA | صفر قبل هذا المشروع |

### المشكلة

- العربية لديها **٤٢٢ مليون ناطق أصلي** عبر ٢٧ دولة
- أقل من ٣٪ من جميع ملفات SKILL.md في السجلات العامة تحتوي على أي محتوى عربي
- أطر العمل مثل LangChain و AutoGPT ليس لديها **أي مكافئات مكيفة للعربية**
- تطوير LLM العربية (Falcon, JAIS, ALLaM, METABRAIN, Humain) يتسارع بسرعة — لكن لا توجد **مكتبات مهارات** للمطورين الذين يبنون عليها
- NCA ECC, SAMA CSF, PDPL — أطر الامتثال الفريدة في المنطقة — ليس لديها **أي قوالب مهارات** في أي مكان
- كل مطور في منطقة الشرق الأوسط يبني وكلاء ذكاء اصطناعي يكتب مطالبات عربية من الصفر، في كل مرة

---

## 📦 المحتويات

### فئات المهارات (٥٠ مهارة مقررة للإصدار v1.0)

| الفئة | المهارات | الحالة |
|-------|----------|--------|
| 🏛️ حوكمة وامتثال | ٧ | قيد التنفيذ |
| 📚 تعليم | ٧ | قيد التنفيذ |
| 💼 أعمال واحترافي | ٧ | قيد التنفيذ |
| 💻 أدوات المطورين | ٧ | قيد التنفيذ |
| 🏥 صحة | ٥ | مقررة |
| 📰 إعلام ومحتوى | ٧ | مقررة |
| 🔒 أمن وإدارة المخاطر | ٤ | مقررة |
| 🌍 ترجمة ولغويات | ٦ | مقررة |

### مهارات مميزة

| المهارة | الوصف | اللغة |
|---------|-------|-------|
| [`nca-ecc-audit`](skills/government/nca-ecc-audit/SKILL.md) | مراجعة الكود وفق متطلبات هيئة الأمن السيبراني | ثنائية |
| [`sama-csf-review`](skills/government/sama-csf-review/SKILL.md) | مراجعة امتثال إطار SAMA للأمن السيبراني | ثنائية |
| [`arabic-email-drafter`](skills/business/arabic-email-drafter/SKILL.md) | كتابة رسائل بريد إلكتروني احترافية | عربية |
| [`arabic-proofreader`](skills/linguistics/arabic-proofreader/SKILL.md) | تدقيق النص العربي للقواعد والأسلوب | عربية |
| [`rtl-css-skill`](skills/developer/rtl-css-skill/SKILL.md) | توليد CSS متوافق مع RTL لواجهات الويب العربية | ثنائية |

---

## 🚀 البدء السريع

### تثبيت مهارة

```bash
# باستخدام agency-agents-cli
agency-agents-cli install arabic-email-drafter --lang ar

# أو استنساخ المستودع
git clone https://github.com/salmandev/arabic-skills-library.git
```

### استخدام مهارة

١. انتقل إلى دليل المهارة (مثال: `skills/government/nca-ecc-audit/`)
٢. اقرأ ملف `SKILL.md`
٣. انسخ التعليمات إلى Prompt النظام الخاص بوكيل LLM الخاص بك
٤. استخدم الكلمات المفتاحية المدرجة في المهارة للتشغيل

---

## 📁 هيكل المستودع

```
arabic-skills-library/
├── README.ar.md                       # أنت هنا
├── README.md                          # README بالإنجليزية
├── CONTRIBUTING.ar.md                 # دليل المتطوعين (عربي)
├── CONTRIBUTING.md                    # دليل المتطوعين (ثنائي)
├── SKILL_TEMPLATE.md                  # قالب فارغ للمساهمين
├── SKILL_TEMPLATE_BILINGUAL.md        # قالب ثنائي اللغة
├── skills/
│   ├── government/                    # حوكمة وامتثال
│   ├── education/                     # تعليم
│   ├── business/                      # أعمال
│   ├── developer/                     # أدوات المطورين
│   ├── healthcare/                    # صحة
│   ├── media/                         # إعلام ومحتوى
│   ├── security/                      # أمن وإدارة المخاطر
│   └── linguistics/                   # ترجمة ولغويات
├── dialects/
│   ├── gulf/                          # خليجي
│   ├── levantine/                     # شامي
│   └── egyptian/                      # مصري
├── llm-compatibility/                 # ملاحظات خاصة بكل LLM
├── tools/                             # أدوات CLI
├── docs/                              # التوثيق
└── .github/                           # قوالب GitHub وسير العمل
```

---

## 🤝 المساهمة

نرحب بالمتطوعين! راجع [CONTRIBUTING.ar.md](CONTRIBUTING.ar.md) لمعرفة:

- كيفية المساهمة بمهارة
- معايير الجودة
- شارات المتطوعين والتقدير
- طلبات المهارات ذات الأولوية

### الطلبات ذات الأولوية (حرج 🔴)

١. مهارات امتثال NCA ECC و SAMA CSF (سياق الرياض/السعودية)
٢. قوالب التقارير الطبية بالعربية
٣. متغيرات اللهجة الخليجية للمهارات الإنجليزية الموجودة
٤. مهارات CSS/UI العربية RTL للمطورين

---

## 📜 الترخيص

ترخيص MIT — راجع [LICENSE](LICENSE) للتفاصيل.

---

## 🌟 المساهمون

<!-- markdownlint-disable-next-line -->
<table>
  <tr>
    <td align="center">
      <strong>المساهم المؤسس</strong><br/>
      سلمان 
    </td>
  </tr>
</table>

---

## 📬 التواصل

- **مشكلات GitHub**: [الإبلاغ عن خطأ أو طلب مهارة](https://github.com/arabic-skills-library/arabic-skills-library/issues)
- **سجل SkillForge**: يتم إرسال المهارات تلقائياً إلى SkillForge تحت فئة "Arabic/MENA"

---

<div align="center">

**صُنع بحب ❤️ لمجتمع المطورين الناطقين بالعربية**

Built with ❤️ for the Arabic-speaking developer community

</div>
