---
date: 2026-08-17
description: تعلم كيفية قص ملف psd باستخدام Aspose.PSD للـ Java – طريقة سريعة ودقيقة
  لتقليم مستندات Photoshop في تطبيقات Java الخاصة بك.
keywords:
- crop psd file java
- aspose.psd java
- java image cropping
lastmod: 2026-08-17
linktitle: قص ملف PSD
og_description: قص ملف psd باستخدام Aspose.PSD للـ Java. يوضح لك هذا الدليل خطوة بخطوة
  كيفية تقليم ملفات Photoshop بكفاءة، مع شروحات خالية من الكود ونصائح لأفضل الممارسات.
og_image_alt: Guide showing how to crop a PSD file in Java using Aspose.PSD
og_title: قص ملف psd باستخدام Aspose.PSD – قص سريع للصور
schemas:
- author: Aspose
  dateModified: '2026-08-17'
  description: Learn how to crop psd file java with Aspose.PSD for Java – a fast,
    precise way to trim Photoshop documents in your Java applications.
  headline: Crop psd file java using Aspose.PSD
  type: TechArticle
- description: Learn how to crop psd file java with Aspose.PSD for Java – a fast,
    precise way to trim Photoshop documents in your Java applications.
  name: Crop psd file java using Aspose.PSD
  steps:
  - name: set document directory
    text: Replace “Your Document Directory” with the absolute or relative path that
      contains the PSD you want to process.
  - name: load PSD file
    text: The `RasterImage` class is Aspose.PSD’s entry point for raster‑based operations
      on a PSD file. Loading the file creates an in‑memory representation that you
      can manipulate.
  - name: define crop area
    text: '`Rectangle` defines the X and Y coordinates together with width and height
      of the region to keep. This class is part of the standard Java AWT package and
      is used by Aspose.PSD to specify cropping bounds.'
  - name: save cropped PSD
    text: After applying the crop, you can persist the result back to PSD format.
      The library writes only the cropped pixels, keeping the original color mode
      and bit depth.
  - name: save cropped image as PNG
    text: If you need a web‑friendly version, export the cropped raster to PNG. Aspose.PSD
      provides PNG save options that let you control compression level and interlacing.
  type: HowTo
- questions:
  - answer: Aspose.PSD for Java.
    question: What library handles PSD cropping in Java?
  - answer: Two API calls after loading the image.
    question: How many lines of code are required for a basic crop?
  - answer: Yes, using the built‑in PNG save options.
    question: Can I export the cropped area as PNG?
  - answer: A commercial license is needed beyond the trial period.
    question: Is a license required for production use?
  - answer: Java 8 and later, including Java 11, 17, and 21.
    question: What Java versions are supported?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- crop psd
- aspose.psd
- java image processing
title: قص ملف psd باستخدام Aspose.PSD للـ Java
url: /ar/java/image-processing/crop-psd-file/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# اقتصاص ملف PSD باستخدام Aspose.PSD في Java

## مقدمة

إذا كنت بحاجة إلى تقليم مستندات Photoshop برمجياً، فإن **crop psd file java** هو مهمة شائعة لمطوري Java الذين يعملون في خطوط أنابيب الرسومات، أو خطوط أنابيب الأصول، أو تدفقات العمل التصميمية المؤتمتة. يوفر Aspose.PSD للـ Java واجهة برمجة تطبيقات مخصصة تتيح لك تحديد مستطيل واستخراج المنطقة التي تحتاجها في بضع أسطر من الشيفرة فقط. في هذا الدرس ستتعلم لماذا تم بناء المكتبة لتوفير اقتصاص عالي الأداء، وكيفية إعداد بيئتك، والخطوات الدقيقة لإنتاج نتائج بصيغة PSD و PNG.

## إجابات سريعة
- **ما المكتبة التي تتعامل مع اقتصاص PSD في Java؟** Aspose.PSD للـ Java.
- **كم عدد الأسطر المطلوبة لاقتصاص أساسي؟** استدعاءان للـ API بعد تحميل الصورة.
- **هل يمكنني تصدير المنطقة المقصوصة كـ PNG؟** نعم، باستخدام خيارات حفظ PNG المدمجة.
- **هل يلزم الحصول على ترخيص للاستخدام في الإنتاج؟** يلزم ترخيص تجاري بعد فترة التجربة.
- **ما إصدارات Java المدعومة؟** Java 8 وما بعدها، بما في ذلك Java 11، 17، و 21.

## ما هو اقتصاص ملف PSD في Java؟

Crop psd file java يشير إلى عملية قطع منطقة مستطيلة برمجياً من مستند Photoshop (.psd) باستخدام شيفرة Java. مع Aspose.PSD يمكنك تنفيذ هذه العملية دون تشغيل Photoshop، مما يجعلها مثالية لخطوط أنابيب الصور على الخادم.

## لماذا تستخدم Aspose.PSD للـ Java؟

يدعم Aspose.PSD **أكثر من 30 تنسيق إدخال وإخراج** ويمكنه معالجة ملفات PSD تصل إلى **500 ميغابايت** دون تحميل المستند بالكامل في الذاكرة، بفضل هندسة البث الخاصة به. تحافظ المكتبة على الطبقات، الأقنعة، وملفات تعريف الألوان، مما ينتج نتيجة مقصوصة تتطابق مع مخرجات Photoshop الأصلية. هذه الأداء الكمي يتيح لك التعامل مع وظائف الدُفعات على عتاد عادي باستخدام استهلاك ذاكرة متوقع.

## المتطلبات المسبقة

