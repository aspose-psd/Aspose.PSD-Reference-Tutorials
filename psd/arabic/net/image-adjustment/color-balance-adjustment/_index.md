---
title: تطبيق ضبط توازن اللون في Aspose.PSD لـ .NET
linktitle: تطبيق ضبط توازن اللون
second_title: Aspose.PSD.NET API
description: قم بتحسين ألوان صور PSD بسهولة باستخدام Aspose.PSD لميزة ضبط توازن الألوان الخاصة بـ .NET. اتبع دليلنا خطوة بخطوة للحصول على نتائج مذهلة.
type: docs
weight: 14
url: /ar/net/image-adjustment/color-balance-adjustment/
---
## مقدمة

مرحبًا بك في هذا الدليل الشامل حول تطبيق ضبط توازن اللون في Aspose.PSD لـ .NET! Aspose.PSD هي مكتبة .NET قوية تتيح للمطورين العمل مع ملفات PSD بكفاءة. في هذا البرنامج التعليمي، سوف نركز على ميزة ضبط توازن اللون، مما يتيح لك تحسين توازن الألوان لصور PSD الخاصة بك بسهولة.

## المتطلبات الأساسية

قبل أن نتعمق في البرنامج التعليمي، تأكد من توفر المتطلبات الأساسية التالية:

-  Aspose.PSD لـ .NET Library: قم بتنزيل المكتبة وتثبيتها من ملف .NET Library[موقع Aspose.PSD](https://releases.aspose.com/psd/net/).
- بيئة التطوير: تأكد من أن لديك بيئة تطوير .NET عاملة تم إعدادها على جهازك.
- ملف PSD: جهز ملف PSD الذي تريد تطبيق ضبط توازن اللون عليه.

## استيراد مساحات الأسماء

في مشروع .NET الخاص بك، قم بتضمين مساحات الأسماء الضرورية لاستخدام ميزات Aspose.PSD. أضف الأسطر التالية إلى الكود الخاص بك:

```csharp
using Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers;
```

الآن، دعونا نقسم عملية ضبط توازن اللون إلى خطوات متعددة:

## الخطوة 1: قم بتحميل ملف PSD

```csharp
string dataDir = "Your Document Directory";
var filePath = dataDir + "ColorBalance.psd";
var outputPath = dataDir + "ColorBalance_out.psd";

using (var im = (FileFormats.Psd.PsdImage)Image.Load(filePath))
{
    // ستتم إضافة رمز ضبط توازن اللون في الخطوات التالية.
}
```

## الخطوة 2: الوصول إلى توازن الألوان وضبطه

```csharp
foreach (var layer in im.Layers)
{
    var cbLayer = layer as ColorBalanceAdjustmentLayer;
    if (cbLayer != null)
    {
        cbLayer.ShadowsCyanRedBalance = 30;
        cbLayer.ShadowsMagentaGreenBalance = -15;
        cbLayer.ShadowsYellowBlueBalance = 40;
        cbLayer.MidtonesCyanRedBalance = -90;
        cbLayer.MidtonesMagentaGreenBalance = -25;
        cbLayer.MidtonesYellowBlueBalance = 20;
        cbLayer.HighlightsCyanRedBalance = -30;
        cbLayer.HighlightsMagentaGreenBalance = 67;
        cbLayer.HighlightsYellowBlueBalance = -95;
        cbLayer.PreserveLuminosity = true;
    }
}
```

## الخطوة 3: احفظ الصورة المعدلة

```csharp
im.Save(outputPath);
```

لقد نجحت الآن في تطبيق ضبط توازن اللون على ملف PSD الخاص بك باستخدام Aspose.PSD لـ .NET!

## خاتمة

تهانينا! لقد تعلمت كيفية تحسين توازن الألوان لصور PSD الخاصة بك باستخدام Aspose.PSD لـ .NET. قم بتجربة قيم توازن مختلفة لتحقيق التأثيرات المرئية المطلوبة.

## الأسئلة الشائعة

### س1: هل يمكنني تطبيق ضبط توازن اللون على طبقات متعددة؟

ج1: نعم، يمكنك تكرار كل الطبقات في ملف PSD الخاص بك وضبط توازن الألوان حسب الحاجة.

### س2: هل Aspose.PSD for .NET مناسب للمعالجة المجمعة لملفات PSD؟

ج2: بالتأكيد! يوفر Aspose.PSD إمكانات معالجة مجمعة فعالة لملفات PSD.

### س3: كيف يمكنني الحصول على ترخيص مؤقت لـ Aspose.PSD لـ .NET؟

 ج3: زيارة[Aspose.PSD الترخيص المؤقت](https://purchase.aspose.com/temporary-license/) للحصول على ترخيص مؤقت.

### س4: أين يمكنني العثور على المزيد من الأمثلة والوثائق؟

 ج4: اكتشف[وثائق Aspose.PSD](https://reference.aspose.com/psd/net/) للحصول على أمثلة وأدلة مفصلة.

### س5: ما هي خيارات الدعم المتوفرة لـ Aspose.PSD لـ .NET؟

 ج5: قم بزيارة[منتدى Aspose.PSD](https://forum.aspose.com/c/psd/34) لدعم المجتمع والمناقشات.
