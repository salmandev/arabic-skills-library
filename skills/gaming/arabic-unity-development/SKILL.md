---
name: arabic-unity-development
name_ar: تطوير يونيتي
description: Master Unity game development in Arabic
description_ar: إتقان تطوير الألعاب بيونيتي بالعربية
category: gaming
language: ar
dialect: msa
rtl: true
platform_all: true
version: 1.0.0
author: salman-shaikh
---

## الهدف

إتقان أساسيات تطوير الألعاب باستخدام Unity.

## مفاهيم أساسية

### ١. واجهة Unity

**النوافذ:**
- Scene View
- Game View
- Hierarchy
- Project
- Inspector

### ٢. GameObjects و Components

```
GameObject:
  - Transform
  - Mesh Renderer
  - Collider
  - Rigidbody
  - Scripts (C#)
```

### ٣. البرمجة بـ C#

```csharp
using UnityEngine;

public class PlayerController : MonoBehaviour
{
    void Update()
    {
        float moveX = Input.GetAxis("Horizontal");
        transform.Translate(Vector3.right * moveX);
    }
}
```

## أنواع الألعاب

| النوع | الأمثلة |
|-------|---------|
| **2D** | Platformers, Puzzle |
| **3D** | FPS, RPG, Adventure |
| **VR/AR** | Virtual/Augmented Reality |
| **Mobile** | Casual, Hyper-casual |

## أفضل الممارسات

✅ ابدأ بمشاريع صغيرة
✅ تعلم C# أساسيات
✅ استخدم Asset Store
✅ اختبر باستمرار

❌ لا تبالغ في النطاق
❌ لا تهمل الأداء
❌ لا تنسَ النشر

---

## الكلمات المفتاحية

عربي: "يونيتي", "Unity", "تطوير ألعاب", "C#"
English: "Unity arabic", "game development", "C#", "Unity3D"

---

## سجل التغييرات

### v1.0.0
- الإصدار الأولي
