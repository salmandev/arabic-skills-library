---
name: arabic-docker-kubernetes
name_ar: دوكر وكوبرنتيس
description: Master Docker and Kubernetes in Arabic
description_ar: إتقان دوكر وكوبرنتيس بالعربية
category: devops-advanced
language: ar
dialect: msa
rtl: true
platform_all: true
version: 1.0.0
author: salman-shaikh
---

## الهدف

إتقان أساسيات Docker و Kubernetes لإدارة الحاويات.

## Docker أساسيات

### ١. صور وحاويات

```
✓ بناء صور
✓ تشغيل حاويات
✓ إدارة volumes
✓ شبكات حاويات
```

### ٢. Dockerfile

```dockerfile
FROM python:3.9
WORKDIR /app
COPY . .
RUN pip install -r requirements.txt
CMD ["python", "app.py"]
```

## Kubernetes أساسيات

### ١. موارد أساسية

**الأنواع:**
- Pods
- Deployments
- Services
- ConfigMaps
- Secrets

### ٢. أوامر أساسية

```bash
kubectl get pods
kubectl apply -f deployment.yaml
kubectl scale deployment my-app --replicas=3
kubectl logs my-pod
```

## أفضل الممارسات

✅ صور صغيرة
✅ Health Checks
✅ Resource Limits
✅ Security Context

❌ لا تشغل كـ root
❌ لا تهمل موارد
❌ لا تهمل أمان

---

## الكلمات المفتاحية

عربي: "دوكر", "كوبرنتيس", "Docker", "Kubernetes", "حاويات"
English: "Docker arabic", "Kubernetes arabic", "containers", "container orchestration"

---

## سجل التغييرات

### v1.0.0
- الإصدار الأولي
