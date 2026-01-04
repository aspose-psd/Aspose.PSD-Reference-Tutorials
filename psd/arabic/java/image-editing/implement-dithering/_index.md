---
date: 2026-01-04
description: تعلم كيفية القضاء على تدرج الألوان وتحسين جودة الصورة التي يمكن لمطوري
  جافا تحقيقها باستخدام تقنية التخفيف في Aspose.PSD for Java.
linktitle: Implement Dithering for Raster Images
second_title: Aspose.PSD Java API
title: كيفية القضاء على تدرج اللون باستخدام التمويه في Aspose.PSD للـ Java
url: /ar/java/image-editing/implement-dithering/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# كيفية القضاء على تدرج اللون باستخدام Dithering في Aspose.PSD للـ Java

إذا كنت مطور Java تبحث عن **كيفية القضاء على تدرج اللون**، فإن Aspose.PSD يقدم طريقة بسيطة لكنها قوية للقيام بذلك. في هذا البرنامج التعليمي سنستعرض عملية تطبيق Dithering على الصور النقطية، والتي لا تزيل فقط التدرج غير المرغوب فيه بل **تحسن جودة الصورة** التي يمكن لتطبيقات Java تقديمها. في النهاية ستحصل على عينة كود جاهزة للتنفيذ تنتج تدرجات أكثر سلاسة ونتائج بصرية أغنى.

## إجابات سريعة
- **ما هو الهدف الرئيسي من Dithering؟** يضيف ضوضاءً مُتحكمًا فيها لتقليل تدرج اللون وتنعيم التدرجات.  
- **أي طريقة Dithering يستخدمها المثال؟** Floyd‑Steinberg (ThresholdDithering).  
- **هل أحتاج إلى ترخيص لتشغيل الكود؟** النسخة التجريبية المجانية تكفي للتقييم؛ الترخيص مطلوب للإنتاج.  
- **هل يمكنني حفظ الناتج بصيغ غير BMP؟** نعم، يدعم Aspose.PSD صيغ PNG، JPEG، TIFF، إلخ.  
- **كم من الوقت تستغرق عملية التنفيذ؟** حوالي 10‑15 دقيقة للإعداد الأساسي.

## ما هو تدرج اللون وكيفية القضاء عليه؟
يحدث تدرج اللون عندما تحتوي الصورة على عدد محدود من الألوان، مما يسبب ظهور “خطوات” مرئية في ما يجب أن يكون تدرجات ناعمة. يخفف Dithering من ذلك عن طريق توزيع بكسلات الألوان المجاورة، مما يخلق وهمًا بألوان وسطية. لذا فإن تنفيذ Dithering يُعد تقنية موثوقة **للقضاء على تدرج اللون** في الرسومات النقطية.

## لماذا نستخدم Dithering لتحسين جودة الصورة في Java؟
استخدام إمكانيات Dithering في Aspose.PSD يتيح لك:

- إنتاج صور ذات جودة احترافية دون الحاجة إلى أدوات طرف ثالث مكلفة.  
- إبقاء المعالجة بالكامل داخل قاعدة شفرة Java الخاصة بك، مما يبسط عملية النشر.  
- الحفاظ على التحكم الكامل في صيغة الإخراج وخيارات الضغط.

## المتطلبات المسبقة

- معرفة أساسية ببرمجة Java.  
- إضافة مكتبة Aspose.PSD للـ Java إلى مشروعك (Maven/Gradle أو JAR يدوي).  
- ملف PSD تجريبي للتجربة.

## استيراد الحزم

في مشروع Java الخاص بك، استورد الفئات الضرورية من Aspose.PSD:

```java
import com.aspose.psd.DitheringMethod;
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.BmpOptions;
```

## الخطوة 1: تحميل الصورة

أولاً، حمّل ملف PSD موجود إلى كائن `PsdImage`. عدّل المسار ليشير إلى ملفك التجريبي الخاص.

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// Load an existing image into an instance of RasterImage class
PsdImage image = (PsdImage)Image.load(sourceFile);
```

## الخطوة 2: تنفيذ Dithering

طبق Dithering من نوع Floyd‑Steinberg (ThresholdDithering) على الصورة المحمّلة. هذه الخطوة هي جوهر **كيفية القضاء على تدرج اللون**.

```java
// Peform Floyd Steinberg dithering on the current image
image.dither(DitheringMethod.ThresholdDithering, 4);
```

## الخطوة 3: حفظ الصورة الناتجة

أخيرًا، احفظ الصورة المعالجة إلى القرص. المثال يحفظها بصيغة BMP، لكن يمكنك اختيار أي صيغة مدعومة.

```java
String destName = dataDir + "SampleImage_out.bmp";

// Save the resultant image
image.save(destName, new BmpOptions());
```

## المشكلات الشائعة والنصائح

- **مسار الملف غير صحيح** – تأكد من أن `dataDir` ينتهي بالفاصل المناسب للملفات (`/` أو `\\`).  
- **صيغة غير مدعومة** – إذا كنت بحاجة إلى PNG أو JPEG، استبدل `BmpOptions` بـ `PngOptions` أو `JpegOptions`.  
- **استخدام الذاكرة** – ملفات PSD الكبيرة قد تستهلك ذاكرة RAM كبيرة؛ فكر في المعالجة على أجزاء أو زيادة حجم heap الخاص بـ JVM.

## الأسئلة المتكررة

**س:** هل يمكنني تطبيق Dithering على أي نوع من الصور النقطية؟  
**ج:** نعم، يدعم Aspose.PSD تطبيق Dithering لمعظم صيغ الصور النقطية مثل BMP، PNG، JPEG، وTIFF.

**س:** كيف يحسن Dithering جودة الصورة؟  
**ج:** من خلال إدخال ضوضاء خفيفة، يقوم Dithering بتنعيم انتقالات التدرجات، مما يقضي بفعالية على تدرج اللون.

**س:** هل Aspose.PSD مناسب لمعالجة الصور على مستوى الإنتاج؟  
**ج:** بالتأكيد. إنها مكتبة ناضجة تستخدمها الشركات في سير عمل رسومات عالية الأداء.

**س:** هل هناك طرق Dithering أخرى متاحة؟  
**ج:** نعم، يقدم Aspose.PSD عدة طرق (مثل OrderedDithering، FloydSteinberg) يمكنك اختيارها عبر `DitheringMethod`.

**س:** هل يمكنني دمج هذا في مشروع Java موجود؟  
**ج:** بالطبع. فقط أضف ملف JAR الخاص بـ Aspose.PSD (أو تبعية Maven/Gradle) واستخدم نمط الكود نفسه الموضح أعلاه.

---

**آخر تحديث:** 2026-01-04  
**تم الاختبار مع:** Aspose.PSD للـ Java 24.12  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}