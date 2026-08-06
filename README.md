# 🧾 Smart Invoice Platform

A Google Workspace–powered automation platform that transforms manual warehouse invoices into secure, searchable, and fully traceable digital records — triggered by a single click.

---

## 🛠️ Tech Stack

![Google Apps Script](https://img.shields.io/badge/Google%20Apps%20Script-4285F4?style=for-the-badge&logo=google&logoColor=white)
![Google Sheets](https://img.shields.io/badge/Google%20Sheets-34A853?style=for-the-badge&logo=google-sheets&logoColor=white)
![Google Drive](https://img.shields.io/badge/Google%20Drive-4285F4?style=for-the-badge&logo=google-drive&logoColor=white)
![HTML](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![CSS](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)

---

## 📌 المشكلة

قبل هذه المنصة، كانت عملية إصدار فواتير المستودعات تتم يدوياً بالكامل:

- قام المشغلون بطباعة وتعبئة الفواتير يدويًا
- تبادل السائقون صورًا غير واضحة عبر واتساب عندما كان الفرع يطلب نسخة من الفاتورة
- تعرضت الفواتير المطبوعة للتلف أو الفقدان أو التلاعب
- لم يكن هناك مصدر موثوق للتحقق من صحة الفاتورة
- لم يكن هناك قاعدة بيانات يتم تسجيل الفواتير فيها

---

## ✅ الحل

### 1. نظرة عامة على المنصة
![Platform Overview](01-overview.png)

تطبيق ويب واحد مدعوم بـ Google Workspace — يربط Apps Script كمحرك للأتمتة، وGoogle Sheets كقاعدة بيانات للمنتجات، وGoogle Drive كأرشيف سحابي، وPDF كمخرج نهائي. واجهة واحدة، متكاملة بالكامل.

---

### 2. نموذج الفاتورة
![Invoice Form](02-invoice-form.png)

المشغل يُدخل فقط **رقم المنتج (SKU)** — وكل شيء آخر يتم تلقائيًا:

| الحقل | المصدر |
|---|---|
| POD ID | يتولد تلقائيًا |
| Submitted By | يُكتشف تلقائيًا (البريد الإلكتروني للمستخدم) |
| QR Code | يتولد تلقائيًا |
| Ship Date & Time | يُملأ تلقائيًا (الوقت الحالي) |
| Description | يُسترجع تلقائيًا من Google Sheets |
| Barcode | يُسترجع تلقائيًا من Google Sheets |
| Remaining Qty | القيمة الوحيدة التي تُدخل يدويًا |

---

### 3. نقرة واحدة ← سبع إجراءات تلقائية
![One Click Automation](03-one-click-automation.png)

الضغط على **Submit & Print** يُشغّل 7 خطوات تلقائية في آنٍ واحد:

| # | الإجراء | الحالة |
|---|---|---|
| 1 | توليد معرّف فاتورة فريد | ✅ تلقائي |
| 2 | التقاط بريد المستخدم المُرسِل | ✅ تلقائي |
| 3 | توليد QR Code قابل للمسح | ✅ تلقائي |
| 4 | توليد فاتورة PDF جاهزة للطباعة | ✅ تلقائي |
| 5 | تسجيل البيانات في Google Sheets | ✅ تلقائي |
| 6 | رفع الـ PDF إلى Google Drive | ✅ تلقائي |
| 7 | إرسال الفاتورة إلى الطابعة | ✅ تلقائي |

---

### 4. بوابة البحث عن الفواتير
![Invoice Lookup Portal](04-invoice-lookup-portal.png)

يستطيع أي موظف في الفرع استرداد الفاتورة الأصلية فورًا عن طريق إدخال رقم الشحنة (ST Number) — دون واتساب، دون بحث يدوي، ودون خطر تقديم نسخة مزوّرة. كل فرع يسحب من نفس المصدر الموثوق.

---

## 📁 هيكل المستودع

```
smart-invoice-platform/
├── index.html      → واجهة نموذج الفاتورة (Frontend)
├── Code.gs         → الكود الخلفي (Google Apps Script)
└── screenshots/    → صور عرض المشروع
```

---

> تم بناؤه كجزء من محفظة أتمتة — لتحويل سير العمل اليدوي إلى أنظمة رقمية موثوقة وقابلة للتتبع.
