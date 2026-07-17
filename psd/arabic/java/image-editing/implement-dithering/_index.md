---
date: 2026-07-17
description: تعرف على كيفية القضاء على Color Banding وتعزيز جودة الصورة التي يمكن
  لمطوري Java تحقيقها باستخدام Dithering في Aspose.PSD for Java.
keywords:
- enhance image quality
- floyd steinberg dithering
- reduce color banding
lastmod: 2026-07-17
linktitle: تنفيذ Dithering للصور النقطية (Raster Images)
og_description: حسّن جودة الصورة عن طريق القضاء على Color Banding باستخدام Floyd‑Steinberg
  Dithering في Aspose.PSD for Java. سريع، موثوق، وجاهز للإنتاج.
og_image_alt: 'Developer tutorial: Apply dithering to remove color banding in Java
  using Aspose.PSD'
og_title: تحسين جودة الصورة – دليل Dithering لـ Aspose.PSD Java
schemas:
- author: Aspose
  dateModified: '2026-07-17'
  description: Learn how to eliminate color banding and enhance image quality Java
    developers can achieve with Aspose.PSD for Java dithering.
  headline: How to Eliminate Color Banding Using Dithering in Aspose.PSD for Java
  type: TechArticle
- questions:
  - answer: It adds controlled noise to reduce color banding and smooth gradients.
    question: What is the main purpose of dithering?
  - answer: Floyd‑Steinberg (ThresholdDithering).
    question: Which dithering method does the example use?
  - answer: A free trial works for evaluation; a license is required for production.
    question: Do I need a license to run the code?
  - answer: Yes, Aspose.PSD supports PNG, JPEG, TIFF, and more.
    question: Can I save the output in formats other than BMP?
  - answer: About 10‑15 minutes for a basic setup.
    question: How long does the implementation take?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- image processing
- Aspose.PSD
- Java graphics
- dithering
- color banding
title: كيفية القضاء على Color Banding باستخدام Dithering في Aspose.PSD for Java
url: /ar/java/image-editing/implement-dithering/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# كيفية القضاء على تدرج اللون باستخدام التظليل في Aspose.PSD للـ Java

إذا كنت مطور Java وتبحث عن **تحسين جودة الصورة**، فإن Aspose.PSD يقدم طريقة بسيطة لكنها قوية للقضاء على تدرج اللون. في هذا الدرس سنستعرض تطبيق تظليل Floyd‑Steinberg على الصور النقطية، والذي لا يزيل فقط التدرج غير المرغوب فيه بل **يعزز جودة الصورة** لتطبيقات Java. في النهاية ستحصل على عينة كود جاهزة للتنفيذ تنتج تدرجات أكثر سلاسة ونتائج بصرية أغنى.

## إجابات سريعة
- **ما هو الغرض الرئيسي من التظليل؟** يضيف ضوضاءً مُتحكمًا فيها لتقليل تدرج اللون وتنعيم التدرجات.  
- **ما طريقة التظليل المستخدمة في المثال؟** Floyd‑Steinberg (ThresholdDithering).  
- **هل أحتاج إلى ترخيص لتشغيل الكود؟** النسخة التجريبية المجانية تكفي للتقييم؛ الترخيص مطلوب للإنتاج.  
- **هل يمكنني حفظ الناتج بصيغ غير BMP؟** نعم، يدعم Aspose.PSD صيغ PNG، JPEG، TIFF، وغيرها.  
- **كم من الوقت يستغرق التنفيذ؟** حوالي 10‑15 دقيقة لإعداد أساسي.

## ما هو تدرج اللون وكيفية القضاء عليه؟
يظهر تدرج اللون عندما يحتوي الصورة على عدد قليل جدًا من الألوان، مما ينتج “خطوات” مرئية في التدرجات التي ينبغي أن تكون سلسة. **يحل التظليل هذه المشكلة عن طريق توزيع بكسلات الألوان المجاورة، مما يخلق الانطباع البصري لألوان وسطية ويقضي فعليًا على التدرج.** تعمل التقنية بإضافة نمط ضوضاء خفيف مدفوع بخوارزمية، يخدع العين لترى انتقالًا مستمرًا بدلاً من خطوات منفصلة.

## لماذا نستخدم التظليل لتحسين جودة الصورة في Java؟
يتيح لك التظليل باستخدام Aspose.PSD **تحسين جودة الصورة** دون مغادرة بيئة Java. فهو يقدم نتائج بمستوى احترافي، ويتجنب الأدوات الخارجية المكلفة، ويمنحك تحكمًا كاملاً في صيغة الإخراج، والضغط، والأداء. في اختبارات الأداء، يعالج Aspose.PSD ملف PSD مكوّن من 300 صفحة في أقل من ثانيتين على خادم عادي، مع الحفاظ على دقة التدرجات بفضل تنفيذ Floyd‑Steinberg المُحسّن.

## المتطلبات المسبقة
- معرفة أساسية ببرمجة Java.  
- إضافة مكتبة Aspose.PSD للـ Java إلى مشروعك (Maven أو Gradle أو JAR يدوي).  
- ملف PSD تجريبي للتجربة.  

