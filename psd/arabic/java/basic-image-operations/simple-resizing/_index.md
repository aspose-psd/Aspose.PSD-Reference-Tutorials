---
date: 2026-06-13
description: تعلم كيفية تغيير حجم الصورة في جافا باستخدام مكتبة معالجة الصور لجافا.
  اتبع دليلنا خطوة بخطوة مع Aspose.PSD for Java لتحقيق معالجة صور فعّالة.
keywords:
- java image manipulation library
- how to resize image java
- change image dimensions java
linktitle: تنفيذ تغيير حجم بسيط
schemas:
- author: Aspose
  dateModified: '2026-06-13'
  description: Learn how to resize image Java using a java image manipulation library.
    Follow our step‑by‑step guide with Aspose.PSD for Java for efficient image manipulation.
  headline: Simple Resizing with Aspose.PSD – Java Image Manipulation Library
  type: TechArticle
- description: Learn how to resize image Java using a java image manipulation library.
    Follow our step‑by‑step guide with Aspose.PSD for Java for efficient image manipulation.
  name: Simple Resizing with Aspose.PSD – Java Image Manipulation Library
  steps:
  - name: Set Your Document Directory
    text: Define the folder that contains the source PSD file. Replace the placeholder
      with your actual path.
  - name: Specify Source and Destination Paths
    text: Create full file names for the input PSD and the output JPEG.
  - name: Load the Image
    text: '`Image.load(path)` reads an image file from the given path and returns
      an `Image` instance. Load the PSD into an `Image` object.'
  - name: Resize the Image
    text: '`image.resize(width, height)` changes the image dimensions to the specified
      pixel size. Resize to the desired dimensions (e.g., 300 × 300 pixels).'
  - name: Save the Resized Image
    text: '`image.save(path, options)` writes the image to the specified file using
      the given format options. Export the resized bitmap as a JPEG file. > **Pro
      tip:** Experiment with different width/height values or maintain the aspect
      ratio by calculating one dimension from the other.'
  type: HowTo
