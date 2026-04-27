---
name: arabic-docker
name_ar: دوكر وحاويات
description: Master Docker and containerization in Arabic
description_ar: إتقان دوكر والحاويات باللغة العربية
category: developer
language: ar
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

## الهدف (Purpose)

يساعد هذه المهارة في إتقان Docker والحاويات باللغة العربية، بما في ذلك إنشاء الصور، إدارة الحاويات، الشبكات، التخزين، و Docker Compose لتسهيل نشر التطبيقات.

---

## مثال (Example)

**الطلب:**
```
اشرح Docker للمبتدئين.
```

**النتيجة المتوقعة:**
```
# دليل Docker الشامل

## Complete Docker Guide

---

## ١. المفاهيم الأساسية

| المصطلح | العربية | الوصف |
|---------|---------|-------|
| Image | الصورة | قالب جاهز للتطبيق |
| Container | الحاوية | نسخة قابلة للتشغيل من الصورة |
| Dockerfile | ملف دوكر | تعليمات بناء الصورة |
| Registry | السجل | مستودع الصور (Docker Hub) |
| Volume | المجلد | تخزين مستمر |
| Network | الشبكة | اتصال بين الحاويات |

---

## ٢. التثبيت والإعداد

```bash
# تثبيت Docker (Ubuntu)
sudo apt update
sudo apt install docker.io docker-compose

# إضافة المستخدم لمجموعة docker
sudo usermod -aG docker $USER

# التحقق من التثبيت
docker --version
docker run hello-world
```

---

## ٣. الأوامر الأساسية

### الصور (Images)

```bash
# سحب صورة
docker pull nginx:latest
docker pull python:3.11-slim

# عرض الصور
docker images
docker image ls

# حذف صورة
docker rmi nginx
docker image rm python:3.11

# بناء صورة من Dockerfile
docker build -t myapp:1.0 .
```

### الحاويات (Containers)

```bash
# تشغيل حاوية
docker run -d --name web -p 80:80 nginx

# عرض الحاويات
docker ps              # النشطة
docker ps -a           # جميعها

# إيقاف/تشغيل
docker stop web
docker start web
docker restart web

# حذف حاوية
docker rm web
docker rm -f web       # فرض الحذف

# الدخول للحاوية
docker exec -it web bash
docker exec -it web sh
```

---

## ٤. Dockerfile

### مثال كامل

```dockerfile
# صورة الأساس
FROM python:3.11-slim

# معلومات الصيانة
LABEL maintainer="ahmed@example.com"
LABEL version="1.0"

# متغيرات البيئة
ENV PYTHONDONTWRITEBYTECODE=1
ENV PYTHONUNBUFFERED=1

# مجلد العمل
WORKDIR /app

# نسخ المتطلبات
COPY requirements.txt .

# تثبيت التبعيات
RUN pip install --no-cache-dir -r requirements.txt

# نسخ الكود
COPY . .

# المنفذ
EXPOSE 8000

# أمر التشغيل
CMD ["python", "manage.py", "runserver", "0.0.0.0:8000"]
```

### تعليمات Dockerfile

| التعليمات | الوصف | مثال |
|-----------|-------|------|
| FROM | صورة الأساس | FROM node:18 |
| RUN | تشغيل أمر | RUN apt update |
| COPY | نسخ ملفات | COPY . /app |
| ADD | نسخ مع استخراج | ADD app.tar.gz /app |
| WORKDIR | مجلد العمل | WORKDIR /app |
| ENV | متغير بيئة | ENV NODE_ENV=production |
| EXPOSE | فتح منفذ | EXPOSE 3000 |
| CMD | أمر افتراضي | CMD ["npm", "start"] |
| ENTRYPOINT | نقطة الدخول | ENTRYPOINT ["python"] |

---

## ٥. Docker Compose

### ملف docker-compose.yml

```yaml
version: '3.8'

