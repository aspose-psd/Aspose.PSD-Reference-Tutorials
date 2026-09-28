---
date: 2026-09-28
description: يظهر دليل معالجة الصور في Java كيفية ضبط سطوع صورة باستخدام Aspose.PSD
  for Java. اتبع التعليمات خطوة بخطوة لتحميل وتعديل وحفظ ملفات PSD أو TIFF.
keywords:
- java image processing
- aspose psd java
- java image manipulation
- adjust brightness java
lastmod: 2026-09-28
linktitle: ضبط سطوع الصورة
og_description: يظهر دليل معالجة الصور في Java كيفية ضبط سطوع صورة باستخدام Aspose.PSD
  for Java. اتبع التعليمات خطوة بخطوة لتحميل وتعديل وحفظ ملفات PSD أو TIFF.
og_image_alt: Guide to adjusting image brightness in Java using Aspose.PSD
og_title: 'معالجة الصور في Java: ضبط السطوع باستخدام Aspose.PSD'
schemas:
- author: Aspose
  dateModified: '2026-09-28'
  description: Java image processing tutorial shows how to adjust brightness of an
    image using Aspose.PSD for Java. Follow step‑by‑step code to load, modify, and
    save PSD or TIFF files.
  headline: 'Java image processing: adjust brightness with Aspose.PSD'
  type: TechArticle
- description: Java image processing tutorial shows how to adjust brightness of an
    image using Aspose.PSD for Java. Follow step‑by‑step code to load, modify, and
    save PSD or TIFF files.
  name: 'Java image processing: adjust brightness with Aspose.PSD'
  steps:
  - name: Load the image
    text: The `RasterImage` class represents a rasterized version of a PSD or TIFF
      file in memory. It provides direct pixel access for color‑correction operations.
      In this step, we load the target image and cast it to a `RasterImage` for further
      processing.
  - name: Adjust brightness
    text: '`adjustBrightness(int value)` changes the lightness of every pixel by the
      specified integer value. Positive numbers brighten the image; negative numbers
      darken it. The method processes the image in‑place, so no additional object
      creation is required. Here, we use the `adjustBrightness` method to mod'
  - name: Set TiffOptions
    text: '`TiffOptions` specifies the encoding parameters for TIFF output, such as
      bits per sample and photometric interpretation. It lets you control how the
      resulting file is encoded. Configure the `TiffOptions` for saving the adjusted
      image. Adjust the `bitsPerSample` and `photometric` properties based on '
  - name: Save the resultant image
    text: Calling `save` writes the processed raster data to a file using the previously
      defined options. The operation is atomic and guarantees that the output file
      is a valid TIFF image. Finally, save the modified image using the specified
      `TiffOptions`.
  type: HowTo
