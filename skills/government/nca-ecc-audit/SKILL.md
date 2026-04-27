---
name: nca-ecc-audit
name_ar: مراجعة متطلبات هيئة الأمن السيبراني
description: Audit systems against Saudi NCA ECC 2.0 cybersecurity controls
description_ar: مراجعة منهجية للأنظمة وفق الضوابط الأساسية للأمن السيبراني (الإصدار ٢.٠) الصادرة عن الهيئة الوطنية للأمن السيبراني
category: government
language: bilingual
dialect: msa
rtl: true
platform_claude: true
platform_gpt: true
platform_qwen: true
platform_jais: true
platform_falcon: true
platform_allam: true
compliance: [nca-ecc, vision2030]
version: 1.0.0
author: salman-shaikh
contributor_volunteer: true
---

## Purpose | الهدف

**English**: Systematically review infrastructure, processes, and code against the Saudi National Cybersecurity Authority's Essential Cybersecurity Controls (ECC 2.0). Generate compliance reports with control-by-control findings and remediation recommendations.

**العربية**: مراجعة منهجية للبنية التحتية والعمليات والكود البرمجي وفق الضوابط الأساسية للأمن السيبراني (الإصدار ٢.٠) الصادرة عن الهيئة الوطنية للأمن السيبراني السعودي. إنشاء تقارير امتثال مع نتائج لكل ضابط وتوصيات معالجة.

---

## When to Use | متى تستخدم هذه المهارة

**English**: Use this skill when you need to:

- Conduct NCA ECC compliance audit for Saudi government entities
- Prepare for NCA certification or external audit
- Assess cybersecurity posture against Saudi regulatory requirements
- Generate compliance reports for NCA submission
- Identify gaps in ECC control implementation

**العربية**: استخدم هذه المهارة عندما تحتاج إلى:

- إجراء مراجعة امتثال NCA ECC للكيان الحكومية السعودية
- التحضير لشهادة NCA أو مراجعة خارجية
- تقييم وضع الأمن السيبراني وفق المتطلبات التنظيمية السعودية
- إنشاء تقارير امتثال لتقديمها للهيئة
- تحديد الفجوات في تطبيق ضوابط ECC

---

## Model Instructions | تعليمات النموذج

### English Instructions

You are an NCA ECC compliance auditor with expertise in Saudi cybersecurity regulations. When conducting an audit:

1. **Review Control Domains**: Systematically assess all 4 ECC domains:
   - Domain 1: Cybersecurity Governance (حوكمة الأمن السيبراني)
   - Domain 2: Cybersecurity Defense (الدفاع السيبراني)
   - Domain 3: Cybersecurity Resilience (مرونة الأمن السيبراني)
   - Domain 4: Third-Party & Cloud Security (أمن الطرف الثالث والحوسبة السحابية)

2. **Evaluate Each Control**: For each control (e.g., 1-1, 2-1, 3-1):
   - Document evidence reviewed
   - Assess implementation status (Compliant/Partially Compliant/Non-Compliant)
   - Note gaps and deficiencies
   - Assign risk rating (Critical/High/Medium/Low)

3. **Generate Report**: Produce a structured compliance report with:
   - Executive Summary (Arabic)
   - Control-by-control findings table
   - Overall compliance percentage
   - Prioritized remediation roadmap

### التعليمات بالعربية

أنت مراجع امتثال NCA ECC خبير بأنظمة الأمن السيبراني السعودية. عند إجراء المراجعة:

١. **مراجعة مجالات الضوابط**: قيّم جميع مجالات ECC الأربعة منهجياً:
   - المجال ١: حوكمة الأمن السيبراني
   - المجال ٢: الدفاع السيبراني
   - المجال ٣: مرونة الأمن السيبراني
   - المجال ٤: أمن الطرف الثالث والحوسبة السحابية

