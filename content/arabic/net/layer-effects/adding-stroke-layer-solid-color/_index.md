---
title: إضافة طبقة السكتة الدماغية ذات اللون الصلب في Aspose.PSD لـ .NET
linktitle: إضافة طبقة السكتة الدماغية مع اللون الصلب
second_title: Aspose.PSD.NET API
description: عزز مهاراتك في معالجة صور .NET باستخدام Aspose.PSD. تعلم كيفية إضافة طبقات السكتة الدماغية بألوان صلبة خطوة بخطوة.
type: docs
weight: 11
url: /ar/net/layer-effects/adding-stroke-layer-solid-color/
---
## مقدمة

في مجال تطوير .NET، يعد إنشاء صور جذابة بصريًا مطلبًا شائعًا. يوفر Aspose.PSD for .NET مجموعة قوية من الأدوات لمعالجة الصور وتحسينها بسلاسة. إحدى الميزات الأساسية هي إضافة طبقة حدود ذات لون خالص، مما يضفي الحيوية والعمق على صورك. في هذا البرنامج التعليمي، سنرشدك خلال العملية خطوة بخطوة باستخدام Aspose.PSD لـ .NET.

## المتطلبات الأساسية

قبل الغوص في البرنامج التعليمي، تأكد من أن لديك المتطلبات الأساسية التالية:

- المعرفة الأساسية بتطوير .NET.
- تم تثبيت Visual Studio على جهازك.
- Aspose.PSD لمكتبة .NET. يمكنك تنزيله من[موقع إلكتروني](https://releases.aspose.com/psd/net/).

## استيراد مساحات الأسماء

ابدأ باستيراد مساحات الأسماء الضرورية للاستفادة من وظائف Aspose.PSD لـ .NET:

```csharp
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.FileFormats.Psd.Layers.FillSettings;
using Aspose.PSD.FileFormats.Psd.Layers.LayerEffects;
using Aspose.PSD.ImageLoadOptions;
using System;
using Aspose.PSD.FileFormats.Core.Blending;
```

## الخطوة 1: قم بتحميل ملف PSD

ابدأ بتحميل ملف PSD الذي تريد تحسينه باستخدام طبقة الحد. تأكد من أن لديك مسار الملف الصحيح:

```csharp
string dataDir = "Your Document Directory";
string sourceFileName = dataDir + "Stroke.psd";

var loadOptions = new PsdLoadOptions()
{
    LoadEffectsResource = true
};

using (var im = (PsdImage)Image.Load(sourceFileName, loadOptions))
{
    // سيتم إضافة رمز لمزيد من الخطوات هنا
}
```

## الخطوة 2: الوصول إلى خصائص تأثير السكتة الدماغية

استرجاع خصائص تأثير السكتة الدماغية من ملف PSD:

```csharp
var colorStroke = (StrokeEffect)im.Layers[1].BlendingOptions.Effects[0];

if ((colorStroke.BlendMode != BlendMode.Normal) ||
    (colorStroke.Opacity != 255) ||
    (colorStroke.IsVisible != true))
{
    throw new Exception("Color stroke effect was read wrong");
}
```

## الخطوة 3: ضبط إعدادات السكتة الدماغية

قم بتعديل إعدادات السكتة الدماغية وفقًا لتفضيلاتك. في هذا المثال، قمنا بتغيير اللون إلى اللون الأصفر، وضبط العتامة على 127، واستخدام وضع مزج الألوان:

```csharp
var fillSettings = (ColorFillSettings)colorStroke.FillSettings;

if ((fillSettings.Color != Color.Black) || (fillSettings.FillType != FillType.Color))
{
    throw new Exception("Color stroke effect settings were read wrong");
}

fillSettings.Color = Color.Yellow;
colorStroke.Opacity = 127;
colorStroke.BlendMode = BlendMode.Color;
```

## الخطوة 4: احفظ الصورة المعدلة

احفظ الصورة بعد تطبيق تغييرات طبقة الحد:

```csharp
string exportPath = dataDir + "StrokeGradientChanged.psd";
im.Save(exportPath);
```

## الخطوة 5: التحقق من التغييرات

تأكد من تطبيق التغييرات بشكل صحيح عن طريق تحميل الصورة المحررة وفحصها:

```csharp
using (var im = (PsdImage)Image.Load(exportPath, loadOptions))
{
    // سيتم إضافة رمز للتحقق من التغييرات هنا
}
```

كرر هذه الخطوات لإجراء تعديلات إضافية أو قم بتجربة تأثيرات حدود مختلفة لتحقيق التأثير البصري المطلوب.

## خاتمة

تهانينا! لقد تعلمت بنجاح كيفية إضافة طبقة حد ذات لون خالص باستخدام Aspose.PSD لـ .NET. تفتح هذه الميزة القوية عالمًا من الإمكانيات لتحسين صورك في بيئة .NET.

## الأسئلة الشائعة

### س1: هل يتوافق Aspose.PSD for .NET مع أحدث إصدارات .NET Framework؟

ج1: نعم، يتم تحديث Aspose.PSD لـ .NET بانتظام لضمان التوافق مع أحدث إصدارات .NET Framework.

### س2: هل يمكنني استخدام Aspose.PSD لـ .NET للمشاريع التجارية؟

ج2: بالتأكيد! Aspose.PSD for .NET هو منتج تجاري، ويمكنك استخدامه في مشاريعك عن طريق شراء ترخيص.

### س3: أين يمكنني العثور على المزيد من الأمثلة والوثائق الخاصة بـ Aspose.PSD لـ .NET؟

 ج3: اكتشف[توثيق](https://reference.aspose.com/psd/net/) للحصول على أمثلة وإرشادات شاملة.

### س4: هل هناك نسخة تجريبية مجانية متاحة لـ Aspose.PSD لـ .NET؟

 ج4: نعم، يمكنك الحصول على نسخة تجريبية مجانية من[صفحة الإصدارات](https://releases.aspose.com/).

### س5: كيف يمكنني الحصول على دعم Aspose.PSD لـ .NET؟

 ج5: قم بزيارة[منتدى Aspose.PSD](https://forum.aspose.com/c/psd/34) لطلب المساعدة والتواصل مع المجتمع.