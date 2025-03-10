---
title: تدوير صورة في Aspose.PSD لـ .NET
linktitle: تدوير الصورة
second_title: Aspose.PSD.NET API
description: تعلم كيفية تدوير الصور بسهولة في .NET باستخدام Aspose.PSD. اتبع البرنامج التعليمي خطوة بخطوة.
weight: 15
url: /ar/net/image-manipulation/rotate-image/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# تدوير صورة في Aspose.PSD لـ .NET

## مقدمة

إذا كنت تغوص في عالم معالجة الصور باستخدام .NET، فإن Aspose.PSD هو أداتك المفضلة لمعالجة الصور بسلاسة وكفاءة. في هذا البرنامج التعليمي، سوف نركز على مهمة أساسية – وهي تدوير الصورة باستخدام Aspose.PSD لـ .NET. تابع معنا بينما نقوم بتقسيم العملية إلى خطوات بسيطة وقابلة للتنفيذ.

## المتطلبات الأساسية

قبل أن نبدأ، تأكد من توفر المتطلبات الأساسية التالية:

-  Aspose.PSD لـ .NET Library: قم بتنزيل المكتبة وتثبيتها من ملف .NET Library[وثائق Aspose.PSD .NET](https://reference.aspose.com/psd/net/).

- دليل المستندات الخاص بك: قم بإعداد دليل حيث يتم تخزين الصور الخاصة بك. استبدل "دليل المستندات الخاص بك" في مقتطف الشفرة بالمسار إلى هذا الدليل.

## استيراد مساحات الأسماء

تأكد من تضمين مساحات الأسماء الضرورية للوصول إلى وظيفة Aspose.PSD. أضف الأسطر التالية في بداية مشروع .NET الخاص بك:

```csharp
using Aspose.PSD.ImageOptions;
```

## الخطوة 1: تحميل الصورة

```csharp
string sourceFile = dataDir + @"sample.psd";

// قم بتحميل صورة موجودة في مثيل لفئة RasterImage
using (Image image = Image.Load(sourceFile))
{
```

## الخطوة 2: تدوير الصورة

```csharp
    // قم بتدوير الصورة 270 درجة في اتجاه عقارب الساعة
    image.RotateFlip(RotateFlipType.Rotate270FlipNone);
```

## الخطوة 3: احفظ الصورة التي تم تدويرها

```csharp
    // احفظ الصورة التي تم تدويرها كملف JPEG
    string destName = dataDir + @"RotatingAnImage_out.jpg";
    image.Save(destName, new JpegOptions());
}
```

هذا كل شيء! باستخدام بضعة أسطر من التعليمات البرمجية، نجحت في تدوير الصورة باستخدام Aspose.PSD لـ .NET.

## خاتمة

في هذا البرنامج التعليمي، اكتشفنا أساسيات تدوير الصور باستخدام Aspose.PSD لـ .NET. يوفر Aspose.PSD مجموعة قوية من الأدوات لمعالجة الصور، مما يجعله مكتبة أساسية لمطوري .NET. قم بتجربة دورات مختلفة واستكشف المزيد من الإمكانات لتحسين سير عمل معالجة الصور لديك.

## الأسئلة الشائعة

### س1: هل يمكنني تدوير الصور بزاوية مخصصة باستخدام Aspose.PSD؟

 نعم، يتيح لك Aspose.PSD تحديد زاوية مخصصة للتدوير. ببساطة استبدل`RotateFlipType.Rotate270FlipNone` يتماشى مع زاوية الدوران المطلوبة.

### س2: هل Aspose.PSD متوافق مع تنسيقات الصور المختلفة؟

 قطعاً. يدعم Aspose.PSD مجموعة واسعة من تنسيقات الصور، بما في ذلك PSD وJPEG وPNG والمزيد. تحقق من[الوثائق](https://reference.aspose.com/psd/net/) للحصول على القائمة الكاملة.

### س3: كيف يمكنني الحصول على ترخيص مؤقت لـ Aspose.PSD؟

 قم بزيارة[صفحة الترخيص المؤقتة](https://purchase.aspose.com/temporary-license/) على موقع Aspose للحصول على ترخيص مؤقت لأغراض التقييم.

### س4: أين يمكنني العثور على الدعم لـ Aspose.PSD؟

 لأية استفسارات أو مساعدة، قم بزيارة[منتدى Aspose.PSD](https://forum.aspose.com/c/psd/34) والتواصل مع المجتمع.

### س5: هل يمكنني شراء Aspose.PSD للاستخدام التجاري؟

 بالتأكيد. استكشف[صفحة الشراء](https://purchase.aspose.com/buy) للحصول على ترخيص يناسب احتياجاتك.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
