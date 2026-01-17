---
date: 2026-01-17
description: تعلم كيفية رسم قوس باستخدام رسومات جافا مع Aspose.PSD لجافا. دليل خطوة
  بخطوة مع أمثلة شفرة لتطبيقات الرسوميات.
linktitle: Java Graphics Draw Arc with Aspose.PSD
second_title: Aspose.PSD Java API
title: رسم قوس في رسومات جافا باستخدام Aspose.PSD – دليل خطوة بخطوة
url: /ar/java/java-graphics-drawing/drawing-arcs/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java Graphics Draw Arc with Aspose.PSD

## Introduction
في هذا البرنامج التعليمي ستكتشف كيفية **java graphics draw arc** باستخدام مكتبة Aspose.PSD للغة Java. رسم الأقواس برمجيًا مفيد للمكونات المخصصة لواجهة المستخدم، التصورات البيانية، أو أي رسم يتطلب تحكمًا دقيقًا في المنحنى. سنمرّ بكل خطوة — من إعداد المشروع إلى رسم القوس وحفظ النتيجة — حتى تتمكن من إضافة هذه القدرة إلى تطبيقات Java الخاصة بك فورًا.

## Quick Answers
- **أي مكتبة تسمح لـ Java برسم الأقواس بسهولة؟** Aspose.PSD للغة Java.  
- **هل أحتاج إلى ترخيص للتطوير؟** نسخة تجريبية مجانية تكفي للاختبار؛ الترخيص مطلوب للإنتاج.  
- **ما صيغ الإخراج المدعومة؟** BMP، PNG، JPEG، TIFF، GIF، وأكثر.  
- **هل يمكنني تغيير سمك القوس أو لونه؟** نعم — عدّل خصائص كائن `Pen`.  
- **هل الكود متوافق مع Java 8+؟** بالتأكيد، الـ API تستهدف Java 8 وما فوق.

## What is “java graphics draw arc”?
تشير العبارة إلى استخدام كود Java لتصيير جزء منحني (قوس) على لوحة رسومات. مع Aspose.PSD، تحصل على فئة `Graphics` عالية المستوى التي تبسط عمليات الرسم، وتتعامل مع إدارة الألوان، وإزالة التعرجات، وتصدير الملفات خلف الكواليس.

## Why use Aspose.PSD for arc drawing?
- **دعم كامل لملفات PSD** – إنشاء أو تعديل ملفات Photoshop دون الحاجة إلى تثبيت Photoshop.  
- **API غني للرسم** – طرق مثل `drawArc` تتيح لك تحديد الحجم، الزوايا، والتنسيق في استدعاء واحد.  
- **تصدير متعدد الصيغ** – احفظ القوس إلى BMP، PNG، JPEG، إلخ، ببضع أسطر من الكود فقط.  
- **موجه للأداء** – مُحسّن للصور الكبيرة ومعالجة الدُفعات.

