---
title: توسيع الصور واقتصاصها في Aspose.PSD لـ .NET
linktitle: توسيع واقتصاص الصور
second_title: Aspose.PSD.NET API
description: تعرف على كيفية توسيع الصور واقتصاصها ديناميكيًا باستخدام Aspose.PSD لـ .NET. اتبع دليلنا خطوة بخطوة لمعالجة الصور بسلاسة.
weight: 13
url: /ar/net/image-manipulation/expand-crop-images/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# توسيع الصور واقتصاصها في Aspose.PSD لـ .NET

## مقدمة

Aspose.PSD for .NET عبارة عن مكتبة تصوير شاملة تتيح للمطورين العمل مع تنسيقات صور متنوعة في تطبيقات .NET الخاصة بهم. إحدى ميزاته البارزة هي القدرة على معالجة الصور بسهولة. في هذا البرنامج التعليمي، سنركز على توسيع الصور واقتصاصها، مما يوفر لك دليلًا عمليًا لتحقيق هذه المهام باستخدام Aspose.PSD.

## المتطلبات الأساسية

قبل الغوص في البرنامج التعليمي، تأكد من توفر المتطلبات الأساسية التالية:

-  Aspose.PSD لمكتبة .NET: تأكد من تثبيت Aspose.PSD لمكتبة .NET. يمكنك تنزيله من[Aspose.PSD لوثائق .NET](https://reference.aspose.com/psd/net/).

- صورة نموذجية: قم بإعداد ملف صورة نموذجي (على سبيل المثال، "example1.psd") الذي ستستخدمه في البرنامج التعليمي.

الآن، دعونا نبدأ مع الدليل خطوة بخطوة.

## استيراد مساحات الأسماء

ابدأ باستيراد مساحات الأسماء الضرورية للاستفادة من الوظائف التي يوفرها Aspose.PSD لـ .NET. أضف مساحات الأسماء التالية إلى التعليمات البرمجية الخاصة بك:

```csharp
using Aspose.PSD.ImageOptions;
```

## الخطوة 1: إعداد المشروع

 تأكد من أن لديك مشروعًا تم إعداده باستخدام Aspose.PSD لـ .NET المتكامل. إذا لم يكن كذلك، اتبع[الوثائق](https://reference.aspose.com/psd/net/) للتوجيه.

## الخطوة 2: تحميل الصورة

قم بتحميل الصورة النموذجية باستخدام الكود التالي:

```csharp
string dataDir = RunExamples.GetDataDir_DrawingAndFormattingImages();
string sourceFile = dataDir + @"example1.psd";

// قم بتحميل الصورة
using (RasterImage rasterImage = (RasterImage)Image.Load(sourceFile))
{
    // سيتم وضع رمز إضافي لمعالجة الصور هنا
}
```

## الخطوة 3: تخزين بيانات الصورة مؤقتًا

قم بتخزين بيانات الصورة مؤقتًا لتحسين الأداء:

```csharp
rasterImage.CacheData();
```

## الخطوة 4: تحديد مستطيل الوجهة

قم بإنشاء مثيل لفئة المستطيل وحدد X وY والعرض والارتفاع للمستطيل. ستكون هذه هي المنطقة التي سيتم توسيع الصورة أو اقتصاصها.

```csharp
Rectangle destRect = new Rectangle { X = -200, Y = -200, Width = 300, Height = 300 };
```

## الخطوة 5: احفظ صورة الإخراج

احفظ الصورة الناتجة بالخيارات المحددة ومستطيل الوجهة:

```csharp
string destName = dataDir + @"jpeg_out.jpg";
rasterImage.Save(destName, new JpegOptions(), destRect);
```

## خاتمة

تهانينا! لقد تعلمت بنجاح كيفية توسيع الصور واقتصاصها باستخدام Aspose.PSD لـ .NET. تفتح هذه المكتبة القوية عالمًا من الإمكانيات لمعالجة الصور داخل تطبيقات .NET الخاصة بك.

## الأسئلة الشائعة

### س1: هل يستطيع Aspose.PSD التعامل مع تنسيقات الصور الأخرى إلى جانب PSD؟

ج1: نعم، يدعم Aspose.PSD نطاقًا واسعًا من تنسيقات الصور، بما في ذلك JPEG وPNG وGIF والمزيد.

### س2: أين يمكنني العثور على الدعم لـ Aspose.PSD؟

 ج2: يمكنك العثور على الدعم والتفاعل مع المجتمع على[منتدى Aspose.PSD](https://forum.aspose.com/c/psd/34).

### س3 هل تتوفر نسخة تجريبية مجانية من Aspose.PSD لـ .NET؟

 ج3: نعم، يمكنك استكشاف الميزات من خلال النسخة التجريبية المجانية المتاحة على[Aspose.PSD نسخة تجريبية مجانية](https://releases.aspose.com/).

### س4: كيف يمكنني الحصول على ترخيص مؤقت لـ Aspose.PSD؟

 ج4: يمكنك الحصول على ترخيص مؤقت من[Aspose.PSD الترخيص المؤقت](https://purchase.aspose.com/temporary-license/).

### س5: أين يمكنني شراء Aspose.PSD لـ .NET؟

 ج5: يمكنك شراء المكتبة من[صفحة شراء Aspose.PSD](https://purchase.aspose.com/buy).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
