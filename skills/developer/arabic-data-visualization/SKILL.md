---
name: arabic-data-visualization
name_ar: تصور البيانات بالعربية
description: Create Arabic data visualizations with proper RTL formatting and localization
description_ar: إنشاء تصورات بيانات عربية مع تنسيق RTL وترجمة صحيحة
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

يساعد هذه المهارة في إنشاء تصورات بيانات (Data Visualizations) باللغة العربية مع دعم كامل لاتجاه RTL، والأرقام العربية المشرقية، والترجمة الصحيحة للمصطلحات التقنية، وتنسيقات التواريخ العربية.

---

## متى تستخدم هذه المهارة (When to Use)

استخدم هذه المهارة عندما تحتاج إلى:

- إنشاء رسوم بيانية بالعربية
- تصميم لوحات معلومات (Dashboards) عربية
- تحويل أرقام غربية إلى مشرقية
- تنسيق تواريخ هجرية
- تعريب مصطلحات تقنية في الرسوم

---

## تعليمات النموذج (Model Instructions)

أنت خبير في تصور البيانات وتعريب الواجهات. عند إنشاء التصور:

### مبادئ التصور العربي

١. **اتجاه RTL**: دعم كامل لليمين لليسار
٢. **الأرقام**: استخدام المشرقية (٠١٢٣) أو الغربية حسب السياق
٣. **الخطوط**: خطوط عربية واضحة ومناسبة
٤. **التنسيق**: تواريخ هجرية وعملة ريال/درهم

### الأدوات المدعومة

- Matplotlib/Seaborn (Python)
- Plotly/Dash
- Tableau
- Power BI
- D3.js
- Chart.js

---

## مثال (Example)

**الطلب:**
```
أنشئ رسم بياني للمبيعات بالعربية.
```

**النتيجة المتوقعة:**
```
# تصور البيانات بالعربية

## Arabic Data Visualization Guide

---

## ١. إعداد البيئة

### ١.١ المكتبات المطلوبة

```python
import matplotlib.pyplot as plt
import seaborn as sns
import plotly.express as px
import pandas as pd
from arabic_reshaper import ArabicReshaper
from bidi.algorithm import get_display
```

### ١.٢ تكوين الخطوط العربية

```python
# إعداد الخط العربي
ARABIC_FONT = 'Arial'  # أو 'Noto Sans Arabic'
FONT_SIZE = 14

plt.rcParams['font.family'] = ARABIC_FONT
plt.rcParams['font.size'] = FONT_SIZE
plt.rcParams['axes.unicode_minus'] = False
```

---

## ٢. معالجة النصوص العربية

### ٢.١ إعادة تشكيل النص

```python
from arabic_reshaper import ArabicReshaper
from bidi.algorithm import get_display

def format_arabic_text(text):
    """إعادة تشكيل النص العربي للعرض الصحيح"""
    reshaper = ArabicReshaper()
    reshaped = reshaper.reshape(text)
    return get_display(reshaped)

# مثال
text = "المبيعات الشهرية"
formatted = format_arabic_text(text)
# النتيجة: "المبيعات الشهرية" (بشكل صحيح)
```

### ٢.٢ تحويل الأرقام

```python
def convert_to_arabic_indic(number):
    """تحويل الأرقام الغربية إلى مشرقية"""
    arabic_indic_digits = str.maketrans('0123456789', '٠١٢٣٤٥٦٧٨٩')
    return str(number).translate(arabic_indic_digits)

def convert_to_western(number):
    """تحويل الأرقام المشرقية إلى غربية"""
    western_digits = str.maketrans('٠١٢٣٤٥٦٧٨٩', '0123456789')
    return str(number).translate(western_digits)

# أمثلة
print(convert_to_arabic_indic(1234))  # ١٢٣٤
print(convert_to_western('٥٦٧'))  # 567
```

---

## ٣. رسوم Matplotlib بالعربية

### ٣.١ رسم عمودي

```python
import matplotlib.pyplot as plt

