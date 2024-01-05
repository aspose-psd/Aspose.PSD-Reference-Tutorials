---
title: قم بتدوير الصورة في Aspose.PSD لـ Java
linktitle: تدوير صورة
second_title: Aspose.PSD جافا API
description: استكشف تدوير الصور في Java بسهولة باستخدام Aspose.PSD. قم بتدوير ملفات PSD وقلبها وحفظها بسهولة.
type: docs
weight: 19
url: /ar/java/advanced-image-manipulation/rotate-image/
---
## مقدمة

يوفر Aspose.PSD for Java مجموعة قوية من الميزات للعمل مع الصور، مما يسمح للمطورين بمعالجة ملفات PSD ومعالجتها بكفاءة. في هذا البرنامج التعليمي، سنركز على مهمة واحدة محددة: تدوير الصورة. سواء كنت تقوم بإنشاء تطبيق لتحرير الصور أو تحتاج ببساطة إلى ضبط اتجاه الصورة، فإن Aspose.PSD يجعل العملية واضحة.

## المتطلبات الأساسية

قبل الغوص في البرنامج التعليمي، تأكد من توفر المتطلبات الأساسية التالية:

-  Aspose.PSD لمكتبة Java: تأكد من تنزيل وتثبيت Aspose.PSD لمكتبة Java. يمكنك العثور على المكتبة والوثائق التفصيلية[هنا](https://reference.aspose.com/psd/java/).

- بيئة تطوير Java: تأكد من إعداد بيئة تطوير Java على جهازك.

-  نموذج ملف PSD: قم بإعداد نموذج ملف PSD الذي تريد تدويره. أضبط ال`sourceFile` متغير في رمز المثال مع المسار إلى ملف PSD الخاص بك.

## حزم الاستيراد

ابدأ باستيراد الحزم اللازمة للاستفادة من إمكانيات Aspose.PSD:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RotateFlipType;

import com.aspose.psd.imageoptions.JpegOptions;
```

## الخطوة 1: تحميل الصورة

 قم بتحميل الصورة الموجودة في مثيل`Image` فصل:

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";
Image image = Image.load(sourceFile);
```

## الخطوة 2: تدوير الصورة

 قم بتدوير الصورة باستخدام`rotateFlip` طريقة. في هذا المثال، نقوم بتدوير الصورة بمقدار 270 درجة:

```java
image.rotateFlip(RotateFlipType.Rotate270FlipNone);
```

## الخطوة 3: احفظ الصورة التي تم تدويرها

 احفظ الصورة التي تم تدويرها باستخدام`save` الطريقة وتحديد تنسيق الإخراج (JPEG، في هذه الحالة):

```java
String destName = dataDir + "RotatedImage_out.jpg";
image.save(destName, new JpegOptions());
```

## خاتمة

تهانينا! لقد قمت بتدوير صورة بنجاح باستخدام Aspose.PSD لـ Java. تفتح هذه المكتبة البسيطة والقوية عالمًا من الإمكانيات لمعالجة الصور في تطبيقات Java الخاصة بك.

## الأسئلة الشائعة

### س1: هل يتوافق Aspose.PSD مع تنسيقات الصور المختلفة؟

A1: نعم، يدعم Aspose.PSD تنسيقات الصور المختلفة، بما في ذلك PSD وJPEG وPNG والمزيد.

### س2: هل يمكنني تطبيق عمليات تدوير مخصصة، وليس فقط عمليات قلب محددة مسبقًا؟

ج2: بالتأكيد! يوفر Aspose.PSD المرونة لتطبيق عمليات التدوير المخصصة لتلبية متطلباتك المحددة.

### س3: أين يمكنني العثور على دعم أو مساعدة إضافية؟

 ج3: إذا كانت لديك أي استفسارات أو مشكلات، قم بزيارة[منتدى Aspose.PSD](https://forum.aspose.com/c/psd/34) لدعم المجتمع.

### س4: هل هناك نسخة تجريبية مجانية متاحة؟

 ج4: نعم، يمكنك استكشاف Aspose.PSD باستخدام ملف[تجربة مجانية](https://releases.aspose.com/).

### س5: كيف يمكنني الحصول على ترخيص مؤقت؟

 ج5: إذا كنت بحاجة إلى ترخيص مؤقت، يمكنك الحصول عليه[هنا](https://purchase.aspose.com/temporary-license/).