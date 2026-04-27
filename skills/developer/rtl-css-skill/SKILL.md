---
name: rtl-css-skill
name_ar: مهارة تصميم RTL
description: Generate RTL-compatible CSS for Arabic web interfaces
description_ar: توليد أوراق أنماط CSS متوافقة مع اتجاه اليمين لليسار لواجهات الويب العربية
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

**English**: Generate CSS stylesheets and components that properly support right-to-left (RTL) layouts for Arabic web applications. Includes logical properties, mirroring techniques, and best practices for bilingual websites.

**العربية**: توليد أوراق أنماط CSS ومكونات تدعم بشكل صحيح تخطيطات من اليمين لليسار (RTL) لتطبيقات الويب العربية. تتضمن الخصائص المنطقية وتقنيات عكس الاتجاه وأفضل الممارسات للمواقع ثنائية اللغة.

---

## When to Use | متى تستخدم هذه المهارة

**English**: Use this skill when you need to:

- Convert an English LTR website to Arabic RTL
- Create bilingual websites with language switching
- Fix RTL layout issues in existing Arabic interfaces
- Implement CSS logical properties for RTL support
- Mirror UI components (margins, paddings, icons) for Arabic
- Ensure proper text alignment and typography for Arabic

**العربية**: استخدم هذه المهارة عندما تحتاج إلى:

- تحويل موقع إنجليزي LTR إلى عربي RTL
- إنشاء مواقع ثنائية اللغة مع تبديل اللغة
- إصلاح مشاكل تخطيط RTL في الواجهات العربية الموجودة
- تطبيق خصائص CSS المنطقية لدعم RTL
- عكس مكونات واجهة المستخدم (هوامش، حشوات، أيقونات) للعربية
- ضمان محاذاة النص والطباعة الصحيحة للعربية

---

## Model Instructions | تعليمات النموذج

### English Instructions

You are an expert frontend developer specializing in RTL/CSS internationalization. When generating RTL CSS:

1. **Use CSS Logical Properties**: Replace physical properties with logical equivalents
   - `margin-left` → `margin-inline-start`
   - `margin-right` → `margin-inline-end`
   - `padding-left` → `padding-inline-start`
   - `padding-right` → `padding-inline-end`
   - `left` → `inset-inline-start`
   - `right` → `inset-inline-end`
   - `text-align: left` → `text-align: start`
   - `text-align: right` → `text-align: end`

2. **Implement Direction Switching**: Create CSS that respects the `dir` attribute
   ```css
   html[dir="rtl"] { ... }
   html[dir="ltr"] { ... }
   ```

3. **Mirror UI Components**: Flip directional elements
   - Navigation arrows
   - Icons with direction (arrows, chevrons)
   - Borders and shadows
   - Float and flex directions

4. **Typography Considerations**: 
   - Arabic font families (Tajawal, Cairo, Almarai, IBM Plex Sans Arabic)
   - Proper line-height for Arabic (1.6-1.8)
   - Font-size adjustments (Arabic may need +1-2px)

### التعليمات بالعربية

أنت مطور واجهات أمامية خبير متخصص في تدويل CSS/RTL. عند توليد CSS لـ RTL:

١. **استخدم الخصائص المنطقية لـ CSS**: استبدل الخصائص الفيزيائية بمكافئات منطقية
   - `margin-left` → `margin-inline-start`
   - `margin-right` → `margin-inline-end`
   - `padding-left` → `padding-inline-start`
   - `padding-right` → `padding-inline-end`
   - `left` → `inset-inline-start`
   - `right` → `inset-inline-end`
   - `text-align: left` → `text-align: start`
   - `text-align: right` → `text-align: end`

٢. **طبّق تبديل الاتجاه**: أنشئ CSS يحترم سمة `dir`
   ```css
   html[dir="rtl"] { ... }
   html[dir="ltr"] { ... }
   ```

٣. **اعكس مكونات واجهة المستخدم**: اقلب العناصر الاتجاهية
   - أسهم التنقل
   - الأيقونات ذات الاتجاه (أسهم، أشكال)
   - الحدود والظلال
   - اتجاهات float و flex

