---
title: تراكب تأثيرات الألوان على الصور في Aspose.PSD لـ .NET
linktitle: تراكب تأثيرات الألوان على الصور
second_title: Aspose.PSD.NET API
description: اكتشف سحر Aspose.PSD لـ .NET من خلال برنامجنا التعليمي حول تراكب تأثيرات الألوان. ارفع مستوى لعبة معالجة الصور الخاصة بك دون عناء.
type: docs
weight: 11
url: /ar/net/image-effects/overlay-color-effect/
---
## مقدمة

يوفر Aspose.PSD for .NET مجموعة قوية من الميزات لمعالجة الصور، مما يسمح للمطورين بتحقيق تأثيرات مذهلة دون عناء. إحدى هذه الإمكانات هي تراكب تأثيرات الألوان على الصور. في هذا البرنامج التعليمي، سنركز على تأثير ColorOverlay ونوضح كيفية تطبيقه على الصورة، وتحويل جاذبيتها البصرية.

## المتطلبات الأساسية

قبل الغوص في البرنامج التعليمي، تأكد من توفر المتطلبات الأساسية التالية:

-  Aspose.PSD لـ .NET: قم بتنزيل المكتبة وتثبيتها من[هنا](https://releases.aspose.com/psd/net/).
- دليل المستندات الخاص بك: قم بإعداد دليل لتخزين ملفات المصدر والإخراج الخاصة بك.

## استيراد مساحات الأسماء

للبدء، قم باستيراد مساحات الأسماء الضرورية في مشروع .NET الخاص بك:

```csharp
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.FileFormats.Psd.Layers.LayerEffects;
using Aspose.PSD.ImageLoadOptions;
using System;
```

الآن، دعونا نقسم المثال إلى خطوات متعددة.

## الخطوة 1: تحميل الصورة

```csharp
string sourceFileName = dataDir + "ColorOverlay.psd";
var loadOptions = new PsdLoadOptions()
{
    LoadEffectsResource = true
};

using (var im = (PsdImage)Image.Load(sourceFileName, loadOptions))
{
    // سيتم وضع الرمز الخاص بك لمزيد من الخطوات هنا
}
```

## الخطوة 2: الوصول إلى تأثير ColorOverlay

```csharp
var colorOverlay = (ColorOverlayEffect)(im.Layers[1].BlendingOptions.Effects[0]);
```

## الخطوة 3: التحقق من إعدادات ColorOverlay وتعديلها

```csharp
if (colorOverlay.Color != Color.Red || colorOverlay.Opacity != 153)
{
    throw new Exception("Color overlay read wrong");
}

colorOverlay.Color = Color.Green;
colorOverlay.Opacity = 128;
```

## الخطوة 4: احفظ الصورة المعدلة

```csharp
string psdPathAfterChange = dataDir + "ColorOverlayChanged.psd";
im.Save(psdPathAfterChange);
```

باتباع هذه الخطوات، تكون قد نجحت في تطبيق تأثير ColorOverlay على صورتك باستخدام Aspose.PSD لـ .NET.

## خاتمة

في الختام، يعمل Aspose.PSD for .NET على تمكين المطورين من إضفاء الحيوية على الصور من خلال تأثيرات الألوان الجذابة. لقد زودك هذا البرنامج التعليمي بالمعرفة اللازمة لدمج تأثير ColorOverlay بسلاسة في مشاريع معالجة الصور الخاصة بك. قم بتجربة واستكشاف ورفع مستوى لعبة معالجة الصور الخاصة بك باستخدام Aspose.PSD!

## الأسئلة الشائعة

### س1: هل يمكنني استخدام Aspose.PSD لـ .NET مع أطر عمل .NET أخرى؟

A1: نعم، Aspose.PSD for .NET متوافق مع أطر عمل .NET المتنوعة، بما في ذلك .NET Core و.NET Standard.

### س2: أين يمكنني العثور على وثائق شاملة لـ Aspose.PSD لـ .NET؟

ج2: يمكنك الرجوع إلى الوثائق[هنا](https://reference.aspose.com/psd/net/) للحصول على معلومات مفصلة وعينات التعليمات البرمجية.

### س3: هل هناك نسخة تجريبية مجانية متاحة لـ Aspose.PSD لـ .NET؟

ج3: نعم، يمكنك استكشاف إمكانيات Aspose.PSD لـ .NET عن طريق تنزيل النسخة التجريبية المجانية[هنا](https://releases.aspose.com/).

### س4: كيف يمكنني الحصول على دعم Aspose.PSD لـ .NET؟

 ج4: بالنسبة لأية استفسارات متعلقة بالدعم، قم بزيارة[منتدى Aspose.PSD](https://forum.aspose.com/c/psd/34) للتواصل مع المجتمع والخبراء.

### س5: هل يمكنني الحصول على ترخيص مؤقت لـ Aspose.PSD لـ .NET؟

 ج5: نعم، يمكنك الحصول على ترخيص مؤقت[هنا](https://purchase.aspose.com/temporary-license/) لأغراض التقييم.