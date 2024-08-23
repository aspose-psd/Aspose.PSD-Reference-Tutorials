---
title: اضبط جاما الصورة باستخدام Aspose.PSD لـ Java
linktitle: ضبط جاما الصورة
second_title: Aspose.PSD جافا API
description: تعلم كيفية ضبط جاما الصورة بسهولة باستخدام Aspose.PSD لـ Java. اتبع دليلنا خطوة بخطوة للحصول على أفضل النتائج.
type: docs
weight: 23
url: /ar/java/advanced-techniques/adjust-gamma/
---
## مقدمة

في مجال معالجة الصور، يعد ضبط جاما الصورة خطوة حاسمة لتعزيز جاذبيتها البصرية. يوفر Aspose.PSD for Java حلاً قويًا لمطوري Java لمعالجة جاما الصور دون عناء. في هذا البرنامج التعليمي، سنستكشف كيفية ضبط جاما باستخدام Aspose.PSD، مع تفصيل كل خطوة لضمان التنفيذ السلس.

## المتطلبات الأساسية

قبل الغوص في البرنامج التعليمي، تأكد من إعداد المتطلبات الأساسية التالية:

1. بيئة تطوير Java: تأكد من تثبيت بيئة تطوير Java على نظامك.
2.  مكتبة Aspose.PSD: قم بتنزيل مكتبة Aspose.PSD ودمجها في مشروع Java الخاص بك. يمكنك العثور على الموارد اللازمة في[الوثائق](https://reference.aspose.com/psd/java/).
3. صورة نموذجية: قم بإعداد نموذج لصورة PSD التي ستستخدمها لتطبيق ضبط جاما.

## حزم الاستيراد

لبدء العملية، قم باستيراد الحزم المطلوبة في مشروع Java الخاص بك. وهذا يمهد الطريق لاستخدام وظائف Aspose.PSD بسلاسة.

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

## الخطوة 1: تحميل الصورة

 ابدأ بتحميل نموذج صورة PSD إلى مثيل ملف`RasterImage` فصل. وهذا هو الأساس لتعديلات جاما اللاحقة.

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// قم بتحميل صورة موجودة في مثيل لفئة RasterImage
Image image = Image.load(sourceFile);

// إرسال كائن الصورة إلى RasterImage
RasterImage rasterImage = (RasterImage)image;

// تحقق مما إذا تم تخزين RasterImage مؤقتًا للحصول على أداء أفضل
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

## الخطوة 2: ضبط جاما

 الآن، قم بضبط جاما الصورة المحملة باستخدام`adjustGamma` طريقة. قم بضبط قيم جاما وفقًا لمتطلباتك.

```java
// ضبط جاما
rasterImage.adjustGamma(2.2f, 2.2f, 2.2f);
```

## الخطوة 3: إنشاء TiffOptions

 إنشاء مثيل ل`TiffOptions` للصورة الناتجة. قم بتعيين خصائص مختلفة، مثل البتات لكل عينة وخيارات القياس الضوئي، لتخصيص الإخراج وفقًا لمواصفاتك.

```java
// قم بإنشاء مثيل TiffOptions للصورة الناتجة
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
int[] ushort = { 8, 8, 8 };
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);
```

## الخطوة 4: احفظ الصورة الناتجة

 احفظ الصورة التي تم التلاعب بها بتنسيق TIFF باستخدام التنسيق المحدد مسبقًا`TiffOptions`.

```java
// احفظ الصورة الناتجة بتنسيق TIFF
String destName = dataDir + "AdjustGamma_out.tiff";
rasterImage.save(destName, tiffOptions);
```

## خاتمة

تهانينا! لقد نجحت في ضبط جاما الصورة باستخدام Aspose.PSD لـ Java. تعمل هذه العملية على تمكين المطورين من تحسين جودة الصورة دون عناء، مما يساهم في توفير تجربة مستخدم جذابة بصريًا.

## الأسئلة الشائعة

### س1: أين يمكنني العثور على وثائق Aspose.PSD؟

 ج1: يمكنك الوصول إلى الوثائق على[https://reference.aspose.com/psd/Java/](https://reference.aspose.com/psd/java/).

### س2: كيف يمكنني تنزيل Aspose.PSD لـ Java؟

 ج2: قم بتحميل المكتبة من[https://releases.aspose.com/psd/Java/](https://releases.aspose.com/psd/java/).

### س3: أين يمكنني شراء Aspose.PSD؟

 ج3: زيارة[https://purchase.aspose.com/buy](https://purchase.aspose.com/buy) لشراء Aspose.PSD.

### س4: هل هناك نسخة تجريبية مجانية متاحة؟

 ج4: نعم، يمكنك استكشاف النسخة التجريبية المجانية على[https://releases.aspose.com/](https://releases.aspose.com/).

### س5: أين يمكنني طلب الدعم لـ Aspose.PSD؟

 ج5: للحصول على الدعم، قم بزيارة منتدى Aspose.PSD على[https://forum.aspose.com/c/psd/34](https://forum.aspose.com/c/psd/34).