## Prerequisites
1. **بيئة تطوير Java** – ثبّت Java (JDK 8 أو أحدث). حمّلها من [موقع Oracle](https://www.oracle.com/java/).  
2. **Aspose.PSD للغة Java** – احصل على المكتبة من [صفحة التحميل](https://releases.aspose.com/psd/java/) وأضف ملف الـ JAR إلى مسار الـ classpath في مشروعك.

## Import Packages
أولاً، استورد الفئات المطلوبة من Aspose.PSD:

```java
import com.aspose.psd.Color;
import static com.aspose.psd.ColorAdjustType.Pen;
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;
import com.aspose.psd.Pen;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.BmpOptions;
```

تمنحك هذه الاستيرادات إمكانية الوصول إلى تعريفات الألوان، أدوات الرسم، حاويات الصور، وخيارات حفظ الملفات.

## Step‑by‑Step Guide

### Step 1: Set Up Your Java Project
أنشئ مشروع Maven أو Gradle جديد، أضف ملف Aspose.PSD JAR، وتأكد من أن بيئة التطوير تتعرف على الاستيرادات دون أخطاء.

### Step 2: Initialize Image and Graphics Objects
أنشئ لوحة `PsdImage` فارغة وكائن `Graphics` للرسم عليها:

```java
String dataDir = "Your Document Directory";
// Initialize PsdImage object
PsdImage image = new PsdImage(100, 100);
// Initialize Graphics object and clear surface
Graphics graphics = new Graphics(image);
graphics.clear(Color.getYellow());
```

استبدل `"Your Document Directory"` بالمجلد الذي تريد حفظ ملف الإخراج فيه.

### Step 3: Define Arc Parameters
حدد الأبعاد والزوايا التي تشكّل القوس:

```java
int width = 100;
int height = 200;
int startAngle = 45;
int sweepAngle = 270;
```

لا تتردد في تعديل هذه القيم لتتناسب مع النمط البصري الذي تحتاجه.

### Step 4: Draw and Save the Arc
استخدم طريقة `drawArc`، ثم صدّر الصورة:

```java
// Draw arc with specified Pen object (black color) and parameters
graphics.drawArc(new Pen(Color.getBlack()), 0, 0, width, height, startAngle, sweepAngle);
// Save the image in BMP format
String outputPath = dataDir + "Arc.bmp";
BmpOptions saveOptions = new BmpOptions();
saveOptions.setBitsPerPixel(32);
image.save(outputPath, saveOptions);
```

يقوم الكود برسم قوس أسود على خلفية صفراء ويكتب النتيجة إلى `Arc.bmp`. غيّر `outputPath` و`BmpOptions` إذا رغبت بصيغة أو جودة مختلفة.

## Common Issues & Solutions
- **خطأ الملف غير موجود** – تأكد من أن `dataDir` ينتهي بفاصل مسار (`/` أو `\\`) وأن الدليل موجود.  
- **القوس يظهر كخط** – تحقق من أن `width` و`height` أكبر من الصفر وأن `sweepAngle` ليس مضاعفًا للـ 360° (ما سيؤدي إلى رسم إهليلج كامل).  
- **اللون غير مطبق** – استخدم `new Pen(Color.getRed())` أو عيّن `pen.setWidth(2)` لتظهر التأثير بوضوح أكبر.

## Frequently Asked Questions

**س: هل يمكن لـ Aspose.PSD للغة Java التعامل مع أشكال أخرى غير الأقواس؟**  
ج: نعم، يدعم المستطيلات، الإهليلجات، الخطوط، والمسارات المخصصة عبر نفس API الـ `Graphics`.

**س: كيف أغيّر سمك القوس أو لونه؟**  
ج: أنشئ `Pen` بالـ `Color` و`Width` المطلوبين (مثال: `new Pen(Color.getBlue(), 3)`) ومرره إلى `drawArc`.

**س: هل يمكن تصدير القوس إلى صيغ غير BMP؟**  
ج: بالتأكيد. استخدم `PngOptions` أو `JpegOptions` أو `TiffOptions` بدلاً من `BmpOptions`.

**س: أين يمكنني العثور على مزيد من الأمثلة والدعم؟**  
ج: زر [منتدى Aspose.PSD](https://forum.aspose.com/c/psd/34) للحصول على مساعدة المجتمع، الوثائق الرسمية، وعينات الكود.

## Conclusion
أصبحت الآن تمتلك مثالًا كاملاً وجاهزًا للإنتاج حول كيفية **java graphics draw arc** باستخدام Aspose.PSD للغة Java. من خلال تعديل المعلمات، إعدادات القلم، وخيارات الإخراج، يمكنك دمج أقواس مخصصة في أي سير عمل رسومي يعتمد على Java.

---

**آخر تحديث:** 2026-01-17  
**تم الاختبار مع:** Aspose.PSD للغة Java 24.12  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}