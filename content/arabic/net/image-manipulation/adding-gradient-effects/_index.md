---
title: إضافة تأثيرات متدرجة إلى الصور في Aspose.PSD لـ .NET
linktitle: إضافة تأثيرات متدرجة على الصور
second_title: Aspose.PSD.NET API
description: قم بتحسين صورك بتأثيرات متدرجة جذابة باستخدام Aspose.PSD لـ .NET. اتبع البرنامج التعليمي خطوة بخطوة للتحولات البصرية الإبداعية.
type: docs
weight: 11
url: /ar/net/image-manipulation/adding-gradient-effects/
---
## مقدمة

يمكن أن يؤدي تحسين الصور بتأثيرات متدرجة إلى إضافة بُعد آسر إلى المحتوى المرئي الخاص بك. يوفر Aspose.PSD for .NET منصة قوية لدمج التراكبات المتدرجة في صورك. في هذا البرنامج التعليمي، سنرشدك خلال عملية إضافة تأثيرات التدرج باستخدام Aspose.PSD لـ .NET.

## المتطلبات الأساسية

قبل الغوص في البرنامج التعليمي، تأكد من توفر المتطلبات الأساسية التالية:

-  Aspose.PSD لـ .NET Library: قم بتنزيل المكتبة وتثبيتها من[Aspose.PSD لتوثيق .NET](https://reference.aspose.com/psd/net/).
- بيئة .NET: تأكد من إعداد بيئة .NET عاملة على جهازك.

## استيراد مساحات الأسماء

ابدأ باستيراد مساحات الأسماء الضرورية إلى مشروعك:

```csharp
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.FileFormats.Psd.Layers.FillSettings;
using Aspose.PSD.FileFormats.Psd.Layers.LayerEffects;
using Aspose.PSD.ImageLoadOptions;
using System;
using Aspose.PSD.FileFormats.Core.Blending;
using System.IO;
```

## الخطوة 1: قم بتحميل الصورة وتحديد المسارات

```csharp
// المسار إلى دليل المستندات.
string SourceDir = "Your Document Directory";
string OutputDir = "Your Output Directory";

string sourceFileName = Path.Combine(SourceDir, "GradientOverlay.psd");
string exportPath = Path.Combine(OutputDir, "GradientOverlayChanged.psd");

var loadOptions = new PsdLoadOptions()
{
    LoadEffectsResource = true
};
```

## الخطوة 2: تأكيد الإعدادات الأولية

تأكد من أن الإعدادات الأولية لتراكب التدرج هي كما هو متوقع:

```csharp
using (var im = (PsdImage)Image.Load(sourceFileName, loadOptions))
{
    var gradientOverlay = (GradientOverlayEffect)im.Layers[1].BlendingOptions.Effects[0];

    // يتحقق التأكيد من الإعدادات الأولية
    // ...

    // نقاط اللون
    // ...

    //نقاط الشفافية
    // ...
}
```

## الخطوة 3: تعديل إعدادات تراكب التدرج

اضبط إعدادات تراكب التدرج وفقًا لتفضيلاتك:

```csharp
// تحرير الاختبار
settings.Color = Color.Green;

gradientOverlay.Opacity = 193;
gradientOverlay.BlendMode = BlendMode.Lighten;

settings.AlignWithLayer = false;
settings.GradientType = GradientType.Radial;
settings.Angle = 45;
settings.Dither = true;
settings.HorizontalOffset = 15;
settings.VerticalOffset = 11;
settings.Reverse = true;

// أضف نقطة لون جديدة
// ...

// تغيير موقع النقطة السابقة
// ...

// أضف نقطة شفافية جديدة
// ...

// تغيير موقع نقطة الشفافية السابقة
// ...

im.Save(exportPath);
```

## الخطوة 4: التحقق من صحة الملف المحرر

تحقق مما إذا تم تطبيق التعديلات بنجاح:

```csharp
// اختبار الملف بعد التعديل
using (var im = (PsdImage)Image.Load(exportPath, loadOptions))
{
    var gradientOverlay = (GradientOverlayEffect)im.Layers[1].BlendingOptions.Effects[0];
    try
    {
        // يتحقق التأكيد من الإعدادات المعدلة
        // ...
    }
    catch (Exception e)
    {
        string ex = e.StackTrace;
    }
}
```

## خاتمة

تؤدي إضافة تأثيرات متدرجة إلى الصور باستخدام Aspose.PSD لـ .NET إلى فتح عالم من الإمكانيات الإبداعية. قم بتجربة الإعدادات المختلفة لتحقيق التأثير المرئي المطلوب في صورك.

## الأسئلة الشائعة

### س1: هل يمكنني تطبيق تأثيرات التدرج على طبقات متعددة في وقت واحد؟

A1: نعم، يمكنك تطبيق تأثيرات التدرج على طبقات متعددة من خلال التكرار خلال كل طبقة وتطبيق الإعدادات المطلوبة.

### س2: ما هي تنسيقات الملفات التي يدعمها Aspose.PSD لـ .NET؟

ج2: يدعم Aspose.PSD for .NET العديد من تنسيقات ملفات الصور، بما في ذلك PSD وPNG وJPEG وBMP وGIF.

### س3: هل هناك إصدار تجريبي متاح لـ Aspose.PSD لـ .NET؟

 ج3: نعم، يمكنك استكشاف إمكانيات Aspose.PSD لـ .NET عن طريق تنزيل النسخة التجريبية المجانية من[هنا](https://releases.aspose.com/).

### س4: كيف يمكنني الحصول على دعم Aspose.PSD لـ .NET؟

 ج4: للحصول على أي مساعدة أو استفسارات، قم بزيارة[Aspose.PSD لمنتدى دعم .NET](https://forum.aspose.com/c/psd/34).

### س5: أين يمكنني شراء Aspose.PSD لـ .NET؟

 ج5: يمكنك شراء المكتبة من[Aspose.PSD لصفحة شراء .NET](https://purchase.aspose.com/buy).