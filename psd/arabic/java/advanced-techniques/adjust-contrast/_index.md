---
title: ضبط تباين الصورة باستخدام Aspose.PSD لـ Java
linktitle: ضبط تباين الصورة
second_title: Aspose.PSD جافا API
description: استكشف عالم تعديل تباين الصورة في Java باستخدام Aspose.PSD. اتبع دليلنا خطوة بخطوة لمعالجة الصور بسلاسة.
type: docs
weight: 22
url: /ar/java/advanced-techniques/adjust-contrast/
---
## مقدمة

في مجال معالجة الصور باستخدام Java، يبرز Aspose.PSD كأداة قوية. من بين ميزاته التي لا تعد ولا تحصى، يعد ضبط تباين الصورة مطلبًا شائعًا. سيرشدك هذا البرنامج التعليمي خلال عملية ضبط تباين الصورة باستخدام Aspose.PSD لـ Java. سواء كنت مطورًا متمرسًا أو بدأت للتو، سيساعدك هذا الدليل على إتقان هذا الجانب الأساسي من معالجة الصور.

## المتطلبات الأساسية

قبل الغوص في البرنامج التعليمي، تأكد من توفر المتطلبات الأساسية التالية:

- الفهم الأساسي لبرمجة جافا.
-  تم تثبيت Aspose.PSD لمكتبة Java. يمكنك تنزيله[هنا](https://releases.aspose.com/psd/java/).

## حزم الاستيراد

للبدء، تحتاج إلى استيراد الحزم الضرورية إلى مشروع Java الخاص بك. أضف الأسطر التالية إلى الكود الخاص بك:

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

// قم بتحميل صورة موجودة في مثيل لفئة RasterImage
Image image = Image.load(sourceFile);
```

 في هذه الخطوة، نقوم بتحميل الصورة النموذجية ("sample.psd") باستخدام الملف`Image.load` طريقة.

## الخطوة 2: الإرسال إلى RasterImage وبيانات ذاكرة التخزين المؤقت

```java
// إرسال كائن الصورة إلى RasterImage
RasterImage rasterImage = (RasterImage)image;

// تحقق مما إذا تم تخزين RasterImage مؤقتًا وذاكرة التخزين المؤقت RasterImage للحصول على أداء أفضل
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

 هنا، نلقي العام`Image` يعترض على أ`RasterImage` لمعالجة محددة. يؤدي التخزين المؤقت لبيانات الصورة إلى تحسين الأداء.

## الخطوة 3: ضبط التباين

```java
// ضبط التباين
rasterImage.adjustContrast(50);
```

 ال`adjustContrast`يتم استخدام الطريقة لتعديل تباين الصورة. في هذا المثال، يتم زيادة التباين بنسبة 50%.

## الخطوة 4: إنشاء TiffOptions وحفظها

```java
// قم بإنشاء مثيل TiffOptions للصورة الناتجة
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
int[] ushort = { 8, 8, 8 };
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);

// احفظ الصورة الناتجة بتنسيق TIFF
String destName = dataDir + "AdjustContrast_out.tiff";
rasterImage.save(destName, tiffOptions);
```

 هنا، أنشأنا`TiffOptions` للصورة الناتجة، مع تحديد التنسيق والخصائص الأخرى. يتم بعد ذلك حفظ الصورة النهائية في ملف TIFF.

## خاتمة

تهانينا! لقد نجحت في ضبط تباين الصورة باستخدام Aspose.PSD لـ Java. غطى هذا البرنامج التعليمي الخطوات الأساسية، بدءًا من استيراد الحزم وحتى حفظ الصورة المعالجة.

## الأسئلة الشائعة

### س1: هل Aspose.PSD متوافق مع تنسيقات الصور المختلفة؟

ج1: نعم، يدعم Aspose.PSD تنسيقات الصور المختلفة، مما يوفر المرونة في مشروعاتك.

### س2: كيف يمكنني الحصول على ترخيص مؤقت لـ Aspose.PSD؟

 ج2: يمكنك الحصول على ترخيص مؤقت[هنا](https://purchase.aspose.com/temporary-license/).

### س3: أين يمكنني العثور على وثائق Aspose.PSD؟

ج3: الوثائق متاحة[هنا](https://reference.aspose.com/psd/java/).

### س4: ما هي خيارات الدعم المتوفرة لـ Aspose.PSD؟

 ج4: للحصول على الدعم، قم بزيارة[منتدى Aspose.PSD](https://forum.aspose.com/c/psd/34).

### س5: هل يمكنني شراء Aspose.PSD؟

 ج5: نعم، يمكنك شراء Aspose.PSD[هنا](https://purchase.aspose.com/buy).