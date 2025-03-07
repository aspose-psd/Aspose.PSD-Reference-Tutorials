---
title: تغيير حجم بسيط للصور في Aspose.PSD لـ .NET
linktitle: تغيير حجم الصور بشكل بسيط
second_title: Aspose.PSD.NET API
description: تغيير حجم الصورة بشكل رئيسي باستخدام Aspose.PSD لـ .NET. فعالة، سلسة، وقوية. ارفع مستوى مشروعات .NET الخاصة بك دون عناء.
weight: 17
url: /ar/net/image-manipulation/simple-resizing/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# تغيير حجم بسيط للصور في Aspose.PSD لـ .NET

## مقدمة

في المجال الديناميكي لتطوير .NET، تعد معالجة الصور ضرورة شائعة. يأتي Aspose.PSD for .NET للإنقاذ بفضل إمكاناته القوية، مما يوفر تجربة سلسة لتغيير حجم الصورة. في هذا البرنامج التعليمي، سنتعمق في العملية البسيطة والحاسمة لتغيير حجم الصور باستخدام Aspose.PSD لـ .NET. اربط حزام الأمان بينما نبدأ رحلة لتعزيز مهاراتك في معالجة الصور.

## المتطلبات الأساسية

قبل أن نتعمق في البرنامج التعليمي، دعنا نتأكد من إعداد كل شيء للحصول على تجربة سلسة:

## استيراد مساحات الأسماء

تأكد من استيراد مساحات الأسماء الضرورية للوصول إلى وظائف Aspose.PSD لـ .NET:

```csharp
using Aspose.PSD.ImageOptions;
```

الآن، دعونا نقسم عملية تغيير حجم الصور إلى خطوات متعددة:

## الخطوة 1: قم بتعيين دليل المستندات الخاص بك

ابدأ بتعيين المسار إلى دليل المستندات الخاص بك:

```csharp
string dataDir = "Your Document Directory";
```

## الخطوة 2: تحميل الصورة

قم بتحميل صورة موجودة في مثيل لفئة RasterImage:

```csharp
string sourceFile = dataDir + @"sample.psd";
using (Image image = Image.Load(sourceFile))
{
    // الرمز الخاص بك هنا
}
```

## الخطوة 3: تغيير حجم الصورة

 يعد تغيير حجم الصورة أمرًا بسيطًا مثل استدعاء ملف`Resize` الطريقة على كائن الصورة:

```csharp
image.Resize(300, 300);
```

## الخطوة 4: احفظ الصورة التي تم تغيير حجمها

احفظ الصورة التي تم تغيير حجمها بالتنسيق والخيارات المفضلة لديك. في هذا المثال، نقوم بحفظه بتنسيق JPEG:

```csharp
string destName = dataDir + @"SimpleResizing_out.jpg";
image.Save(destName, new JpegOptions());
```

وهذا كل شيء! لقد قمت بتغيير حجم الصورة بنجاح باستخدام Aspose.PSD لـ .NET.

## خاتمة

يعد إتقان تغيير حجم الصورة مهارة أساسية في مجموعة الأدوات لأي مطور .NET. مع Aspose.PSD for .NET، لا تصبح العملية فعالة فحسب، بل ممتعة أيضًا. الآن، مسلحًا بهذه المعرفة، انطلق وارفع قدراتك على معالجة الصور في مشاريع .NET الخاصة بك.

## الأسئلة الشائعة

### س1: هل يمكنني تغيير حجم الصور إلى نسبة عرض إلى ارتفاع معينة باستخدام Aspose.PSD لـ .NET؟

A1: نعم، يمكنك الحفاظ على نسبة عرض إلى ارتفاع معينة أثناء تغيير حجم الصور عن طريق ضبط العرض أو الارتفاع وفقًا لذلك.

### س2: هل يدعم Aspose.PSD for .NET تنسيقات الصور الأخرى إلى جانب JPEG؟

ج2: بالتأكيد! يدعم Aspose.PSD for .NET مجموعة متنوعة من تنسيقات الصور، بما في ذلك PNG وGIF وBMP والمزيد.

### س3: هل يتوفر ترخيص مؤقت لـ Aspose.PSD لـ .NET؟

ج3: نعم، يمكنك الحصول على ترخيص مؤقت لـ Aspose.PSD لـ .NET لتقييم إمكانياته قبل إجراء عملية شراء.

### س4: أين يمكنني العثور على وثائق شاملة لـ Aspose.PSD لـ .NET؟

 ج4: استكشف الوثائق التفصيلية على[Aspose.PSD لتوثيق .NET](https://reference.aspose.com/psd/net/).

### س5: كيف يمكنني الحصول على الدعم أو التواصل مع مجتمع Aspose.PSD لـ .NET؟

 ج5: قم بزيارة[Aspose.PSD لمنتدى .NET](https://forum.aspose.com/c/psd/34) لدعم المجتمع والمناقشات.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
