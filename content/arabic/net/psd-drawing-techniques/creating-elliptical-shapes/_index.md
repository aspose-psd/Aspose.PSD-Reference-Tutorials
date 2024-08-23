---
title: إنشاء أشكال بيضاوية باستخدام Aspose.PSD لـ .NET
linktitle: إنشاء أشكال بيضاوية باستخدام Aspose.PSD لـ .NET
second_title: Aspose.PSD.NET API
description: تعرف على كيفية رسم الأشكال البيضاوية في .NET باستخدام Aspose.PSD. دليل خطوة بخطوة مع أمثلة التعليمات البرمجية. قم بإنشاء رسومات مذهلة دون عناء.
type: docs
weight: 13
url: /ar/net/psd-drawing-techniques/creating-elliptical-shapes/
---
## مقدمة

مرحبًا بك في دليلنا الشامل حول إنشاء الأشكال البيضاوية باستخدام Aspose.PSD لـ .NET. Aspose.PSD هي مكتبة .NET قوية تسمح للمطورين بمعالجة ملفات Photoshop وتحويلها دون الحاجة إلى Adobe Photoshop. في هذا البرنامج التعليمي، سنرشدك خلال عملية رسم الأشكال البيضاوية باستخدام المكتبة.

## المتطلبات الأساسية

قبل أن نتعمق في البرنامج التعليمي، تأكد من توفر المتطلبات الأساسية التالية:

- Aspose.PSD لمكتبة .NET: تأكد من تثبيت مكتبة Aspose.PSD في مشروع .NET الخاص بك. يمكنك تنزيله من[Aspose.PSD لتوثيق .NET](https://reference.aspose.com/psd/net/).

- بيئة .NET: يفترض هذا البرنامج التعليمي أن لديك معرفة عملية بإطار عمل .NET.

## استيراد مساحات الأسماء

للبدء، قم باستيراد مساحات الأسماء الضرورية إلى مشروعك. وهذا يضمن أن لديك إمكانية الوصول إلى الفئات والأساليب المطلوبة لرسم الأشكال البيضاوية. هنا مثال:

```csharp
using Aspose.PSD.Brushes;
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.ImageOptions;
```

الآن، دعونا نقسم عملية إنشاء الأشكال البيضاوية إلى خطوات متعددة:

## الخطوة 1: إعداد دليل المستندات

```csharp
// المسار إلى دليل المستندات.
string dataDir = "Your Document Directory";
```

## الخطوة 2: إنشاء مثيل لـ BmpOptions

```csharp
// قم بإنشاء مثيل لـ BmpOptions وقم بتعيين خصائصه المختلفة
string outpath = dataDir + "Ellipse.bmp";
BmpOptions saveOptions = new BmpOptions();
saveOptions.BitsPerPixel = 32;
```

## الخطوة 3: إنشاء مثيل للصورة

```csharp
// إنشاء مثيل للصورة
using (Image image = new PsdImage(100, 100))
{
    // إنشاء وتهيئة مثيل لفئة الرسومات وسطح Clear Graphics
    Graphics graphic = new Graphics(image);
    graphic.Clear(Color.Yellow);
```

## الخطوة 4: ارسم شكل القطع الناقص المنقط

```csharp
    // ارسم شكلًا بيضاويًا منقطًا عن طريق تحديد كائن القلم ذو اللون الأحمر والمستطيل المحيط به
    graphic.DrawEllipse(new Pen(Color.Red), new Rectangle(30, 10, 40, 80));
```

## الخطوة 5: ارسم شكلًا بيضاويًا مستمرًا

```csharp
    //ارسم شكلًا بيضاويًا مستمرًا عن طريق تحديد كائن القلم الذي يحتوي على فرشاة صلبة ذات لون أزرق ومستطيل محيط به
    graphic.DrawEllipse(new Pen(new SolidBrush(Color.Blue)), new Rectangle(10, 30, 80, 40));

    // تصدير الصورة إلى تنسيق ملف bmp.
    image.Save(outpath, saveOptions);
}
```

## خاتمة

تهانينا! لقد نجحت في إنشاء أشكال بيضاوية باستخدام Aspose.PSD لـ .NET. غطى هذا البرنامج التعليمي الخطوات الأساسية، بدءًا من إعداد البيئة وحتى رسم الأشكال البيضاوية المنقطة والمستمرة.

## الأسئلة الشائعة

### س1: أين يمكنني العثور على الوثائق الخاصة بـ Aspose.PSD لـ .NET؟

 ج1: الوثائق متاحة[هنا](https://reference.aspose.com/psd/net/).

### س2: كيف يمكنني تنزيل Aspose.PSD لـ .NET؟

 ج2: يمكنك تنزيله من صفحة الإصدار[هنا](https://releases.aspose.com/psd/net/).

### س3: هل هناك نسخة تجريبية مجانية متاحة؟

 ج3: نعم، يمكنك الوصول إلى النسخة التجريبية المجانية[هنا](https://releases.aspose.com/).

### س4: كيف يمكنني الحصول على دعم Aspose.PSD لـ .NET؟

 ج4: قم بزيارة منتدى الدعم[هنا](https://forum.aspose.com/c/psd/34).

### س5: هل أحتاج إلى ترخيص مؤقت للاختبار؟

 ج5: نعم، يمكنك الحصول على ترخيص مؤقت[هنا](https://purchase.aspose.com/temporary-license/).