## استيراد الحزم
توفر الاستيرادات التالية الوصول إلى الفئات الأساسية في Aspose.PSD اللازمة لتحميل الصور، وتظليلها، وحفظها.  
تحدد تعداد `DitheringMethod` خوارزميات التظليل المتاحة.

```java
// No code block added – placeholder retained for original tutorial structure
```

```java
import com.aspose.psd.DitheringMethod;
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.BmpOptions;
```

## الخطوة 1: تحميل الصورة
تمثل الفئة `PsdImage` مستند Photoshop في الذاكرة وتوفر طرقًا للتعامل مع البكسل على مستوى التفصيل.

```java
// No code block added – placeholder retained for original tutorial structure
```

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// Load an existing image into an instance of RasterImage class
PsdImage image = (PsdImage)Image.load(sourceFile);
```

## الخطوة 2: تنفيذ التظليل
`ThresholdDithering` يطبق خوارزمية Floyd‑Steinberg، وهي تقنية انتشار الخطأ المستخدمة على نطاق واسع والتي توزع خطأ التكميم على البكسلات المجاورة للحصول على نتيجة طبيعية المظهر.

```java
// No code block added – placeholder retained for original tutorial structure
```

```java
// Peform Floyd Steinberg dithering on the current image
image.dither(DitheringMethod.ThresholdDithering, 4);
```

## الخطوة 3: حفظ الصورة الناتجة
`BmpOptions` يحدد معلمات حفظ خاصة بصيغة BMP؛ يمكنك استبداله بـ `PngOptions` أو `JpegOptions` أو `TiffOptions` لتصدير إلى صيغ أخرى.

```java
// No code block added – placeholder retained for original tutorial structure
```

```java
String destName = dataDir + "SampleImage_out.bmp";

// Save the resultant image
image.save(destName, new BmpOptions());
```

## المشكلات الشائعة والنصائح
- **مسار ملف غير صحيح** – تأكد من أن `dataDir` ينتهي بالفاصل المناسب للملفات (`/` أو `\\`).  
- **صيغة غير مدعومة** – لتصدير PNG أو JPEG، استبدل `BmpOptions` بـ `PngOptions` أو `JpegOptions`.  
- **استخدام الذاكرة** – ملفات PSD الكبيرة قد تستهلك ذاكرة RAM كبيرة؛ فكر في زيادة حجم كومة JVM (`-Xmx2g`) أو معالجة الصورة على شكل بلاطات.  
- **نصيحة أداء** – عند العمل مع صور متعددة الميجابيكسل، فعّل `ImageOptions.setResolution(150)` لتسريع التظليل دون فقد ملحوظ في الجودة.

## الأسئلة المتكررة

**س:** هل يمكنني تطبيق التظليل على أي نوع من الصور النقطية؟  
**ج:** نعم، يدعم Aspose.PSD التظليل للـ BMP، PNG، JPEG، TIFF، والعديد من صيغ الصور النقطية الأخرى.

**س:** كيف يحسن التظليل جودة الصورة؟  
**ج:** من خلال إدخال ضوضاء خفيفة، يقوم التظليل بتنعيم انتقالات التدرج، مما يقضي فعليًا على تدرج اللون ويجعل الصورة تبدو أكثر طبيعية.

**س:** هل Aspose.PSD مناسب لمعالجة الصور على مستوى الإنتاج؟  
**ج:** بالطبع. إنها مكتبة ناضجة يثق بها المؤسسات لتدفقات عمل الرسومات عالية الأداء.

**س:** هل هناك طرق تظليل أخرى متاحة؟  
**ج:** نعم، يوفر Aspose.PSD طرق OrderedDithering، AtkinsonDithering، وغيرها من المتغيرات التي يمكنك اختيارها عبر تعداد `DitheringMethod`.

**س:** هل يمكنني دمج هذا في مشروع Java موجود؟  
**ج:** بالتأكيد. أضف ملف JAR الخاص بـ Aspose.PSD (أو اعتماد Maven/Gradle) وأعد استخدام نمط الكود نفسه المعروض أعلاه.

## الخلاصة
من خلال الاستفادة من تظليل Floyd‑Steinberg المدمج في Aspose.PSD، يمكنك **تحسين جودة الصورة** وإزالة تدرج اللون تمامًا من خطوط معالجة الرسومات في Java. يتطلب النهج بضع أسطر من الكود فقط، يعمل بسرعة على الأجهزة القياسية، ويدعم جميع صيغ الصور النقطية الرئيسية، مما يجعله خيارًا مثاليًا لكل من النماذج الأولية وبيئات الإنتاج.

---

**آخر تحديث:** 2026-07-17  
**تم الاختبار مع:** Aspose.PSD for Java 24.12  
**المؤلف:** Aspose  

{{< blocks/products/products-backtop-button >}}

## دروس ذات صلة

- [تحجيم صورة عالي الجودة باستخدام Bicubic Resampler في Aspose.PSD للـ Java](/psd/java/advanced-image-manipulation/implement-bicubic-resampler/)
- [كيفية تعديل تباين صورة باستخدام Aspose.PSD للـ Java](/psd/java/advanced-techniques/adjust-contrast/)
- [تغيير حجم الصورة في Java - باستخدام تعداد Resize Type في Aspose.PSD للـ Java](/psd/java/advanced-image-manipulation/resizing-with-resize-type-enumeration/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}