٢. **تقييم كل ضابط**: لكل ضابط (مثال: ١-١، ٢-١، ٣-١):
   - وثّق الأدلة التي تمت مراجعتها
   - قيّم حالة التطبيق (متوافق/متوافق جزئياً/غير متوافق)
   - دوّن الفجوات وأوجه القصور
   - عيّن تصنيف المخاطر (حرج/عالي/متوسط/منخفض)

٣. **إنشاء التقرير**: أنتج تقرير امتثال منظم يتضمن:
   - ملخص تنفيذي (بالعربية)
   - جدول النتائج لكل ضابط
   - نسبة الامتثال الإجمالية
   - خريطة طريق معالجة ذات أولوية

---

## Control Domains | مجالات الضوابط

### Domain 1: Cybersecurity Governance | المجال ١: حوكمة الأمن السيبراني

#### Control 1-1: Cybersecurity Strategy | ضابط ١-١: استراتيجية الأمن السيبراني

**English**: Review for:
- Documented cybersecurity strategy aligned with organizational objectives
- Strategy approved by senior management
- Regular strategy reviews (at least annually)

**العربية**: راجع:
- استراتيجية أمن سيبراني موثقة متوافقة مع أهداف المؤسسة
- استراتيجية معتمدة من الإدارة العليا
- مراجعات استراتيجية منتظمة (سنوياً على الأقل)

#### Control 1-2: Cybersecurity Roles & Responsibilities | ضابط ١-٢: أدوار ومسؤوليات الأمن السيبراني

**English**: Review for:
- Defined cybersecurity organizational structure
- CISO appointment and independence
- Clear roles and responsibilities documented

**العربية**: راجع:
- هيكل تنظيمي محدد للأمن السيبراني
- تعيين مدير أمن المعلومات (CISO) واستقلاليته
- أدوار ومسؤوليات واضحة موثقة

#### Control 1-3: Asset Management | ضابط ١-٣: إدارة الأصول

**English**: Review for:
- Asset inventory (hardware, software, data, personnel)
- Asset classification (Secret/Confidential/Internal/Public)
- Asset ownership assignment
- Acceptable use policy

**العربية**: راجع:
- جرد الأصول (أجهزة، برمجيات، بيانات، موظفين)
- تصنيف الأصول (سري للغاية/سري/داخلي/عام)
- تعيين ملكية الأصول
- سياسة الاستخدام المقبول

#### Control 1-4: Identity & Access Management | ضابط ١-٤: إدارة الهوية والوصول

**English**: Review for:
- User registration and de-registration processes
- Access control policy (least privilege)
- Privileged access management
- Multi-factor authentication implementation

**العربية**: راجع:
- عمليات تسجيل وإلغاء تسجيل المستخدمين
- سياسة التحكم في الوصول (أقل امتيازات)
- إدارة الوصول المميز
- تطبيق المصادقة متعددة العوامل

---

### Domain 2: Cybersecurity Defense | المجال ٢: الدفاع السيبراني

#### Control 2-1: Network Security | ضابط ٢-١: أمن الشبكة

**English**: Review for:
- Network segmentation and DMZ design
- Firewall configuration and rules
- Network monitoring and intrusion detection
- Wireless security controls

**العربية**: راجع:
- تجزئة الشبكة وتصميم المنطقة منزوعة السلاح (DMZ)
- تكوين الجدران النارية والقواعد
- مراقبة الشبكة وكشف التسلل
- ضوابط أمن الشبكات اللاسلكية

#### Control 2-2: Endpoint Security | ضابط ٢-٢: أمن نقاط النهاية

**English**: Review for:
- Antivirus/EDR deployment (100% coverage)
- Device encryption (full disk)
- Mobile device management
- USB and removable media controls

**العربية**: راجع:
- نشر مكافحة الفيروسات/EDR (تغطية ١٠٠٪)
- تشفير الأجهزة (كامل القرص)
- إدارة الأجهزة المحمولة
- ضوابط USB والوسائط القابلة للإزالة

#### Control 2-3: Vulnerability Management | ضابط ٢-٣: إدارة الثغرات

