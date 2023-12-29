---
title: تنفيذ تعديل جاما في Aspose.PSD لـ .NET
linktitle: تنفيذ تعديل غاما
second_title: Aspose.PSD.NET API
description: اكتشف قوة Aspose.PSD لـ .NET من خلال دليلنا خطوة بخطوة حول تنفيذ ضبط Gamma. ضبط سطوع الصورة وتباينها بسهولة.
type: docs
weight: 12
url: /ar/net/image-adjustment/gamma-adjustment/
---
## مقدمة

مرحبًا بك في هذا الدليل الشامل حول تنفيذ ضبط Gamma في Aspose.PSD لـ .NET! يعد ضبط جاما تقنية مهمة لمعالجة الصور تسمح لك بضبط سطوع الصورة وتباينها. في هذا البرنامج التعليمي، سنرشدك خلال العملية باستخدام مكتبة Aspose.PSD القوية لـ .NET.

## المتطلبات الأساسية

قبل الغوص في التنفيذ، تأكد من توفر المتطلبات الأساسية التالية:

-  Aspose.PSD لمكتبة .NET: تأكد من تثبيت مكتبة Aspose.PSD لـ .NET. يمكنك تنزيله[هنا](https://releases.aspose.com/psd/net/).

- .NET Framework: يفترض هذا البرنامج التعليمي أن لديك فهمًا أساسيًا لتطوير .NET وأنك قمت بتثبيت .NET Framework.

- بيئة التطوير المتكاملة (IDE): اختر بيئة التطوير المتكاملة (IDE) المفضلة لديك لتطوير .NET، مثل Visual Studio.

## استيراد مساحات الأسماء

في مشروع .NET الخاص بك، ابدأ باستيراد مساحات الأسماء الضرورية للعمل مع Aspose.PSD:

```csharp
using Aspose.PSD.FileFormats.Tiff.Enums;
using Aspose.PSD.ImageOptions;
```

## الخطوة 1: قم بإعداد مشروعك

قم بإنشاء مشروع .NET جديد في بيئة التطوير المتكاملة (IDE) التي اخترتها. تأكد من إضافة مراجع إلى مكتبة Aspose.PSD.

## الخطوة 2: تحديد دليل المستندات

```csharp
string dataDir = "Your Document Directory";
```

## الخطوة 3: تحميل الصورة

```csharp
string sourceFile = dataDir + @"sample.psd";
using (var image = Image.Load(sourceFile))
{
    // سيتم تنفيذ خطوات إضافية داخل هذه الكتلة باستخدام.
}
```

## الخطوة 4: الإرسال إلى RasterImage وبيانات ذاكرة التخزين المؤقت

```csharp
RasterImage rasterImage = (RasterImage)image;
if (!rasterImage.IsCached)
{
    rasterImage.CacheData();
}
```

## الخطوة 5: ضبط جاما

```csharp
rasterImage.AdjustGamma(2.2f, 2.2f, 2.2f);
```

## الخطوة 6: إنشاء TiffOptions وحفظها

```csharp
string destName = dataDir + @"AdjustGamma_out.tiff";
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.BitsPerSample = new ushort[] { 8, 8, 8 };
tiffOptions.Photometric = TiffPhotometrics.Rgb;
rasterImage.Save(destName, tiffOptions);
```

## خاتمة

تهانينا! لقد قمت بنجاح بتنفيذ ضبط Gamma باستخدام Aspose.PSD لـ .NET. توفر هذه المكتبة القوية إمكانات قوية لمعالجة الصور، مما يجعلها أداة قيمة لمطوري .NET.

## الأسئلة الشائعة

### س1: أين يمكنني العثور على وثائق Aspose.PSD؟

 ج1: يمكنك الرجوع إلى الوثائق[هنا](https://reference.aspose.com/psd/net/).

### س2: كيف يمكنني تنزيل Aspose.PSD لـ .NET؟

 ج2: يمكنك تنزيل المكتبة[هنا](https://releases.aspose.com/psd/net/).

### س3: هل هناك نسخة تجريبية مجانية متاحة؟

 ج3: نعم، يمكنك الحصول على نسخة تجريبية مجانية[هنا](https://releases.aspose.com/).

### س4: أين يمكنني الحصول على الدعم لـ Aspose.PSD؟

 ج4: يمكنك زيارة منتدى الدعم[هنا](https://forum.aspose.com/c/psd/34).

### س5: هل أحتاج إلى ترخيص مؤقت؟

 ج5: إذا لزم الأمر، يمكنك الحصول على ترخيص مؤقت[هنا](https://purchase.aspose.com/temporary-license/).