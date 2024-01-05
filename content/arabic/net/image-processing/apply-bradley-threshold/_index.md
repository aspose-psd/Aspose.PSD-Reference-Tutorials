---
title: تطبيق عتبة برادلي في Aspose.PSD لـ .NET
linktitle: تطبيق عتبة برادلي
second_title: Aspose.PSD.NET API
description: تحسين تجزئة الصورة باستخدام Bradley Threshold في Aspose.PSD لـ .NET. دليل خطوة بخطوة لتحقيق الثنائية الفعالة.
type: docs
weight: 15
url: /ar/net/image-processing/apply-bradley-threshold/
---
## مقدمة

مرحبًا بك في برنامجنا التعليمي الشامل حول تطبيق Bradley Threshold في Aspose.PSD لـ .NET. Aspose.PSD for .NET هي مكتبة قوية تتيح لك العمل مع ملفات Photoshop في تطبيقات .NET الخاصة بك. تعد تقنية Bradley Thresholding تقنية تستخدم في ثنائية الصورة، مما يساعد على فصل الكائنات عن الخلفية بشكل فعال.

في هذا البرنامج التعليمي، سنرشدك خلال عملية تطبيق Bradley Threshold باستخدام Aspose.PSD لـ .NET. قبل أن نتعمق في الخطوات، تأكد من أن لديك المتطلبات الأساسية اللازمة.

## المتطلبات الأساسية

قبل البدء، تأكد من أن لديك الإعداد التالي:

-  Aspose.PSD لـ .NET Library: قم بتنزيل المكتبة وتثبيتها من ملف .NET Library[Aspose.PSD لوثائق .NET](https://reference.aspose.com/psd/net/).
- دليل المستندات: قم بإنشاء دليل لتخزين ملف PSD المصدر والصورة الثنائية الناتجة.

الآن بعد أن أصبحت المتطلبات الأساسية جاهزة، فلنتابع الدليل خطوة بخطوة.

## استيراد مساحات الأسماء

في مشروع .NET الخاص بك، تأكد من استيراد مساحات الأسماء المطلوبة للوصول إلى وظيفة Aspose.PSD:

```csharp
// استيراد مساحات أسماء Aspose.PSD
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.ImageOptions;
```

## الخطوة 1: قم بتحميل الصورة المزعجة

حدد المسار إلى ملف PSD المصدر الخاص بك ووجهة الإخراج الثنائي:

```csharp
// المسار إلى دليل المستندات.
string dataDir = "Your Document Directory";

string sourceFile = dataDir + @"sample.psd";
string destName = dataDir + @"binarized_out.png";
```

## الخطوة 2: قم بتضمين الصورة باستخدام عتبة برادلي

قم بتحميل صورة PSD، وحدد قيمة العتبة، وقم بتطبيق عتبة برادلي، واحفظ الإخراج كصورة PNG:

```csharp
// قم بتحميل صورة
using (PsdImage image = (PsdImage)Image.Load(sourceFile))
{
    //تحديد قيمة العتبة
    double threshold = 0.15;

    // قم باستدعاء أسلوب BinarizeBradley وتمرير قيمة العتبة كمعلمة
    image.BinarizeBradley(threshold);

    // احفظ الصورة الناتجة
    image.Save(destName, new PngOptions());
}
```

## خاتمة

تهانينا! لقد قمت بتطبيق Bradley Threshold بنجاح في Aspose.PSD لـ .NET. هذه التقنية لا تقدر بثمن لتعزيز تجزئة الصورة في التطبيقات المختلفة.

لا تتردد في استكشاف المزيد من الميزات والوظائف التي يوفرها Aspose.PSD لـ .NET لتحسين مهام معالجة الصور لديك.

## الأسئلة الشائعة

### س1: هل يمكنني تطبيق عتبة برادلي على أي نوع من الصور؟

A1: نعم، تعد تقنية Bradley Thresholding تقنية متعددة الاستخدامات ومناسبة لأنواع الصور المختلفة.

### س2: أين يمكنني العثور على وثائق Aspose.PSD إضافية؟

 ج2: راجع[توثيق](https://reference.aspose.com/psd/net/) للحصول على معلومات تفصيلية حول Aspose.PSD لـ .NET.

### س3: هل هناك نسخة تجريبية مجانية متاحة؟

 ج3: نعم، يمكنك استكشاف النسخة التجريبية المجانية من Aspose.PSD لـ .NET[هنا](https://releases.aspose.com/).

### س4: كيف يمكنني الحصول على الدعم لـ Aspose.PSD؟

 ج4: قم بزيارة[منتدى Aspose.PSD](https://forum.aspose.com/c/psd/34) لدعم المجتمع والمناقشات.

### س5: أين يمكنني شراء ترخيص Aspose.PSD؟

 ج5: يمكنك شراء ترخيص[هنا](https://purchase.aspose.com/buy).