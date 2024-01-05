---
title: قم بتغيير حجم الصورة بشكل متناسب باستخدام Aspose.PSD لـ Java
linktitle: تغيير حجم الصورة بشكل متناسب
second_title: Aspose.PSD جافا API
description: قم بتحسين تطبيقات Java الخاصة بك باستخدام Aspose.PSD. اتبع دليلنا لتغيير حجم الصور بشكل متناسب دون عناء. تعزيز قدرات معالجة الصور الخاصة بك اليوم.
type: docs
weight: 17
url: /ar/java/advanced-image-manipulation/resize-image-proportionally/
---
## مقدمة

مرحبًا بك في دليلنا خطوة بخطوة حول تغيير حجم الصور بشكل متناسب باستخدام Aspose.PSD لـ Java. إذا كنت تتطلع إلى تحسين تطبيقات Java الخاصة بك من خلال إمكانيات فعالة لتغيير حجم الصور، فقد وصلت إلى المكان الصحيح. في هذا البرنامج التعليمي، سنرشدك خلال العملية باستخدام خطوات واضحة وموجزة.

## المتطلبات الأساسية

قبل الغوص في البرنامج التعليمي، تأكد من توفر المتطلبات الأساسية التالية:

1. بيئة Java: تأكد من تثبيت Java على نظامك.
2.  مكتبة Aspose.PSD: قم بتنزيل وتثبيت مكتبة Aspose.PSD. يمكنك العثور على الموارد اللازمة[هنا](https://releases.aspose.com/psd/java/).

## حزم الاستيراد

بمجرد فرز متطلباتك الأساسية، قم باستيراد الحزم المطلوبة إلى مشروع Java الخاص بك. تأكد من الإشارة بشكل صحيح إلى مكتبة Aspose.PSD في مشروعك.

```java
import com.aspose.psd.Image;

import com.aspose.psd.imageoptions.PngOptions;
```

## الخطوة 1: تحميل الصورة

ابدأ بتحميل الصورة التي تريد تغيير حجمها إلى تطبيق Java الخاص بك.

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

Image image = Image.load(sourceFile);

if (!image.isCached()) {
    image.cacheData();
}
```

## الخطوة 2: تحديد العرض والارتفاع

حدد العرض والارتفاع الجديد لصورتك التي تم تغيير حجمها. في هذا المثال، سنقوم بتغيير حجم الصورة إلى نصف أبعادها الأصلية.

```java
int newWidth = image.getWidth() / 2;
image.resizeWidthProportionally(newWidth);

int newHeight = image.getHeight() / 2;
image.resizeHeightProportionally(newHeight);
```

## الخطوة 3: احفظ الصورة التي تم تغيير حجمها

احفظ الصورة التي تم تغيير حجمها إلى الموقع الذي تريده، مع تحديد خيارات التنسيق (PNG، في هذه الحالة).

```java
String destName = dataDir + "SimpleResizeImageProportionally_out.png";
image.save(destName, new PngOptions());
```

وهناك لديك! لقد نجحت في تغيير حجم الصورة بشكل متناسب باستخدام Aspose.PSD لـ Java.

## خاتمة

في هذا البرنامج التعليمي، قمنا بتغطية الخطوات الأساسية لتغيير حجم الصور بشكل متناسب باستخدام مكتبة Aspose.PSD لـ Java. والآن، يمكنك دمج هذه الوظيفة بسهولة في تطبيقات Java الخاصة بك لتحسين معالجة الصور.

## الأسئلة الشائعة

### س1: هل Aspose.PSD متوافق مع كافة تنسيقات الصور؟

 A1: يدعم Aspose.PSD تنسيقات الصور المختلفة، بما في ذلك PSD وPNG وJPEG والمزيد. افحص ال[توثيق](https://reference.aspose.com/psd/java/) للحصول على قائمة شاملة.

### س2: هل يمكنني استخدام Aspose.PSD للمشاريع التجارية؟

 ج2: نعم يمكنك ذلك. قم بزيارة[صفحة الشراء](https://purchase.aspose.com/buy) للحصول على تفاصيل الترخيص.

### س3: هل التراخيص المؤقتة متاحة لأغراض الاختبار؟

 ج3: نعم، يمكنك الحصول على ترخيص مؤقت[هنا](https://purchase.aspose.com/temporary-license/) للتقييم.

### س4: أين يمكنني العثور على الدعم لـ Aspose.PSD؟

 ج4: قم بزيارة[منتدى Aspose.PSD](https://forum.aspose.com/c/psd/34) لدعم المجتمع ومساعدته.

### س5: كيف يمكنني الوصول إلى وثائق Aspose.PSD؟

 ج5: ارجع إلى الوثائق التفصيلية[هنا](https://reference.aspose.com/psd/java/).
`