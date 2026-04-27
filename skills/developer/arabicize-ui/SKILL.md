---
name: arabicize-ui
name_ar: عربة واجهة المستخدم
description: Convert English UI strings to natural Arabic with proper RTL layout
description_ar: تحويل نصوص واجهة المستخدم الإنجليزية إلى عربية طبيعية مع تخطيط RTL الصحيح
category: developer
language: bilingual
dialect: msa
rtl: true
platform_claude: true
platform_gpt: true
platform_qwen: true
platform_jais: true
platform_falcon: true
platform_allam: true
compliance: []
version: 1.0.0
author: salman-shaikh
contributor_volunteer: true
---

## Purpose | الهدف

**English**: Convert English UI strings, labels, and interface text to natural, concise Arabic suitable for apps and websites with RTL support.

**العربية**: تحويل نصوص واجهة المستخدم الإنجليزية والتسميات والنصوص الواجهية إلى عربية طبيعية وموجزة مناسبة للتطبيقات والمواقع مع دعم RTL.

---

## When to Use | متى تستخدم هذه المهارة

**English**: Use this skill when you need to:
- Localize app interfaces to Arabic
- Translate website UI elements
- Convert button labels and menu items
- Adapt forms for Arabic users
- RTL-ify your application

**العربية**: استخدم هذه المهارة عندما تحتاج إلى:
- تعريب واجهات التطبيقات
- ترجمة عناصر واجهة الموقع
- تحويل تسميات الأزرار وعناصر القائمة
- تكييف النماذج للمستخدمين العرب
- جعل تطبيقك متوافقاً مع RTL

---

## Model Instructions | تعليمات النموذج

### English Instructions

You are a UI/UX localization specialist. When translating UI:

1. **Keep it Short**:
   - Arabic text can be 30-50% longer
   - Plan for text expansion
   - Use concise phrasing

2. **Common UI Patterns**:
   - Use standard Arabic UI terminology
   - Maintain consistency
   - Consider cultural appropriateness

3. **RTL Considerations**:
   - Icons may need mirroring
   - Layout direction changes
   - Number formatting

### التعليمات بالعربية

أنت متخصص في تعريب واجهات المستخدم. عند ترجمة الواجهة:

١. **اجعلها قصيرة**:
   - النص العربي قد يكون أطول بنسبة ٣٠-٥٠٪
   - خطط لتوسع النص
   - استخدم صياغة موجزة

٢. **أنماط واجهة شائعة**:
   - استخدم مصطلحات واجهة عربية قياسية
   - حافظ على الاتساق
   - راعِ الملاءمة الثقافية

٣. **اعتبارات RTL**:
   - الأيقونات قد تحتاج عكس
   - تغيير اتجاه التخطيط
   - تنسيق الأرقام

---

## Output Format | صيغة المخرجات

```markdown
# تعريب واجهة المستخدم | UI Localization

## التنقل | Navigation

| English | العربية | Notes |
|---------|---------|-------|
| Home | الرئيسية | |
| About | من نحن | |
| Services | الخدمات | |
| Contact | اتصل بنا | |
| Login | تسجيل الدخول | |
| Sign Up | إنشاء حساب | |
| Logout | تسجيل الخروج | |
| Profile | الملف الشخصي | |
| Settings | الإعدادات | |
| Search | بحث | |

## الأزرار | Buttons

| English | العربية | Context |
|---------|---------|---------|
| Submit | إرسال | Forms |
| Cancel | إلغاء | |
| Save | حفظ | |
| Delete | حذف | |
| Edit | تعديل | |
| Add | إضافة | |
| Remove | إزالة | |
| Confirm | تأكيد | |
| Back | رجوع | |
| Next | التالي | |
| Previous | السابق | |
| Continue | متابعة | |

## النماذج | Forms

| English | العربية | Placeholder |
|---------|---------|-------------|
| Full Name | الاسم الكامل | أدخل اسمك الكامل |
| Email | البريد الإلكتروني | example@email.com |
| Password | كلمة المرور | •••••••• |
| Confirm Password | تأكيد كلمة المرور | •••••••• |
| Phone Number | رقم الهاتف | +966 XX XXX XXXX |
| Address | العنوان | أدخل عنوانك |
| City | المدينة | |
| Country | الدولة | |
| Postal Code | الرمز البريدي | |

## الرسائل | Messages

| English | العربية | Type |
|---------|---------|------|
| Success! | نجح! | Success |
| Error | خطأ | Error |
| Warning | تحذير | Warning |
| Loading... | جاري التحميل... | Info |
| No results found | لا توجد نتائج | Info |
| Please try again | يرجى المحاولة مرة أخرى | Info |
| Are you sure? | هل أنت متأكد؟ | Confirm |
| Changes saved | تم حفظ التغييرات | Success |
| Invalid input | إدخال غير صالح | Error |
| Field required | الحقل مطلوب | Error |

## القوائم | Menus

| English | العربية |
|---------|---------|
| Dashboard | لوحة التحكم |
| Reports | التقارير |
| Analytics | التحليلات |
| Users | المستخدمين |
| Products | المنتجات |
| Orders | الطلبات |
| Invoices | الفواتير |
| Notifications | الإشعارات |
| Messages | الرسائل |
| Help | المساعدة |

## RTL CSS Considerations | اعتبارات RTL CSS

```css
/* Original LTR */
.container {
  margin-left: 20px;
  padding-right: 10px;
  text-align: left;
}

/* RTL Version */
[dir="rtl"] .container {
  margin-left: 0;
  margin-right: 20px;
  padding-right: 0;
  padding-left: 10px;
  text-align: right;
}

/* Or use logical properties */
.container {
  margin-inline-start: 20px;
  padding-inline-end: 10px;
  text-align: start;
}
```
```

---

## Trigger Keywords | الكلمات المفتاحية

### Arabic Keywords | الكلمات العربية
- "تعريب واجهة"
- "UI عربي"
- "ترجمة تطبيق"
- "RTL عربي"
- "توطين واجهة"

### English Keywords | الكلمات الإنجليزية
- "arabic ui translation"
- "ui localization arabic"
- "arabic interface"
- "rtl arabic ui"
- "arabic app translation"

---

## Changelog | سجل التغييرات

### v1.0.0
- Initial release