services:
  web:
    build: .
    ports:
      - "8000:8000"
    volumes:
      - .:/app
      - static_volume:/app/static
    environment:
      - DEBUG=1
      - DATABASE_URL=postgres://user:pass@db:5432/mydb
    depends_on:
      - db
    networks:
      - app-network

  db:
    image: postgres:15
    volumes:
      - postgres_data:/var/lib/postgresql/data
    environment:
      - POSTGRES_DB=mydb
      - POSTGRES_USER=user
      - POSTGRES_PASSWORD=pass
    networks:
      - app-network

  redis:
    image: redis:7-alpine
    networks:
      - app-network

volumes:
  postgres_data:
  static_volume:

networks:
  app-network:
    driver: bridge
```

### أوامر Compose

```bash
# تشغيل
docker-compose up
docker-compose up -d        # خلفية

# إيقاف
docker-compose down
docker-compose down -v      # مع حذف volumes

# عرض الحالة
docker-compose ps
docker-compose logs
docker-compose logs -f web  # تتبع

# إعادة بناء
docker-compose build
docker-compose build --no-cache

# تشغيل أمر
docker-compose exec web bash
docker-compose run web python manage.py migrate
```

---

## ٦. الشبكات (Networks)

```bash
# إنشاء شبكة
docker network create my-network

# عرض الشبكات
docker network ls

# توصيل حاوية
docker run -d --network my-network --name web nginx

# فحص الشبكة
docker network inspect my-network

# أنواع الشبكات:
# - bridge (افتراضي)
# - host (مباشرة مع النظام)
# - none (بدون شبكة)
# - overlay (بين hosts متعددة)
```

---

## ٧. التخزين (Volumes)

```bash
# إنشاء volume
docker volume create my-data

# عرض volumes
docker volume ls

# فحص volume
docker volume inspect my-data

# حذف volume
docker volume rm my-data

# أنواع التخزين:
# - Volume: يديره Docker
# - Bind Mount: مجلد من النظام
# - tmpfs: في الذاكرة فقط
```

---

## ٨. أمثلة عملية

### تطبيق Node.js

```dockerfile
FROM node:18-alpine
WORKDIR /app
COPY package*.json ./
RUN npm ci --only=production
COPY . .
EXPOSE 3000
CMD ["node", "server.js"]
```

### تطبيق Python/Django

```dockerfile
FROM python:3.11-slim
ENV PYTHONDONTWRITEBYTECODE=1
ENV PYTHONUNBUFFERED=1
WORKDIR /app
COPY requirements.txt .
RUN pip install -r requirements.txt
COPY . .
EXPOSE 8000
CMD ["gunicorn", "--bind", "0.0.0.0:8000", "myapp.wsgi"]
```

### تطبيق PHP/Laravel

```dockerfile
FROM php:8.2-fpm
RUN apt update && apt install -y \
    git curl libpng-dev libonig-dev libxml2-dev
RUN docker-php-ext-install pdo_mysql mbstring exif pcntl bcmath gd
COPY --from=composer:latest /usr/bin/composer /usr/bin/composer
WORKDIR /var/www
COPY . .
RUN composer install
RUN chown -R www-data:www-data /var/www/storage
EXPOSE 9000
CMD ["php-fpm"]
```

---

## ٩. أفضل الممارسات

✅ استخدم صور رسمية
✅ صور صغيرة (Alpine)
✅ طبقات قليلة في Dockerfile
✅ .dockerignore للملفات غير الضرورية
✅ volumes للبيانات المستمرة
✅ شبكات معزولة
✅ متغيرات بيئة للأسرار

❌ لا تخزن بيانات في الحاوية
❌ لا تستخدم latest في الإنتاج
❌ لا تشغل كـ root
❌ لا تكرر الأسرار في الصورة

---

## المراجع

- Docker Documentation
- Docker Hub
- Awesome Docker (GitHub)

---

## سجل التغييرات

### v1.0.0
- الإصدار الأولي
```

---

## الكلمات المفتاحية

### العربية:
- "دوكر"
- "حاويات"
- "docker compose"
- "dockerfile"
- "نشر تطبيقات"

### English:
- "docker arabic"
- "containerization"
- "docker tutorial"
- "docker compose arabic"
- "devops arabic"

---

## سجل التغييرات

### v1.0.0
- الإصدار الأولي