**English**: Review for:
- Vulnerability scanning schedule (monthly minimum)
- Patch management SLAs:
  - Critical: 72 hours
  - High: 1 week
  - Medium: 1 month
  - Low: 3 months
- Penetration testing (annual)

**العربية**: راجع:
- جدول فحص الثغرات (شهرياً كحد أدنى)
- اتفاقيات مستوى خدمة إدارة التصحيحات:
  - حرج: ٧٢ ساعة
  - عالي: أسبوع واحد
  - متوسط: شهر واحد
  - منخفض: ٣ أشهر
- اختبار الاختراق (سنوي)

---

### Domain 3: Cybersecurity Resilience | المجال ٣: مرونة الأمن السيبراني

#### Control 3-1: Backup & Recovery | ضابط ٣-١: النسخ الاحتياطي والاسترداد

**English**: Review for:
- Backup frequency (daily for critical systems)
- Backup encryption (in transit and at rest)
- Offsite backup storage
- Backup restoration testing (quarterly)

**العربية**: راجع:
- تكرار النسخ الاحتياطي (يومياً للأنظمة الحرجة)
- تشفير النسخ الاحتياطي (أثناء النقل وفي حالة السكون)
- تخزين النسخ الاحتياطي خارج الموقع
- اختبار استعادة النسخ الاحتياطي (ربع سنوي)

#### Control 3-2: Business Continuity & Disaster Recovery | ضابط ٣-٢: استمرارية الأعمال والتعافي من الكوارث

**English**: Review for:
- BCP/DRP documentation
- RTO/RPO defined and tested
- DR drill frequency (annual minimum)
- Crisis management procedures

**العربية**: راجع:
- توثيق BCP/DRP
- تحديد واختبار RTO/RPO
- تكرار تدريبات التعافي من الكوارث (سنوياً كحد أدنى)
- إجراءات إدارة الأزمات

#### Control 3-3: Incident Management | ضابط ٣-٣: إدارة الحوادث

**English**: Review for:
- Incident response plan
- Incident classification and escalation
- NCA incident reporting (within 24 hours for critical)
- Post-incident review process

**العربية**: راجع:
- خطة الاستجابة للحوادث
- تصنيف الحوادث وتصعيدها
- الإبلاغ عن الحوادث للهيئة (خلال ٢٤ ساعة للحرجة)
- عملية مراجعة ما بعد الحادث

---

### Domain 4: Third-Party & Cloud Security | المجال ٤: أمن الطرف الثالث والحوسبة السحابية

#### Control 4-1: Third-Party Risk Management | ضابط ٤-١: إدارة مخاطر الطرف الثالث

**English**: Review for:
- Vendor risk assessment process
- Cybersecurity requirements in contracts
- Third-party access controls
- Continuous monitoring of third parties

**العربية**: راجع:
- عملية تقييم مخاطر الموردين
- متطلبات الأمن السيبراني في العقود
- ضوابط وصول الطرف الثالث
- المراقبة المستمرة للأطراف الثالثة

#### Control 4-2: Cloud Security | ضابط ٤-٢: أمن الحوسبة السحابية

**English**: Review for:
- Cloud service provider agreements
- Data residency requirements (Saudi data must stay in KSA for government)
- Cloud security configuration
- Exit strategy for cloud services

**العربية**: راجع:
- اتفاقيات مقدمي الخدمات السحابية
- متطلبات توطين البيانات (البيانات السعودية يجب أن تبقى في المملكة للجهات الحكومية)
- تكوين أمن السحابة
- استراتيجية الخروج من الخدمات السحابية

---

## Output Format | صيغة المخرجات

### Compliance Report Structure | هيكل تقرير الامتثال

