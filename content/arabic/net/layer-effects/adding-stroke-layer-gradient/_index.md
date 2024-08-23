---
title: إضافة طبقة السكتة الدماغية مع التدرج في Aspose.PSD لـ .NET
linktitle: إضافة طبقة السكتة الدماغية مع التدرج
second_title: Aspose.PSD.NET API
description: تعرف على كيفية إضافة طبقة حدود متدرجة في Aspose.PSD لـ .NET. ارفع مهاراتك في معالجة الصور من خلال هذا البرنامج التعليمي الشامل.
type: docs
weight: 12
url: /ar/net/layer-effects/adding-stroke-layer-gradient/
---
## مقدمة

إذا كنت تتطلع إلى تحسين تطبيقات .NET الخاصة بك باستخدام تأثيرات رسومية مذهلة، فإن Aspose.PSD for .NET هو الحل الأمثل لك. في هذا البرنامج التعليمي، سوف نتعمق في عملية إضافة طبقة حدود بتدرج باستخدام Aspose.PSD لـ .NET. سيمكنك هذا الدليل التفصيلي خطوة بخطوة من رفع مستوى الجاذبية المرئية لصورك دون عناء.

## المتطلبات الأساسية

قبل أن نبدأ هذه الرحلة، تأكد من توفر المتطلبات الأساسية التالية:

- معرفة عملية بتطوير C# و.NET.
-  تم تثبيت Aspose.PSD لمكتبة .NET. يمكنك تنزيله[هنا](https://releases.aspose.com/psd/net/).
- محرر التعليمات البرمجية، مثل Visual Studio، لتنفيذ الأمثلة المقدمة.

## استيراد مساحات الأسماء

لبدء الأمور، دعونا نقوم باستيراد مساحات الأسماء الضرورية إلى مشروعنا. تعد مساحات الأسماء هذه ضرورية للاستفادة من وظائف Aspose.PSD لـ .NET.

```csharp
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.FileFormats.Psd.Layers.FillSettings;
using Aspose.PSD.FileFormats.Psd.Layers.LayerEffects;
using Aspose.PSD.ImageLoadOptions;
using System;
using Aspose.PSD.FileFormats.Core.Blending;
```

## الخطوة 1: إعداد دليل المستندات

ابدأ بتحديد المسار إلى دليل المستندات الخاص بك في الكود. وهذا يضمن تحميل الملفات الضرورية وحفظها من الموقع الصحيح.

```csharp
string dataDir = "Your Document Directory";
```

## الخطوة 2: قم بتحميل ملف PSD

قم بتحميل ملف PSD المصدر باستخدام Aspose.PSD لـ .NET. تأكد من تحميل مصدر التأثيرات لمعالجة الطبقات بفعالية.

```csharp
string sourceFileName = dataDir + "Stroke.psd";
string exportPath = dataDir + "StrokeGradientChanged.psd";

var loadOptions = new PsdLoadOptions()
{
    LoadEffectsResource = true
};

using (var im = (PsdImage)Image.Load(sourceFileName, loadOptions))
{
    // يأتي رمز التعامل مع ملف PSD هنا
}
```

## الخطوة 3: التحقق من إعدادات حد التدرج

تأكد من تكوين طبقة الحد ذات التدرج بشكل صحيح عن طريق التحقق من الإعدادات المختلفة مثل وضع المزج، والعتامة، والرؤية.

```csharp
var gradientStroke = (StrokeEffect)im.Layers[2].BlendingOptions.Effects[0];

// يتحقق التأكيد من إعدادات حد التدرج
AssertIsTrue(gradientStroke.BlendMode == BlendMode.Normal);
AssertIsTrue(gradientStroke.Opacity == 255);
AssertIsTrue(gradientStroke.IsVisible);

// مزيد من عمليات التحقق من التأكيد لإعدادات التعبئة
// ...
```

استمر في تنفيذ عمليات التحقق من التأكيد لإعدادات التعبئة الأخرى، بما في ذلك نقاط اللون ونقاط الشفافية.

## الخطوة 4: تحرير إعدادات حد التدرج

الآن، دعونا نجري بعض التغييرات على إعدادات حدود التدرج. قم بتعديل المعلمات مثل اللون والعتامة ووضع المزج ونوع التدرج لتحقيق التأثير المرئي المطلوب.

```csharp
// رمز لتعديل إعدادات حدود التدرج
// ...
```

## الخطوة 5: احفظ ملف PSD المعدل

احفظ ملف PSD الذي تم تحريره في مسار التصدير المحدد.

```csharp
im.Save(exportPath);
```

## خاتمة

تهانينا! لقد نجحت في إضافة طبقة حدود بتدرج باستخدام Aspose.PSD لـ .NET. لقد زوّدك هذا البرنامج التعليمي بالمعرفة اللازمة لتحسين صورك برمجيًا.

## الأسئلة الشائعة

### س1: هل يمكنني استخدام Aspose.PSD لـ .NET مع أطر عمل .NET أخرى؟

A1: نعم، Aspose.PSD لـ .NET متوافق مع أطر عمل .NET المختلفة.

### س2: هل هناك نسخة تجريبية مجانية متاحة لـ Aspose.PSD لـ .NET؟

 ج2: نعم، يمكنك الوصول إلى النسخة التجريبية المجانية[هنا](https://releases.aspose.com/).

### س3: كيف يمكنني الحصول على دعم Aspose.PSD لـ .NET؟

 ج3: قم بزيارة[منتدى Aspose.PSD](https://forum.aspose.com/c/psd/34) لدعم المجتمع.

### س4: أين يمكنني العثور على وثائق شاملة لـ Aspose.PSD لـ .NET؟

 ج4: راجع[الوثائق](https://reference.aspose.com/psd/net/) للحصول على معلومات مفصلة.

### س5: كيف يمكنني شراء ترخيص Aspose.PSD لـ .NET؟

 ج5: يمكنك شراء ترخيص[هنا](https://purchase.aspose.com/buy).