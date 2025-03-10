---
title: تدوير صورة بزاوية محددة في Aspose.PSD لـ .NET
linktitle: تدوير الصورة بزاوية محددة
second_title: Aspose.PSD.NET API
description: اكتشف قوة Aspose.PSD لـ .NET. قم بتدوير الصور بسهولة على زوايا محددة. قم بتنزيل المكتبة وابدأ في معالجة الصور بسلاسة.
weight: 16
url: /ar/net/image-manipulation/rotate-image-specific-angle/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# تدوير صورة بزاوية محددة في Aspose.PSD لـ .NET

إذا كنت تتعمق في عالم معالجة الصور باستخدام .NET، فإن Aspose.PSD يوفر حلاً قويًا. في هذا البرنامج التعليمي، سنرشدك خلال عملية تدوير الصورة بزاوية معينة باستخدام Aspose.PSD. قبل أن نتعمق في الخطوات، دعونا نهيئ المسرح بمقدمة.

## مقدمة

Aspose.PSD for .NET هي مكتبة متعددة الاستخدامات تمكن المطورين من العمل مع تنسيقات PSD والصور النقطية بسلاسة. إحدى ميزاته الرئيسية هي القدرة على تدوير الصور بزوايا دقيقة، مما يوفر المرونة في معالجة الصور. سيرشدك هذا البرنامج التعليمي خلال خطوات تدوير الصورة بزاوية معينة باستخدام Aspose.PSD لـ .NET.

## المتطلبات الأساسية

قبل أن نبدأ هذه الرحلة، تأكد من توفر المتطلبات الأساسية التالية:

-  Aspose.PSD لـ .NET Library: قم بتنزيل المكتبة وتثبيتها من ملف .NET Library[صفحة التحميل](https://releases.aspose.com/psd/net/).
- دليل المستندات: قم بإعداد دليل لتخزين ملفات المصدر والإخراج الخاصة بك.

## استيراد مساحات الأسماء

للبدء، قم باستيراد مساحات الأسماء الضرورية في مشروع .NET الخاص بك:

```csharp
using Aspose.PSD.ImageOptions;
```

الآن، دعونا نقسم المثال إلى خطوات متعددة بتنسيق دليل خطوة بخطوة.

## الخطوة 1: قم بتعيين دليل المستندات الخاص بك

```csharp
string dataDir = "Your Document Directory";
```

 يستبدل`"Your Document Directory"` مع المسار إلى الدليل حيث تقوم بتخزين ملفات المصدر والإخراج الخاصة بك.

## الخطوة 2: تحميل الصورة

```csharp
string sourceFile = dataDir + @"sample.psd";
string destName = dataDir + @"RotatingImageOnSpecificAngle_out.jpg";

using (RasterImage image = (RasterImage)Image.Load(sourceFile))
{
    // سيتم إدراج خطوات إضافية هنا
}
```

 قم بتحميل الصورة التي تريد تدويرها إلى مثيل لها`RasterImage`.

## الخطوة 3: تخزين بيانات الصورة مؤقتًا

```csharp
if (!image.IsCached)
{
    image.CacheData();
}
```

قم بتخزين بيانات الصورة مؤقتًا للحصول على أداء أفضل أثناء التدوير.

## الخطوة 4: تدوير الصورة

```csharp
image.Rotate(20f, true, Color.Red);
```

قم بتدوير الصورة بمقدار 20 درجة، مع الحفاظ على الحجم المتناسب، واستخدام خلفية حمراء.

## الخطوة 5: حفظ النتيجة

```csharp
image.Save(destName, new JpegOptions());
```

احفظ الصورة التي تم تدويرها باستخدام الخيارات المحددة (في هذه الحالة، بتنسيق JPEG).

## خاتمة

 تهانينا! لقد نجحت في تدوير صورة بزاوية معينة باستخدام Aspose.PSD لـ .NET. توفر هذه المكتبة مجموعة قوية من الأدوات لمعالجة الصور، وهذا البرنامج التعليمي هو مجرد غيض من فيض. استكشف[الوثائق](https://reference.aspose.com/psd/net/) لمزيد من الميزات والخيارات.

## الأسئلة الشائعة

### س1: هل يمكنني تدوير الصور بزوايا غير 20 درجة؟

 A1: نعم، يمكنك تخصيص معلمة الزاوية في`image.Rotate` الطريقة إلى أي قيمة مطلوبة.

### س2: هل يدعم Aspose.PSD تنسيقات الصور الأخرى إلى جانب JPEG؟

ج2: بالتأكيد! يدعم Aspose.PSD مجموعة واسعة من التنسيقات، بما في ذلك PNG وGIF وBMP وTIFF.

### س3: هل التخزين المؤقت لبيانات الصورة ضروري قبل التدوير؟

A3: على الرغم من أن التخزين المؤقت للبيانات ليس إلزاميًا، إلا أنه يمكن أن يؤدي إلى تحسين الأداء بشكل ملحوظ، خاصة بالنسبة للصور الأكبر حجمًا.

### س4: أين يمكنني الحصول على الدعم للاستعلامات المتعلقة بـ Aspose.PSD؟

 ج4: قم بزيارة[منتدى Aspose.PSD](https://forum.aspose.com/c/psd/34) لدعم المجتمع والمناقشات.

### س5: هل يمكنني تجربة Aspose.PSD قبل الشراء؟

 ج5: بالتأكيد! الاستيلاء على الخاص بك[تجربة مجانية](https://releases.aspose.com/)لاستكشاف إمكانيات المكتبة.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