- **بيئة تطوير Java** – JDK 8 أو أحدث مثبتة ومُعَدة.
- **Aspose.PSD للـ Java** – حمّل أحدث ملف JAR والوثائق [Aspose.PSD for Java documentation](https://reference.aspose.com/psd/java/).
- **ملف PSD تجريبي** – ضع ملف .psd داخل دليل مشروعك حتى يتمكن الشيفرة من العثور عليه.

## كيفية اقتصاص ملف PSD في Java؟

حمّل الملف المصدر، عرّف المستطيل الذي تريد الاحتفاظ به، طبّق الاقتصاص، وأخيراً احفظ النتيجة بالصيغ المطلوبة. يتطلب سير العمل الكامل خمس خطوات بسيطة، كل واحدة موضحة بمكان لإدراج الشيفرة الخاصة بك.

### الخطوة 1: تعيين دليل المستند

استبدل “Your Document Directory” بالمسار المطلق أو النسبي الذي يحتوي على ملف PSD الذي تريد معالجته.

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;
import com.aspose.psd.Rectangle;

import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.imageoptions.PsdOptions;
import com.aspose.psd.xmp.types.complex.colorant.ColorType;
```

### الخطوة 2: تحميل ملف PSD

الفئة `RasterImage` هي نقطة الدخول في Aspose.PSD للعمليات القائمة على البكسل لملف PSD. تحميل الملف يُنشئ تمثيلاً في الذاكرة يمكنك التلاعب به.

```java
String dataDir = "Your Document Directory";
```

### الخطوة 3: تعريف منطقة الاقتصاص

`Rectangle` تُعرّف إحداثيات X و Y مع العرض والارتفاع للمنطقة التي تريد الاحتفاظ بها. هذه الفئة جزء من حزمة Java AWT القياسية وتُستخدم من قبل Aspose.PSD لتحديد حدود الاقتصاص.

```java
String sourceFileName = dataDir + "1.psd";
RasterImage image = (RasterImage)Image.load(sourceFileName);
```

### الخطوة 4: حفظ PSD المقصوص

بعد تطبيق الاقتصاص، يمكنك حفظ النتيجة مرة أخرى بصيغة PSD. المكتبة تكتب فقط البكسلات المقصوصة، مع الحفاظ على وضع اللون الأصلي وعمق البت.

```java
image.crop(new Rectangle(10, 30, 100, 100));
```

### الخطوة 5: حفظ الصورة المقصوصة كـ PNG

إذا كنت بحاجة إلى نسخة صديقة للويب، صدّر البكسل المقصوص إلى PNG. يوفر Aspose.PSD خيارات حفظ PNG تتيح لك التحكم في مستوى الضغط والتداخل.

```java
String exportPathPsd = dataDir + "CropTest.psd";
image.save(exportPathPsd, new PsdOptions());
```

## المشكلات الشائعة والحلول

- **إحداثيات المستطيل غير صحيحة** – تأكد من أن قيم X/Y تبدأ من 0 للزاوية العلوية اليسرى؛ القيم السالبة ستؤدي إلى استثناء `ArgumentException`.
- **ارتفاع استهلاك الذاكرة في الملفات الكبيرة** – استخدم الخيار `loadOptions.setLoadOnlyVisibleLayers(true)` لتقليل الذاكرة عندما لا تحتاج إلى الطبقات المخفية.
- **فقدان ملف تعريف اللون** – احفظ ملف تعريف ICC الأصلي عبر استدعاء `image.getColorProfile()` قبل الاقتصاص وأعد تعيينه بعد العملية.

## الأسئلة المتكررة

### س1: هل يمكنني استخدام Aspose.PSD للـ Java لاقتصاص الصور بصيغ أخرى؟

A1: Aspose.PSD يستهدف أساساً ملفات PSD، لكنه يدعم أيضاً BMP، GIF، JPEG، PNG، TIFF والعديد من صيغ الصور النقطية الأخرى للإدخال والإخراج.

### س2: هل Aspose.PSD للـ Java مناسب لمعالجة الصور على نطاق واسع؟

A2: نعم. تُعالج بنية البث في المكتبة ملفات PSD متعددة المئات من الصفحات بذاكرة أقل من 100 ميغابايت، مما يجعلها مثالية للوظائف الدُفعية.

### س3: هل هناك اعتبارات ترخيص لاستخدام Aspose.PSD للـ Java؟

A3: يلزم الحصول على ترخيص تجاري للنشر في بيئات الإنتاج. التفاصيل متوفرة على [صفحة شراء Aspose.PSD للـ Java](https://purchase.aspose.com/buy).

### س4: كيف يمكنني الحصول على دعم لمشكلات Aspose.PSD للـ Java؟

A4: زر [منتدى Aspose.PSD للـ Java](https://forum.aspose.com/c/psd/34) لطرح الأسئلة، مشاركة مقتطفات الشيفرة، والحصول على مساعدة من المجتمع ومهندسي المنتج.

### س5: هل يمكنني تجربة Aspose.PSD للـ Java قبل الشراء؟

A5: نعم، يمكن تنزيل نسخة تجريبية مجانية كاملة الوظائف من [Aspose.PSD free trial download](https://releases.aspose.com/).

{{< blocks/products/products-backtop-button >}}

```java
String exportPathPng = dataDir + "CropTest.png";
PngOptions options = new PngOptions();
options.setColorType(PngColorType.TruecolorWithAlpha);
image.save(exportPathPng, options);
```

## دروس ذات صلة

- [Crop Image by Rectangle in Aspose.PSD for Java](/psd/java/image-editing/crop-image-by-rectangle/)
- [Crop Image by Shifts in Aspose.PSD for Java](/psd/java/image-editing/crop-image-by-shifts/)
- [How to Rotate Image in Java with Aspose.PSD](/psd/java/advanced-image-manipulation/rotate-image/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}