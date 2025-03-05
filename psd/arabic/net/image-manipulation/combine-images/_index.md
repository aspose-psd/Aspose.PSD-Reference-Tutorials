---
title: دمج الصور في Aspose.PSD لـ .NET
linktitle: الجمع بين الصور
second_title: Aspose.PSD.NET API
description: قم بدمج الصور بسهولة في .NET باستخدام Aspose.PSD. اتبع برنامجنا التعليمي خطوة بخطوة لمعالجة الصور بسلاسة.
type: docs
weight: 10
url: /ar/net/image-manipulation/combine-images/
---
## مقدمة

مرحبًا بك في برنامجنا التعليمي خطوة بخطوة حول دمج الصور باستخدام Aspose.PSD لـ .NET! Aspose.PSD هي مكتبة .NET قوية تتيح للمطورين العمل مع ملفات Adobe Photoshop بسلاسة. في هذا البرنامج التعليمي، سنرشدك خلال عملية دمج الصور باستخدام Aspose.PSD، ونزودك بأمثلة عملية وخطوات تفصيلية.

## المتطلبات الأساسية

قبل أن نتعمق في البرنامج التعليمي، تأكد من توفر المتطلبات الأساسية التالية:

-  مكتبة Aspose.PSD: تأكد من تثبيت مكتبة Aspose.PSD. يمكنك تنزيله من[هنا](https://releases.aspose.com/psd/net/).

الآن، دعونا نتعمق في البرنامج التعليمي!

## استيراد مساحات الأسماء

أولاً، تحتاج إلى استيراد مساحات الأسماء الضرورية للعمل مع Aspose.PSD. أضف مقتطف التعليمات البرمجية التالي في بداية ملف .NET الخاص بك:

```csharp
using Aspose.PSD.ImageOptions;
using Aspose.PSD.Sources;
```

## الخطوة 1: إعداد البيئة

ابدأ بإعداد البيئة وتحديد الدليل لصورك.

```csharp
// المسار إلى دليل المستندات.
string dataDir = RunExamples.GetDataDir_DrawingAndFormattingImages();
```

## الخطوة 2: إنشاء مثيل PsdOptions

قم بإنشاء مثيل لـ PsdOptions، وقم بتعيين خصائصه حسب الحاجة.

```csharp
PsdOptions imageOptions = new PsdOptions();
```

## الخطوة 3: إنشاء FileCreateSource

قم بإنشاء مثيل FileCreateSource وقم بتعيينه إلى خاصية المصدر الخاصة بـ imageOptions.

```csharp
imageOptions.Source = new FileCreateSource(dataDir + "Two_images_result_out.psd", false);
```

## الخطوة 4: إنشاء مثيل الصورة

قم بإنشاء مثيل للصورة وحدد حجم اللوحة القماشية.

```csharp
using (var image = Image.Create(imageOptions, 600, 600))
```

## الخطوة 5: تهيئة الرسومات ورسم الصور

قم بتهيئة مثيل للرسومات، وقم بمسح سطح الصورة باللون الأبيض، ثم ارسم الصور على اللوحة القماشية.

```csharp
var graphics = new Graphics(image);
graphics.Clear(Color.White);
graphics.DrawImage(Image.Load(dataDir + "example1.psd"), 0, 0, 300, 600);
graphics.DrawImage(Image.Load(dataDir + "example2.psd"), 300, 0, 300, 600);
```

## الخطوة 6: احفظ الصورة المدمجة

احفظ الصورة المدمجة النهائية.

```csharp
image.Save();
```

تهانينا! لقد نجحت في دمج صورتين باستخدام Aspose.PSD لـ .NET.

## خاتمة

في هذا البرنامج التعليمي، قمنا بإرشادك خلال عملية دمج الصور باستخدام Aspose.PSD. بفضل واجهة برمجة التطبيقات (API) البديهية، يعمل Aspose.PSD على تمكين المطورين من التعامل مع ملفات Photoshop بسلاسة في تطبيقات .NET الخاصة بهم.

## الأسئلة الشائعة

### س1: هل Aspose.PSD متوافق مع كافة إصدارات .NET؟

ج1: نعم، Aspose.PSD متوافق مع كافة إصدارات .NET، مما يضمن تعدد الاستخدامات في مشاريع التطوير الخاصة بك.

### س2: هل يمكنني استخدام Aspose.PSD لأغراض تجارية؟

ج2: نعم، يمكن استخدام Aspose.PSD للأغراض الشخصية والتجارية. التحقق من تفاصيل الترخيص[هنا](https://purchase.aspose.com/buy).

### س3: كيف يمكنني الحصول على الدعم لـ Aspose.PSD؟

 ج3: قم بزيارة[منتدى Aspose.PSD](https://forum.aspose.com/c/psd/34) للحصول على دعم المجتمع أو فكر في شراء خطة دعم.

### س4: هل هناك نسخة تجريبية مجانية متاحة لـ Aspose.PSD؟

 ج4: نعم، يمكنك الوصول إلى النسخة التجريبية المجانية[هنا](https://releases.aspose.com/).

### س5: هل يمكنني الحصول على ترخيص مؤقت لـ Aspose.PSD؟

ج5: نعم، يمكنك الحصول على ترخيص مؤقت[هنا](https://purchase.aspose.com/temporary-license/).