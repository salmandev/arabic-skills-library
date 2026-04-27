---
name: arabic-system-design
name_ar: تصميم الأنظمة
description: Master system design principles in Arabic
description_ar: إتقان مبادئ تصميم الأنظمة بالعربية
category: developer
language: ar
dialect: msa
rtl: true
platform_all: true
version: 1.0.0
author: salman-shaikh
---

## الهدف

إتقان تصميم الأنظمة الموزعة والمعقدة باللغة العربية.

## المفاهيم الأساسية

| المفهوم | الوصف |
|---------|-------|
| Scalability | قابلية التوسع |
| Availability | التوفر |
| Reliability | الموثوقية |
| Consistency | الاتساق |
| Latency | زمن الوصول |
| Throughput | الإنتاجية |

## مبادئ التصميم

### ١. التحميل (Load Balancing)
```
Clients → Load Balancer → [Server 1, Server 2, Server 3]
```

### ٢. التخزين المؤقت (Caching)
```
Request → Cache? → Yes: Return | No: DB → Cache → Return
```

### ٣. قاعدة البيانات

#### أنواع قواعد البيانات:
- **SQL**: MySQL, PostgreSQL (علاقات، ACID)
- **NoSQL**: MongoDB, Redis (مرنة، سريعة)

#### استراتيجيات:
- **Replication**: نسخ متعددة
- **Sharding**: تقسيم البيانات
- **Partitioning**: تجزئة الجداول

### ٤. الطابور (Message Queue)
```
Producer → Queue → Consumer
```

## CAP Theorem

| CP | AP |
|----|----|
| Consistency + Partition | Availability + Partition |
| اختيار الاتساق | اختيار التوفر |

## تصميم نظام: مثال Twitter

### المتطلبات
- ١٠٠ مليون مستخدم نشط
- نشر تغريدات
- متابعة مستخدمين
- Timeline شخصي

### المكونات

```
┌──────────┐     ┌───────────┐
│   CDN    │────▶│   Web     │
└──────────┘     │  Server   │
                 └─────┬─────┘
                       │
            ┌──────────┼──────────┐
            │          │          │
            ▼          ▼          ▼
       ┌────────┐ ┌────────┐ ┌────────┐
       │  User  │ │  Tweet │ │  Feed  │
       │   DB   │ │   DB   │ │ Cache  │
       └────────┘ └────────┘ └────────┘
            │          │
            └──────────┘
                   │
             ┌─────▼─────┐
             │   Queue   │
             └───────────┘
```

## مقاييس الأداء

| المقياس | الهدف |
|---------|-------|
| Latency (P99) | < 100ms |
| Availability | 99.99% |
| Throughput | 100K req/s |

## أفضل الممارسات

✅ تصميم للفشل
✅ مراقبة شاملة
✅ توسع أفقي
✅ Caching استراتيجي
✅ Async processing

---

## الكلمات المفتاحية

عربي: "تصميم أنظمة", "system design", "هندسة برمجيات"
English: "system design arabic", "architecture", "scalability"

---

## سجل التغييرات

### v1.0.0
- الإصدار الأولي
