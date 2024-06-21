---
title: دعم تأثير التوهج الخارجي في Aspose.PSD لـ .NET
linktitle: دعم تأثير الوهج الخارجي
second_title: Aspose.PSD.NET API
description: اكتشف قوة تأثير التوهج الخارجي في Aspose.PSD لـ .NET. ارفع مستوى تصميمات صورك باستخدام هذا البرنامج التعليمي خطوة بخطوة.
type: docs
weight: 16
url: /ar/net/image-manipulation/supporting-outer-glow-effect/
---
## مقدمة

مرحبًا بك في دليلنا خطوة بخطوة حول دعم تأثير التوهج الخارجي في Aspose.PSD لـ .NET. Aspose.PSD هي مكتبة قوية تتيح المعالجة السلسة لملفات PSD في تطبيقات .NET. في هذا البرنامج التعليمي، سوف نستكشف تنفيذ تأثير التوهج الخارجي ونقدم إرشادات تفصيلية لدمجه في مشاريعك.

## المتطلبات الأساسية

قبل أن نتعمق في البرنامج التعليمي، تأكد من توفر المتطلبات الأساسية التالية:

-  Aspose.PSD لمكتبة .NET: قم بتنزيل المكتبة من ملف[وثائق Aspose.PSD .NET](https://reference.aspose.com/psd/net/).

- بيئة التطوير: قم بإعداد بيئة تطوير .NET المفضلة لديك.

- أدلة المستندات والمخرجات: حدد أدلة المستندات والمخرجات الخاصة بك في الكود المقدم.

## استيراد مساحات الأسماء

في هذا القسم، سنقوم باستيراد مساحات الأسماء اللازمة لبدء تنفيذ تأثير التوهج الخارجي. اتبع الخطوات التالية:

```csharp
using System;
using System.IO;
using Aspose.PSD.FileFormats.Core.Blending;
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.FileFormats.Psd.Layers.FillSettings;
using Aspose.PSD.FileFormats.Psd.Layers.LayerEffects;
using Aspose.PSD.ImageOptions;
```

الآن، دعونا نقسم المثال المقدم إلى خطوات متعددة لتحقيق تأثير التوهج الخارجي.

## الخطوة 1: تعيين مسارات المستند والإخراج

```csharp
string baseDir = "Your Document Directory";
string outputDir = "Your Output Directory";
```

## الخطوة 2: تحميل صورة PSD

```csharp
string src = Path.Combine(baseDir, "GreenLayer.psd");
using (var image = (PsdImage)Image.Load(src))
{
    // سيتم إضافة خطوات التنفيذ أدناه.
}
```

## الخطوة 3: إضافة تأثير الوهج الخارجي

```csharp
OuterGlowEffect effect = image.Layers[1].BlendingOptions.AddOuterGlow();
```

## الخطوة 4: تكوين معلمات التوهج الخارجي

```csharp
effect.Range = 10;
effect.Spread = 10;
((IColorFillSettings)effect.FillColor).Color = Color.Red;
effect.Opacity = 128;
effect.BlendMode = BlendMode.Normal;
```

## الخطوة 5: احفظ الصورة

```csharp
string outputPng = Path.Combine(outputDir, "output261.png");
image.Save(outputPng, new PngOptions());
```

## الخطوة 6: التنظيف

```csharp
File.Delete(outputPng);
```

## الخطوة 7: عرض رسالة النجاح

```csharp
Console.WriteLine("SupportOfOuterGlowEffect executed successfully");
```

## خاتمة

تهانينا! لقد نجحت في تنفيذ تأثير التوهج الخارجي باستخدام Aspose.PSD لـ .NET. تعمل هذه الميزة القوية على تحسين المظهر المرئي لصورك، مما يوفر لمسة فريدة لتصميماتك.

## الأسئلة الشائعة

### س1: هل Aspose.PSD متوافق مع جميع أطر عمل .NET؟

ج1: نعم، يدعم Aspose.PSD نطاقًا واسعًا من أطر عمل .NET، مما يضمن التوافق مع بيئات التطوير المختلفة.

### س2: أين يمكنني العثور على وثائق إضافية لـ Aspose.PSD؟

 ج2: راجع[وثائق Aspose.PSD .NET](https://reference.aspose.com/psd/net/) للحصول على معلومات وأمثلة شاملة.

### س3: كيف يمكنني الحصول على ترخيص مؤقت لـ Aspose.PSD؟

 ج3: زيارة[Aspose.PSD الترخيص المؤقت](https://purchase.aspose.com/temporary-license/) لخيارات الترخيص المؤقت.

### س4: ما هو الدعم المتوفر لمستخدمي Aspose.PSD؟

 ج4: انضم إلى[منتدى Aspose.PSD](https://forum.aspose.com/c/psd/34) لدعم المجتمع والمناقشات.

### س5: هل يمكنني شراء Aspose.PSD لـ .NET؟

 ج5: نعم، استكشف خيارات الترخيص وقم بالشراء.[هنا](https://purchase.aspose.com/buy).