---
title: تنفيذ ضبط التباين في Aspose.PSD لـ .NET
linktitle: تنفيذ تعديل التباين
second_title: Aspose.PSD.NET API
description: تعرف على كيفية تنفيذ ضبط التباين في Aspose.PSD لـ .NET باستخدام هذا الدليل التفصيلي خطوة بخطوة.
type: docs
weight: 11
url: /ar/net/image-adjustment/contrast-adjustment/
---
## مقدمة

مرحبًا بك في هذا الدليل الشامل حول تنفيذ ضبط التباين في Aspose.PSD لـ .NET! في هذا البرنامج التعليمي، سنستكشف عملية تحسين تباين الصورة باستخدام Aspose.PSD، وهي مكتبة تصوير NET قوية. بحلول نهاية هذا الدليل، سيكون لديك فهم قوي لكيفية تطبيق تعديلات التباين على صورك بسلاسة.

## المتطلبات الأساسية

قبل أن نتعمق في العملية خطوة بخطوة، تأكد من توفر المتطلبات الأساسية التالية:

1.  Aspose.PSD لمكتبة .NET: قم بتنزيل وتثبيت Aspose.PSD لمكتبة .NET. يمكنك العثور على رابط التحميل[هنا](https://releases.aspose.com/psd/net/).

2. دليل المستندات: قم بإعداد دليل حيث سيتم تخزين ملفات المصدر والوجهة الخاصة بك. استبدل "دليل المستندات الخاص بك" في الكود المقدم بالمسار إلى هذا الدليل.

والآن بعد أن انتهينا من متطلباتنا الأساسية، فلنبدأ في التنفيذ.

## استيراد مساحات الأسماء

في هذه الخطوة، سنقوم باستيراد مساحات الأسماء الضرورية للوصول إلى الوظائف التي توفرها مكتبة Aspose.PSD.

```csharp
using Aspose.PSD.FileFormats.Tiff.Enums;
using Aspose.PSD.ImageOptions;
```

## الخطوة 1: تحميل الصورة

قم بتحميل الصورة المصدر في مثيل`RasterImage` فصل.

```csharp
//ExStart:تحميل الصورة
string sourceFile = dataDir + @"sample.psd";
using (var image = Image.Load(sourceFile))
{
    RasterImage rasterImage = (RasterImage)image;
    if (!rasterImage.IsCached)
    {
        rasterImage.CacheData();
    }
    // انتقل إلى الخطوة التالية...
}
//ExEnd:LoadImage
```

## الخطوة 2: ضبط التباين

في هذه الخطوة، سنقوم بضبط تباين الصورة المحملة.

```csharp
//ExStart:ضبط التباين
rasterImage.AdjustContrast(50); // ضبط التباين بنسبة 50%
// انتقل إلى الخطوة التالية...
//ExEnd:ضبط التباين
```

## الخطوة 3: إنشاء خيارات TIFF

 إنشاء مثيل ل`TiffOptions` بالنسبة للصورة الناتجة، قم بتعيين خصائص مختلفة، واحفظ الصورة بتنسيق TIFF.

```csharp
//ExStart:CreateTiffOptions
string destName = dataDir + @"AdjustContrast_out.tiff";
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.BitsPerSample = new ushort[] { 8, 8, 8 };
tiffOptions.Photometric = TiffPhotometrics.Rgb;
rasterImage.Save(destName, tiffOptions);
//ExEnd:CreateTiffOptions
```

تهانينا! لقد نجحت في تنفيذ ضبط التباين باستخدام Aspose.PSD لـ .NET.

## خاتمة

في هذا البرنامج التعليمي، استكشفنا عملية تحسين تباين الصورة باستخدام Aspose.PSD لـ .NET. توفر المكتبة طريقة مباشرة لمعالجة خصائص الصورة، مما يسمح للمطورين بإنشاء صور جذابة بصريًا دون عناء.

## الأسئلة الشائعة

### س1: هل Aspose.PSD for .NET مناسب للمبتدئين؟

ج1: تم تصميم Aspose.PSD for .NET ليكون ملائمًا للمطورين، مما يجعله مناسبًا لكل من المطورين المبتدئين وذوي الخبرة.

### س2: هل يمكنني استخدام Aspose.PSD للمشاريع التجارية؟

 ج2: نعم، يمكن استخدام Aspose.PSD لـ .NET في المشاريع التجارية. للحصول على تفاصيل الترخيص، قم بزيارة[هنا](https://purchase.aspose.com/buy).

### س3: هل هناك نسخة تجريبية مجانية متاحة؟

 ج3: نعم، يمكنك استكشاف النسخة التجريبية المجانية من Aspose.PSD لـ .NET.[هنا](https://releases.aspose.com/).

### س 4: أين يمكنني العثور على دعم لـ Aspose.PSD لـ .NET؟

 ج4: قم بزيارة منتدى دعم Aspose.PSD لـ .NET[هنا](https://forum.aspose.com/c/psd/34) للمساعدة.

### س5: كيف يمكنني الحصول على ترخيص مؤقت؟

 ج5: إذا لزم الأمر، يمكنك الحصول على ترخيص مؤقت.[هنا](https://purchase.aspose.com/temporary-license/).