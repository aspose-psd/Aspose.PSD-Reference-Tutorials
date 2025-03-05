---
title: صور ذات تدرج رمادي باستخدام Aspose.PSD لـ .NET
linktitle: صور ذات تدرج رمادي باستخدام Aspose.PSD لـ .NET
second_title: Aspose.PSD.NET API
description: تعرف على كيفية تطبيق تأثيرات التدرج الرمادي على الصور بسهولة باستخدام Aspose.PSD لـ .NET.
type: docs
weight: 14
url: /ar/net/image-processing/grayscaling-images/
---
## مقدمة

مرحبًا بك في برنامجنا التعليمي الشامل حول الصور ذات التدرج الرمادي باستخدام Aspose.PSD لـ .NET! يعد تدرج الرمادي تقنية قوية يمكنها تحسين المظهر المرئي لصورك عن طريق تحويلها إلى ظلال رمادية. في هذا الدليل، سنرشدك خلال عملية تحقيق تأثيرات التدرج الرمادي المذهلة دون عناء.

## المتطلبات الأساسية

قبل أن نتعمق في البرنامج التعليمي، تأكد من توفر المتطلبات الأساسية التالية:

-  Aspose.PSD لـ .NET Library: قم بتنزيل المكتبة وتثبيتها من ملف .NET Library[وثائق Aspose.PSD](https://reference.aspose.com/psd/net/).

- بيئة التطوير: تأكد من إعداد بيئة تطوير .NET صالحة للعمل.

- ملف الصورة: قم بإعداد ملف صورة نموذجي بتنسيق PSD للتدرج الرمادي.

## استيراد مساحات الأسماء

في مشروع .NET الخاص بك، قم باستيراد مساحات الأسماء الضرورية لاستخدام وظائف Aspose.PSD:

```csharp
using Aspose.PSD.ImageOptions;
```

## الخطوة 1: قم بإعداد مشروعك

قم بإنشاء مشروع .NET جديد أو افتح مشروعًا موجودًا في بيئة التطوير المفضلة لديك.

## الخطوة 2: تهيئة Aspose.PSD

قم بتهيئة مكتبة Aspose.PSD في مشروعك عن طريق إضافة الكود التالي:

```csharp
string dataDir = "Your Document Directory";
```

## الخطوة 3: تحميل الصورة

قم بتحميل الصورة النموذجية من مسار الملف المحدد باستخدام الكود التالي:

```csharp
string sourceFile = dataDir + @"sample.psd";
string destName = dataDir + @"Grayscaling_out.jpg";

using (Image image = Image.Load(sourceFile))
{
    // سيتم إضافة رمز إضافي في الخطوات التالية.
}
```

## الخطوة 4: التحقق من الصورة وتخزينها مؤقتًا

تحقق مما إذا كانت الصورة المحملة مخزنة مؤقتًا، وإذا لم يكن الأمر كذلك، فقم بتخزينها مؤقتًا للحصول على أداء أفضل:

```csharp
RasterCachedImage rasterCachedImage = (RasterCachedImage)image;
if (!rasterCachedImage.IsCached)
{
    rasterCachedImage.CacheData();
}
```

## الخطوة 5: التحويل إلى التدرج الرمادي

قم بتحويل الصورة المحملة إلى تمثيلها بالتدرج الرمادي:

```csharp
rasterCachedImage.Grayscale();
```

## الخطوة 6: احفظ الصورة الناتجة

احفظ الصورة ذات التدرج الرمادي بالكود التالي:

```csharp
rasterCachedImage.Save(destName, new JpegOptions());
```

## خاتمة

تهانينا! لقد نجحت في تغيير حجم الصورة إلى اللون الرمادي باستخدام Aspose.PSD لـ .NET. يمكن لهذه العملية المباشرة أن تضيف لمسة من الرقي إلى صورك.

## الأسئلة الشائعة

### س1: هل يمكنني استخدام Aspose.PSD لـ .NET مع تنسيقات الصور الأخرى؟

A1: نعم، يدعم Aspose.PSD تنسيقات الصور المختلفة، بما في ذلك PSD وBMP وPNG وJPEG.

### س2: هل يتوفر ترخيص مؤقت لـ Aspose.PSD لـ .NET؟

 ج2: نعم، يمكنك الحصول على ترخيص مؤقت من[هنا](https://purchase.aspose.com/temporary-license/).

### س3: أين يمكنني العثور على دعم لـ Aspose.PSD لـ .NET؟

 ج3: قم بزيارة[منتدى Aspose.PSD](https://forum.aspose.com/c/psd/34) لأية مساعدة أو استفسار.

### س4: هل يمكنني تنزيل Aspose.PSD لمكتبة .NET مجانًا؟

 ج4: نعم، يمكنك تنزيل المكتبة من[صفحة الإصدار](https://releases.aspose.com/psd/net/).

### س5: كيف يمكنني شراء ترخيص Aspose.PSD لـ .NET؟

 ج5: يمكنك شراء ترخيص من[صفحة الشراء](https://purchase.aspose.com/buy).