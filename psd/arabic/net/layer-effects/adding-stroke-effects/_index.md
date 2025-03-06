---
title: إضافة تأثيرات السكتة الدماغية إلى الطبقات في Aspose.PSD لـ .NET
linktitle: إضافة تأثيرات السكتة الدماغية إلى الطبقات
second_title: Aspose.PSD.NET API
description: قم بتعزيز جماليات الصورة باستخدام Aspose.PSD لـ .NET. تعلم كيفية إضافة تأثيرات السكتة الدماغية خطوة بخطوة. قم بتنزيل الإصدار التجريبي المجاني أو شراؤه أو تجربته الآن.
weight: 10
url: /ar/net/layer-effects/adding-stroke-effects/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# إضافة تأثيرات السكتة الدماغية إلى الطبقات في Aspose.PSD لـ .NET

## مقدمة

مرحبًا بك في هذا البرنامج التعليمي خطوة بخطوة حول إضافة تأثيرات الحدود إلى الطبقات في Aspose.PSD لـ .NET. يعد تحسين المظهر المرئي لصورك أمرًا سهلاً مع تأثير السكتة الدماغية، كما أن Aspose.PSD يجعلها سهلة لمطوري .NET. في هذا الدليل، سنرشدك خلال العملية، ونقدم لك خطوات وأمثلة واضحة لمساعدتك على إتقان هذه الميزة القوية.

## المتطلبات الأساسية

قبل أن نتعمق في البرنامج التعليمي، تأكد من توفر المتطلبات الأساسية التالية:

- Aspose.PSD لـ .NET: قم بتنزيل وتثبيت مكتبة Aspose.PSD من ملف .NET[موقع إلكتروني](https://releases.aspose.com/psd/net/).

- دليل المستندات: قم بإعداد دليل يحتوي على مستند PSD الذي تريد تطبيق تأثيرات الحدود عليه.

- دليل الإخراج: لديك دليل منفصل لتخزين الصور الناتجة مع تأثيرات الحدود.

- Visual Studio: تأكد من إعداد Visual Studio أو أي بيئة تطوير NET مفضلة أخرى.

## استيراد مساحات الأسماء

في مشروعك .NET، قم بتضمين مساحات الأسماء الضرورية للاستفادة من وظيفة Aspose.PSD:

```csharp
using System;
using System.IO;
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.FileFormats.Psd.Layers.FillSettings;
using Aspose.PSD.FileFormats.Psd.Layers.LayerEffects;
using Aspose.PSD.ImageLoadOptions;
using Aspose.PSD.ImageOptions;
```

## الخطوة 1: قم بتحميل مستند PSD

```csharp
string srcFile = Path.Combine(SourceDir, "AddStrokeEffect.psd");
string outputFilePng = Path.Combine(OutputDir, "AddStrokeEffect.png");

using (var psdImage = (PsdImage)Image.Load(srcFile, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    // الكود الخاص بك لتحميل مستند PSD موجود هنا
}
```

## الخطوة 2: إضافة تأثير لون السكتة الدماغية

```csharp
// يضيف تعبئة اللون، في الموضع بالداخل
strokeEffect = psdImage.Layers[1].BlendingOptions.AddStroke(FillType.Color);
strokeEffect.Size = 7;
strokeEffect.Position = StrokePosition.Inside;
colorFillSettings = strokeEffect.FillSettings as IColorFillSettings;
colorFillSettings.Color = Color.Green;
```

## الخطوة 3: الموقف الخارجي

```csharp
// يضيف تعبئة اللون، في الموضع بالخارج
strokeEffect = psdImage.Layers[2].BlendingOptions.AddStroke(FillType.Color);
strokeEffect.Size = 7;
strokeEffect.Position = StrokePosition.Outside;
colorFillSettings = strokeEffect.FillSettings as IColorFillSettings;
colorFillSettings.Color = Color.Green;
```

## الخطوة 4: موقف المركز

```csharp
// يضيف تعبئة اللون، في الموضع الأوسط
strokeEffect = psdImage.Layers[3].BlendingOptions.AddStroke(FillType.Color);
strokeEffect.Size = 7;
strokeEffect.Position = StrokePosition.Center;
colorFillSettings = strokeEffect.FillSettings as IColorFillSettings;
colorFillSettings.Color = Color.Green;
```

كرر الخطوات المشابهة للتعبئة المتدرجة والنمط، واضبط الإعدادات وفقًا لذلك.

## خاتمة

تهانينا! لقد تعلمت بنجاح كيفية إضافة تأثيرات الحدود إلى الطبقات باستخدام Aspose.PSD لـ .NET. قم بتجربة إعدادات مختلفة لتحقيق التأثير المرئي المطلوب في صورك.

## الأسئلة الشائعة

### س1: هل يمكنني تطبيق تأثيرات الحد على طبقات محددة فقط؟

ج1: نعم، يمكنك استهداف طبقات معينة عن طريق ضبط فهرس الطبقة في الكود.

### س2: هل Aspose.PSD متوافق مع أحدث إصدار من .NET Framework؟

ج2: بالتأكيد! تم تصميم Aspose.PSD للتكامل بسلاسة مع أحدث أطر عمل .NET.

### س3: كيف يمكنني تخصيص لون الحد؟

 A3: ما عليك سوى تعديل ملف`Color` خاصية في الكود لتحقيق لون الحد المطلوب.

### س 4: هل يدعم Aspose.PSD المعالجة المجمعة لملفات PSD متعددة؟

ج4: نعم، يمكنك المرور عبر ملفات PSD متعددة وتطبيق تأثير الحد باستخدام أسلوب مماثل.

### س5: هل يمكنني استخدام الإصدار التجريبي قبل شراء Aspose.PSD؟

 ج5: بالتأكيد! الاستيلاء على[تجربة مجانية](https://releases.aspose.com/) لاستكشاف إمكانيات Aspose.PSD قبل إجراء عملية الشراء.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
