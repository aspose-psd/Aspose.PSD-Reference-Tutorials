---
date: 2026-08-11
description: تعلم كيفية تطبيق otsu threshold Java باستخدام Aspose.PSD for Java – تقنية
  قوية لتقسيم الصور.
keywords:
- apply otsu threshold java
- image segmentation with otsu
- java image segmentation tutorial
lastmod: 2026-08-11
linktitle: تحويل إلى ثنائي باستخدام Otsu Threshold
og_description: تطبيق otsu threshold Java باستخدام Aspose.PSD for Java. يوضح هذا الدليل
  خطوة بخطوة كيفية تحويل الصور إلى ثنائية، ويشرح لماذا الطريقة سريعة، ويقدم نصائح
  لحل المشكلات الشائعة.
og_image_alt: Screenshot of Java code applying Otsu threshold using Aspose.PSD
og_title: تطبيق otsu threshold Java باستخدام Aspose.PSD – دليل سريع
schemas:
- author: Aspose
  dateModified: '2026-08-11'
  description: Learn how to apply otsu threshold java using Aspose.PSD for Java –
    a powerful image segmentation technique.
  headline: Apply otsu threshold java with Aspose.PSD
  type: TechArticle
- description: Learn how to apply otsu threshold java using Aspose.PSD for Java –
    a powerful image segmentation technique.
  name: Apply otsu threshold java with Aspose.PSD
  steps:
  - name: set up your document directory
    text: Define the folder that contains the source PSD file and the output location
      for the binarized image.
  - name: load the PSD file
    text: '`PsdImage` is the top‑level Aspose.PSD class that represents a PSD document
      and gives access to its layers, metadata, and pixel data.'
  - name: cache the image
    text: '`RasterImage` holds the raster representation of a layer; calling `cache()`
      loads the pixel data into memory so subsequent operations are fast.'
  - name: binarize image with Otsu threshold
    text: '`applyOtsuThreshold()` evaluates all possible gray levels and selects the
      optimal cutoff, producing a binary image that separates foreground objects from
      the background.'
  - name: save the resultant image
    text: '`JpegOptions` configures JPEG‑specific settings such as quality and compression
      when saving the processed image. You can also choose PNG or BMP by swapping
      the options class – the API supports over **30 image formats** for output. {{<
      blocks/products/products-backtop-button >}}'
  type: HowTo
- questions:
  - answer: It automatically finds the gray‑level that minimizes intra‑class variance,
      producing a binary image in one step.
    question: What does Otsu Threshold do?
  - answer: A free trial works for development; a commercial license is required for
      production.
    question: Do I need a license to run the sample?
  - answer: Aspose.PSD for Java supports Java 8 through Java 21.
    question: Which Java version is supported?
  - answer: Yes – you can iterate over each layer and apply the threshold individually.
    question: Can I process multi‑layer PSD files?
  - answer: For a 1920 × 1080 image the Otsu binarization finishes in under 30 ms
      on a typical laptop CPU.
    question: How fast is the operation?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- apply otsu threshold java
- image segmentation
- Aspose.PSD
- Java image processing
title: تطبيق otsu threshold Java باستخدام Aspose.PSD
url: /ar/java/image-processing/binarization-otsu-threshold/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# تطبيق عتبة أوتسو في جافا باستخدام Aspose.PSD

## مقدمة

في هذا البرنامج التعليمي ستتعلم كيفية **apply otsu threshold java** باستخدام مكتبة Aspose.PSD للغة Java. التحويل إلى ثنائي باستخدام عتبة أوتسو هو أحد أكثر تقنيات تقسيم الصورة موثوقية، حيث يختار تلقائيًا مستوى رمادي أمثل للفصل بين المقدمة والخلفية. بنهاية الدليل ستحصل على مقتطف Java يعمل يحول أي طبقة PSD إلى صورة سوداء‑بيضاء نظيفة.

