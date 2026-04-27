---
name: arabic-terraform
name_ar: تيرا فورم
description: Master Infrastructure as Code with Terraform in Arabic
description_ar: إتقان البنية التحتية ككود مع تيرا فورم بالعربية
category: developer
language: ar
dialect: msa
rtl: true
platform_all: true
version: 1.0.0
author: salman-shaikh
---

## الهدف

إتقان إدارة البنية التحتية ككود باستخدام Terraform باللغة العربية.

## المفاهيم الأساسية

| المصطلح | العربية | الوصف |
|---------|---------|-------|
| Provider | المزود | AWS, Azure, GCP |
| Resource | المورد | خادم، قاعدة بيانات |
| State | الحالة | ملف tfstate |
| Module | الوحدة | مكون قابل لإعادة الاستخدام |
| Variable | المتغير | معامل قابل للتخصيص |
| Output | المخرج | قيمة مصدرة |

## هيكل الملف

```
project/
├── main.tf
├── variables.tf
├── outputs.tf
├── terraform.tfvars
└── modules/
```

## أوامر Terraform

```bash
# تهيئة
terraform init

# تنسيق الكود
terraform fmt

# التحقق
terraform validate

# عرض الخطة
terraform plan

# تطبيق
terraform apply

# تدمير
terraform destroy

# عرض الحالة
terraform state list
```

## مثال كامل

```hcl
# المزود
provider "aws" {
  region = "us-east-1"
}

# متغيرات
variable "instance_type" {
  description = "نوع المثيل"
  type        = string
  default     = "t2.micro"
}

# مورد EC2
resource "aws_instance" "web" {
  ami           = "ami-0c55b159cbfafe1f0"
  instance_type = var.instance_type

  tags = {
    Name  = "خادم ويب"
    Environment = "إنتاج"
  }
}

# Security Group
resource "aws_security_group" "web_sg" {
  name = "web-sg"

  ingress {
    from_port   = 80
    to_port     = 80
    protocol    = "tcp"
    cidr_blocks = ["0.0.0.0/0"]
  }

  egress {
    from_port   = 0
    to_port     = 0
    protocol    = "-1"
    cidr_blocks = ["0.0.0.0/0"]
  }
}

# مخرجات
output "instance_ip" {
  value = aws_instance.web.public_ip
}
```

## Modules

```hcl
module "vpc" {
  source = "terraform-aws-modules/vpc/aws"

  name = "my-vpc"
  cidr = "10.0.0.0/16"

  azs             = ["us-east-1a", "us-east-1b"]
  private_subnets = ["10.0.1.0/24", "10.0.2.0/24"]
  public_subnets  = ["10.0.101.0/24", "10.0.102.0/24"]
}
```

## أفضل الممارسات

✅ استخدام remote state (S3 + DynamoDB)
✅ استخدام modules لإعادة الاستخدام
✅ تسمية واضحة للموارد
✅ استخدام tags بشكل متسق
✅ مراجعة plan قبل apply
✅ استخدام workspaces للبيئات

❌ لا commit ملف tfstate
❌ لا تستخدم hard-coded values
❌ لا تشارك access keys

---

## الكلمات المفتاحية

عربي: "تيرا فورم", "بنية تحتية ككود", "IaC"
English: "terraform arabic", "infrastructure as code", "devops"

---

## سجل التغييرات

### v1.0.0
- الإصدار الأولي
