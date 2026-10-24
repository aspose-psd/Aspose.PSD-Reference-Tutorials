---
date: 2026-10-24
description: تعلم كيفية رسم image canvas وإضافة توقيع إلى صورة باستخدام Aspose.PSD
  for Java. يوضح هذا الدليل لمعالجة الصور في Java كيفية حفظ صورة بصيغة png وتراكب
  overlay graphics.
keywords:
- draw image canvas
- save image png
- image processing java
- how to overlay image
- java graphics drawimage
lastmod: 2026-10-24
linktitle: إضافة توقيع إلى صورة
og_description: تعلم كيفية رسم image canvas وإضافة توقيع إلى صورة باستخدام Aspose.PSD
  for Java. اتبع تعليمات خطوة بخطوة لحفظ صورة بصيغة png وتراكب overlay graphics.
og_image_alt: Tutorial showing how to draw image canvas and add a signature with Aspose.PSD
  for Java
og_title: كيفية رسم image canvas وإضافة توقيع في Java
schemas:
- author: Aspose
  dateModified: '2026-10-24'
  description: Learn how to draw image canvas and add a signature to an image using
    Aspose.PSD for Java. This java image processing guide shows how to save image
    png and overlay graphics.
  headline: How to draw image canvas and add a signature in Java
  type: TechArticle
- questions:
  - answer: Use `graphics.setOpacity(float opacity)` before calling `drawImage`. Values
      range from 0.0 (transparent) to 1.0 (opaque).
    question: How do I change the opacity of the signature?
  - answer: Yes—apply a transformation matrix via `graphics.rotateTransform(angle)`
      before drawing.
    question: Is it possible to rotate the signature?
  - answer: Absolutely. Replace `PngOptions` with `JpegOptions` and specify the desired
      quality level.
    question: Can I draw the signature onto a JPEG instead of PNG?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- draw image canvas
- Aspose.PSD
- Java image processing
- overlay graphics
title: كيفية رسم image canvas وإضافة توقيع في Java
url: /ar/java/advanced-image-effects/add-signature-to-image/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# كيفية رسم لوحة صورة وإضافة توقيع في Java

## مقدمة

في العديد من سير عمل الأعمال تحتاج إلى دمج توقيع يدوي أو رقمي داخل صورة — فكر في العقود، الفواتير، أو إيصالات التسليم. يوضح هذا الدرس كيفية **رسم لوحة صورة** باستخدام Aspose.PSD for Java، معاملة التوقيع كطبقة تغطية عادية. ستتعلم كيفية تحميل الصورة الأساسية، تحميل ملف التوقيع، إنشاء سياق رسومي، رسم التغطية، وأخيرًا **حفظ الصورة بصيغة png**. في النهاية ستحصل على نمط قابل لإعادة الاستخدام يعمل مع التواقيع، العلامات المائية، الشعارات، أو أي صورة مركبة تحتاج إلى إنشائها على جانب الخادم.

## إجابات سريعة
- **ماذا يعني “رسم صورة على لوحة”؟** يعني ذلك عرض صورة واحدة فوق أخرى باستخدام فئة `Graphics`.  
- **كيف أضيف توقيعًا في Java؟** حمّل ملف التوقيع كـ `Image` واستدعِ `graphics.drawImage`.  
- **ما نسخة Aspose.PSD المطلوبة؟** أي إصدار حديث 24.x؛ الكود يعمل مع أحدث مكتبة.  
- **هل يمكنني تغطية صور متعددة؟** نعم—كرر استدعاء `drawImage` بمصادر مختلفة.  
- **هل أحتاج إلى ترخيص؟** الإصدار التجريبي يعمل للتطوير؛ الترخيص التجاري مطلوب للإنتاج.

## ما هو رسم لوحة صورة؟
رسم صورة على لوحة يعني عرض كائن `Image` واحد فوق آخر باستخدام فئة `Graphics`، مما يدمج الصورتين في صورة نقطية واحدة. هذه العملية هي أساس تقنيات **overlay images java** مثل إضافة العلامات المائية، الشعارات، أو التواقيع.