## إجابات سريعة
- **What does Otsu Threshold do?** إنه يجد تلقائيًا مستوى الرمادي الذي يقلل من تباين داخل الفئة، منتجًا صورة ثنائية في خطوة واحدة.  
- **Do I need a license to run the sample?** النسخة التجريبية المجانية تعمل للتطوير؛ يلزم الحصول على ترخيص تجاري للإنتاج.  
- **Which Java version is supported?** يدعم Aspose.PSD للغة Java الإصدارات من Java 8 حتى Java 21.  
- **Can I process multi‑layer PSD files?** نعم – يمكنك التكرار على كل طبقة وتطبيق العتبة بشكل منفصل.  
- **How fast is the operation?** بالنسبة لصورة بحجم 1920 × 1080، يكتمل تحويل أوتسو إلى ثنائي في أقل من 30 مللي ثانية على معالج لابتوب عادي.

## ما هو apply otsu threshold java؟

Apply otsu threshold java هو العملية التي تستخدم فيها شفرة Java لاستدعاء خوارزمية أوتسو على صورة، مما ينتج نتيجة ثنائية (سوداء‑بيضاء). تقوم الخوارزمية بتقييم كل مستوى رمادي محتمل، وتختار المستوى الذي يعطي أقل تباين داخل الفئة المرجح، ثم تصنف كل بكسل كـ مقدمة أو خلفية. يزيل هذا النهج الآلي الحاجة إلى اختيار العتبة يدويًا ويعمل بشكل جيد على الصور ذات التوزيعات الثنائية، مما يجعله مثاليًا لمعالجة دفعات كبيرة من مجموعات الصور.

## لماذا تستخدم Aspose.PSD للغة Java؟

يدعم Aspose.PSD للغة Java **أكثر من 50 تنسيقًا للإدخال والإخراج** (بما في ذلك PSD و JPEG و PNG و BMP و TIFF) ويمكنه معالجة ملفات يصل حجمها إلى **2 GB** دون تحميل المستند بالكامل في الذاكرة. تنفيذ Otsu المدمج في المكتبة يعمل بزمن خطي، مما يتيح لك معالجة مئات الصور دفعةً واحدة في بضع ثوانٍ.

## المتطلبات المسبقة

