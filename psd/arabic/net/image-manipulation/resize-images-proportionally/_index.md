---
title: تغيير حجم الصور بشكل متناسب في Aspose.PSD لـ .NET
linktitle: تغيير حجم الصور بشكل متناسب
second_title: Aspose.PSD.NET API
description: اكتشف تغيير حجم الصورة بسلاسة باستخدام Aspose.PSD لـ .NET. قم بتنزيل المكتبة، واتبع برنامجنا التعليمي، وعزز قدرات معالجة الصور لديك.
weight: 14
url: /ar/net/image-manipulation/resize-images-proportionally/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# تغيير حجم الصور بشكل متناسب في Aspose.PSD لـ .NET

في مجال معالجة الصور، يبرز Aspose.PSD for .NET كمجموعة أدوات قوية توفر للمطورين القدرة على تغيير حجم الصور بشكل متناسب بسهولة. في هذا الدليل التفصيلي خطوة بخطوة، سنرشدك خلال عملية تغيير حجم الصور باستخدام Aspose.PSD لـ .NET، مما يضمن احتفاظ صورك بنسبها بشكل لا تشوبه شائبة.

## مقدمة

يعد تغيير حجم الصور بشكل متناسب مهمة شائعة في العديد من التطبيقات، ويعمل Aspose.PSD for .NET على تبسيط هذه العملية للمطورين. سواء كنت تعمل على تطبيق ويب، أو برنامج سطح مكتب، أو تطبيق جوال، فإن فهم كيفية تغيير حجم الصور مع الحفاظ على نسبة العرض إلى الارتفاع أمر بالغ الأهمية للحفاظ على الجاذبية البصرية والاتساق.

## المتطلبات الأساسية

قبل الغوص في سحر تغيير الحجم باستخدام Aspose.PSD لـ .NET، تأكد من توفر المتطلبات الأساسية التالية:

1.  Aspose.PSD لمكتبة .NET: تأكد من تثبيت Aspose.PSD لمكتبة .NET. يمكنك تنزيله من[Aspose.PSD لإصدارات .NET](https://releases.aspose.com/psd/net/) صفحة.

2. دليل المستندات: قم بإنشاء دليل لتخزين مستنداتك، واستبدل "دليل المستندات الخاص بك" في الكود المقدم بالمسار الفعلي لهذا الدليل.

الآن بعد أن قمت بإعداد المتطلبات الأساسية، دعنا ننتقل إلى الدليل خطوة بخطوة.

## استيراد مساحات الأسماء

```csharp
using Aspose.PSD.ImageOptions;
```

قم باستيراد مساحات الأسماء الضرورية للوصول إلى الفئات والأساليب المطلوبة.

## الخطوة 1: تحميل الصورة

```csharp
// المسار إلى دليل المستندات.
string dataDir = "Your Document Directory";

string sourceFile = dataDir + @"sample.psd";

// قم بتحميل صورة موجودة في مثيل لفئة RasterImage
using (Image image = Image.Load(sourceFile))
{
	if (!image.IsCached)
	{
		image.CacheData();
	}
	// بقية الخطوات تذهب هنا
}
```

 قم بتحميل الصورة المصدر باستخدام`Image.Load` طريقة.

## الخطوة 2: تحديد العرض والارتفاع

```csharp
// تحديد العرض والارتفاع
int newWidth = image.Width / 2;
image.ResizeWidthProportionally(newWidth);

int newHeight = image.Height / 2;
image.ResizeHeightProportionally(newHeight);
```

تحديد العرض والارتفاع الجديد للصورة التي تم تغيير حجمها. في هذا المثال، تم خفض العرض والارتفاع إلى النصف، ولكن يمكنك ضبط هذه القيم بناءً على متطلباتك.

## الخطوة 3: احفظ الصورة التي تم تغيير حجمها

```csharp
string destName = dataDir + @"SimpleResizeImageProportionally_out.png";

image.Save(destName, new PngOptions());
```

 احفظ الصورة التي تم تغيير حجمها باستخدام`Save` الطريقة مع الخيارات المحددة. في هذه الحالة، نقوم بحفظه كملف PNG.

## خاتمة

يعد تغيير حجم الصور بشكل متناسب في Aspose.PSD لـ .NET عملية مباشرة تضيف قيمة إلى سير عمل معالجة الصور لديك. لقد زودك هذا الدليل بالمعرفة اللازمة لدمج هذه الوظيفة بسلاسة في تطبيقاتك.

## الأسئلة الشائعة

### س1: هل يمكنني تغيير حجم الصور إلى أبعاد محددة؟

ج1: نعم، يمكنك تخصيص العرض والارتفاع الجديد وفقًا لمتطلباتك في الكود.

### س2: هل Aspose.PSD for .NET مناسب لتغيير حجم الصور المجمعة؟

ج2: بالتأكيد! يمكنك دمج هذه الخطوات في حلقة لمعالجة صور متعددة دفعة واحدة.

### س3: هل توجد ميزات أخرى لمعالجة الصور في Aspose.PSD لـ .NET؟

ج3: نعم، يوفر Aspose.PSD for .NET نطاقًا واسعًا من الميزات، بما في ذلك الاقتصاص والتدوير وتطبيق المرشحات على الصور.

### س4: هل هناك نسخة تجريبية مجانية متاحة لـ Aspose.PSD لـ .NET؟

 ج4: نعم، يمكنك استكشاف إمكانيات Aspose.PSD لـ .NET من خلال النسخة التجريبية المجانية. يزور[هنا](https://releases.aspose.com/) للبدء.

### س5: أين يمكنني العثور على دعم لـ Aspose.PSD لـ .NET؟

 ج5: قم بزيارة[Aspose.PSD لمنتدى .NET](https://forum.aspose.com/c/psd/34) لدعم المجتمع والمناقشات.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