# البيانات
categories = ['الرياض', 'جدة', 'الدمام', 'مكة', 'المدينة']
values = [450, 380, 290, 520, 310]

# معالجة النصوص
categories_ar = [format_arabic_text(c) for c in categories]
values_label = [convert_to_arabic_indic(v) for v in values]

# إنشاء الرسم
fig, ax = plt.subplots(figsize=(10, 6))
bars = ax.bar(categories_ar, values, color=['#1f77b4', '#ff7f0e', '#2ca02c', '#d62728', '#9467bd'])

# تنسيق المحاور
ax.set_xlabel(format_arabic_text('المدن'), fontsize=14, fontname=ARABIC_FONT)
ax.set_ylabel(format_arabic_text('المبيعات (ألف ريال)'), fontsize=14, fontname=ARABIC_FONT)
ax.set_title(format_arabic_text('المبيعات حسب المدينة - ٢٠٢٥'), fontsize=16, fontname=ARABIC_FONT, pad=20)

# إضافة القيم على الأعمدة
for bar, val in zip(bars, values):
    height = bar.get_height()
    ax.text(bar.get_x() + bar.get_width()/2., height,
            f'{convert_to_arabic_indic(val)}',
            ha='center', va='bottom', fontsize=12, fontname=ARABIC_FONT)

# عكس الاتجاه لـ RTL
ax.invert_xaxis()

plt.tight_layout()
plt.savefig('arabic_bar_chart.png', dpi=300, bbox_inches='tight')
plt.show()
```

### ٣.٢ رسم دائري

```python
# البيانات
labels = ['إلكترونيات', 'ملابس', 'منزل', 'رياضة', 'أخرى']
sizes = [35, 25, 20, 15, 5]
colors = ['#ff9999', '#66b3ff', '#99ff99', '#ffcc99', '#c2c2f0']

# معالجة النصوص
labels_ar = [format_arabic_text(l) for l in labels]
sizes_label = [convert_to_arabic_indic(s) for s in sizes]

# إنشاء الرسم الدائري
fig, ax = plt.subplots(figsize=(8, 8))
wedges, texts, autotexts = ax.pie(sizes, labels=labels_ar, colors=colors,
                                   autopct=lambda pct: f'{convert_to_arabic_indic(int(pct))}%',
                                   startangle=90, counterclock=False)

# تنسيق الخط
for text in texts + autotexts:
    text.set_fontname(ARABIC_FONT)
    text.set_fontsize(12)

ax.set_title(format_arabic_text('توزيع المبيعات حسب الفئة'), fontsize=16, fontname=ARABIC_FONT, pad=20)

plt.savefig('arabic_pie_chart.png', dpi=300, bbox_inches='tight')
plt.show()
```

### ٣.٣ رسم خطي

```python
import numpy as np

# البيانات - الأشهر الهجرية
months = ['محرم', 'صفر', 'ربيع الأول', 'ربيع الثاني', 'جمادى الأولى', 'جمادى الآخرة',
          'رجب', 'شعبان', 'رمضان', 'شوال', 'ذو القعدة', 'ذو الحجة']
sales = [120, 135, 145, 138, 155, 162, 148, 170, 220, 165, 158, 175]

# معالجة النصوص
months_ar = [format_arabic_text(m) for m in months]
sales_ar = [convert_to_arabic_indic(s) for s in sales]

# إنشاء الرسم
fig, ax = plt.subplots(figsize=(14, 6))
ax.plot(months_ar, sales, marker='o', linewidth=2, markersize=8, color='#2e86ab')
ax.fill_between(months_ar, sales, alpha=0.3, color='#2e86ab')

# تنسيق
ax.set_xlabel(format_arabic_text('الشهر الهجري'), fontsize=14, fontname=ARABIC_FONT)
ax.set_ylabel(format_arabic_text('المبيعات (ألف ريال)'), fontsize=14, fontname=ARABIC_FONT)
ax.set_title(format_arabic_text('المبيعات الشهرية - العام الهجري ١٤٤٦'), fontsize=16, fontname=ARABIC_FONT, pad=20)