- **Java development environment** – JDK 8 أو أحدث مثبت ومُكوَّن.  
- **Aspose.PSD for Java library** – قم بتنزيل وتثبيت المكتبة من صفحة التحميل الرسمية لـ Aspose.PSD للغة Java. يمكنك العثور على رابط التحميل [Aspose.PSD for Java download page](https://releases.aspose.com/psd/java/).  
- **Sample PSD file** – احصل على ملف PSD يحتوي على طبقة نقطية واحدة على الأقل لاختبار التحويل إلى ثنائي.  
- بالنسبة لمنتجات Aspose الأخرى يمكنك أيضًا تصفح صفحة الإصدارات العامة على [Aspose releases](https://releases.aspose.com/).

## استيراد الحزم

استورد الفئات `PsdImage` و `RasterImage` و `JpegOptions` من مكتبة Aspose.PSD، والتي توفر الوصول إلى ملفات PSD والبيانات النقطية وخيارات تصدير JPEG.  
```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterCachedImage;

import com.aspose.psd.imageoptions.JpegOptions;
```

## كيفية تطبيق apply otsu threshold java؟

حمّل ملف PSD الخاص بك، استخرج طبقة النقاط المطلوبة، واستدعِ طريقة التحويل إلى ثنائي باستخدام Otsu – يتناسب سير العمل بالكامل مع خمس جمل مختصرة. أولاً، تنشئ كائن `PsdImage` الذي يمثل ملف المصدر، ثم تحصل على `RasterImage` للطبقة المستهدفة، وتستدعي `applyOtsuThreshold()` عليها، وأخيرًا تحفظ النتيجة باستخدام `JpegOptions`. يضمن هذا النهج الحد الأدنى من استهلاك الذاكرة وأقصى أداء.

### الخطوة 1: إعداد دليل المستند الخاص بك

حدد المجلد الذي يحتوي على ملف PSD المصدر وموقع الإخراج للصورة المحوّلة إلى ثنائي.  
```java
String dataDir = "Your Document Directory";
```

### الخطوة 2: تحميل ملف PSD

`PsdImage` هي الفئة العليا في Aspose.PSD التي تمثل مستند PSD وتوفر الوصول إلى طبقاته والبيانات الوصفية وبيانات البكسل.  
```java
String sourceFile = dataDir + "sample.psd";
Image image = Image.load(sourceFile);
```

### الخطوة 3: تخزين الصورة مؤقتًا

`RasterImage` تحتفظ بالتمثيل النقطي لطبقة؛ استدعاء `cache()` يحمل بيانات البكسل في الذاكرة بحيث تكون العمليات اللاحقة سريعة.  
```java
RasterCachedImage rasterCachedImage = (RasterCachedImage)image;

if (!rasterCachedImage.isCached()) {
    rasterCachedImage.cacheData();
}
```

### الخطوة 4: تحويل الصورة إلى ثنائي باستخدام عتبة أوتسو

`applyOtsuThreshold()` تقيم جميع مستويات الرمادي الممكنة وتختار القطع الأمثل، مما ينتج صورة ثنائية تفصل بين كائنات المقدمة والخلفية.  
```java
rasterCachedImage.binarizeOtsu();
```

### الخطوة 5: حفظ الصورة الناتجة

`JpegOptions` يضبط إعدادات JPEG الخاصة مثل الجودة والضغط عند حفظ الصورة المعالجة. يمكنك أيضًا اختيار PNG أو BMP عن طريق استبدال فئة الخيارات – يدعم API أكثر من **30 تنسيق صورة** للإخراج.  
```java
String destName = dataDir + "BinarizationWithOtsuThreshold_out.jpg";
rasterCachedImage.save(destName, new JpegOptions());
```

{{< blocks/products/products-backtop-button >}}

## المشكلات الشائعة والحلول

- **Memory‑out‑of‑bounds errors** – تأكد من استدعاء `cache()` على الطبقات الكبيرة قبل المعالجة؛ هذا يجبر Aspose.PSD على استخدام نهج البث.  
- **Incorrect colors after binarization** – تحقق من أن طبقة المصدر هي صورة رمادية حقيقية؛ يجب تحويل طبقات اللون إلى رمادية أولاً باستخدام `convertToGrayscale()`.

## الأسئلة المتكررة

### س1: ما هو التحويل إلى ثنائي باستخدام عتبة أوتسو؟

التحويل إلى ثنائي باستخدام عتبة أوتسو هو طريقة تُستخدم لتقسيم الصورة، حيث يتم فصل الصورة إلى مقدمة وخلفية بناءً على عتبة مثالية.

### س2: هل يمكنني استخدام Aspose.PSD للغة Java مجانًا؟

Aspose.PSD للغة Java هي مكتبة تجارية، ولكن يمكنك استكشاف ميزاتها من خلال نسخة تجريبية مجانية. احصل عليها من [Aspose.PSD for Java download page](https://releases.aspose.com/psd/java/).

### س3: أين يمكنني العثور على وثائق Aspose.PSD للغة Java؟

الوثائق متاحة على موقع المرجع الرسمي لـ Aspose.PSD للغة Java: [Aspose.PSD Java API reference](https://reference.aspose.com/psd/java/).

### س4: كيف أحصل على الدعم لـ Aspose.PSD للغة Java؟

قم بزيارة منتدى مجتمع Aspose.PSD للحصول على المساعدة: [Aspose.PSD forum](https://forum.aspose.com/c/psd/34).

### س5: هل توجد رخصة مؤقتة متاحة لـ Aspose.PSD للغة Java؟

نعم، يمكنك الحصول على رخصة مؤقتة من صفحة الرخصة المؤقتة لـ Aspose: [Aspose temporary license](https://purchase.aspose.com/temporary-license/).

---

**آخر تحديث:** 2026-08-11  
**تم الاختبار باستخدام:** Aspose.PSD للغة Java 24.11  
**المؤلف:** Aspose

## دروس ذات صلة

- [تحويل صورة إلى تدرج رمادي باستخدام Aspose.PSD للغة Java](/psd/java/advanced-techniques/grayscale-image/)
- [دروس معالجة الصور في Java - تعديل سطوع الصورة باستخدام Aspose.PSD للغة Java](/psd/java/advanced-techniques/adjust-brightness/)
- [كيفية تعديل جاما في معالجة الصور بـ Java باستخدام Aspose.PSD](/psd/java/advanced-techniques/adjust-gamma/)

{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}