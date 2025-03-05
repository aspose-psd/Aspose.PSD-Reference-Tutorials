---
title: إضافة تأثيرات في وقت التشغيل في Aspose.PSD لـ .NET
linktitle: إضافة تأثيرات في وقت التشغيل
second_title: Aspose.PSD.NET API
description: اكتشف تحسينات الصورة الديناميكية باستخدام Aspose.PSD لـ .NET. أضف التأثيرات في وقت التشغيل بسهولة.
type: docs
weight: 10
url: /ar/net/image-effects/add-effect-runtime/
---
## مقدمة

يعد تعزيز المظهر المرئي للصور متطلبًا شائعًا في تطبيقات التصميم الجرافيكي ومعالجة الصور. في هذا البرنامج التعليمي، سوف نستكشف كيفية إضافة تأثيرات في وقت التشغيل باستخدام Aspose.PSD لـ .NET. Aspose.PSD عبارة عن واجهة برمجة تطبيقات قوية تتيح للمطورين العمل مع ملفات Adobe Photoshop بسلاسة. 

## المتطلبات الأساسية

قبل أن نتعمق في الدليل التفصيلي، تأكد من أن لديك ما يلي:

- المعرفة الأساسية بـ C# و.NET Framework.
-  تم تثبيت Aspose.PSD لـ .NET. يمكنك تنزيله من[هنا](https://releases.aspose.com/psd/net/).

## استيراد مساحات الأسماء

للبدء، تأكد من تضمين مساحات الأسماء الضرورية في مشروع C# الخاص بك. تعتبر مساحات الأسماء هذه حيوية للاستفادة من الوظائف التي يوفرها Aspose.PSD.

```csharp
using Aspose.PSD.FileFormats.Core.Blending;
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.ImageLoadOptions;
```

## الخطوة 1: قم بإعداد دليل المستندات الخاص بك

```csharp
string dataDir = "Your Document Directory";
```

استبدل "دليل المستندات الخاص بك" بالمسار الفعلي الذي توجد به ملفات PSD الخاصة بك.

## الخطوة 2: قم بتحميل صورة PSD باستخدام موارد التأثيرات

```csharp
string sourceFileName = dataDir + "ThreeRegularLayers.psd";
string exportPath = dataDir + "ThreeRegularLayersChanged.psd";

var loadOptions = new PsdLoadOptions()
{
    LoadEffectsResource = true
};

using (var im = (PsdImage)Image.Load(sourceFileName, loadOptions))
```

تقوم هذه الخطوة بتحميل صورة PSD، مما يتيح تحميل موارد التأثيرات.

## الخطوة 3: إضافة تأثير طبقة تراكب اللون

```csharp
var effect = im.Layers[1].BlendingOptions.AddColorOverlay();
effect.Color = Color.Green;
effect.Opacity = 128;
effect.BlendMode = BlendMode.Normal;
```

هنا، نضيف تأثير تراكب الألوان إلى الطبقة الثانية من صورة PSD. يمكنك تخصيص اللون والعتامة ووضع المزج وفقًا لتفضيلاتك.

## الخطوة 4: احفظ الصورة المعدلة

```csharp
im.Save(exportPath);
```

وأخيرًا، احفظ الصورة بالتأثير المطبق على مسار التصدير المحدد.

## خاتمة

تعد إضافة التأثيرات في وقت التشغيل في Aspose.PSD لـ .NET عملية مباشرة. باستخدام بضعة أسطر فقط من التعليمات البرمجية، يمكنك تحسين المظهر المرئي لصورك ديناميكيًا. قم بتجربة تأثيرات ومعايير مختلفة لتحقيق النتائج المرجوة.

## الأسئلة الشائعة

### س1: هل Aspose.PSD متوافق مع أحدث إصدار من .NET Framework؟

ج1: نعم، يتم تحديث Aspose.PSD بانتظام لضمان التوافق مع أحدث إصدارات إطار عمل .NET.

### س2: هل يمكنني تطبيق تأثيرات متعددة على طبقة واحدة؟

ج2: بالتأكيد! يمكنك ربط تأثيرات متعددة على الطبقة لإنشاء تحسينات مرئية معقدة.

### س3: هل هناك أي قيود على أنواع التأثيرات التي يمكنني إضافتها؟

ج3: يوفر Aspose.PSD نطاقًا واسعًا من التأثيرات، ولكن يُنصح بمراجعة الوثائق للحصول على تفاصيل محددة حول التأثيرات المدعومة.

### س4: كيف يمكنني الحصول على ترخيص مؤقت لأغراض الاختبار؟

 ج4: يمكنك الحصول على ترخيص مؤقت[هنا](https://purchase.aspose.com/temporary-license/) للاختبار والتقييم.

### س5: أين يمكنني العثور على دعم إضافي ومناقشات مجتمعية؟

 ج5: قم بزيارة[منتدى Aspose.PSD](https://forum.aspose.com/c/psd/34) للدعم والمناقشات.