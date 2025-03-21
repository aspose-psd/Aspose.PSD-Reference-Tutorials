---
title: طمس صورة في Aspose.PSD لـ .NET
linktitle: عدم وضوح الصورة
second_title: Aspose.PSD.NET API
description: تعرف على كيفية تعتيم الصور بسهولة باستخدام Aspose.PSD لـ .NET. دليل خطوة بخطوة لمعالجة الصور بسلاسة في مشاريع C# الخاصة بك.
weight: 13
url: /ar/net/image-adjustment/blur-image/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# طمس صورة في Aspose.PSD لـ .NET

## مقدمة

في مجال تطوير .NET، يثبت Aspose.PSD أنه حليف قوي لمعالجة الصور. يركز هذا البرنامج التعليمي على مهمة محددة: طمس الصورة باستخدام Aspose.PSD لـ .NET. إذا كنت حريصًا على تحسين مهارات معالجة الصور لديك أو تبحث ببساطة عن طريقة فعالة لطمس الصور برمجيًا، فأنت في المكان الصحيح.

## المتطلبات الأساسية

قبل الغوص في البرنامج التعليمي، تأكد من توفر المتطلبات الأساسية التالية:

-  Aspose.PSD لـ .NET: تأكد من تثبيت مكتبة Aspose.PSD. يمكنك تنزيله من[هنا](https://releases.aspose.com/psd/net/).

- بيئة التطوير: قم بإعداد بيئة تطوير .NET، واحصل على فهم أساسي لـ C#.

- صورة عينة: قم بإعداد صورة عينة بتنسيق PSD. يمكنك استخدام واحدة خاصة بك أو تنزيلها للاختبار.

## استيراد مساحات الأسماء

ابدأ باستيراد مساحات الأسماء الضرورية في كود C# الخاص بك:

```csharp
using Aspose.PSD.ImageFilters.FilterOptions;
using Aspose.PSD.ImageOptions;
```

## الخطوة 1: تحديد دليل المستندات الخاص بك

```csharp
// المسار إلى دليل المستندات.
string dataDir = "Your Document Directory";
```

## الخطوة 2: تحميل الصورة

```csharp
//ExStart:BluranImage

string sourceFile = dataDir + @"sample.psd";

// قم بتحميل صورة موجودة في مثيل لفئة RasterImage
using (var image = Image.Load(sourceFile))
{
    // تابع إلى الخطوات التالية ضمن كتلة الاستخدام هذه
}
```

## الخطوة 3: تحويل الصورة إلى RasterImage

```csharp
RasterImage rasterImage = (RasterImage)image;
```

## الخطوة 4: تطبيق مرشح التمويه الضبابي

```csharp
rasterImage.Filter(rasterImage.Bounds, new GaussianBlurFilterOptions(15, 15));
```

 هنا،`GaussianBlurFilterOptions` يتم استخدام الفئة بنصف قطر محدد يبلغ 15 لكل من التمويه الأفقي والرأسي.

## الخطوة 5: احفظ الصورة غير الواضحة

```csharp
string destName = dataDir + @"BlurAnImage_out.gif";
rasterImage.Save(destName, new GifOptions());
```

## خاتمة

تهانينا! لقد نجحت في تعتيم الصورة باستخدام Aspose.PSD لـ .NET. يوفر هذا البرنامج التعليمي لمحة عن إمكانيات Aspose.PSD ويفتح الباب أمام عدد لا يحصى من إمكانيات معالجة الصور في تطبيقات .NET الخاصة بك.

## الأسئلة الشائعة

### س1: هل يمكنني تطبيق درجات تمويه مختلفة على أجزاء مختلفة من الصورة؟

ج1: نعم، يسمح لك Aspose.PSD بتطبيق مرشحات ذات معلمات مختلفة على مناطق معينة من الصورة، مما يوفر تحكمًا دقيقًا في عملية التمويه.

### س2: هل Aspose.PSD متوافق مع جميع تنسيقات الصور؟

ج2: بينما يدعم Aspose.PSD نطاقًا واسعًا من تنسيقات الصور، فمن المستحسن مراجعة الوثائق للحصول على القائمة الكاملة وأي اعتبارات خاصة بالتنسيق.

### س3: كيف يمكنني الحصول على ترخيص مؤقت لـ Aspose.PSD؟

 ج3: يمكنك الحصول على ترخيص مؤقت من[هنا](https://purchase.aspose.com/temporary-license/) لأغراض الاختبار والتقييم.

### س4: هل توجد ميزات أخرى لمعالجة الصور في Aspose.PSD؟

ج4: بالتأكيد! يقدم Aspose.PSD مجموعة شاملة من الميزات، بما في ذلك تغيير الحجم والاقتصاص وتعديل الألوان. استكشف الوثائق للحصول على قائمة كاملة.

### س5: أين يمكنني طلب المساعدة أو التواصل مع مجتمع Aspose.PSD؟

 ج5: إذا كانت لديك أية استفسارات أو مناقشات، توجه إلى[منتدى Aspose.PSD](https://forum.aspose.com/c/psd/34).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