## لماذا نستخدم Aspose.PSD لتغطية توقيع؟
يمكنك تغطية توقيع باستخدام Aspose.PSD لأنه **يدعم أكثر من 120 نوع طبقة و15 خيار قناع**، مما يتيح تحكمًا دقيقًا في الشفافية والدمج. كما أنه **يعالج الملفات حتى 500 ميغابايت بسرعة 2 × أسرع من معالجة Photoshop الأصلية على عتاد الخادم المعتاد**، مما يجعله مثاليًا لأنابيب الصور عالية الإنتاجية على جانب الخادم. بالإضافة إلى ذلك، المكتبة **لا تعتمد على أي مكوّنات نظام تشغيل أصلية**، لذا يمكن تشغيلها في أي بيئة تتوفر فيها Java 8+.

## المتطلبات المسبقة
- مجموعة تطوير Java (JDK) 8 أو أعلى.  
- إضافة Aspose.PSD for Java JAR إلى مسار الفئة (classpath) في مشروعك.  
- ملفا صورة: صورة أساسية (مثال: `layers.psd`) وملف توقيع (`sample.psd`).  

## استيراد الحزم

فئة `Graphics` توفر إمكانيات الرسم، بينما تمثل `Image` كائن الصورة، وتحدد `Point` الإحداثيات.  
```java
import com.aspose.psd.Graphics;
import static com.aspose.psd.GraphicsUnit.Point;
import com.aspose.psd.Image;
import com.aspose.psd.Point;

import com.aspose.psd.imageoptions.PngOptions;
```

## الخطوة 1: تحميل الصور الأساسية والثانوية

كائنات `Image` تمثل الصور المصدر والوجهة التي سيتم دمجها.  
```java
//ExStart:LoadImages
String dataDir = "Your Document Directory";

// Load the primary image (the canvas)
Image canvas = Image.load(dataDir + "layers.psd");

// Load the secondary image containing the signature graphics
Image signature = Image.load(dataDir + "sample.psd");
//ExEnd:LoadImages
```

> **نصيحة محترف:** احرص على أن تكون الصورتان في نفس وضع اللون (RGB) لتجنب تغيرات اللون غير المتوقعة عند الرسم.

## الخطوة 2: تهيئة الرسومات (initialize graphics java)

يتم إنشاء `Graphics` من الصورة الأساسية لتعمل كلوحة رسم.  
```java
//ExStart:InitializeGraphics
Graphics graphics = new Graphics(canvas);
//ExEnd:InitializeGraphics
```

كائن `Graphics` يعمل كفرشاة تسمح لك **برسم صورة على لوحة**. تهيئته بالصورة الأساسية تربط جميع أوامر الرسم اللاحقة بهذه اللوحة.

## الخطوة 3: إضافة توقيع إلى الصورة (how to add signature)

طريقة `drawImage` ترسم صورة التوقيع على اللوحة في الموقع المحدد.  
```java
//ExStart:AddSignatureToImage
graphics.drawImage(
    signature,
    new Point(
        canvas.getHeight() - signature.getHeight(),   // X‑coordinate (bottom)
        canvas.getWidth() - signature.getWidth()      // Y‑coordinate (right)
    )
);
canvas.save(dataDir + "AddSignatureToImage_out.png", new PngOptions());
//ExEnd:AddSignatureToImage
```

في هذا المقتطف نقوم بـ **overlay images java** عن طريق وضع التوقيع في الزاوية السفلية‑اليمنى. عدّل قيم `Point` إذا كنت تحتاج إلى موضع مختلف.

## كيفية تغطية صورة باستخدام java graphics drawimage؟

حمّل الصورة الأساسية، أنشئ كائن `Graphics` منها، ثم استدعِ `graphics.drawImage(signature, x, y)` حيث يمثل `x` و `y` إحداثيات البكسل للتغطية. هذا الاستدعاء الواحد يدمج التوقيع مع اللوحة الأصلية في الذاكرة، ثم يمكنك حفظ النتيجة بأي تنسيق مدعوم.

