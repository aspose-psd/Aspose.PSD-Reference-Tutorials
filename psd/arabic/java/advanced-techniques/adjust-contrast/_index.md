---
date: 2026-02-25
description: تعلم كيفية تحويل ملفات PSD إلى TIFF وإجراء تعديل تباين الصورة باستخدام
  Aspose.PSD for Java، مكتبة رائدة لمعالجة الصور بلغة جافا.
linktitle: Convert PSD to TIFF and Adjust Contrast
second_title: Aspose.PSD Java API
title: كيفية تحويل PSD إلى TIFF وضبط التباين باستخدام Aspose.PSD للـ Java
url: /ar/java/advanced-techniques/adjust-contrast/
weight: 22
---

 names, URLs.

Let's produce Arabic.

We'll keep bold formatting.

Let's write.

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# كيفية تحويل PSD إلى TIFF وضبط التباين باستخدام Aspose.PSD للـ Java

## المقدمة

إذا كنت بحاجة إلى **تحويل PSD إلى TIFF** مع ضبط جودة الرسومات بصريًا، فأنت في المكان المناسب. في هذا الدرس سنستعرض سير العمل الكامل باستخدام Aspose.PSD للـ Java—مكتبة **java image manipulation** قوية. ستتعلم كيفية تحسين **ضبط تباين الصورة**، وتخزين بيانات الراستر الكبيرة مؤقتًا للأداء، وأخيرًا **حفظ الصورة كـ TIFF** للمعالجة اللاحقة. هيا نبدأ!

## إجابات سريعة
- **ماذا يعني “ضبط التباين”؟** يغيّر الفرق بين أغمق وأفتح البكسلات، مما يجعل التفاصيل بارزة.  
- **أي مكتبة تتولى ذلك؟** Aspose.PSD للـ Java – مجموعة أدوات معالجة الصور المتكاملة.  
- **هل أحتاج إلى ترخيص؟** **ترخيص aspose مؤقت** يكفي للاختبار؛ الترخيص الكامل مطلوب للإنتاج.  
- **هل يمكنني **تحويل PSD إلى TIFF**؟** بالطبع – سنستخدم `TiffOptions` لتصدير الصورة المعالجة.  
- **كم يستغرق تشغيل الكود؟** عادةً أقل من ثانية لملفات PSD ذات الحجم العادي على الأجهزة الحديثة.

## ما هو ضبط تباين الصورة؟
ضبط التباين يغيّر النطاق اللوني للصورة، معززًا الفارق بين المناطق الفاتحة والداكنة. يكون ذلك مفيدًا خاصةً عندما تبدو الصور مسطحة بعد المسح أو عند إعداد الرسومات للطباعة.

## لماذا نستخدم Aspose.PSD للـ Java؟
- **دعم صيغ غني** – افتح، حرّر، و**احفظ الصورة كـ TIFF**، PNG، JPEG والعديد غيرها.  
- **أداء عالي** – التخزين المؤقت وتحسينات صور الراستر تقلل من استهلاك الذاكرة، وهو أمر حاسم لملفات PSD الكبيرة.  
- **واجهة برمجة تطبيقات بسيطة** – استدعاءات طريقة واحدة مثل `adjustContrast` تجعل الكود سهل القراءة والصيانة.  
- **قدرات شاملة لمعالجة الصور في Java** تناسب كل من السكريبتات البسيطة وتطبيقات المؤسسات.

## المتطلبات المسبقة

قبل البدء، تأكد من وجود:

- معرفة أساسية ببرمجة Java.  
- مكتبة Aspose.PSD للـ Java مثبتة. يمكنك تنزيلها [هنا](https://releases.aspose.com/psd/java/).

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

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// Load an existing image into an instance of RasterImage class
Image image = Image.load(sourceFile);
```

نقوم بتحميل ملف PSD المصدر (`sample.psd`) إلى كائن `Image`، والذي يُعد نقطة الدخول لجميع عمليات المعالجة اللاحقة.

## الخطوة 2: تحويل إلى RasterImage وتخزين البيانات مؤقتًا

```java
// Cast object of Image to RasterImage
RasterImage rasterImage = (RasterImage)image;

// Check if RasterImage is cached and Cache RasterImage for better performance
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

التحويل إلى `RasterImage` يمنحنا إمكانية الوصول إلى عمليات على مستوى البكسل. التخزين المؤقت يحسن الأداء، خاصةً للملفات الكبيرة.

## كيفية ضبط تباين الصورة

```java
// Adjust the contrast
rasterImage.adjustContrast(50);
```

طريقة `adjustContrast` تأخذ عددًا صحيحًا يمثل نسبة التغيير. في هذا المثال نقوم بزيادة التباين بنسبة **50 %**.

## تحويل PSD إلى TIFF باستخدام Aspose.PSD

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

هنا نقوم بتكوين `TiffOptions` (عدد البتات لكل عينة، تفسير الفوتومتري) و**حفظ الصورة كـ TIFF**. هذه الخطوة تُكمل سير عمل **تحويل PSD إلى TIFF**.

## المشكلات الشائعة والحلول
- **الصورة غير مخزنة مؤقتًا:** احرص دائمًا على استدعاء `cacheData()` للملفات الكبيرة لتجنب `OutOfMemoryError`.  
- **تحول غير متوقع في الألوان:** تأكد من أن `setPhotometric` يتطابق مع مساحة اللون المستهدفة (RGB مقابل CMYK).  
- **الملف غير موجود:** تحقق من أن `dataDir` يشير إلى المجلد الصحيح وأن اسم الملف مكتوب بشكل صحيح.

## الأسئلة المتكررة

### س1: هل Aspose.PSD متوافق مع صيغ صور مختلفة؟

ج1: نعم، يدعم Aspose.PSD صيغ صور متعددة، مما يوفر مرونة في مشاريعك.

### س2: كيف يمكنني الحصول على ترخيص مؤقت لـ Aspose.PSD؟

ج2: يمكنك الحصول على ترخيص مؤقت [هنا](https://purchase.aspose.com/temporary-license/).

### س3: أين يمكنني العثور على وثائق Aspose.PSD؟

ج3: الوثائق متاحة [هنا](https://reference.aspose.com/psd/java/).

### س4: ما هي خيارات الدعم المتاحة لـ Aspose.PSD؟

ج4: للحصول على الدعم، زر منتدى [Aspose.PSD](https://forum.aspose.com/c/psd/34).

### س5: هل يمكنني شراء Aspose.PSD؟

ج5: نعم، يمكنك شراء Aspose.PSD [هنا](https://purchase.aspose.com/buy).

## الخلاصة

الآن تعرف **كيفية تحويل PSD إلى TIFF** وإجراء **ضبط تباين الصورة** باستخدام Aspose.PSD للـ Java. تمنحك هذه الخطوات تحكمًا دقيقًا في جودة الصورة مع الحفاظ على نظافة الكود وسهولة صيانته. لا تتردد في تجربة طرق ضبط أخرى مثل `adjustBrightness` أو `adjustGamma` لتلبية احتياجاتك الخاصة.

---

**آخر تحديث:** 2026-02-25  
**تم الاختبار مع:** Aspose.PSD للـ Java 24.12  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}