# تدوير التسميات
plt.xticks(rotation=45, ha='right', fontname=ARABIC_FONT)

# إضافة شبكة
ax.grid(True, alpha=0.3)

plt.tight_layout()
plt.savefig('arabic_line_chart.png', dpi=300, bbox_inches='tight')
plt.show()
```

---

## ٤. Plotly التفاعلي

### ٤.١ رسم تفاعلي

```python
import plotly.express as px
import plotly.io as pio

# إعدادات RTL
pio.templates.default = 'plotly_white'
pio.kaleido.scope.mathjax = None

# البيانات
df = pd.DataFrame({
    'المنطقة': ['المنطقة الشرقية', 'منطقة الرياض', 'منطقة مكة', 'منطقة المدينة', 'منطقة القصيم'],
    'المبيعات': [850, 1200, 980, 420, 310],
    'الأرباح': [120, 180, 145, 65, 48]
})

# معالجة النصوص
df['المنطقة'] = df['المنطقة'].apply(format_arabic_text)

# إنشاء الرسم
fig = px.bar(df, x='المنطقة', y='المبيعات', 
             title=format_arabic_text('المبيعات والأرباح حسب المنطقة'),
             labels={'المنطقة': format_arabic_text('المنطقة'), 
                     'المبيعات': format_arabic_text('المبيعات (ألف ريال)')},
             color='المبيعات',
             color_continuous_scale='Blues')

# تنسيق RTL
fig.update_layout(
    font=dict(family=ARABIC_FONT, size=14),
    title_font=dict(family=ARABIC_FONT, size=18),
    xaxis_title=format_arabic_text('المنطقة'),
    yaxis_title=format_arabic_text('المبيعات'),
    xaxis={'categoryorder': 'total descending'},
    height=600,
    width=1000
)

fig.write_html('arabic_interactive_chart.html')
fig.show()
```

---

## ٥. لوحة معلومات كاملة

### ٥.١ Dashboard بالعربية

```python
import dash
from dash import dcc, html
import plotly.graph_objects as go

app = dash.Dash(__name__)

# تصميم RTL
app.layout = html.Div([
    html.Div([
        html.H1(format_arabic_text('لوحة معلومات المبيعات'), 
                style={'textAlign': 'right', 'fontFamily': ARABIC_FONT}),
    ], style={'backgroundColor': '#2e86ab', 'padding': '20px', 'color': 'white'}),
    
    html.Div([
        # الرسم ١
        html.Div([
            html.H3(format_arabic_text('المبيعات حسب المنطقة'), 
                    style={'textAlign': 'right', 'fontFamily': ARABIC_FONT}),
            dcc.Graph(id='region-chart', figure=region_fig)
        ], className='six columns'),
        
        # الرسم ٢
        html.Div([
            html.H3(format_arabic_text('المبيعات الشهرية'), 
                    style={'textAlign': 'right', 'fontFamily': ARABIC_FONT}),
            dcc.Graph(id='monthly-chart', figure=monthly_fig)
        ], className='six columns'),
    ], className='row'),
    
    # الجدول
    html.Div([
        html.H3(format_arabic_text('تفاصيل المبيعات'), 
                style={'textAlign': 'right', 'fontFamily': ARABIC_FONT}),
        html.Table([
            html.Thead([
                html.Tr([html.Th(format_arabic_text(col)) for col in ['المنطقة', 'المبيعات', 'الأرباح', 'النمو']])
            ]),
            html.Tbody([
                html.Tr([
                    td(format_arabic_text(str(row['المنطقة']))),
                    td(convert_to_arabic_indic(row['المبيعات'])),
                    td(convert_to_arabic_indic(row['الأرباح'])),
                    td(convert_to_arabic_indic(f"{row['النمو']}%"))
                ]) for _, row in df.iterrows()
            ])
        ])
    ], style={'marginTop': '20px'}),
    
], style={'direction': 'rtl', 'fontFamily': ARABIC_FONT})

