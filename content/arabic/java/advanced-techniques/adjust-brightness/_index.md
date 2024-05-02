---
title: ضبط سطوع الصورة باستخدام Aspose.PSD لـ Java
linktitle: ضبط سطوع الصورة
second_title: Aspose.PSD جافا API
description: قم بتحسين سطوع الصورة في Java باستخدام Aspose.PSD. دليل خطوة بخطوة لضبط سطوع الصورة برمجياً.
type: docs
weight: 21
url: /ar/java/advanced-techniques/adjust-brightness/
---
## مقدمة

يعد تحسين الصور متطلبًا شائعًا في التصميم الجرافيكي والتصوير الرقمي. يوفر Aspose.PSD for Java حلاً قويًا لضبط سطوع الصورة برمجيًا. في هذا البرنامج التعليمي، سوف نستكشف كيفية استخدام Aspose.PSD لمكتبة Java لضبط سطوع الصورة، خطوة بخطوة.

## المتطلبات الأساسية

قبل الغوص في البرنامج التعليمي، تأكد من أن لديك المتطلبات الأساسية التالية:

-  Aspose.PSD لمكتبة Java: قم بتنزيل المكتبة وتثبيتها من ملف[Aspose.PSD لوثائق جافا](https://reference.aspose.com/psd/java/).

## حزم الاستيراد

للبدء، قم باستيراد الحزم الضرورية إلى مشروع Java الخاص بك. في هذا المثال سنستخدم ما يلي:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

الآن، دعونا نقسم عملية ضبط سطوع الصورة إلى خطوات بسيطة:

## الخطوة 1: تحميل الصورة

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "AdjustBrightness_out.tiff";

// قم بتحميل صورة موجودة في مثيل لفئة RasterImage
Image image = Image.load(sourceFile);
// إرسال كائن الصورة إلى RasterImage
RasterImage rasterImage = (RasterImage) image;

// تحقق مما إذا تم تخزين RasterImage مؤقتًا وذاكرة التخزين المؤقت RasterImage للحصول على أداء أفضل
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

 في هذه الخطوة، نقوم بتحميل الصورة المستهدفة ونقلها إلى ملف`RasterImage` لمزيد من المعالجة.

## الخطوة 2: ضبط السطوع

```java
// ضبط السطوع
rasterImage.adjustBrightness(-50);
```

 وهنا نستخدم`adjustBrightness`طريقة تعديل سطوع الصورة. في هذا المثال، قمنا بتقليل السطوع بمقدار 50 وحدة، ولكن يمكنك تخصيص هذه القيمة بناءً على متطلباتك.

## الخطوة 3: قم بتعيين خيارات Tiff

```java
int[] ushort = {8, 8, 8};
// قم بإنشاء مثيل TiffOptions للصورة الناتجة
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);
```

 تكوين`TiffOptions` لحفظ الصورة المعدلة. أضبط ال`bitsPerSample` و`photometric` خصائص بناء على احتياجاتك المحددة.

## الخطوة 4: احفظ الصورة الناتجة

```java
// احفظ الصورة الناتجة
rasterImage.save(destName, tiffOptions);
```

 وأخيرا، احفظ الصورة المعدلة باستخدام المحدد`TiffOptions`.

## خاتمة

أصبح ضبط سطوع الصورة برمجيًا أمرًا سهلاً باستخدام Aspose.PSD لـ Java. قدم هذا البرنامج التعليمي دليلاً شاملاً حول تنفيذ هذه الوظيفة في تطبيقات Java الخاصة بك.

## الأسئلة الشائعة

### س1: هل يمكنني ضبط السطوع في تنسيقات الصور الأخرى إلى جانب PSD؟

ج1: نعم، يدعم Aspose.PSD for Java تنسيقات صور متنوعة مثل JPEG، وPNG، وTIFF.

### س2: كيف يمكنني معالجة الأخطاء أثناء عملية ضبط الصورة؟

ج٢: يمكنك تنفيذ معالجة الأخطاء باستخدام كتل محاولة الالتقاط لإدارة الاستثناءات التي قد تحدث.

### س3: هل هناك حد لنطاق تعديل السطوع؟

ج3: يعتمد نطاق الضبط على محتوى الصورة وتنسيقها، ولكن Aspose.PSD يوفر المرونة في التخصيص.

### س4: هل يمكنني استخدام Aspose.PSD لـ Java في المشاريع التجارية؟

 ج4: نعم، Aspose.PSD for Java هي مكتبة تجارية، ويمكنك الحصول على ترخيص منها[هنا](https://purchase.aspose.com/buy).

### س5: هل هناك نسخة تجريبية مجانية متاحة لـ Aspose.PSD لـ Java؟

 ج5: نعم، يمكنك استكشاف المكتبة من خلال نسخة تجريبية مجانية من[هنا](https://releases.aspose.com/).