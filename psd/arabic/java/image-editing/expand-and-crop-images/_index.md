---
date: 2026-07-08
description: 'دروس مكتبة تحرير الصور لجافا: تعلم كيفية Crop Image باستخدام Aspose.PSD
  for Java، resize، expand canvas، وتحويل PSD إلى JPEG.'
keywords:
- java image editing library
- java image processing tutorial
- how to crop image java
lastmod: 2026-07-08
linktitle: Expand و Crop Images
og_description: دروس مكتبة تحرير الصور لجافا توضح كيفية Crop، expand canvas، وتحويل
  PSD إلى JPEG باستخدام Aspose.PSD for Java في دقائق.
og_image_alt: 'Guide: Crop and expand images in Java with Aspose.PSD'
og_title: مكتبة تحرير الصور لجافا – Crop Image مع Aspose.PSD
schemas:
- author: Aspose
  dateModified: '2026-07-08'
  description: 'Java image editing library tutorial: learn how to crop image java
    using Aspose.PSD for Java, resize, expand canvas, and convert PSD to JPEG.'
  headline: Java Image Editing Library – Crop Image with Aspose.PSD
  type: TechArticle
- questions:
  - answer: Aspose.PSD for Java.
    question: What library handles crop image java?
  - answer: A free trial works for testing; a commercial license is required for production.
    question: Do I need a license for development?
  - answer: Yes, using `JpegOptions` together with a cropping rectangle.
    question: Can I convert PSD to JPEG while cropping?
  - answer: Aspose.PSD supports Java 8 and newer versions.
    question: Is Java 8 supported?
  - answer: Typically under 10 minutes for a basic crop operation.
    question: How long does the implementation take?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- java image editing
- Aspose.PSD
- image cropping
- PSD to JPEG
title: مكتبة تحرير الصور لجافا – Crop Image مع Aspose.PSD
url: /ar/java/image-editing/expand-and-crop-images/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# مكتبة تحرير الصور لجافا: قص الصورة بجافا باستخدام Aspose.PSD

## مقدمة

في هذا الدرس ستتعلم كيفية استخدام **java image editing library**—وتحديدًا Aspose.PSD for Java—لقص وتوسيع وتحويل ملفات PSD إلى JPEG. سواءً كنت تُعد الأصول لبوابة ويب أو تُ automatisation توليد الصور المصغرة، فإن الخطوات أدناه توفر لك سير عمل قابل للتكرار وجاهز للإنتاج يمكنك دمجه في أي مشروع Java 8+.

## إجابات سريعة
- **ما المكتبة التي تتعامل مع قص الصورة بجافا؟** Aspose.PSD for Java.  
- **هل أحتاج إلى ترخيص للتطوير؟** نسخة تجريبية مجانية تعمل للاختبار؛ يلزم ترخيص تجاري للإنتاج.  
- **هل يمكنني تحويل PSD إلى JPEG أثناء القص؟** نعم، باستخدام `JpegOptions` مع مستطيل القص.  
- **هل Java 8 مدعومة؟** Aspose.PSD تدعم Java 8 والإصدارات الأحدث.  
- **كم يستغرق تنفيذ العملية؟** عادةً أقل من 10 دقائق لعملية قص أساسية.

## ما هو “crop image java”؟

قص الصورة بجافا يعني اختيار منطقة مستطيلة من الصورة الأصلية وحذف كل ما يقع خارج تلك المنطقة. باستخدام Aspose.PSD، تقوم بإنشاء `Rectangle` يحدد المنطقة، وتطبيقه على `RasterImage`، ثم حفظ النتيجة بأي تنسيق مدعوم مثل JPEG.

## لماذا تستخدم Aspose.PSD لقص الصور في Java؟