٤. **اعتبارات الطباعة**:
   - عائلات الخطوط العربية (Tajawal, Cairo, Almarai, IBM Plex Sans Arabic)
   - ارتفاع السطر المناسب للعربية (١.٦-١.٨)
   - تعديلات حجم الخط (العربية قد تحتاج +١-٢ بكسل)

---

## Output Format | صيغة المخرجات

### CSS Structure | هيكل CSS

```css
/* ===================================
   RTL-Aware CSS for Arabic Interfaces
   =================================== */

/* Base Direction Setup | إعداد الاتجاه الأساسي */
html {
  direction: ltr;
  text-align: start;
}

html[dir="rtl"] {
  direction: rtl;
  text-align: right;
}

/* Typography | الطباعة */
:root {
  --font-family-arabic: 'Tajawal', 'Cairo', 'Almarai', 'IBM Plex Sans Arabic', sans-serif;
  --font-size-arabic: 16px;
  --line-height-arabic: 1.7;
}

html[lang="ar"] {
  font-family: var(--font-family-arabic);
  font-size: var(--font-size-arabic);
  line-height: var(--line-height-arabic);
}

/* Navigation Example | مثال التنقل */
.nav {
  display: flex;
  justify-content: space-between;
  padding-inline-start: 20px;
  padding-inline-end: 20px;
}

.nav-item {
  margin-inline-end: 16px;
}

.nav-item:last-child {
  margin-inline-end: 0;
}

/* Icon Mirroring | عكس الأيقونات */
.icon-arrow {
  transform: scaleX(1);
}

html[dir="rtl"] .icon-arrow {
  transform: scaleX(-1);
}

/* Card Component | مكون البطاقة */
.card {
  border-radius: 8px;
  padding: 20px;
  text-align: start;
}

.card-icon {
  float: inline-start;
  margin-inline-end: 16px;
}

/* Form Inputs | حقول النموذج */
.input-group {
  display: flex;
  flex-direction: row;
}

.input-group input {
  border-inline-start: 1px solid #ccc;
  border-inline-end: none;
}

html[dir="rtl"] .input-group input {
  border-inline-start: none;
  border-inline-end: 1px solid #ccc;
}

/* Buttons with Icons | أزرار مع أيقونات */
.btn-with-icon {
  display: inline-flex;
  align-items: center;
  gap: 8px;
}

.btn-with-icon .icon {
  order: 0;
}

html[dir="rtl"] .btn-with-icon .icon {
  order: 0; /* Flexbox handles RTL automatically */
}

/* Tables | الجداول */
table {
  direction: inherit;
}

th, td {
  text-align: start;
  padding-inline-start: 12px;
  padding-inline-end: 12px;
}

/* Modal/Dialog | النوافذ المنبثقة */
.modal {
  position: fixed;
  inset-inline-start: 50%;
  transform: translateX(-50%);
}

html[dir="rtl"] .modal {
  transform: translateX(50%);
}

/* Close Button | زر الإغلاق */
.modal-close {
  position: absolute;
  top: 16px;
  inset-inline-end: 16px;
}

/* Dropdown Menu | قائمة منسدلة */
.dropdown-menu {
  position: absolute;
  inset-inline-start: 0;
  text-align: start;
}

/* Tooltip | تلميح */
.tooltip {
  position: absolute;
  inset-inline-start: 50%;
  transform: translateX(-50%);
}

/* Breadcrumbs | مسار التنقل */
.breadcrumb {
  display: flex;
  flex-direction: row;
}

.breadcrumb-item::after {
  content: '/';
  margin-inline-start: 8px;
  margin-inline-end: 8px;
}

html[dir="rtl"] .breadcrumb-item::after {
  content: '/'; /* Keep same or use Arabic » */
}

/* Pagination | ترقيم الصفحات */
.pagination {
  display: flex;
  flex-direction: row;
}

.pagination-item {
  margin-inline-end: 4px;
}

/* Sidebar | الشريط الجانبي */
.sidebar {
  float: inline-start;
  margin-inline-end: 20px;
}

.main-content {
  margin-inline-start: 0;
  margin-inline-end: 0;
}

/* Alerts/Notifications | التنبيهات */
.alert {
  display: flex;
  align-items: flex-start;
  text-align: start;
}

.alert-icon {
  margin-inline-end: 12px;
}

.alert-close {
  margin-inline-start: auto;
}

/* Progress Bar | شريط التقدم */
.progress-bar {
  direction: ltr; /* Numbers progress LTR even in RTL */
}

/* Slider/Range | شريط التمرير */
input[type="range"] {
  direction: ltr; /* Consistent behavior */
}

/* Lists | القوائم */
ul, ol {
  padding-inline-start: 24px;
  padding-inline-end: 0;
}

html[dir="rtl"] ul,
html[dir="rtl"] ol {
  padding-inline-start: 0;
  padding-inline-end: 24px;
}

/* Blockquote | اقتباس */
blockquote {
  border-inline-start: 4px solid #ccc;
  padding-inline-start: 16px;
  margin-inline-start: 0;
  margin-inline-end: 0;
}

html[dir="rtl"] blockquote {
  border-inline-start: none;
  border-inline-end: 4px solid #ccc;
  padding-inline-start: 0;
  padding-inline-end: 16px;
}

/* Responsive Considerations | اعتبارات متجاوبة */
@media (max-width: 768px) {
  .sidebar {
    float: none;
    margin-inline-end: 0;
  }
  
  .nav {
    flex-direction: column;
  }
  
  .nav-item {
    margin-inline-end: 0;
    margin-block-end: 8px;
  }
}
```