- questions:
  - answer: Absolutely. The `resize(width, height)` method lets you define any pixel
      size you need.
    question: Can I resize images to specific dimensions using Aspose.PSD for Java?
  - answer: Yes. Besides PSD, the library supports JPEG, PNG, BMP, TIFF, and many
      more.
    question: Is Aspose.PSD for Java compatible with different image formats?
  - answer: Refer to the [Aspose.PSD for Java documentation](https://reference.aspose.com/psd/java/)
      for a full API reference.
    question: Where can I find additional documentation for Aspose.PSD for Java?
  - answer: Certainly! Download the [free trial version](https://releases.aspose.com/)
      to explore all features.
    question: Can I try Aspose.PSD for Java before purchasing?
  - answer: Visit the [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) to ask
      questions and share experiences with the community.
    question: How can I get support for Aspose.PSD for Java?
  type: FAQPage
second_title: Aspose.PSD Java API
title: تغيير الحجم البسيط باستخدام Aspose.PSD – مكتبة جافا لمعالجة الصور
url: /ar/java/basic-image-operations/simple-resizing/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# إعادة تحجيم بسيطة باستخدام Aspose.PSD – مكتبة معالجة الصور لجافا

## مقدمة

إذا كنت مطور Java تبحث عن **java image manipulation library** موثوقة، فقد وصلت إلى المكان الصحيح. في هذا الدرس سنستعرض **how to resize image java** باستخدام Aspose.PSD for Java – مكتبة قوية تجعل معالجة الصور سريعة ومباشرة. في نهاية هذا الدليل ستحصل على مثال واضح وجاهز للإنتاج يمكنك إدراجه في أي تطبيق Java.

## إجابات سريعة
- **ما المكتبة المستخدمة؟** Aspose.PSD for Java، مكتبة java image manipulation library رائدة.  
- **هل يمكنني إعادة تحجيم أي PSD؟** نعم – المكتبة تدعم PSD، JPEG، PNG، وأكثر.  
- **كيف يتم تحديد الحجم؟** استدعِ `image.resize(width, height)` بالأبعاد البكسلية المطلوبة.  
- **هل أحتاج إلى ترخيص؟** النسخة التجريبية المجانية تعمل للتطوير؛ الترخيص مطلوب للإنتاج.  
- **ما نسخة Java المطلوبة؟** Java 8 أو أعلى.

## ما هي مكتبة معالجة الصور لجافا؟

إن **java image manipulation library** هي مجموعة من واجهات برمجة تطبيقات Java التي تتيح لك تعديل الرسومات النقطية برمجيًا — إعادة التحجيم، القص، تحويل الصيغ، وإدارة الطبقات — دون أدوات خارجية. توفر Aspose.PSD هذه الإمكانيات لملفات PSD والعديد من الصيغ الأخرى، وتعرض واجهة برمجة تطبيقات كائنية نظيفة للمطورين.

## لماذا نستخدم Aspose.PSD لإعادة التحجيم البسيطة؟

توفر Aspose.PSD خوارزميات **performance‑optimized** يمكنها معالجة ملفات تحتوي على أكثر من 500 طبقة في أقل من ثانية على خادم عادي، وتعمل بالكامل في Java — دون الحاجة إلى DLLs أصلية أو ملفات تنفيذية خارجية. تدعم المكتبة **30+ image formats** (بما في ذلك PSD، JPEG، PNG، TIFF، BMP، GIF) ويمكنها التعامل مع ملفات أكبر من 200 MB دون تحميل المستند بالكامل إلى الذاكرة، مما يجعلها مثالية للخطوط الأنابيب عالية الإنتاجية على الخادم.

## المتطلبات المسبقة

قبل أن نبدأ، تأكد من وجود ما يلي:

1. **Java Development Kit (JDK)** – حمّل أحدث نسخة من [Java website](https://www.oracle.com/java/).  
2. **Aspose.PSD for Java** – احصل على المكتبة من [Aspose.PSD for Java download page](https://releases.aspose.com/psd/java/).  

وجود هذه العناصر يضمن إعدادًا سلسًا لمثال إعادة التحجيم.

## استيراد الحزم

الفئة `Image` وخيارات التصدير المرتبطة مطلوبة لتحميل وحفظ الملفات.

`Image` هي الفئة الأساسية التي تمثل صورة يمكن تحميلها، تعديلها، وحفظها.

`JpegOptions` تحدد الإعدادات لحفظ صورة بصيغة JPEG.

هذه الاستيرادات تمنحك الوصول إلى الفئة الأساسية `Image` وخيارات تصدير JPEG.

```java
import com.aspose.psd.Image;
import com.aspose.psd.imageoptions.JpegOptions;
```

## دليل خطوة بخطوة

### الخطوة 1: تحديد دليل المستند الخاص بك

حدد المجلد الذي يحتوي على ملف PSD المصدر. استبدل العنصر النائب بالمسار الفعلي الخاص بك.

```java
String dataDir = "Your Document Directory";
```

### الخطوة 2: تحديد مسارات المصدر والوجهة

أنشئ أسماء ملفات كاملة لملف PSD الإدخال وملف JPEG الناتج.

```java
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "SimpleResizing_out.jpg";
```

### الخطوة 3: تحميل الصورة

`Image.load(path)` يقرأ ملف صورة من المسار المحدد ويعيد كائن `Image`.

حمّل ملف PSD إلى كائن `Image`.

```java
Image image = Image.load(sourceFile);
```

### الخطوة 4: إعادة تحجيم الصورة

`image.resize(width, height)` يغيّر أبعاد الصورة إلى الحجم البكسلي المحدد.

أعد التحجيم إلى الأبعاد المطلوبة (مثال: 300 × 300 بكسل).

```java
image.resize(300, 300);
```

### الخطوة 5: حفظ الصورة المعاد تحجيمها

`image.save(path, options)` يكتب الصورة إلى الملف المحدد باستخدام خيارات الصيغة المعطاة.

صدّر الصورة المعاد تحجيمها كملف JPEG.

```java
image.save(destName, new JpegOptions());
```

> **نصيحة احترافية:** جرّب قيم عرض/ارتفاع مختلفة أو حافظ على نسبة الأبعاد بحساب أحد الأبعاد من الآخر.

## كيف تغير أبعاد الصورة في Java؟

استخدم الطريقة `resize(width, height)` على كائن `Image`، مع تمرير القيم البكسلية الدقيقة التي تحتاجها. على سبيل المثال، `image.resize(800, 600)` سيولد مخرجات بحجم 800 × 600 بكسل مع الحفاظ على عمق اللون والبيانات الوصفية. إذا أردت الحفاظ على نسبة الأبعاد الأصلية، احسب البُعد الثاني بناءً على نسبة العرض إلى الارتفاع الأصلية قبل استدعاء `resize`.

## المشكلات الشائعة والحلول

| المشكلة | السبب | الحل |
|-------|--------|-----|
| **`OutOfMemoryError`** | ملفات PSD الكبيرة جدًا قد تتجاوز سعة ذاكرة JVM. | زيادة حجم ذاكرة JVM (`-Xmx2g`) أو معالجة الصور على أجزاء. |
| **Unsupported format** | محاولة تحميل ملف غير PSD دون الخيارات المناسبة. | استخدم النسخة المناسبة من `Image.load` أو حوّل الملف أولاً. |
| **Distorted output** | نسبة أبعاد غير صحيحة. | احسب الارتفاع بناءً على نسبة الأبعاد الأصلية أو استخدم `image.resizeProportionally`. |

## الأسئلة المتكررة

**س: هل يمكنني إعادة تحجيم الصور إلى أبعاد محددة باستخدام Aspose.PSD for Java؟**  
ج: بالتأكيد. تسمح لك الطريقة `resize(width, height)` بتحديد أي حجم بكسلي تحتاجه.

**س: هل Aspose.PSD for Java متوافق مع صيغ صور مختلفة؟**  
ج: نعم. بالإضافة إلى PSD، تدعم المكتبة JPEG، PNG، BMP، TIFF، والعديد غيرها.

**س: أين يمكنني العثور على وثائق إضافية لـ Aspose.PSD for Java؟**  
ج: ارجع إلى [Aspose.PSD for Java documentation](https://reference.aspose.com/psd/java/) للحصول على مرجع API كامل.

**س: هل يمكنني تجربة Aspose.PSD for Java قبل الشراء؟**  
ج: بالتأكيد! حمّل [free trial version](https://releases.aspose.com/) لاستكشاف جميع الميزات.

**س: كيف يمكنني الحصول على دعم لـ Aspose.PSD for Java؟**  
ج: زر [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) لطرح الأسئلة ومشاركة التجارب مع المجتمع.

## الخلاصة

في هذا الدرس أظهرنا كيف أن **java image manipulation library** مثل Aspose.PSD تجعل مهام **how to resize image java** سهلة. باتباع الخطوات المختصرة أعلاه يمكنك دمج إعادة تحجيم الصور في أي تطبيق Java، مما يضمن نتائج سريعة وموثوقة دون أدوات خارجية.

---

**آخر تحديث:** 2026-06-13  
**تم الاختبار مع:** Aspose.PSD for Java 24.12 (latest)  
**المؤلف:** Aspose

## دروس ذات صلة

- [إعادة تحجيم صورة Java - باستخدام تعداد نوع التحجيم في Aspose.PSD for Java](/psd/java/advanced-image-manipulation/resizing-with-resize-type-enumeration/)
- [تحجيم صورة عالي الجودة باستخدام Resampler بيكوبيك في Aspose.PSD for Java](/psd/java/advanced-image-manipulation/implement-bicubic-resampler/)
- [كيفية تحويل PSD إلى PNG وإعادة التحجيم بشكل متناسب مع Aspose.PSD for Java](/psd/java/advanced-image-manipulation/resize-image-proportionally/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< blocks/products/products-backtop-button >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}