توفر Aspose.PSD **java image editing library** التي تتعامل مع ملفات PSD أصلاً، وتدعم أكثر من 100 ميزة طبقة، ويمكنها معالجة الصور حتى 10 000 × 10 000 بيكسل مع الحفاظ على استهلاك الذاكرة أقل من 500 ميغابايت. كما أنها تقدم تحويلًا مدمجًا إلى JPEG و PNG و BMP وغيرها، دون الحاجة إلى أدوات خارجية. هذا يجعل خطوط معالجة الدفعات سريعة، موثوقة، وسهلة الصيانة.

## المتطلبات المسبقة

1. **Java Development Kit (JDK)** – تم تثبيت Java 8 أو أحدث.  
2. **Aspose.PSD for Java** – قم بتنزيل المكتبة من الموقع الرسمي **[here](https://releases.aspose.com/psd/java/)**.  

> **نصيحة احترافية:** أضف ملف Aspose.PSD JAR إلى مسار الفئة (classpath) في مشروعك أو إلى تبعيات Maven/Gradle لتجنب `ClassNotFoundException`.

## استيراد الحزم

أضف الاستيرادات المطلوبة إلى ملف Java المصدر الخاص بك. هذه الفئات تمنحك الوصول إلى تحميل الصور، ومعالجة الراستر، وتعريف المستطيل، وخيارات تصدير JPEG.

## كيفية قص الصورة بجافا باستخدام Aspose.PSD؟

حمّل ملف PSD المصدر باستخدام `RasterImage`، عرّف `Rectangle` الذي يصف منطقة القص (يمكن للإحداثيات السالبة توسيع القماش)، وأخيرًا احفظ النتيجة باستخدام `JpegOptions`. هذا التدفق المكوّن من ثلاث خطوات يتعامل مع القص وتحويل الصيغة في خطوة واحدة، مما يلغي الحاجة إلى ملفات وسيطة.

## الخطوة 1: تحديد دليل المستند الخاص بك

حدد المجلد الذي يحتوي على ملف PSD المصدر. استبدل العنصر النائب بالمسار الفعلي على جهازك.

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;
import com.aspose.psd.Rectangle;

import com.aspose.psd.imageoptions.JpegOptions;
```

## الخطوة 2: تحديد مسارات المصدر والوجهة

حدد مكان قراءة ملف PSD ومن أين سيتم كتابة ملف JPEG المقصوص.

```java
String dataDir = "Your Document Directory";
```

## الخطوة 3: تحميل الصورة وتخزينها مؤقتًا

`RasterImage` تمثل نسخة راستر من ملف PSD في الذاكرة.  
حمّل ملف PSD إلى كائن `RasterImage`. التخزين المؤقت يحسن الأداء للعمليات اللاحقة مثل القص.

```java
String sourceFile = dataDir + "example1.psd";
String destName = dataDir + "jpeg_out.jpg";
```

## الخطوة 4: إنشاء مستطيل للقص

`Rectangle` يحدد إحداثيات X, Y وعرض/ارتفاع منطقة القص.  
أنشئ `Rectangle` يصف المنطقة التي تريد الاحتفاظ بها. يمكن أن تكون الإحداثيات سالبة **لتوسيع** القماش قبل القص، وهو مفيد لإضافة حد حول الصورة الأصلية.

```java
RasterImage rasterImage = (RasterImage)Image.load(sourceFile);
rasterImage.cacheData();
```

> **لماذا تستخدم إحداثيات سالبة؟**  
> قيم X/Y السالبة تحرك منطقة القص إلى اليسار/الأعلى، مما يضيف مساحة فارغة (توسيع) حول المحتوى الأصلي قبل القص النهائي.

## الخطوة 5: حفظ الصورة المقصوصة

`JpegOptions` يحدد إعدادات إخراج JPEG، مثل الجودة والضغط.  
أخيرًا، احفظ الصورة الناتجة باستخدام `JpegOptions`. تُظهر هذه الخطوة أيضًا **convert psd jpeg** أثناء تطبيق مستطيل القص.

```java
Rectangle destRect = new Rectangle(-200, -200, 300, 300);
```

> **النتيجة:** `jpeg_out.jpg` الآن يحتوي على صورة بحجم 300 × 300 بكسل تم توسيعها بمقدار 200 بكسل على كل جانب ثم قصها إلى المستطيل المحدد.

تهانينا! لقد نجحت في تنفيذ **java image cropping**، وتوسيع القماش، وتحويل ملف PSD إلى JPEG—كل ذلك في بضع أسطر مختصرة من الشيفرة.

## حالات الاستخدام الشائعة

- **تحضير الأصول للويب** – قص وإعادة تحجيم لقطات الشاشة أو التصاميم قبل الرفع.  
- **إنشاء صور مصغرة** – استخراج منطقة محددة من PSD كبير لأغراض المعاينة.  
- **معالجة دفعات تلقائية** – التكرار عبر مجلد من ملفات PSD، وتطبيق نفس مستطيل القص على كل منها.

## استكشاف الأخطاء وإصلاحها & نصائح

| المشكلة | الإصلاح المقترح |
|-------|----------------|
| `OutOfMemoryError` عند تحميل ملفات PSD الكبيرة | استدعِ `rasterImage.cacheData()` مبكرًا وفكّر في زيادة حجم الذاكرة المخصصة للـ JVM (`-Xmx`). |
| منطقة القص غير مركزة | تحقق من إزاحات X/Y للمستطيل؛ تذكّر أن القيم السالبة توسع القماش. |
| ملف JPEG الناتج يبدو غير واضح | قم بضبط إعداد جودة `JpegOptions` (مثال: `new JpegOptions { Quality = 90 }`). |

## الأسئلة المتكررة

### س1: هل Aspose.PSD متوافق مع إصدارات Java المختلفة؟

A1: نعم، Aspose.PSD يدعم Java 8 و 11 و 17 والإصدارات الأحدث، مما يضمن توافقًا واسعًا عبر بيئات التطوير.

### س2: هل يمكنني استخدام Aspose.PSD للمشاريع التجارية؟

A2: بالتأكيد، توفر Aspose.PSD تراخيص تجارية للمطورين، مما يسمح باستخدامها في التطبيقات الشخصية والتجارية على حد سواء.

### س3: هل هناك أي قيود على صيغ ملفات الصور المدعومة؟

A3: تدعم Aspose.PSD أكثر من 30 صيغة صورة، بما في ذلك PSD و JPEG و PNG و BMP و TIFF وغيرها. راجع [documentation](https://reference.aspose.com/psd/java/) للحصول على القائمة الكاملة.

### س4: كيف يمكنني الحصول على دعم لاستفسارات متعلقة بـ Aspose.PSD؟

A4: زر [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) للحصول على مساعدة من المجتمع أو فريق دعم Aspose.

### س5: هل تتوفر نسخة تجريبية مجانية؟

A5: نعم، يمكنك استكشاف Aspose.PSD عبر نسخة تجريبية مجانية. قم بتنزيلها [here](https://releases.aspose.com/).

**آخر تحديث:** 2026-07-08  
**تم الاختبار مع:** Aspose.PSD for Java 24.12  
**المؤلف:** Aspose  

{{< blocks/products/products-backtop-button >}}

```java
rasterImage.save(destName, new JpegOptions(), destRect);
```

## دروس ذات صلة

- [تغيير الحجم البسيط باستخدام Aspose.PSD – مكتبة معالجة الصور لجافا](/psd/java/basic-image-operations/simple-resizing/)
- [كيفية تدوير الصورة 270 درجة باستخدام Aspose.PSD لجافا](/psd/java/advanced-image-manipulation/rotate-image/)
- [كيفية تعديل جاما في معالجة الصور بجافا باستخدام Aspose.PSD](/psd/java/advanced-techniques/adjust-gamma/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}