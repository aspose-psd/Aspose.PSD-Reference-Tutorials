---
date: 2026-07-27
description: تعرف على كيفية تحويل PSD إلى TIFF وإجراء ضبط تباين الصورة باستخدام Aspose.PSD
  للـ Java، وهي مكتبة رائدة لمعالجة الصور بلغة Java.
keywords:
- convert psd to tiff
- java image processing
- improve image contrast
lastmod: 2026-07-27
linktitle: تحويل PSD إلى TIFF وضبط التباين
og_description: تحويل PSD إلى TIFF مع ضبط التباين باستخدام Aspose.PSD للـ Java. يوضح
  هذا الدليل الشيفرة خطوة بخطوة، ونصائح الأداء، وخيارات التصدير لإنتاج ملفات TIFF
  عالية الجودة.
og_image_alt: 'Guide: Convert PSD to TIFF and adjust contrast using Aspose.PSD for
  Java'
og_title: تحويل PSD إلى TIFF & ضبط التباين – Aspose.PSD Java
schemas:
- author: Aspose
  dateModified: '2026-07-27'
  description: Learn how to convert PSD to TIFF and perform image contrast adjustment
    using Aspose.PSD for Java, a leading java image manipulation library.
  headline: Convert PSD to TIFF and Adjust Contrast with Aspose.PSD for Java
  type: TechArticle
- questions:
  - answer: It changes the difference between the darkest and brightest pixels, making
      details pop.
    question: What does “adjust contrast” mean?
  - answer: Aspose.PSD for Java – a full‑featured image processing toolkit.
    question: Which library handles this?
  - answer: A **temporary Aspose license** works for testing; a full license is required
      for production.
    question: Do I need a license?
  - answer: Absolutely – we’ll use `TiffOptions` to export the processed image.
    question: Can I convert PSD to TIFF?
  - answer: For a typical 30 MB PSD the whole pipeline runs under one second on a
      modern CPU.
    question: How fast is the conversion?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- convert psd
- Aspose.PSD
- Java image manipulation
- tiff export options
title: تحويل PSD إلى TIFF وضبط التباين باستخدام Aspose.PSD للـ Java
url: /ar/java/advanced-techniques/adjust-contrast/
weight: 22
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# كيفية تحويل PSD إلى TIFF وضبط التباين باستخدام Aspose.PSD للغة Java

## مقدمة

إذا كنت بحاجة إلى **تحويل PSD إلى TIFF** مع ضبط جودة الرسومات بصريًا، فأنت في المكان المناسب. في هذا البرنامج التعليمي سنستعرض سير العمل الكامل باستخدام Aspose.PSD للغة Java — مكتبة **java image manipulation** قوية. ستتعلم كيفية تحسين **ضبط تباين الصورة**، وتخزين بيانات الراستر الكبيرة مؤقتًا للأداء، وأخيرًا **حفظ الصورة كـ TIFF** للمعالجة اللاحقة. هيا نبدأ!

## إجابات سريعة
- **ماذا يعني “adjust contrast”؟** يغيّر الفرق بين أغمق وأفتح البكسلات، مما يجعل التفاصيل بارزة.  
- **أي مكتبة تتعامل مع ذلك؟** Aspose.PSD للغة Java – مجموعة أدوات معالجة الصور كاملة الميزات.  
- **هل أحتاج إلى ترخيص؟** **ترخيص Aspose مؤقت** يعمل للاختبار؛ الترخيص الكامل مطلوب للإنتاج.  
- **هل يمكنني تحويل PSD إلى TIFF؟** بالتأكيد – سنستخدم `TiffOptions` لتصدير الصورة المعالجة.  
- **ما مدى سرعة التحويل؟** بالنسبة لملف PSD بحجم 30 ميغابايت تقريبًا، يعمل سير العمل بالكامل خلال أقل من ثانية على معالج حديث.

## ما هو ضبط تباين الصورة؟
يقوم ضبط التباين بتعديل النطاق اللوني للصورة، مما يزيد من التمييز بين المناطق الفاتحة والغامقة. يكون ذلك مفيدًا بشكل خاص عندما تبدو الصور مسطحة بعد المسح أو عند إعداد الرسومات للطباعة. يعمل عن طريق تمديد أو ضغط هيستوغرام شدة البكسلات، مما يجعل الظلال أعمق والإضاءات أكثر سطوعًا، مما يعزز العمق والتفاصيل المتصورة.

## لماذا نستخدم Aspose.PSD للغة Java؟
توفر Aspose.PSD محركًا عالي الأداء وغنيًا بالميزات يمكنه التعامل مع **أكثر من 50 تنسيقًا للراستر والمتجه**، ومعالجة ملفات تصل إلى 500 ميغابايت دون تحميل كامل للذاكرة، وتصدير إلى TIFF مع تحكم دقيق في عدد البتات لكل عينة وتفسير الفوتومتري. تجعل هذه القدرات القابلة للقياس تجعلها خيارًا رئيسيًا لسلاسل معالجة الصور على مستوى المؤسسات.

## المتطلبات المسبقة

