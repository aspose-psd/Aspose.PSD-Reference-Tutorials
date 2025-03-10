---
title: قص الصور عن طريق التحولات في Aspose.PSD لـ .NET
linktitle: قص الصور عن طريق التحولات
second_title: Aspose.PSD.NET API
description: تعلم كيفية اقتصاص الصور بسهولة باستخدام Aspose.PSD لـ .NET. اتبع دليلنا خطوة بخطوة لإجراء تعديلات دقيقة على الصورة.
weight: 12
url: /ar/net/image-manipulation/crop-image-shifts/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# قص الصور عن طريق التحولات في Aspose.PSD لـ .NET

## مقدمة

في مجال تطوير .NET، يبرز Aspose.PSD كمجموعة أدوات قوية لمهام معالجة الصور. إحدى ميزاته البارزة هي القدرة على اقتصاص الصور بدقة، وذلك بفضل وظيفة "الاقتصاص حسب التحولات". في هذا الدليل المفصّل خطوة بخطوة، سنرشدك خلال عملية قص الصور بسلاسة باستخدام Aspose.PSD for .NET.

## المتطلبات الأساسية

قبل الخوض في البرنامج التعليمي، تأكد من توفر المتطلبات الأساسية التالية:

-  Aspose.PSD لمكتبة .NET: تأكد من تثبيت المكتبة. إذا لم يكن الأمر كذلك، يمكنك تنزيله من[صفحة الإصدار](https://releases.aspose.com/psd/net/).

- بيئة .NET: تأكد من إعداد بيئة تطوير .NET على جهازك.

- صورة نموذجية: قم بإعداد صورة نموذجية بتنسيق PSD التي ترغب في العمل بها.

## استيراد مساحات الأسماء

ابدأ باستيراد مساحات الأسماء الضرورية إلى مشروع .NET الخاص بك. توفر مساحات الأسماء هذه إمكانية الوصول إلى فئات Aspose.PSD والأساليب المطلوبة لاقتصاص الصور.

```csharp
using Aspose.PSD.ImageOptions;
```

## الخطوة 1: تحديد دليل المستندات الخاص بك

قم بتعيين المسار إلى دليل المستند الخاص بك حيث سيتم تحديد موقع الملفات المصدر والوجهة.

```csharp
string dataDir = "Your Document Directory";
```

## الخطوة 2: تحميل الصورة المصدر

قم بتحميل صورة PSD التي تريد اقتصاصها. تأكد من استبدال "sample.psd" باسم الملف المصدر الخاص بك.

```csharp
string sourceFile = dataDir + @"sample.psd";
string destName = dataDir + @"CroppingByShifts_out.jpg";
```

## الخطوة 3: تخزين بيانات الصورة مؤقتًا للحصول على أداء أفضل

قبل الاقتصاص، يُنصح بتخزين بيانات الصورة مؤقتًا لتحسين الأداء.

```csharp
using (RasterImage rasterImage = (RasterImage)Image.Load(sourceFile))
{
    if (!rasterImage.IsCached)
    {
        rasterImage.CacheData();
    }
```

## الخطوة 4: تحديد قيم التحول للاقتصاص

حدد قيم الإزاحة للجوانب اليسرى واليمنى والعلوية والسفلى من الصورة. اضبط هذه القيم بناءً على متطلبات الاقتصاص لديك.

```csharp
int leftShift = 10;
int rightShift = 10;
int topShift = 10;
int bottomShift = 10;
```

## الخطوة 5: تطبيق الاقتصاص وحفظ النتائج

 الاستفادة من`Crop` طريقة لتطبيق التحولات المحددة وحفظ الصورة التي تم اقتصاصها في الملف الوجهة.

```csharp
rasterImage.Crop(leftShift, rightShift, topShift, bottomShift);
rasterImage.Save(destName, new JpegOptions());
}
```

## خاتمة

تهانينا! لقد تعلمت بنجاح كيفية اقتصاص الصور عن طريق التحولات باستخدام Aspose.PSD لـ .NET. توفر لك هذه الوظيفة القوية الدقة والتحكم اللازمين لمهام معالجة الصور المختلفة.

## الأسئلة الشائعة

### س1: هل يمكنني قص الصور بتنسيقات مختلفة، وليس PSD فقط؟

ج1: نعم، يدعم Aspose.PSD تنسيقات الصور المختلفة، مما يسمح لك باقتصاص الصور بتنسيقات مثل JPEG وPNG والمزيد.

### س2: هل هناك إصدار تجريبي متاح قبل شراء Aspose.PSD لـ .NET؟

 ج2: بالتأكيد! يمكنك استكشاف مجموعة الأدوات من خلال الإصدار التجريبي المجاني المتاح[هنا](https://releases.aspose.com/).

### س3: كيف يمكنني الحصول على ترخيص مؤقت لـ Aspose.PSD لـ .NET؟

 ج3: يمكنك الحصول على ترخيص مؤقت لأغراض الاختبار[هنا](https://purchase.aspose.com/temporary-license/).

### س4: أين يمكنني العثور على دعم إضافي ومناقشات متعلقة بـ Aspose.PSD؟

 ج4: قم بزيارة[منتدى Aspose.PSD](https://forum.aspose.com/c/psd/34) للحصول على الدعم والمناقشات الجذابة.

### س5: هل يمكنني شراء Aspose.PSD لـ .NET مباشرةً من موقع الويب؟

 ج5: نعم، يمكنك شراء المكتبة بشكل آمن من[صفحة الشراء](https://purchase.aspose.com/buy).

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
