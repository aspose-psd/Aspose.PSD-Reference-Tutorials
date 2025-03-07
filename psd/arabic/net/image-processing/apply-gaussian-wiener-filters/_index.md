---
title: تطبيق مرشحات Gaussian وWiener في Aspose.PSD لـ .NET
linktitle: تطبيق المرشحات غاوس و وينر
second_title: Aspose.PSD.NET API
description: قم بتحسين جودة الصورة بسهولة باستخدام Aspose.PSD لـ .NET. قم بتطبيق مرشحات Gaussian وWiener لتقليل الضوضاء والحصول على المظهر البصري الأمثل.
weight: 10
url: /ar/net/image-processing/apply-gaussian-wiener-filters/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# تطبيق مرشحات Gaussian وWiener في Aspose.PSD لـ .NET

## مقدمة

في مجال معالجة الصور باستخدام .NET، يبرز Aspose.PSD كمجموعة أدوات قوية تمكن المطورين من معالجة الصور بسهولة. إحدى الميزات المفيدة بشكل خاص هي تطبيق مرشحات Gaussian وWiener. تلعب هذه المرشحات دورًا حاسمًا في تحسين جودة الصورة وتقليل الضوضاء وضمان الجاذبية البصرية المثالية.

## المتطلبات الأساسية

قبل الخوض في تطبيق مرشحات Gaussian وWiener باستخدام Aspose.PSD، تأكد من توفر المتطلبات الأساسية التالية:

1. Aspose.PSD لـ .NET: قم بتنزيل المكتبة وتثبيتها من ملف[Aspose.PSD لوثائق .NET](https://reference.aspose.com/psd/net/).

2. صورة عينة: قم بإعداد صورة عينة بتنسيق PSD للتجريب. يمكنك العثور على نماذج الصور في وثائق Aspose.PSD.

3. بيئة التطوير المتكاملة (IDE): قم بتثبيت بيئة تطوير متكاملة متوافقة مع .NET على نظامك، مثل Visual Studio، لتنفيذ مقتطفات التعليمات البرمجية المتوفرة في هذا البرنامج التعليمي بسلاسة.

## استيراد مساحات الأسماء

ابدأ باستيراد مساحات الأسماء الضرورية للاستفادة من وظائف Aspose.PSD لـ .NET:

```csharp
using Aspose.PSD.ImageFilters.FilterOptions;
using Aspose.PSD.ImageOptions;
```

## الخطوة 1: قم بتحميل الصورة المزعجة

لتطبيق مرشحات Gaussian وWiener، ابدأ بتحميل الصورة المزعجة إلى تطبيق .NET الخاص بك:

```csharp
// المسار إلى دليل المستندات.
string dataDir = "Your Document Directory";

string sourceFile = dataDir + @"sample.psd";

// تحميل الصورة الصاخبة
using (Image image = Image.Load(sourceFile))
{
    // رمز لمزيد من المعالجة سوف تذهب هنا
}
```

## الخطوة 2: تحويل إلى RasterImage

 تحويل الصورة المحملة إلى`RasterImage` للتوافق مع المرشحات:

```csharp
RasterImage rasterImage = image as RasterImage;
if (rasterImage == null)
{
    return;
}
```

## الخطوة 3: إنشاء خيارات تصفية Gaussian وWiener

 إنشاء مثيل لـ`GaussWienerFilterOptions` فئة، وتحديد حجم نصف القطر والقيمة السلسة:

```csharp
GaussWienerFilterOptions options = new GaussWienerFilterOptions(12, 3);
options.Grayscale = true;
```

## الخطوة 4: تطبيق المرشحات

 قم بتطبيق خيارات التصفية التي تم إنشاؤها على`RasterImage` هدف:

```csharp
rasterImage.Filter(image.Bounds, options);
```

## الخطوة 5: احفظ الصورة الناتجة

احفظ الصورة التي تمت تصفيتها بالتنسيق المطلوب. في هذا المثال، نحفظه بتنسيق GIF:

```csharp
string destName = dataDir + @"gauss_wiener_out.gif";
image.Save(destName, new GifOptions());
```

## خاتمة

تهانينا! لقد نجحت في تطبيق مرشحات Gaussian وWiener لتحسين جودة صورتك باستخدام Aspose.PSD لـ .NET. تثبت هذه المرشحات أنها لا تقدر بثمن في سيناريوهات مختلفة، بدءًا من تقليل الضوضاء في الصور الفوتوغرافية وحتى تحسين العناصر الرسومية في مشاريع التصميم.

## الأسئلة الشائعة

### س1: هل يمكنني تطبيق هذه المرشحات على الصور بتنسيقات أخرى إلى جانب PSD؟

A1: نعم، يدعم Aspose.PSD تنسيقات الصور المختلفة، بما في ذلك PSD وBMP وJPEG وPNG والمزيد.

### س2: ما أهمية حجم نصف القطر والقيمة السلسة في خيارات التصفية؟

A2: يحدد حجم نصف القطر المنطقة التي يعمل عليها المرشح، بينما تؤثر القيمة الناعمة على مستوى التجانس المطبق على الصورة.

### س3: كيف يمكنني الحصول على ترخيص مؤقت لـ Aspose.PSD؟

 ج3: يمكنك الحصول على ترخيص مؤقت من[Aspose.PSD صفحة الترخيص المؤقتة](https://purchase.aspose.com/temporary-license/).

### س4: أين يمكنني العثور على دعم ومساعدة إضافيين؟

 ج4: لأية استفسارات أو مساعدة، قم بزيارة[منتدى Aspose.PSD](https://forum.aspose.com/c/psd/34).

### س5: هل تتوفر نسخة تجريبية مجانية من Aspose.PSD؟

 ج5: نعم، يمكنك استكشاف ميزات Aspose.PSD عن طريق تنزيل الملف[نسخة تجريبية مجانية](https://releases.aspose.com/).

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