- معرفة أساسية ببرمجة Java.  
- مكتبة Aspose.PSD للغة Java مثبتة. يمكنك تنزيلها [هنا](https://releases.aspose.com/psd/java/).

## استيراد الحزم

أضف الاستيرادات المطلوبة إلى فئة Java الخاصة بك:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

## الخطوة 1: تحميل الصورة

فئة `Image` هي نقطة الدخول في Aspose.PSD التي تمثل أي صورة راستر مدعومة في الذاكرة.  
```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// Load an existing image into an instance of RasterImage class
Image image = Image.load(sourceFile);
```

نقوم بتحميل ملف PSD المصدر (`sample.psd`) إلى كائن `Image`، والذي يعمل كنقطة الدخول لجميع المعالجات اللاحقة.

## الخطوة 2: التحويل إلى RasterImage وتخزين البيانات مؤقتًا

`RasterImage` يوفر وصولًا مباشرًا إلى مستوى البكسل ويمكّن التخزين المؤقت للملفات الكبيرة.  
```java
// Cast object of Image to RasterImage
RasterImage rasterImage = (RasterImage)image;

// Check if RasterImage is cached and Cache RasterImage for better performance
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

التحويل إلى `RasterImage` يمنحنا إمكانية الوصول إلى عمليات مستوى البكسل. التخزين المؤقت يحسن الأداء، خاصةً للملفات الكبيرة.

## كيفية ضبط تباين صورة

طريقة `adjustContrast` هي استدعاء API بسيط يغيّر تباين الصورة بنسبة مئوية.  
```java
// Adjust the contrast
rasterImage.adjustContrast(50);
```

طريقة `adjustContrast` تأخذ عددًا صحيحًا يمثل نسبة التغيير. في هذا المثال نقوم بزيادة التباين بنسبة **50 %**.

## تحويل PSD إلى TIFF باستخدام Aspose.PSD

`TiffOptions` يتيح لك تحديد إعدادات TIFF الخاصة مثل عدد البتات لكل عينة، نوع الضغط، وتفسير الفوتومتري.  
```java
// Create an instance of TiffOptions for the resultant image
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
int[] ushort = { 8, 8, 8 };
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);

// Save the resultant image to TIFF format
String destName = dataDir + "AdjustContrast_out.tiff";
rasterImage.save(destName, tiffOptions);
```

هنا نقوم بتكوين `TiffOptions` (عدد البتات لكل عينة، تفسير الفوتومتري) و**نحفظ الصورة كـ TIFF**. تكمل هذه الخطوة سير عمل **تحويل PSD إلى TIFF**.

## المشكلات الشائعة والحلول
- **الصورة غير مخزنة مؤقتًا:** احرص دائمًا على استدعاء `cacheData()` للـ PSD الكبيرة لتجنب `OutOfMemoryError`.  
- **تحول لون غير متوقع:** تأكد من أن `setPhotometric` يتطابق مع مساحة اللون المستهدفة (RGB مقابل CMYK).  
- **الملف غير موجود:** تأكد من أن `dataDir` يشير إلى المجلد الصحيح وأن اسم الملف مكتوب بشكل صحيح.

## الأسئلة المتكررة

### س1: هل Aspose.PSD متوافق مع صيغ صور مختلفة؟
ج1: نعم، يدعم Aspose.PSD **أكثر من 50 صيغة إدخال وإخراج**، بما في ذلك PSD، TIFF، PNG، JPEG، BMP، و GIF، مما يمنحك مرونة عبر المشاريع.

### س2: كيف يمكنني الحصول على ترخيص مؤقت لـ Aspose.PSD؟
ج2: يمكنك الحصول على ترخيص مؤقت [هنا](https://purchase.aspose.com/temporary-license/).

### س3: أين يمكنني العثور على توثيق Aspose.PSD؟
ج3: الوثائق متاحة [هنا](https://reference.aspose.com/psd/java/).

### س4: ما هي خيارات الدعم المتاحة لـ Aspose.PSD؟
ج4: للحصول على الدعم، زر [منتدى Aspose.PSD](https://forum.aspose.com/c/psd/34).

### س5: هل يمكنني شراء Aspose.PSD؟
ج5: نعم، يمكنك شراء Aspose.PSD [هنا](https://purchase.aspose.com/buy).

## الخلاصة

أنت الآن تعرف **كيفية تحويل PSD إلى TIFF** وإجراء **ضبط تباين الصورة** باستخدام Aspose.PSD للغة Java. تمنحك هذه الخطوات تحكمًا دقيقًا في جودة الصورة مع الحفاظ على شفرة نظيفة وقابلة للصيانة. لا تتردد في تجربة طرق ضبط أخرى مثل `adjustBrightness` أو `adjustGamma` لتلبية احتياجاتك الخاصة.

---

**آخر تحديث:** 2026-07-27  
**تم الاختبار مع:** Aspose.PSD للغة Java 24.12  
**المؤلف:** Aspose

## دروس ذات صلة

- [دليل معالجة الصور في Java - ضبط سطوع الصورة باستخدام Aspose.PSD للغة Java](/psd/java/advanced-techniques/adjust-brightness/)
- [كيفية ضبط Gamma في معالجة الصور في Java باستخدام Aspose.PSD](/psd/java/advanced-techniques/adjust-gamma/)
- [تحويل PSD إلى صيغ صور الراستر باستخدام Aspose.PSD للغة Java](/psd/java/advanced-techniques/convert-psd-to-raster-formats/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}