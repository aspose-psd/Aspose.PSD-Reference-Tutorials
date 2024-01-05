---
title: تنفيذ ضبط السطوع في Aspose.PSD لـ .NET
linktitle: تنفيذ تعديل السطوع
second_title: Aspose.PSD.NET API
description: اكتشف قوة Aspose.PSD لـ .NET في ضبط سطوع الصورة. اتبع دليلنا خطوة بخطوة للتنفيذ السلس.
type: docs
weight: 10
url: /ar/net/image-adjustment/brightness-adjustment/
---
## مقدمة

يعد تحسين سمات الصورة وضبطها متطلبًا شائعًا في العديد من التطبيقات، ويوفر Aspose.PSD for .NET حلاً قويًا لمعالجة ملفات PSD بسلاسة. أحد هذه المعالجات هو تعديل السطوع، مما يسمح لك بتعديل سطوع الصورة دون عناء.

في هذا البرنامج التعليمي، سنتعرف على عملية تنفيذ ضبط السطوع باستخدام Aspose.PSD لـ .NET. اتبع الخطوات أدناه للحصول على فهم شامل لكيفية دمج تعديلات السطوع في ملفات PSD الخاصة بك.

## المتطلبات الأساسية

قبل الغوص في البرنامج التعليمي، تأكد من توفر المتطلبات الأساسية التالية:

-  Aspose.PSD لمكتبة .NET: قم بتنزيل وتثبيت Aspose.PSD لمكتبة .NET من[رابط التحميل](https://releases.aspose.com/psd/net/).

-  دليل المستندات: قم بإعداد دليل لتخزين ملفات PSD الخاصة بك وتحديث ملف`dataDir` متغير في مقتطف التعليمات البرمجية المقدم مع المسار إلى دليل المستند الخاص بك.

## استيراد مساحات الأسماء

في مشروع .NET الخاص بك، قم بتضمين مساحات الأسماء الضرورية للوصول إلى وظيفة Aspose.PSD. أضف مساحات الأسماء التالية إلى التعليمات البرمجية الخاصة بك:

```csharp
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.FileFormats.Tiff.Enums;
using Aspose.PSD.ImageOptions;
```

الآن، دعونا نقسم المثال إلى عدة خطوات:

## الخطوة 1: قم بتحميل ملف PSD

```csharp
// المسار إلى دليل المستندات.
string dataDir = "Your Document Directory";
string sourceFile = dataDir + @"sample.psd";

// قم بتحميل ملف PSD باستخدام Aspose.PSD
using (var image = (PsdImage)Image.Load(sourceFile))
{
    // الكود الخاص بك لمزيد من الخطوات موجود هنا
}
```

## الخطوة 2: الحصول على الصورة النقطية

```csharp
// احصل على الصورة النقطية من ملف PSD الذي تم تحميله
RasterCachedImage rasterImage = image;
```

## الخطوة 3: ضبط السطوع

```csharp
// اضبط قيمة السطوع. تقع قيم السطوع المقبولة في النطاق [-255، 255].
rasterImage.AdjustBrightness(-50);
```

## الخطوة 4: احفظ الصورة المعدلة

```csharp
// احفظ الصورة المعدلة مع السطوع المعدل
string destName = dataDir + @"AdjustBrightness_out.tiff";
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
rasterImage.Save(destName, tiffOptions);
```

الآن بعد أن قمنا بتقسيم المثال إلى خطوات يمكن التحكم فيها، يمكنك دمج ضبط السطوع بسلاسة في مشروع .NET الخاص بك باستخدام Aspose.PSD.

## خاتمة

يعمل Aspose.PSD for .NET على تبسيط عملية تنفيذ تعديلات السطوع في ملفات PSD. باتباع الدليل الموضح أعلاه خطوة بخطوة، يمكنك تحسين المظهر البصري لصورك دون عناء. قم بتجربة قيم سطوع مختلفة لتحقيق النتائج المرجوة.

## الأسئلة الشائعة

### س1: أين يمكنني العثور على الوثائق الخاصة بـ Aspose.PSD لـ .NET؟

 ج1: الوثائق متاحة[هنا](https://reference.aspose.com/psd/net/).

### س2: كيف يمكنني تنزيل Aspose.PSD لمكتبة .NET؟

 ج2: يمكنك تنزيل المكتبة من[صفحة الإصدار](https://releases.aspose.com/psd/net/).

### س3: هل هناك نسخة تجريبية مجانية متاحة لـ Aspose.PSD لـ .NET؟

 ج3: نعم، يمكنك الوصول إلى النسخة التجريبية المجانية[هنا](https://releases.aspose.com/).

### س 4: أين يمكنني الحصول على دعم Aspose.PSD لـ .NET؟

 ج4: للحصول على الدعم، قم بزيارة[منتدى Aspose.PSD](https://forum.aspose.com/c/psd/34).

### س5: كيف يمكنني الحصول على ترخيص مؤقت لـ Aspose.PSD لـ .NET؟

 ج5: يمكنك الحصول على ترخيص مؤقت[هنا](https://purchase.aspose.com/temporary-license/).