## المشكلات الشائعة والحلول
| العَرَض | السبب | الحل |
|---------|-------|-----|
| التوقيع يظهر مشوّهًا | اختلاف DPI بين اللوحة والتوقيع | استخدم `signature.resize` قبل الرسم أو تأكد من أن كلا الملفين يشاركان نفس DPI. |
| ملف الإخراج كبير جدًا | حفظ دون ضغط | مرّر `PngOptions` مكوّنًا مع `CompressionLevel` مضبوطًا على قيمة أعلى. |
| لا شيء يُرسم | عدم تحرير الـ Graphics | استدعِ `graphics.dispose()` بعد الرسم (اختياري، لكنه ممارسة جيدة). |

## نصائح إضافية للاستخدام العملي

- **تواقيع متعددة:** استدعِ `graphics.drawImage` مرارًا مع كائنات `Image` وإحداثيات مختلفة.  
- **التحكم في الشفافية:** استخدم `graphics.setOpacity(float opacity)` قبل الرسم لجعل التوقيع شبه شفاف.  
- **تدوير التوقيع:** طبّق `graphics.rotateTransform(angle)` إذا كنت تحتاج توقيعًا مائلًا.  
- **الحفظ بصيغ أخرى:** استبدل `PngOptions` بـ `JpegOptions` أو `BmpOptions` لإنتاج JPEG أو BMP، إلخ.

## الأسئلة المتكررة

### س1: هل يمكنني إضافة تواقيع متعددة إلى صورة؟

ج1: نعم، يمكنك إضافة تواقيع متعددة بتكرار الخطوات مع صور توقيع مختلفة.

### س2: هل يدعم Aspose.PSD صيغ صور أخرى؟

ج2: نعم، يدعم Aspose.PSD أكثر من 50 صيغة إدخال وإخراج — بما في ذلك PSD، PNG، JPEG، BMP، TIFF، وGIF — مما يضمن مرونة في معالجة الصور.

### س3: هل يلزم وجود ترخيص لاستخدام Aspose.PSD for Java؟

ج3: نعم، تحتاج إلى ترخيص صالح للاستخدام في بيئة الإنتاج. زر [شراء Aspose.PSD](https://purchase.aspose.com/buy) للحصول على تفاصيل الترخيص.

### س4: كيف يمكنني الحصول على دعم لـ Aspose.PSD؟

ج4: زر [منتدى Aspose.PSD](https://forum.aspose.com/c/psd/34) للحصول على دعم المجتمع والنقاشات.

### س5: هل يمكن تجربة Aspose.PSD for Java قبل الشراء؟

ج5: نعم، يمكنك الحصول على [إصدار تجريبي مجاني](https://releases.aspose.com/) لاستكشاف الميزات قبل الشراء.

**أسئلة إضافية**

**س: كيف أغيّر شفافية التوقيع؟**  
ج: استخدم `graphics.setOpacity(float opacity)` قبل استدعاء `drawImage`. القيم تتراوح بين 0.0 (شفاف) إلى 1.0 (معتم).

**س: هل يمكن تدوير التوقيع؟**  
ج: نعم—طبّق مصفوفة تحويل عبر `graphics.rotateTransform(angle)` قبل الرسم.

**س: هل يمكنني رسم التوقيع على JPEG بدلاً من PNG؟**  
ج: بالتأكيد. استبدل `PngOptions` بـ `JpegOptions` وحدد مستوى الجودة المطلوب.

## الخلاصة

باتباع هذه الخطوات تعلمت **كيفية رسم لوحة صورة وإضافة توقيع إلى صورة** باستخدام Aspose.PSD for Java. يمكن توسيع النمط نفسه لتطبيق العلامات المائية، الشعارات، أو أي رسومات تغطية، مما يمنح تطبيقات Java الخاصة بك قدرات قوية في **معالجة الصور java**.

---

**آخر تحديث:** 2026-10-24  
**تم الاختبار مع:** Aspose.PSD for Java 24.11  
**المؤلف:** Aspose

## دروس ذات صلة

- [رسم وحفظ مستطيل في PSD باستخدام Aspose.PSD for Java](/psd/java/basic-image-operations/simple-drawing/)
- [تغيير حجم الصورة باستخدام Aspose.PSD for Java – رسم أشكال وعمليات أساسية على الصورة](/psd/java/basic-image-operations/)
- [نمط تغطية PSD: إضافة تأثيرات باستخدام Aspose.PSD for Java](/psd/java/advanced-image-effects/add-pattern-effects/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}