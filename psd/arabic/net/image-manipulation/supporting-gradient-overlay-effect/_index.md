---
title: دعم تأثير تراكب التدرج في Aspose.PSD لـ .NET
linktitle: دعم تأثير تراكب التدرج
second_title: Aspose.PSD.NET API
description: قم بتحسين الرسومات في .NET باستخدام Aspose.PSD. يرشدك هذا البرنامج التعليمي إلى دعم تأثيرات Gradient Overlay.
type: docs
weight: 18
url: /ar/net/image-manipulation/supporting-gradient-overlay-effect/
---
## مقدمة

مرحبًا بك في هذا البرنامج التعليمي الشامل حول دعم تأثير Gradient Overlay في Aspose.PSD لـ .NET! إذا كنت تتطلع إلى تحسين القدرات الرسومية لتطبيق .NET الخاص بك، فهذا الدليل التفصيلي موجود هنا لمساعدتك. سوف نتعمق في تعقيدات إنشاء وتحرير تأثير Gradient Overlay في طبقة باستخدام Aspose.PSD، وهي مكتبة قوية تعمل على تبسيط معالجة الصور.

## المتطلبات الأساسية

قبل أن نبدأ في هذه الرحلة، تأكد من حصولك على ما يلي:

- فهم أساسي لبرمجة C# و.NET.
-  تم تثبيت Aspose.PSD لـ .NET. يمكنك تنزيله[هنا](https://releases.aspose.com/psd/net/).
- بيئة تطوير تم إعدادها باستخدام IDE المفضل لديك.

## استيراد مساحات الأسماء

للبدء، دعنا نستورد مساحات الأسماء الضرورية في كود C# الخاص بك:

```csharp
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.FileFormats.Psd.Layers;
using Aspose.PSD.FileFormats.Psd.Layers.FillSettings;
using Aspose.PSD.FileFormats.Psd.Layers.LayerEffects;
using Aspose.PSD.ImageLoadOptions;
using System;
using System.IO;
using Aspose.PSD.FileFormats.Core.Blending;
```

الآن بعد أن غطينا الأساسيات، دعونا نقسم كل خطوة بالتفصيل:

## الخطوة 1: قم بتحميل صورة PSD

```csharp
// المسار إلى دليل المستندات.
string SourceDir = "Your Document Directory";
string OutputDir = "Your Output Directory";

string sourceFilePath = Path.Combine(SourceDir, "psdnet256.psd");
string outputFilePath = Path.Combine(OutputDir, "psdnet256.psd_output.psd");

using (var psdImage = (PsdImage)Image.Load(sourceFilePath, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    // رمز الخطوات اللاحقة موجود هنا...
}
```

## الخطوة 2: الوصول إلى خيارات مزج الطبقة

```csharp
BlendingOptions layerBlendOptions = psdImage.Layers[1].BlendingOptions;
```

## الخطوة 3: ابحث عن تأثير تراكب متدرج أو أنشئه

```csharp
GradientOverlayEffect gradientOverlayEffect = null;

foreach (ILayerEffect effect in layerBlendOptions.Effects)
{
    gradientOverlayEffect = effect as GradientOverlayEffect;
    if (gradientOverlayEffect != null)
    {
        break;
    }
}

if (gradientOverlayEffect == null)
{
    gradientOverlayEffect = layerBlendOptions.AddGradientOverlay();
}
```

## الخطوة 4: تكوين تأثير تراكب التدرج

```csharp
gradientOverlayEffect.Opacity = 200;
gradientOverlayEffect.BlendMode = BlendMode.Hue;

GradientFillSettings settings = gradientOverlayEffect.Settings;

settings.ColorPoints = new IGradientColorPoint[]
{
    new GradientColorPoint(Color.GreenYellow, 0, 50),
    new GradientColorPoint(Color.BlueViolet, 4096, 50),
};

settings.Angle = 80;
settings.Scale = 150;
settings.GradientType = GradientType.Linear;

settings.TransparencyPoints[0].Opacity = 100;
settings.TransparencyPoints[1].Opacity = 100;
```

## الخطوة 5: احفظ الصورة المعدلة

```csharp
psdImage.Save(outputFilePath);
```

هذا كل شيء! لقد نجحت في إضافة تأثير تراكب متدرج إلى طبقة باستخدام Aspose.PSD لـ .NET.

## خاتمة

في هذا البرنامج التعليمي، استكشفنا عملية دعم تأثير Gradient Overlay Effect في Aspose.PSD لـ .NET. باتباع الدليل الموضح خطوة بخطوة، يمكنك دمج هذه الميزة بسلاسة في تطبيقات .NET الخاصة بك، مما يعزز المظهر المرئي لصورك.

## الأسئلة الشائعة

### س1: هل Aspose.PSD متوافق مع كافة إصدارات .NET؟

A1: Aspose.PSD for .NET متوافق مع .NET Framework و.NET Core.

### س2: هل يمكنني تطبيق تأثيرات متعددة على طبقة واحدة؟

ج2: نعم، يمكنك تطبيق تأثيرات متنوعة، بما في ذلك Gradient Overlay، على طبقة واحدة.

### س3: أين يمكنني العثور على المزيد من الأمثلة والوثائق؟

 ج3: قم بزيارة[الوثائق](https://reference.aspose.com/psd/net/) للحصول على أمثلة وإرشادات مفصلة.

### س4: هل هناك نسخة تجريبية مجانية متاحة؟

 ج4: نعم، يمكنك الوصول إلى النسخة التجريبية المجانية[هنا](https://releases.aspose.com/).

### س5: كيف يمكنني الحصول على الدعم لـ Aspose.PSD؟

 ج5: قم بزيارة[منتدى Aspose.PSD](https://forum.aspose.com/c/psd/34) لدعم المجتمع.