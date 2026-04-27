# Contributing to Arabic Skills Library | المساهمة في مكتبة المهارات العربية

Welcome, volunteer! / أهلاً بك أيها المتطوع!

---

## Who Should Contribute? | من يجب أن يساهم؟

**English**:
- Arabic speakers building AI agents
- MENA developers frustrated by English-only skill libraries
- Consultants who write NCA/SAMA compliance docs for clients
- Educators building Arabic EdTech
- Doctors/lawyers who need Arabic professional templates

**العربية**:
- الناطقون بالعربية الذين يبنون وكلاء ذكاء اصطناعي
- مطورو MENA المحبطون من مكتبات المهارات الإنجليزية فقط
- الاستشاريون الذين يكتبون وثائق امتثال NCA/SAMA للعملاء
- المعلمون الذين يبنون EdTech عربي
- الأطباء/المحامون الذين يحتاجون قوالب احترافية عربية

---

## What We Need Most (Priority List) | الأكثر احتياجاً

| Priority | Skill Area | Context |
|----------|-----------|---------|
| 🔴 CRITICAL | NCA ECC & SAMA CSF compliance | Riyadh/KSA market |
| 🔴 CRITICAL | Arabic medical report templates | Healthcare sector |
| 🟡 HIGH | Gulf dialect variants | Existing English skills |
| 🟡 HIGH | Arabic RTL CSS/UI skills | Web developers |
| 🟢 MEDIUM | Egyptian & Levantine dialects | Regional variants |
| 🟢 MEDIUM | Pakistani curriculum Arabic | Urdu-Arabic crossover |

---

## Steps to Contribute a Skill | خطوات المساهمة بمهارة

### 1. Fork the Repository | استنساخ المستودع

```bash
git clone https://github.com/your-username/arabic-skills-library.git
cd arabic-skills-library
```

### 2. Choose a Skill Template | اختر قالب المهارة

- For Arabic-only skills: Copy `SKILL_TEMPLATE.md`
- For bilingual skills: Copy `SKILL_TEMPLATE_BILINGUAL.md`

```bash
# Example: Create a new business skill
mkdir -p skills/business/arabic-email-drafter
cp SKILL_TEMPLATE.md skills/business/arabic-email-drafter/SKILL.md
```

### 3. Fill in ALL Fields | املأ جميع الحقول

**Required frontmatter fields:**

```yaml
---
name: skill-slug
name_ar: الاسم بالعربية
description: English description
description_ar: الوصف بالعربية
category: [business|government|education|developer|healthcare|media|security|linguistics]
language: [ar|bilingual|en]
dialect: [msa|gulf|levantine|egyptian|bilingual]
rtl: true
platform_claude: true/false
platform_gpt: true/false
platform_qwen: true/false
platform_jais: true/false
platform_falcon: true/false
platform_allam: true/false
compliance: []  # [nca-ecc|sama-csf|pdpl|vision2030]
version: 1.0.0
---
```

**Required skill body sections:**

| Section | Arabic | Purpose |
|---------|--------|---------|
| Purpose | الهدف | 2-3 sentences |
| When to Use | متى تستخدم هذه المهارة | 3-5 bullet points |
| Model Instructions | تعليمات النموذج | Detailed, numbered steps |
| Language Rules | قواعد اللغة | Arabic writing standards |
| Example | مثال | 1+ sample input/output |
| Trigger Keywords | الكلمات المفتاحية | 4-6 Arabic + 4-6 English |

### 4. Add Examples | أضف أمثلة

Create example input/output pairs:

```bash
mkdir -p skills/business/arabic-email-drafter/examples
```

**example-input.md:**
```markdown
Write an email to a client explaining a project delay due to vendor issues.
```

**example-output.md:**
```markdown
السيد/السيدة [الاسم] المحترم/المحترمة،

تحية طيبة وبعد،

نود إعلامكم بأنه نظراً لظروف طارئة تتعلق بأحد الموردين، نأسف لإبلاغكم بتأجيل...
```

### 5. Validate Your Skill | تحقق من صحتك

Run the validation tool:

```bash
node tools/validate-skill.js skills/business/arabic-email-drafter/SKILL.md
```

**Expected output:**
```
✓ SKILL.md format valid
✓ All required fields present
✓ Arabic text detected
✓ Trigger keywords found
```

### 6. Test Your Skill (Optional) | اختبر مهارتك

```bash
node tools/test-skill.js skills/business/arabic-email-drafter/SKILL.md
```

This runs sample prompts and shows expected outputs.

### 7. Submit a Pull Request | قدم طلب سحب

1. Commit your changes:
```bash
git add skills/business/arabic-email-drafter/
git commit -m "feat: add arabic-email-drafter skill"
git push origin main
```

2. Use the "New Skill" issue template on GitHub
3. Link the issue in your PR description

---

## Quality Standards | معايير الجودة

### Arabic Text Quality | جودة النص العربي

- ✅ Must be proofread by a native speaker
- ✅ No direct translation artifacts (Google Translate style)
- ✅ Proper Arabic punctuation (، ؛ ؟ — not , ; ?)
- ✅ RTL direction maintained throughout

### Trigger Keywords | الكلمات المفتاحية

- ✅ Include Arabic phrases (e.g., "اكتب بريد إلكتروني")
- ✅ Include romanized/English equivalents (e.g., "write arabic email")
- ✅ Include domain-specific terms (e.g., "mena email template")

### Testing | الاختبار

- ✅ At least one example tested on Claude, GPT-4, or JAIS
- ✅ Output matches expected format
- ✅ No hallucinations or off-topic responses

### Compliance Skills | مهارات الامتثال

- ✅ Cite actual regulatory document section numbers
- ✅ Reference official control numbers (e.g., NCA ECC "1-1 Cybersecurity Strategy")
- ✅ Include both Arabic and English regulatory terms

---

## Volunteer Badges | شارات المتطوعين

| Badge | Requirement | Recognition |
|-------|-------------|-------------|
| 🥉 Bronze | Merged 1 skill | Contributor status |
| 🥈 Silver | Merged 5 skills | Featured contributor |
| 🥇 Gold | Merged 10 skills | Domain expert status |
| 🏆 Expert | Domain lead (gov, healthcare, etc.) | Repository maintainer |

---

## Code of Conduct | مدونة السلوك

- Be respectful and inclusive
- Arabic dialect diversity is celebrated
- No political or controversial content in skills
- Focus on professional, educational, and technical domains

---

## Need Help? | تحتاج مساعدة؟

- **Documentation**: Check `docs/` for guides on Arabic RTL writing, dialects, and MENA compliance
- **Issues**: Open a GitHub issue with questions
- **Discussions**: Use GitHub Discussions for skill ideas and feedback

---

## Thank You! | شكراً لك!

**English**: Your contribution helps bridge the Arabic AI gap. Every skill you add makes Arabic more accessible in the AI ecosystem.

**العربية**: مساهمتك تساعد في سد الفجوة العربية في الذكاء الاصطناعي. كل مهارة تضيفها تجعل العربية أكثر سهولة في نظام الذكاء الاصطناعي.

---

<div align="center">

**جزاك الله خيراً • Thank you for contributing!**

</div>