- questions:
  - answer: Yes, Aspose.PSD for Java supports JPEG, PNG, BMP, GIF, and many other
      raster formats in addition to PSD and TIFF.
    question: Can I adjust brightness in other image formats besides PSD?
  - answer: Wrap the processing code in a try‑catch block and catch `IOException`
      or `ImageProcessingException` to manage file‑access and raster‑operation errors.
    question: How can I handle errors during the image adjustment process?
  - answer: The method accepts integer values from –255 to +255; values outside this
      range are clamped to the nearest limit.
    question: Is there a limit to the range of brightness adjustment?
  - answer: Yes, a commercial license is required for production use. Purchase a license
      [here](https://purchase.aspose.com/buy).
    question: Can I use Aspose.PSD for Java in commercial projects?
  - answer: Yes, you can explore the library with a free trial from [here](https://releases.aspose.com/).
    question: Is there a free trial available?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- java image processing
- aspose psd
- java image manipulation
title: 'معالجة الصور في Java: ضبط السطوع باستخدام Aspose.PSD'
url: /ar/java/advanced-techniques/adjust-brightness/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# ضبط سطوع صورة باستخدام Aspose.PSD للـ Java

## مقدمة

في هذا **java image processing** tutorial ستتعلم كيفية ضبط سطوع صورة مباشرةً من خلال كود Java. تعديل السطوع هو مهمة شائعة لمصممي الجرافيك، المصورين، وأي شخص يبني خطوط معالجة الصور. في هذا **java image manipulation** guide سنستعرض سير العمل الكامل — تحميل ملف PSD/TIFF، تطبيق إزاحة سطوع، وحفظ النتيجة — باستخدام مكتبة Aspose.PSD للـ Java.

## إجابات سريعة
- **ما المكتبة التي تتعامل مع السطوع؟** Aspose.PSD for Java.  
- **ما الطريقة التي تغير السطوع؟** `RasterImage.adjustBrightness()`.  
- **هل يمكنني العمل مع ملفات PSD و TIFF؟** Yes, the API supports both formats and 10+ additional image types.  
- **هل أحتاج إلى ترخيص للإنتاج؟** A commercial license is required for non‑evaluation use.  
- **كم يستغرق تنفيذ العملية؟** Typically under 10 minutes for a basic adjustment.

## ما هو java image processing؟
`Java image processing` يشير إلى مجموعة التقنيات التي تتيح لك قراءة، تحويل، وكتابة بيانات الصورة برمجيًا باستخدام Java. تعديل السطوع هو أحد العمليات الأساسية التي تغير الإضاءة العامة لكل بكسل، مما يجعل المناطق الداكنة أكثر إضاءة أو المناطق المضيئة أكثر قتامة.

## لماذا تستخدم Aspose.PSD للـ Java؟
- **يدعم أكثر من 10 صيغ نقطية ومتجهة** – PSD, TIFF, JPEG, PNG, BMP, GIF، وغيرها.  
- **تنفيذ Pure‑Java** – لا توجد DLLs أصلية أو تبعيات خارجية، لذا يعمل على أي JVM.  
- **تخزين مؤقت عالي الأداء** – يمكن تخزين بيانات النقطية مؤقتًا، مما يتيح تحريرًا أسرع حتى 2× على الملفات الكبيرة.  
- **واجهة برمجة تطبيقات غنية** – أكثر من 150 طريقة لتصحيح الألوان، معالجة الطبقات، الأقنعة، والتجميع.

## المتطلبات المسبقة

- مكتبة Aspose.PSD للـ Java: قم بتحميل وتثبيت المكتبة من [Aspose.PSD for Java documentation](https://reference.aspose.com/psd/java/).  
- Java Development Kit (JDK) 8 أو أعلى مثبت على جهازك.  
- بيئة تطوير (IDE) مثل IntelliJ IDEA، Eclipse، أو VS Code.

## استيراد الحزم

لبدء العمل، استورد الحزم اللازمة إلى مشروع Java الخاص بك. في هذا المثال، سنستخدم ما يلي:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

الآن، دعنا نفصل عملية ضبط سطوع صورة إلى خطوات بسيطة:

## كيفية ضبط السطوع باستخدام Aspose.PSD؟

حمّل صورة المصدر، طبّق إزاحة سطوع، اضبط خيارات الحفظ، واكتب النتيجة إلى القرص — كل ذلك في أربع خطوات مختصرة. الأقسام التالية تقدم دليلًا واضحًا خطوة بخطوة يمكنك نسخه إلى مشروعك الخاص. يضمن هذا النهج تنفيذ كل عملية بكفاءة وأن الصورة النهائية تحتفظ بالجودة الأصلية مع انعكاس التغيير المطلوب في السطوع.

### الخطوة 1: تحميل الصورة

فئة `RasterImage` تمثل نسخة نقطية من ملف PSD أو TIFF في الذاكرة. توفر وصولًا مباشرًا إلى البكسل لعمليات تصحيح اللون.

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "AdjustBrightness_out.tiff";

// Load an existing image into an instance of RasterImage class
Image image = Image.load(sourceFile);
// Cast object of Image to RasterImage
RasterImage rasterImage = (RasterImage) image;

// Check if RasterImage is cached and Cache RasterImage for better performance
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

في هذه الخطوة، نقوم بتحميل الصورة المستهدفة وتحويلها إلى `RasterImage` لمزيد من المعالجة.

### الخطوة 2: ضبط السطوع

`adjustBrightness(int value)` يغيّر إضاءة كل بكسل بالقيمة الصحيحة المحددة. الأرقام الموجبة تضيء الصورة؛ الأرقام السالبة تجعلها أغمق. تقوم الطريقة بمعالجة الصورة في الموقع، لذا لا يلزم إنشاء كائن إضافي.

```java
// Adjust the brightness
rasterImage.adjustBrightness(-50);
```

هنا نستخدم طريقة `adjustBrightness` لتعديل سطوع الصورة. في هذا المثال، نقلل السطوع بمقدار 50 وحدة، لكن يمكنك تخصيص هذه القيمة وفقًا لاحتياجاتك.

### الخطوة 3: تعيين TiffOptions

`TiffOptions` يحدد معلمات الترميز لإخراج TIFF، مثل عدد البتات لكل عينة وتفسير الفوتومتري. يتيح لك التحكم في كيفية ترميز الملف الناتج.

```java
int[] ushort = {8, 8, 8};
// Create an instance of TiffOptions for the resultant image
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);
```

قم بتكوين `TiffOptions` لحفظ الصورة المعدلة. اضبط خصائص `bitsPerSample` و `photometric` وفقًا لاحتياجاتك الخاصة.

### الخطوة 4: حفظ الصورة الناتجة

استدعاء `save` يكتب بيانات النقطية المعالجة إلى ملف باستخدام الخيارات المحددة مسبقًا. العملية ذرية وتضمن أن يكون ملف الإخراج صورة TIFF صالحة.

```java
// Save the resultant image
rasterImage.save(destName, tiffOptions);
```

أخيرًا، احفظ الصورة المعدلة باستخدام `TiffOptions` المحددة.

## المشكلات الشائعة والحلول

| المشكلة | السبب | الحل |
|-------|--------|----------|
| **`ClassCastException` عند تحويل Image** | الملف ليس صورة نقطية (مثلاً PSD متجهة). | تحقق من تنسيق الملف المصدر أو استخدم `image instanceof RasterImage` قبل التحويل. |
| **تغيير السطوع لا يؤثر** | لم يتم تخزين الصورة مؤقتًا قبل التعديل. | استدعِ `rasterImage.cacheData()` كما هو موضح في الخطوة 1. |
| **الملف المحفوظ يبدو معطوبًا** | إعدادات `TiffOptions` غير صحيحة. | تأكد من أن `bitsPerSample` يطابق عمق الصورة المصدر (عادةً 8‑bit لكل قناة). |

## الأسئلة المتكررة

**س: هل يمكنني ضبط السطوع في صيغ صور أخرى غير PSD؟**  
**ج:** نعم، Aspose.PSD للـ Java يدعم JPEG، PNG، BMP، GIF، والعديد من صيغ الصور النقطية الأخرى بالإضافة إلى PSD و TIFF.

**س: كيف يمكنني التعامل مع الأخطاء أثناء عملية ضبط الصورة؟**  
**ج:** ضع كود المعالجة داخل كتلة try‑catch والتقط `IOException` أو `ImageProcessingException` لإدارة أخطاء الوصول إلى الملفات وعمليات النقطية.

**س: هل هناك حد لنطاق ضبط السطوع؟**  
**ج:** الطريقة تقبل قيمًا صحيحة من –255 إلى +255؛ القيم خارج هذا النطاق تُقيد إلى أقرب حد.

**س: هل يمكنني استخدام Aspose.PSD للـ Java في مشاريع تجارية؟**  
**ج:** نعم، يلزم الحصول على ترخيص تجاري للاستخدام في الإنتاج. اشترِ ترخيصًا [هنا](https://purchase.aspose.com/buy).

**س: هل هناك نسخة تجريبية مجانية متاحة؟**  
**ج:** نعم، يمكنك تجربة المكتبة بنسخة تجريبية مجانية من [هنا](https://releases.aspose.com/).

**س: هل تؤثر طريقة `adjustBrightness` على رؤية الطبقات؟**  
**ج:** الطريقة تعمل على الصورة المركبة النقطية، لذا تُهمل الطبقات المخفية أثناء التحويل النقطي، مما يحافظ على النتيجة البصرية المقصودة.

**س: هل يمكنني ربط تعديلات متعددة (مثل التباين، التشبع) معًا؟**  
**ج:** بالتأكيد. بعد ضبط السطوع، يمكنك استدعاء `adjustContrast`، `adjustSaturation`، أو طرق تصحيح ألوان أخرى على نفس كائن `RasterImage`.

**آخر تحديث:** 2026-09-28  
**تم الاختبار مع:** Aspose.PSD للـ Java 24.12 (أحدث نسخة وقت الكتابة)  
**المؤلف:** Aspose

## دروس ذات صلة

- [مكتبة معالجة الصور Java: عكس الطبقة باستخدام Aspose.PSD](/psd/java/advanced-image-manipulation/invert-adjustment-layer/)
- [تحويل الصورة إلى تدرج الرمادي باستخدام Aspose.PSD للـ Java](/psd/java/advanced-techniques/grayscale-image/)
- [كيفية تدوير الصورة بزاوية محددة باستخدام Aspose.PSD للـ Java](/psd/java/advanced-image-manipulation/rotate-image-specific-angle/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}