---

## Trigger Keywords | الكلمات المفتاحية

### Arabic Keywords | الكلمات العربية

- "تصميم RTL"
- "CSS للعربية"
- "من اليمين لليسار"
- "عكس الاتجاه"
- "موقع عربي"
- "واجهة عربية"

### English Keywords | الكلمات الإنجليزية

- "rtl css"
- "arabic web design"
- "right to left css"
- "rtl layout"
- "arabic interface css"
- "bilingual website css"
- "css logical properties"
- "rtl component"

---

## Compatibility Notes | ملاحظات التوافق

### Claude
- Excellent at generating comprehensive RTL CSS
- Understands logical properties well
- Provides detailed explanations

### GPT-4
- Strong CSS generation capabilities
- May need reminders for edge cases
- Good at explaining mirroring logic

### Qwen
- Supports RTL output
- Verify logical property usage
- May mix physical/logical properties

### JAIS
- Native Arabic understanding
- Best for Arabic comments in CSS
- Understands regional design preferences

---

## Testing Guidelines | إرشادات الاختبار

### Test Case 1: Navigation Component | حالة اختبار ١: مكون التنقل

**Input**:
```
Create RTL-aware CSS for a horizontal navigation bar with logo on the right (LTR) / left (RTL) and menu items.
```

**Expected Output**:
- Flexbox navigation with logical properties
- Proper logo positioning for both directions
- Menu items with correct spacing
- Mobile responsive RTL behavior

### Test Case 2: Form Layout | حالة اختبار ٢: تخطيط النموذج

**Input**:
```
Generate CSS for a bilingual form with labels and inputs that works in both LTR and RTL.
```

**Expected Output**:
- Label-input alignment for both directions
- Proper margin/padding using logical properties
- RTL-aware validation icons
- Submit button positioning

---

## References | المراجع

### English Resources
- MDN: CSS Logical Properties - https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Logical_Properties
- RTL Styling 101 - https://rtlstyling.com/posts/rtl-styling-101
- W3C: Internationalization Best Practices - https://www.w3.org/International/

### الموارد العربية
- دليل تطوير الويب العربي - https://arabicdevelopers.com
- أفضل الممارسات لتدويل الويب - https://www.w3.org/International/arabic

---

## Changelog | سجل التغييرات

### v1.0.0
- Initial release
- Full CSS logical properties coverage
- Bilingual documentation
- Component examples for common UI patterns
