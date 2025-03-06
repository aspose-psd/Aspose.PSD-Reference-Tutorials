---
title: قم بتطبيق مرشحات Median وWiener باستخدام Aspose.PSD لـ Java
linktitle: قم بتطبيق مرشحات Median وWiener
second_title: Aspose.PSD جافا API
description: اكتشف قوة معالجة الصور في Java باستخدام Aspose.PSD. تعرف على كيفية تطبيق مرشحات Median وWiener خطوة بخطوة. تعزيز جودة الصورة دون عناء.
weight: 12
url: /ar/java/image-processing/apply-median-wiener-filters/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# قم بتطبيق مرشحات Median وWiener باستخدام Aspose.PSD لـ Java

## مقدمة

في عالم برمجة Java، يبرز Aspose.PSD كأداة قوية لمعالجة الصور ومعالجتها. إحدى الوظائف الرئيسية التي تقدمها هي تطبيق مرشحات Median وWiener، التي تلعب دورًا حاسمًا في تحسين جودة الصورة وتقليل الضوضاء. سيرشدك هذا الدليل خطوة بخطوة خلال عملية تطبيق هذه المرشحات باستخدام Aspose.PSD لـ Java.

## المتطلبات الأساسية

قبل الغوص في البرنامج التعليمي، تأكد من توفر المتطلبات الأساسية التالية:

1.  Aspose.PSD لمكتبة Java: قم بتنزيل المكتبة وتثبيتها من[هنا](https://releases.aspose.com/psd/java/).
2. بيئة تطوير Java: تأكد من إعداد بيئة تطوير Java على نظامك.

## حزم الاستيراد

ابدأ باستيراد الحزم اللازمة للاستفادة من وظيفة Aspose.PSD داخل مشروع Java الخاص بك:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.imagefilters.filteroptions.MedianFilterOptions;
import com.aspose.psd.imageoptions.GifOptions;
```

## تطبيق مرشح المتوسط

### الخطوة 1: تحميل الصورة

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

//قم بتحميل الصورة المصدر
Image image = Image.load(sourceFile);
```

### الخطوة 2: إرسال الصورة إلى RasterImage

```java
// إرسال الصورة إلى RasterImage
RasterImage rasterImage = (RasterImage)image;
if (rasterImage == null) {
    return;
}
```

### الخطوة 3: إنشاء مثيل MedianFilterOptions

```java
// قم بإنشاء مثيل لفئة MedianFilterOptions وقم بتعيين حجم عامل التصفية
MedianFilterOptions options = new MedianFilterOptions(4);
```

### الخطوة 4: تطبيق عامل التصفية المتوسط

```java
// قم بتطبيق مرشح MedianFilterOptions على كائن RasterImage
rasterImage.filter(image.getBounds(), options);
```

### الخطوة 5: احفظ الصورة الناتجة

```java
String destName = dataDir + "median_test_denoise_out.gif";
// احفظ الصورة الناتجة بصيغة GIF
image.save(destName, new GifOptions());
```

باتباع هذه الخطوات، تكون قد قمت بنجاح بتطبيق عامل التصفية المتوسط على صورتك باستخدام Aspose.PSD لـ Java.

## خاتمة

في هذا البرنامج التعليمي، استكشفنا عملية تطبيق مرشحات Median وWiener باستخدام Aspose.PSD لـ Java. لا غنى عن هذه المرشحات لتحسين جودة الصورة وتقليل التشويش في تطبيقات Java الخاصة بك. من خلال الاستفادة من قوة Aspose.PSD، يمكنك دمج هذه المرشحات بسهولة في سير عمل معالجة الصور لديك.

## الأسئلة الشائعة

### س1: هل يمكنني تطبيق عوامل التصفية هذه على الصور بأي تنسيق؟

ج1: نعم، يدعم Aspose.PSD نطاقًا واسعًا من تنسيقات الصور، مما يجعله متعدد الاستخدامات لمختلف المشاريع.

### س2: هل هناك نسخة تجريبية مجانية متاحة لـ Aspose.PSD لـ Java؟

 ج2: نعم، يمكنك الحصول على نسخة تجريبية مجانية[هنا](https://releases.aspose.com/).

### س3: كيف يمكنني الحصول على دعم Aspose.PSD لـ Java؟

 ج3: قم بزيارة[منتدى Aspose.PSD](https://forum.aspose.com/c/psd/34) لدعم المجتمع.

### س4: أين يمكنني العثور على الوثائق الخاصة بـ Aspose.PSD لـ Java؟

 ج4: راجع الوثائق[هنا](https://reference.aspose.com/psd/java/).

### س5: كيف يمكنني شراء Aspose.PSD لـ Java؟

 ج5: يمكنك شراء المنتج[هنا](https://purchase.aspose.com/buy).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
