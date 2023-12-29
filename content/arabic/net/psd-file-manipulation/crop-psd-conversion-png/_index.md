---
title: قص ملفات PSD عند التحويل إلى PNG في Aspose.PSD لـ .NET
linktitle: قص ملفات PSD عند التحويل إلى PNG
second_title: Aspose.PSD.NET API
description: تعرف على كيفية قص ملفات PSD بسهولة باستخدام Aspose.PSD لـ .NET. اتبع دليلنا خطوة بخطوة للتحويل السلس إلى PNG.
type: docs
weight: 18
url: /ar/net/psd-file-manipulation/crop-psd-conversion-png/
---
## مقدمة
في مجال تطوير .NET، تعد معالجة الصور وتحويلها مهمة شائعة. يوفر Aspose.PSD for .NET مجموعة قوية من الأدوات لتبسيط هذه العملية. أحد المتطلبات المتكررة هو قص ملفات PSD قبل تحويلها إلى PNG. في هذا البرنامج التعليمي خطوة بخطوة، سنتعمق في العملية باستخدام Aspose.PSD لـ .NET.
## المتطلبات الأساسية
قبل أن نبدأ هذه الرحلة، تأكد من حصولك على ما يلي:
-  Aspose.PSD لـ .NET Library: قم بتنزيل المكتبة وتثبيتها من ملف .NET Library[Aspose.PSD لتوثيق .NET](https://reference.aspose.com/psd/net/).
- نموذج ملف PSD: احصل على ملف PSD جاهز للتجربة. إذا لم يكن لديك واحد، يمكنك استخدام النموذج المقدم في البرنامج التعليمي.
- بيئة .NET: تأكد من إعداد بيئة تطوير .NET صالحة للعمل.
- دليل المستندات: حدد المسار إلى دليل المستندات الخاص بك في الكود.
## استيراد مساحات الأسماء
في مشروع .NET الخاص بك، قم بتضمين مساحات الأسماء الضرورية لـ Aspose.PSD لـ .NET:
```csharp
using Aspose.PSD.ImageOptions;
```
## الخطوة 1: قم بتحميل صورة PSD
```csharp
// المسار إلى دليل المستندات.
string dataDir = "Your Document Directory";
string srcPath = dataDir + @"sample.psd";
// قم بتحميل صورة PSD موجودة
using (RasterImage image = (RasterImage)Image.Load(srcPath))
{
    // سيتم وضع الرمز الخاص بك لمزيد من الخطوات هنا
}
```
## الخطوة 2: تحديد مستطيل الاقتصاص
```csharp
// قم بإنشاء مثيل لفئة المستطيل عن طريق تمرير x وy والعرض والارتفاع
Rectangle cropRectangle = new Rectangle(0, 0, 350, 450);
```
## الخطوة 3: قص الصورة
```csharp
//استدعاء طريقة الاقتصاص لفئة الصورة وتمرير مثيل فئة المستطيل
image.Crop(cropRectangle);
```
## الخطوة 4: تحديد خيارات PNG
```csharp
// قم بإنشاء مثيل لفئة PngOptions
PngOptions pngOptions = new PngOptions();
```
## الخطوة 5: احفظ الصورة التي تم اقتصاصها بتنسيق PNG
```csharp
// قم باستدعاء طريقة الحفظ، وتوفير مسار الإخراج، وPngOptions لتحويل ملف PSD إلى PNG وحفظ الإخراج
string destName = dataDir + @"export.png";
image.Save(destName, pngOptions);
```
## خاتمة

تهانينا! لقد تعلمت بنجاح كيفية قص ملفات PSD عند تحويلها إلى PNG باستخدام Aspose.PSD لـ .NET. يمكن أن تكون هذه القدرة لا تقدر بثمن في سيناريوهات معالجة الصور المختلفة.

## الأسئلة الشائعة

### س1: هل يمكنني استخدام هذه المكتبة في مشروع تجاري؟

 A1: نعم، Aspose.PSD لـ .NET متاح للاستخدام التجاري. تشير إلى[ترخيص Aspose.PSD](https://purchase.aspose.com/buy) للتفاصيل.

### س2: هل هناك نسخة تجريبية مجانية متاحة؟

 ج2: بالتأكيد! يمكنك استكشاف نسخة تجريبية مجانية[هنا](https://releases.aspose.com/).

### س3: أين يمكنني العثور على دعم لـ Aspose.PSD لـ .NET؟

 ج3: قم بزيارة[منتدى Aspose.PSD](https://forum.aspose.com/c/psd/34) لأية مساعدة أو استفسار.

### س4: كيف يمكنني الحصول على ترخيص مؤقت؟

 ج4: إذا كنت بحاجة إلى ترخيص مؤقت، يمكنك الحصول عليه[هنا](https://purchase.aspose.com/temporary-license/).

### س5: هل هناك أي أمثلة أو برامج تعليمية متوفرة في الوثائق؟

 ج5: نعم، يمكنك العثور على وثائق وأمثلة شاملة[هنا](https://reference.aspose.com/psd/net/).