if __name__ == '__main__':
    app.run_server(debug=True)
```

---

## ٦. Power BI / Tableau

### ٦.١ إعدادات Power BI

```
١. File → Options → Regional Format:
   - اختر "Arabic (Saudi Arabia)"

٢. تنسيق الأرقام:
   - تنسيق مخصص: ٠؛-٠؛٠
   - استخدام الأرقام المشرقية

٣. الخطوط:
   - الخط الافتراضي: Arial أو Noto Sans Arabic
   - حجم الخط: ١٤ للعناوين، ١٢ للنصوص

٤. الاتجاه:
   - Page View → Right-to-Left
```

### ٦.٢ تعريب التسميات

| English | العربية |
|---------|---------|
| Sales | المبيعات |
| Revenue | الإيرادات |
| Profit | الربح |
| Cost | التكلفة |
| Quantity | الكمية |
| Date | التاريخ |
| Region | المنطقة |
| Category | الفئة |
| Growth | النمو |
| Target | الهدف |

---

## ٧. أفضل الممارسات

### ٧.١ الخطوط الموصى بها

| الخط | الاستخدام | التوفر |
|------|----------|--------|
| **Arial** | عام | متاح عالمياً |
| **Noto Sans Arabic** | ويب | Google Fonts |
| **Tajawal** | عصري | Google Fonts |
| **Cairo** | عناوين | Google Fonts |
| **IBM Plex Sans Arabic** | تقني | Google Fonts |

### ٧.٢ الألوان المناسبة

```python
# لوحة ألوان مناسبة للثقافة العربية
ARABIC_COLOR_PALETTE = {
    'primary': '#1f77b4',    # أزرق
    'secondary': '#ff7f0e',  # برتقالي
    'success': '#2ca02c',    # أخضر
    'danger': '#d62728',     # أحمر
    'warning': '#ffcc00',    # أصفر
    'info': '#17becf',       # فيروزي
}
```

### ٧.٣ تنسيق التواريخ

```python
from hijri_converter import convert
from datetime import datetime

def format_hijri_date(gregorian_date):
    """تحويل التاريخ الميلادي إلى هجري"""
    h = convert.from_gregorian(
        gregorian_date.year,
        gregorian_date.month,
        gregorian_date.day
    )
    return f"{h.hijri_day()} {h.hijri_month_name()} {h.hijri_year()}هـ"

# مثال
gregorian = datetime(2025, 1, 15)
hijri = format_hijri_date(gregorian)
# النتيجة: "١٥ رجب ١٤٤٦هـ"
```

---

## ٨. قائمة التحقق

### قبل النشر

```
☐ جميع النصوص العربية معادة التشكيل بشكل صحيح
☐ الأرقام بالترسيق المطلوب (مشرقية/غربية)
☐ الاتجاه RTL مطبق
☐ الخطوط العربية واضحة
☐ التواريخ بالتنسيق الهجري (إذا لزم)
☐ العملة بالترميز المحلي (ر.س، د.إ)
☐ العناوين واضحة وموجزة
☐ الألوان مناسبة ومتباينة
☐ الرسم قابل للقراءة على جميع الأجهزة
```

---

## المراجع

- Matplotlib Arabic Text Guide
- Plotly RTL Layout
- Arabic Reshaper Library
- Hijri Converter

---

## سجل التغييرات

### v1.0.0
- الإصدار الأولي
```

---

## الكلمات المفتاحية

### العربية:
- "تصور بيانات عربي"
- "رسم بياني عربي"
- "تعريب رسوم"
- "لوحة معلومات عربية"
- "أرقام مشرقية"

### English:
- "arabic data visualization"
- "RTL charts arabic"
- "arabic dashboard"
- "arabic matplotlib"
- "arabic plotly"

---

## سجل التغييرات

### v1.0.0
- الإصدار الأولي
