---
date: 2025-12-21
description: تعلم كيفية ضبط تباين الصور باستخدام Aspose.PSD للـ Java، مكتبة معالجة
  الصور الرائدة في Java، وتحويل ملفات PSD إلى TIFF بكفاءة.
linktitle: Adjust Contrast of an Image
second_title: Aspose.PSD Java API
title: كيفية تعديل تباين صورة باستخدام Aspose.PSD للـ Java
url: /ar/java/advanced-techniques/adjust-contrast/
weight: 22
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# كيفية تعديل التباين لصورة باستخدام Aspose.PSD for Java

## مقدمة

إذا كنت تبحث عن **how to adjust contrast** في مشاريع Java الخاصة بك، فقد وجدت المكان المناسب. Aspose.PSD for Java هي مكتبة **java image manipulation library** قوية تتيح لك ضبط خصائص الصورة مثل التباين والسطوع والمزيد. في هذا البرنامج التعليمي سنستعرض الخطوات الدقيقة لرفع تباين ملف PSD ثم **convert PSD to TIFF** لتدفقات العمل اللاحقة.

## إجابات سريعة
- **What does “adjust contrast” mean?** يغيّر الفرق بين أغمق وأفتح البكسلات، مما يجعل التفاصيل تبرز.
- **Which library handles this?** Aspose.PSD for Java – مجموعة أدوات معالجة صور متكاملة.
- **Do I need a license?** ترخيص مؤقت يعمل للاختبار؛ ترخيص كامل مطلوب للإنتاج.
- **Can I save the result as TIFF?** نعم، سنستخدم `TiffOptions` لتصدير الصورة المعالجة.
- **How long does the code take to run?** عادةً أقل من ثانية لملفات PSD ذات الحجم القياسي.

## ما هو تعديل التباين؟

تعديل التباين يغيّر النطاق اللوني للصورة، معززًا الفارق بين المناطق الفاتحة والداكنة. يكون ذلك مفيدًا بشكل خاص عندما تبدو الصور مسطحة بعد المسح أو عند إعداد الرسومات للطباعة.

## لماذا تستخدم Aspose.PSD for Java؟

- **Rich format support** – افتح، حرّر، واحفظ PSD، TIFF، PNG، JPEG والعديد غيرها.
- **High performance** – التخزين المؤقت وتحسينات الصور النقطية تقلل من استهلاك الذاكرة.
- **Straight‑forward API** – استدعاءات طريقة واحدة مثل `adjustContrast` تجعل الكود سهل القراءة.

## المتطلبات المسبقة

قبل البدء، تأكد من أن لديك:

- معرفة أساسية ببرمجة Java.
- مكتبة Aspose.PSD for Java مثبتة. يمكنك تنزيلها [here](https://releases.aspose.com/psd/java/).

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

نقوم بتحميل ملف PSD المصدر (`sample.psd`) إلى كائن `Image`، والذي يعمل كنقطة الدخول لجميع المعالجات اللاحقة.

## الخطوة 2: التحويل إلى RasterImage وتخزين البيانات مؤقتًا

```java
// Cast object of Image to RasterImage
RasterImage rasterImage = (RasterImage)image;

// Check if RasterImage is cached and Cache RasterImage for better performance
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

التحويل إلى `RasterImage` يمنحنا إمكانية الوصول إلى عمليات على مستوى البكسل. التخزين المؤقت يحسن الأداء، خاصةً للملفات الكبيرة.

## كيفية تعديل تباين الصورة

```java
// Adjust the contrast
rasterImage.adjustContrast(50);
```

طريقة `adjustContrast` تأخذ عددًا صحيحًا يمثل نسبة التغيير. في هذا المثال نزيد التباين بنسبة **50 %**.

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

هنا نقوم بتكوين `TiffOptions` (عدد البتات لكل عينة، التفسير الضوئي) ونكتب الصورة المعززة بالتباين إلى ملف TIFF.

## المشكلات الشائعة والحلول
- **Image not cached:** احرص دائمًا على استدعاء `cacheData()` للـ PSD الكبيرة لتجنب `OutOfMemoryError`.
- **Unexpected color shift:** تحقق من أن `setPhotometric` يتطابق مع مساحة اللون المستهدفة (RGB مقابل CMYK).
- **File not found:** تأكد من أن `dataDir` يشير إلى المجلد الصحيح وأن اسم الملف مكتوب بشكل صحيح.

## الأسئلة المتكررة

### س1: هل Aspose.PSD متوافق مع صيغ صور مختلفة؟

A1: نعم، يدعم Aspose.PSD صيغ صور متعددة، مما يوفر مرونة في مشاريعك.

### س2: كيف يمكنني الحصول على ترخيص مؤقت لـ Aspose.PSD؟

A2: يمكنك الحصول على ترخيص مؤقت [here](https://purchase.aspose.com/temporary-license/).

### س3: أين يمكنني العثور على وثائق Aspose.PSD؟

A3: الوثائق متاحة [here](https://reference.aspose.com/psd/java/).

### س4: ما هي خيارات الدعم المتاحة لـ Aspose.PSD؟

A4: للدعم، زر [Aspose.PSD forum](https://forum.aspose.com/c/psd/34).

### س5: هل يمكنني شراء Aspose.PSD؟

A5: نعم، يمكنك شراء Aspose.PSD [here](https://purchase.aspose.com/buy).

## الخلاصة

أنت الآن تعرف **how to adjust contrast** لصورة PSD باستخدام Aspose.PSD for Java وكيفية **convert PSD to TIFF** للمعالجة الإضافية. هذه الخطوات تمنحك تحكمًا دقيقًا في جودة الصورة مع الحفاظ على شفافية وصيانة الكود. لا تتردد في تجربة طرق تعديل صور أخرى مثل `adjustBrightness` أو `adjustGamma` لتلبية احتياجاتك الخاصة.

---

**آخر تحديث:** 2025-12-21  
**تم الاختبار مع:** Aspose.PSD for Java 24.12  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}