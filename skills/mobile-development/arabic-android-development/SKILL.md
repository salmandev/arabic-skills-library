---
name: arabic-android-development
name_ar: تطوير أندرويد
description: Master Android development in Arabic
description_ar: إتقان تطوير تطبيقات أندرويد بالعربية
category: mobile-development
language: ar
dialect: msa
rtl: true
platform_all: true
version: 1.0.0
author: salman-shaikh
---

## الهدف

إتقان أساسيات تطوير تطبيقات Android.

## لغات برمجة

| اللغة | الوصف |
|-------|-------|
| **Kotlin** | حديثة، موصى بها |
| **Java** | تقليدية، لا تزال مستخدمة |

## Jetpack Compose أساسيات

```kotlin
import androidx.compose.ui.*

@Composable
fun Greeting(name: String) {
    Text(
        text = "مرحباً $name!",
        fontSize = 24.sp
    )
}

@Composable
fun App() {
    Column {
        Greeting("أحمد")
        Button(onClick = { /* action */ }) {
            Text("اضغط هنا")
        }
    }
}
```

## أدوات التطوير

| الأداة | الوصف |
|--------|-------|
| **Android Studio** | بيئة تطوير متكاملة |
| **Gradle** | نظام بناء |
| **Firebase** | خدمات Google |
| **Play Console** | نشر تطبيق |

## أفضل الممارسات

✅ اتبع Material Design
✅ صمم لأحجام شاشات مختلفة
✅ اختبر على أجهزة متعددة
✅ حسّن استهلاك بطارية

❌ لا تهمل الأداء
❌ لا تهمل الذاكرة
❌ لا تنسَLocalization

---

## الكلمات المفتاحية

عربي: "تطوير أندرويد", "Android", "Kotlin", "Jetpack Compose"
English: "Android development arabic", "Kotlin", "Android apps", "Jetpack Compose"

---

## سجل التغييرات

### v1.0.0
- الإصدار الأولي
