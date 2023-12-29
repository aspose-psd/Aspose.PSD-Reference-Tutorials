---
title: ضبط عتامة تأثير الظل في Aspose.PSD لـ .NET
linktitle: ضبط عتامة تأثير الظل
second_title: Aspose.PSD.NET API
description: تعرف على كيفية ضبط عتامة تأثير الظل في Aspose.PSD لـ .NET باستخدام هذا البرنامج التعليمي الشامل.
type: docs
weight: 15
url: /ar/net/layer-effects/adjusting-shadow-effect-opacity/
---
## مقدمة

مرحبًا بك في دليلنا خطوة بخطوة حول ضبط عتامة تأثير الظل في Aspose.PSD لـ .NET! في هذا البرنامج التعليمي، سنرشدك خلال عملية استخدام خاصية العتامة في DropShadowEffect. Aspose.PSD for .NET هي مكتبة قوية تتيح لك العمل مع ملفات PSD في تطبيقات .NET الخاصة بك بسلاسة.

## المتطلبات الأساسية

قبل أن نتعمق في البرنامج التعليمي، تأكد من أن لديك ما يلي:

-  Aspose.PSD لمكتبة .NET: تأكد من تثبيت Aspose.PSD لمكتبة .NET في مشروعك. يمكنك تنزيله[هنا](https://releases.aspose.com/psd/net/).

- دليل المستندات: قم بإعداد دليل لملف PSD المدخل الخاص بك.

- دليل الإخراج: قم بإنشاء دليل حيث سيتم حفظ الصور الناتجة.

## استيراد مساحات الأسماء

في مشروع .NET الخاص بك، تأكد من استيراد مساحات الأسماء الضرورية:

```csharp
using System;
using System.IO;
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.FileFormats.Psd.Layers;
using Aspose.PSD.FileFormats.Psd.Layers.LayerEffects;
using Aspose.PSD.ImageOptions;
```

## الخطوة 1: قم بتحميل ملف PSD

ابدأ بتحميل ملف PSD الخاص بك باستخدام ملف`Image.Load` طريقة:

```csharp
string inputFile = Path.Combine(baseDir, "input.psd");
using (PsdImage psdImage = (PsdImage)Image.Load(inputFile, new LoadOptions()))
{
    // الكود الخاص بك لمزيد من المعالجة موجود هنا
}
```

## الخطوة 2: الوصول إلى الطبقة وإضافة تأثير الظل المسقط

استرجع الطبقة المطلوبة من ملف PSD وأضف تأثير الظل المسقط:

```csharp
Layer workLayer = psdImage.Layers[1];
DropShadowEffect dropShadowEffect = workLayer.BlendingOptions.AddDropShadow();
dropShadowEffect.Distance = 0;
dropShadowEffect.Size = 8;
```

## الخطوة 3: ضبط العتامة وحفظ الصور

الآن، اضبط خاصية العتامة واحفظ الصور بدرجات عتامة مختلفة:

```csharp
// مثال مع العتامة = 20
dropShadowEffect.Opacity = 20;
psdImage.Save(outputImage20, new PngOptions());

// مثال مع العتامة = 200
dropShadowEffect.Opacity = 200;
psdImage.Save(outputImage200, new PngOptions());
```

## الخطوة 4: التنظيف

بعد حفظ الصور، قم بالتنظيف عن طريق حذف الملفات المؤقتة:

```csharp
File.Delete(outputImage20);
File.Delete(outputImage200);
```

## خاتمة

تهانينا! لقد نجحت في ضبط عتامة تأثير الظل في Aspose.PSD لـ .NET. يوفر هذا البرنامج التعليمي دليلاً مباشرًا لتحسين صور PSD الخاصة بك باستخدام درجات عتامة الظل المختلفة.

## الأسئلة الشائعة

### س1: هل يمكنني تطبيق هذا البرنامج التعليمي على تنسيقات الصور الأخرى؟

ج1: لا، يغطي هذا البرنامج التعليمي تحديدًا ضبط عتامة تأثير الظل في ملفات PSD باستخدام Aspose.PSD لـ .NET.

### س2: هل هناك خصائص ظل إضافية يمكن تعديلها؟

ج٢: نعم، يقدم Aspose.PSD for .NET خصائص متنوعة لضبط تأثيرات الظل.

### س3: كيف يمكنني الحصول على ترخيص مؤقت لـ Aspose.PSD لـ .NET؟

 ج3: يمكنك الحصول على ترخيص مؤقت[هنا](https://purchase.aspose.com/temporary-license/).

### س 4: هل Aspose.PSD لـ .NET متوافق مع .NET Core؟

ج4: نعم، Aspose.PSD for .NET متوافق مع كل من .NET Framework و.NET Core.

### س5: أين يمكنني العثور على دعم المجتمع لـ Aspose.PSD لـ .NET؟

 ج5: قم بزيارة[منتديات Aspose.PSD](https://forum.aspose.com/c/psd/34) لدعم المجتمع والمناقشات.