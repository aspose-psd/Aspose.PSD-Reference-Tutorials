---
date: 2025-12-19
description: تعلم كيفية ضبط سطوع الصورة باستخدام Aspose.PSD للغة Java. يقدم هذا الدليل
  لتعديل الصور بلغة Java إرشادًا خطوة بخطوة.
linktitle: Adjust Brightness of an Image
second_title: Aspose.PSD Java API
title: كيفية ضبط سطوع صورة باستخدام Aspose.PSD للـ Java
url: /ar/java/advanced-techniques/adjust-brightness/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# ضبط سطوع الصورة باستخدام Aspose.PSD للـ Java

## المقدمة

إذا كنت بحاجة إلى **تعلم كيفية ضبط السطوع** لصورة مباشرةً من كود Java، فأنت في المكان الصحيح. تعديل السطوع هو مهمة شائعة للمصممين الجرافيكيين، المصورين، وأي شخص يبني خطوط معالجة الصور. في هذا **دروس معالجة الصور في Java** سنستعرض سير العمل الكامل — تحميل ملف PSD/TIFF، تطبيق إزاحة سطوع، وحفظ النتيجة — باستخدام مكتبة Aspose.PSD للـ Java.

## إجابات سريعة
- **ما المكتبة التي تتعامل مع السطوع؟** Aspose.PSD for Java  
- **ما الطريقة التي تغير السطوع؟** `RasterImage.adjustBrightness()`  
- **هل يمكنني العمل مع ملفات PSD و TIFF؟** نعم، الـ API يدعم كلا الصيغتين.  
- **هل أحتاج إلى ترخيص للإنتاج؟** الترخيص التجاري مطلوب للاستخدام غير التجريبي.  
- **كم من الوقت تستغرق العملية؟** عادةً أقل من 10 دقائق لضبط أساسي.

## ما هو تعديل سطوع الصورة؟

تعديل سطوع الصورة يغيّر الإضاءة العامة لكل بكسل في الصورة. زيادة السطوع تجعل المناطق الداكنة أكثر إضاءة، بينما تقليل السطوع يجعل الصورة بأكملها أغمق. هذه العملية مفيدة لتصحيح الصور ذات التعرض المنخفض، تحضير الأصول للطباعة، أو إنشاء تأثيرات بصرية في التطبيقات.

## لماذا تستخدم Aspose.PSD للـ Java؟

- **دعم كامل للصيغ** – PSD, TIFF, JPEG, PNG، وأكثر.  
- **بدون تبعيات أصلية خارجية** – Java نقي، سهل التكامل.  
- **تخزين مؤقت عالي الأداء** – يمكن تخزين بيانات الـ raster لتسريع العمليات المتكررة.  
- **API غني** – طرق لتصحيح الألوان، الطبقات، الأقنعة، وغيرها من التعديلات المتقدمة.

## المتطلبات المسبقة

قبل الغوص في الدرس، تأكد من توفر المتطلبات التالية:

- مكتبة Aspose.PSD للـ Java: قم بتنزيل وتثبيت المكتبة من [توثيق Aspose.PSD للـ Java](https://reference.aspose.com/psd/java/).

## استيراد الحزم

لبدء العمل، استورد الحزم اللازمة إلى مشروع Java الخاص بك. في هذا المثال، سنستخدم ما يلي:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

الآن، لنقسم عملية ضبط سطوع الصورة إلى خطوات بسيطة:

## كيفية ضبط السطوع باستخدام Aspose.PSD

### الخطوة 1: تحميل الصورة

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

في هذه الخطوة، نقوم بتحميل الصورة المستهدفة وتحويلها إلى كائن `RasterImage` لمزيد من المعالجة.

### الخطوة 2: ضبط السطوع

```java
// Adjust the brightness
rasterImage.adjustBrightness(-50);
```

هنا، نستخدم طريقة `adjustBrightness` لتعديل سطوع الصورة. في هذا المثال، نقوم بخفض السطوع بمقدار 50 وحدة، لكن يمكنك تخصيص هذه القيمة وفقًا لمتطلباتك.

### الخطوة 3: ضبط TiffOptions

```java
int[] ushort = {8, 8, 8};
// Create an instance of TiffOptions for the resultant image
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);
```

قم بتكوين `TiffOptions` لحفظ الصورة المعدلة. اضبط خصائص `bitsPerSample` و `photometric` بناءً على احتياجاتك الخاصة.

### الخطوة 4: حفظ الصورة الناتجة

```java
// Save the resultant image
rasterImage.save(destName, tiffOptions);
```

أخيرًا، احفظ الصورة المعدلة باستخدام `TiffOptions` المحددة.

## المشكلات الشائعة والحلول

| المشكلة | السبب | الحل |
|---------|-------|------|
| **`ClassCastException` عند تحويل Image** | الملف ليس صورة raster (مثال: PSD متجه). | تحقق من صيغة الملف المصدر أو استخدم `image instanceof RasterImage` قبل التحويل. |
| **تغيير السطوع لا يؤثر** | لم يتم تخزين الصورة مؤقتًا قبل الضبط. | استدعِ `rasterImage.cacheData()` كما هو موضح في الخطوة 1. |
| **الملف المحفوظ يبدو معطوبًا** | إعداد `TiffOptions` غير صحيح. | تأكد من أن `bitsPerSample` يطابق عمق الصورة المصدر (عادةً 8‑بت لكل قناة). |

## الأسئلة المتكررة

### س1: هل يمكنني ضبط السطوع في صيغ صور أخرى غير PSD؟

ج1: نعم، Aspose.PSD للـ Java يدعم صيغ صور متعددة مثل JPEG و PNG و TIFF.

### س2: كيف يمكنني التعامل مع الأخطاء أثناء عملية ضبط الصورة؟

ج2: يمكنك تنفيذ معالجة الأخطاء باستخدام كتل try‑catch لإدارة الاستثناءات التي قد تحدث.

### س3: هل هناك حد لنطاق ضبط السطوع؟

ج3: يعتمد نطاق الضبط على محتوى الصورة وصيغتها، لكن Aspose.PSD يوفر مرونة في التخصيص.

### س4: هل يمكنني استخدام Aspose.PSD للـ Java في المشاريع التجارية؟

ج4: نعم، Aspose.PSD للـ Java مكتبة تجارية، ويمكنك الحصول على ترخيص من [هنا](https://purchase.aspose.com/buy).

### س5: هل يتوفر نسخة تجريبية مجانية لـ Aspose.PSD للـ Java؟

ج5: نعم، يمكنك استكشاف المكتبة بنسخة تجريبية مجانية من [هنا](https://releases.aspose.com/).

### س6: هل تؤثر طريقة `adjustBrightness` على رؤية الطبقات؟

ج6: تعمل الطريقة على الصورة المركبة rasterized، لذا يتم احترام رؤية الطبقات أثناء التحويل إلى raster.

### س7: هل يمكنني ربط تعديلات متعددة (مثل التباين، التشبع) معًا؟

ج7: بالتأكيد. بعد ضبط السطوع، يمكنك استدعاء `adjustContrast`، `adjustSaturation`، إلخ، على نفس كائن `RasterImage`.

**Last Updated:** 2025-12-19  
**تم الاختبار مع:** Aspose.PSD for Java 24.12 (latest at time of writing)  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}