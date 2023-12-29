---
title: تطبيق مرشحات Median وWiener في الصور الملونة باستخدام Aspose.PSD لـ .NET
linktitle: تطبيق مرشحات Median وWiener في الصور الملونة باستخدام Aspose.PSD لـ .NET
second_title: Aspose.PSD.NET API
description: قم بتحسين الصور الملونة وتقليل التشويش باستخدام Aspose.PSD لـ .NET باستخدام مرشحات Median وWiener. دليل خطوة بخطوة لمعالجة الصور بسلاسة.
type: docs
weight: 11
url: /ar/net/image-processing/apply-median-wiener-filters-color-images/
---
## مقدمة

مرحبًا بك في هذا الدليل التفصيلي حول تطبيق مرشحات Median وWiener في الصور الملونة باستخدام Aspose.PSD لـ .NET. Aspose.PSD هي مكتبة قوية تمكن مطوري .NET من العمل مع ملفات PSD بسلاسة. في هذا البرنامج التعليمي، سوف نستكشف عملية تطبيق مرشحات Median وWiener لتحسين الصور الملونة وتقليل التشويش عليها.

## المتطلبات الأساسية

قبل أن نتعمق في البرنامج التعليمي، تأكد من توفر المتطلبات الأساسية التالية:

-  Aspose.PSD لـ .NET: تأكد من تثبيت مكتبة Aspose.PSD. يمكنك تنزيله من[Aspose.PSD لوثائق .NET](https://reference.aspose.com/psd/net/).

- صورة نموذجية: قم بإعداد نموذج لملف صورة PSD الذي تريد تقليل التشويش فيه. إذا لم يكن لديك واحد، يمكنك استخدام العينة الخاصة بك أو تنزيلها من أي مصدر موثوق.

- بيئة التطوير: قم بإعداد بيئة تطوير .NET، مثل Visual Studio، لتنفيذ مقتطفات التعليمات البرمجية المتوفرة.

## استيراد مساحات الأسماء

في مشروع .NET الخاص بك، قم باستيراد مساحات الأسماء الضرورية للوصول إلى الوظائف التي يوفرها Aspose.PSD:

```csharp
using Aspose.PSD.ImageFilters.FilterOptions;
using Aspose.PSD.ImageOptions;
```

## الخطوة 1: قم بتحميل الصورة المزعجة

أولاً، قم بتحميل الصورة المزعجة من الملف المصدر. تأكد من استبدال "دليل المستندات الخاص بك" بالمسار الفعلي لدليل المستندات الخاص بك:

```csharp
// المسار إلى دليل المستندات.
string dataDir = "Your Document Directory";

//تحميل الصورة الصاخبة
string sourceFile = dataDir + @"sample.psd";
string destName = dataDir + @"median_test_denoise_out.gif";

using (Image image = Image.Load(sourceFile))
{
    // سيتم وضع رمز إضافي للمعالجة هنا
}
```

## الخطوة 2: إرسال الصورة إلى RasterImage

تحويل الصورة المحملة إلى صورة نقطية:

```csharp
RasterImage rasterImage = image as RasterImage;
if (rasterImage == null)
{
    return; // تعامل مع الحالة التي لا يمكن فيها تحويل الصورة إلى RasterImage
}
```

## الخطوة 3: تطبيق عامل التصفية المتوسط

 إنشاء مثيل لـ`MedianFilterOptions` فئة، قم بتعيين الحجم، وتطبيق عامل التصفية المتوسط على كائن RasterImage، وحفظ الصورة الناتجة:

```csharp
MedianFilterOptions options = new MedianFilterOptions(4);
rasterImage.Filter(image.Bounds, options);
image.Save(destName, new GifOptions());
```

## خاتمة

تهانينا! لقد نجحت في تطبيق مرشحات Median وWiener لتقليل تشويش الصور الملونة باستخدام Aspose.PSD لـ .NET. تفتح هذه المكتبة القوية عالمًا من الإمكانيات لمعالجة الصور في تطبيقات .NET الخاصة بك.

## الأسئلة الشائعة

### س1: هل يمكنني تطبيق هذه المرشحات على تنسيقات صور أخرى إلى جانب PSD؟

ج1: نعم، يدعم Aspose.PSD تنسيقات الصور المختلفة، مما يسمح لك بتطبيق عوامل التصفية على نطاق واسع من الصور.

### س2: كيف يمكنني التعامل مع الاستثناءات أثناء معالجة الصور؟

ج2: يمكنك تطبيق كتل محاولة الالتقاط لمعالجة الاستثناءات التي قد تحدث أثناء معالجة الصور باستخدام Aspose.PSD.

### س3: هل هناك نسخة تجريبية مجانية متاحة لـ Aspose.PSD لـ .NET؟

ج3: نعم، يمكنك استكشاف ميزات Aspose.PSD عن طريق الحصول على نسخة تجريبية مجانية من[هنا](https://releases.aspose.com/).

### س4: أين يمكنني العثور على الدعم المجتمعي لـ Aspose.PSD؟

 ج4: للحصول على دعم المجتمع والمناقشات، قم بزيارة[منتديات Aspose.PSD](https://forum.aspose.com/c/psd/34).

### س5: كيف يمكنني الحصول على ترخيص مؤقت لـ Aspose.PSD؟

 ج5: يمكنك الحصول على ترخيص مؤقت من[هنا](https://purchase.aspose.com/temporary-license/).