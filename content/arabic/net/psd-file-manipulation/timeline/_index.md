---
title: العمل مع الجدول الزمني في Aspose.PSD لـ .NET
linktitle: العمل مع الجدول الزمني
second_title: Aspose.PSD.NET API
description: تحسين معالجة صور PSD باستخدام Aspose.PSD لفئة .NET Timeline. تحكم في خصائص الإطار وحالات الطبقة وأطلق العنان للإمكانيات الإبداعية دون عناء.
type: docs
weight: 16
url: /ar/net/psd-file-manipulation/timeline/
---
## مقدمة
في العالم الديناميكي للتصميم الجرافيكي ومعالجة الصور، تعد القدرة على التحكم في الجدول الزمني للصور ومعالجته أمرًا بالغ الأهمية. يوفر Aspose.PSD for .NET حلاً قويًا من خلال فئة الجدول الزمني الخاصة به. تمكن هذه الميزة عالية المستوى المستخدمين من إجراء تغييرات على المخطط الزمني لـ PsdImage، مثل تغيير تأخير الإطار، وتحرير حالات الطبقة على إطارات محددة، والمزيد.
## المتطلبات الأساسية
قبل التعمق في الإمكانيات المثيرة التي يقدمها فصل الجدول الزمني، تأكد من توفر المتطلبات الأساسية التالية:
-  Aspose.PSD لمكتبة .NET: تأكد من تثبيت Aspose.PSD لمكتبة .NET. يمكنك تنزيله من[Aspose.PSD لوثائق .NET](https://reference.aspose.com/psd/net/).
-  أدلة المستندات والإخراج: حدد مسارات المستندات وأدلة الإخراج في التعليمات البرمجية. أضبط ال`baseDir` و`outputDir` المتغيرات وفقا لهيكل المشروع الخاص بك.
الآن، دعونا نستكشف كيفية الاستفادة من فئة الجدول الزمني خطوة بخطوة.
## استيراد مساحات الأسماء
لبدء العمل مع فئة Timeline، قم باستيراد مساحات الأسماء الضرورية في التعليمات البرمجية الخاصة بك:
```csharp
using System;
using System.Collections.Generic;
using System.IO;
using Aspose.PSD.FileFormats.Core.Blending;
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.FileFormats.Psd.Layers.Animation;
```
## الخطوة 1: تحميل صورة PSD
ابدأ بتحميل صورة PSD من الملف المصدر المحدد. تأكد من ضبط مسار الملف المصدر بشكل صحيح:
```csharp
string sourceFile = Path.Combine(baseDir, "image1219.psd");
using (PsdImage psdImage = (PsdImage)Image.Load(sourceFile))
{
    //الكود الخاص بك لمزيد من العمليات يذهب هنا
}
```
## الخطوة 2: الوصول إلى الجدول الزمني
بمجرد تحميل صورة PSD، قم بالوصول إلى المخطط الزمني باستخدام الكود التالي:
```csharp
Timeline timeline = psdImage.Timeline;
```
## الخطوة 3: تغيير طريقة التخلص
التعامل مع طريقة التخلص من إطار معين. في هذا المثال، قمنا بتغيير طريقة التخلص من الإطار 1:
```csharp
timeline.Frames[0].DisposalMethod = FrameDisposalMethod.DoNotDispose;
```
## الخطوة 4: ضبط تأخير الإطار
تعديل تأخير إطار معين. وهنا نقوم بتغيير تأخير الإطار 2 إلى 15:
```csharp
timeline.Frames[1].Delay = 15;
```
## الخطوة 5: تحرير حالة الطبقة
قم بتغيير عتامة "الطبقة الأولى" في إطار معين. في هذه الحالة، قمنا بتعيين العتامة إلى 50 في الإطار 2:
```csharp
LayerState layerState11 = timeline.Frames[1].LayerStates[1];
layerState11.Opacity = 50;
```
## الخطوة 6: نقل الطبقة
انقل "الطبقة 1" إلى الزاوية اليسرى السفلية في إطار محدد (الإطار 3 في هذا المثال):
```csharp
LayerState layerState21 = timeline.Frames[2].LayerStates[1];
layerState21.PositionOffset = new Point(-50, 230);
```
## الخطوة 7: إضافة إطار جديد
أضف إطارًا جديدًا إلى المخطط الزمني:
```csharp
List<Frame> frames = new List<Frame>(timeline.Frames);
frames.Add(new Frame());
timeline.Frames = frames.ToArray();
```
## الخطوة 8: تغيير وضع المزج
قم بتغيير وضع المزج لـ "الطبقة 1" في إطار محدد (الإطار 4 في هذه الحالة):
```csharp
LayerState layerState31 = timeline.Frames[3].LayerStates[1];
layerState31.BlendMode = BlendMode.Dissolve;
```
## الخطوة 9: حفظ التغييرات
قم بتطبيق التغييرات مرة أخرى على مثيل PsdImage واحفظ صورة PSD المعدلة:
```csharp
psdImage.Save(outputPsd);
```
## الخطوة 10: التنظيف
وأخيرًا، قم بالتنظيف عن طريق حذف ملف الإخراج المؤقت:
```csharp
File.Delete(outputPsd);
```
## خاتمة

في الختام، فإن فئة الجدول الزمني في Aspose.PSD لـ .NET تمكن المطورين من التحكم الدقيق في الجدول الزمني لصور PSD. من خلال سلسلة من الخطوات البسيطة، يمكنك التعامل مع خصائص الإطار وحالات الطبقة والمزيد، مما يفتح عالمًا من الإمكانيات الإبداعية.

## الأسئلة الشائعة

### س1: هل Aspose.PSD for .NET مناسب للمبتدئين؟

ج1: بالتأكيد! يوفر Aspose.PSD for .NET واجهة سهلة الاستخدام ووثائق شاملة، مما يجعله في متناول المبتدئين والمطورين المتمرسين.

### س2: هل يمكنني تطبيق تغييرات المخطط الزمني على صور GIF؟

ج2: تم تصميم فئة المخطط الزمني خصيصًا لصور PSD. لمعالجة ملفات GIF، راجع Aspose.GIF لـ .NET.

### س3: أين يمكنني العثور على دعم إضافي أو مناقشة المشكلات؟

 ج3: قم بزيارة[منتدى Aspose.PSD](https://forum.aspose.com/c/psd/34) لدعم المجتمع ومناقشة القضايا.

### س4: كيف يمكنني الحصول على ترخيص مؤقت لـ Aspose.PSD لـ .NET؟

 ج4: الحصول على ترخيص مؤقت[هنا](https://purchase.aspose.com/temporary-license/).

### س5: ما هي الفوائد الأساسية لاستخدام Aspose.PSD لـ .NET؟

ج5: يوفر Aspose.PSD for .NET إمكانات معالجة الصور المتقدمة ومعالجة ملفات PSD والعرض عالي الأداء.