```markdown
# تقرير امتثال NCA ECC 2.0
# NCA ECC 2.0 Compliance Report

## الملخص التنفيذي | Executive Summary

**نسبة الامتثال الإجمالية | Overall Compliance**: XX%

**تاريخ المراجعة | Audit Date**: YYYY-MM-DD
**الكيان المراجع | Audited Entity**: [Name]

### النتائج الرئيسية | Key Findings
- [X] ضوابط متوافقة | Compliant Controls
- [X] ضوابط متوافقة جزئياً | Partially Compliant Controls
- [X] ضوابط غير متوافقة | Non-Compliant Controls

## جدول النتائج التفصيلي | Detailed Findings Table

| الضابط | الحالة | تصنيف المخاطر | الفجوات | التوصيات |
|--------|--------|---------------|---------|-----------|
| 1-1 | متوافق | - | - | - |
| 1-2 | متوافق جزئياً | متوسط | [فجوات] | [توصيات] |
| ... | ... | ... | ... | ... |

## خريطة طريق المعالجة | Remediation Roadmap

### الأولوية ١ - حرج | Priority 1 - Critical
- [إجراءات فورية]

### الأولوية ٢ - عالي | Priority 2 - High
- [إجراءات خلال أسبوع]

### الأولوية ٣ - متوسط | Priority 3 - Medium
- [إجراءات خلال شهر]
```

---

## Trigger Keywords | الكلمات المفتاحية

### Arabic Keywords | الكلمات العربية

- "مراجعة متطلبات هيئة الأمن السيبراني"
- "فحص NCA ECC"
- "امتثال الأمن السيبراني السعودي"
- "تقرير NCA"
- "ضوابط ECC"
- "مراجعة الامتثال السيبراني"

### English Keywords | الكلمات الإنجليزية

- "nca ecc audit"
- "nca compliance review"
- "saudi cybersecurity compliance"
- "ecc 2.0 checklist"
- "nca ecc assessment"
- "saudi nca audit report"

---

## Compliance References | مراجع الامتثال

### NCA ECC 2.0 Official Controls | ضوابط NCA ECC ٢.٠ الرسمية

| Domain | Control | Reference |
|--------|---------|-----------|
| Cybersecurity Governance | 1-1 to 1-4 | NCA ECC 2.0 Section 1 |
| Cybersecurity Defense | 2-1 to 2-3 | NCA ECC 2.0 Section 2 |
| Cybersecurity Resilience | 3-1 to 3-3 | NCA ECC 2.0 Section 3 |
| Third-Party & Cloud | 4-1 to 4-2 | NCA ECC 2.0 Section 4 |

### Vision 2030 Alignment | محاذاة رؤية ٢٠٣٠

This skill supports Saudi Vision 2030 digital transformation objectives by ensuring cybersecurity compliance across government entities.

تدعم هذه المهارة أهداف التحول الرقمي لرؤية السعودية ٢٠٣٠ من خلال ضمان امتثال الأمن السيبراني عبر الكيانات الحكومية.

---

## Compatibility Notes | ملاحظات التوافق

### Claude
- Excellent for structured compliance analysis
- Strong at generating detailed reports

### GPT-4
- Good understanding of regulatory frameworks
- May need specific NCA ECC control references

### Qwen
- Supports bilingual output well
- Verify Arabic regulatory terminology

### JAIS
- Best for Arabic regulatory language
- Understands Saudi context natively

---

## Testing Guidelines | إرشادات الاختبار

### Test Case 1 | حالة اختبار ١

**Input**:
```
Review our organization's cybersecurity policy document against NCA ECC Control 1-1 (Cybersecurity Strategy).
```

**Expected Output**:
- Assessment of strategy alignment
- Gap analysis with specific control requirements
- Compliance rating with evidence

---

## References | المراجع

### English Resources
- NCA ECC 2.0 Official Documentation: https://nca.gov.sa/en/what-we-do/cybersecurity/ecc
- SAMA Cybersecurity Framework: https://www.sama.gov.sa

### الموارد العربية
- وثائق NCA ECC ٢.٠ الرسمية: https://nca.gov.sa/ar/what-we-do/cybersecurity/ecc
- إطار SAMA للأمن السيبراني: https://www.sama.gov.sa

---

## Changelog | سجل التغييرات

### v1.0.0
- Initial release
- Full NCA ECC 2.0 control coverage
- Bilingual report templates
