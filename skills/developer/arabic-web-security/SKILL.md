---
name: arabic-web-security
name_ar: أمن الويب
description: Master web application security in Arabic
description_ar: إتقان أمن تطبيقات الويب بالعربية
category: developer
language: ar
dialect: msa
rtl: true
platform_all: true
version: 1.0.0
author: salman-shaikh
---

## الهدف

حماية تطبيقات الويب من الثغرات الأمنية الشائعة باللغة العربية.

## OWASP Top 10

### ١. حقن SQL (SQL Injection)

**المشكلة:**
```sql
-- كود غير آمن
query = "SELECT * FROM users WHERE username = '" + user_input + "'"
```

**الحل:**
```python
# استخدام Prepared Statements
cursor.execute("SELECT * FROM users WHERE username = %s", (username,))
```

### ٢. كسر المصادقة (Broken Authentication)

**الحماية:**
```
✅ استخدام HTTPS دائماً
✅ تخزين كلمات مرور مشفرة (bcrypt)
✅ تفعيل MFA
✅ تحديد محاولات الدخول
✅ تجديد Session ID بعد الدخول
```

### ٣. تسرب بيانات حساسة (Data Exposure)

**الحماية:**
```
✅ تشفير البيانات الحساسة
✅ عدم تخزين بيانات غير ضرورية
✅ استخدام TLS 1.3
✅ تعطل الكاش للبيانات الحساسة
```

### ٤. كائنات خارجية غير آمنة (XXE)

**المشكلة:**
```xml
<!-- هجوم XXE -->
<!DOCTYPE foo [<!ENTITY xxe SYSTEM "file:///etc/passwd">]>
```

**الحل:**
```python
# تعطيل DTD
parser = defusedxml.ElementTree.parse(xml_string)
```

### ٥. كسر التحكم في الوصول (Broken Access Control)

**الحماية:**
```python
# التحقق من الصلاحيات
@require_role('admin')
def delete_user(user_id):
    # التحقق من الملكية
    if not current_user.owns(user_id):
        abort(403)
```

### ٦. إعدادات أمان خاطئة (Security Misconfiguration)

**قائمة فحص:**
```
□ تعطيل صفحات الخطأ التفصيلية
□ إزالة ملفات افتراضية
□ تحديث جميع الأنظمة
□ تفعيل Security Headers
□ إغلاق منافذ غير ضرورية
```

### ٧. برمجية فدية (XSS)

**الوقاية:**
```javascript
// تنظيف المدخلات
function sanitize(input) {
    return input.replace(/[<>\"'&]/g, function(c) {
        return {'<':'&lt;','>':'&gt;','"':'&quot;',"'":'&#x27;','&':'&amp;'}[c];
    });
}
```

### ٨. تحميل غير آمن (Insecure Deserialization)

**الحماية:**
```
✅ لا تفك كائنات من مصادر غير موثوقة
✅ تحقق من التوقيع الرقمي
✅ استخدم تنسيق JSON بدلاً من Pickle
```

### ٩. استخدام مكونات بها ثغرات

**الحل:**
```bash
# فحص التبعيات
npm audit
pip-audit
snyk test
```

### ١٠. تسجيل ومراقبة غير كافية (Logging)

**ما يجب تسجيله:**
```
✅ محاولات دخول فاشلة
✅ أخطاء تطبيق
✅ وصول لبيانات حساسة
✅ تغييرات صلاحيات
✅ نشاط مشبوه
```

## Security Headers

```nginx
# Nginx Configuration
add_header X-Frame-Options "DENY" always;
add_header X-Content-Type-Options "nosniff" always;
add_header X-XSS-Protection "1; mode=block" always;
add_header Strict-Transport-Security "max-age=31536000" always;
add_header Content-Security-Policy "default-src 'self'" always;
```

## أفضل الممارسات

✅ تحقق من جميع المدخلات
✅ استخدم مكتبات أمان معتمدة
✅ حدّث التبعيات بانتظام
✅ فعّل HTTPS
✅ استخدم Prepared Statements
✅ طبّق Principle of Least Privilege
✅ راقب وسجّل النشاط

❌ لا تثق بمدخلات المستخدم
❌ لا تخزن كلمات مرور بنص واضح
❌ لا تعرض معلومات حساسة في أخطاء
❌ لا تستخدم كود قديم بدون مراجعة

---

## الكلمات المفتاحية

عربي: "أمن ويب", "حماية تطبيقات", "OWASP", "ثغرات"
English: "web security arabic", "application security", "OWASP"

---

## سجل التغييرات

### v1.0.0
- الإصدار الأولي
