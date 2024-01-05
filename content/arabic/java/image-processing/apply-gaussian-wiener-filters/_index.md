---
title: قم بتطبيق مرشحات Gaussian وWiener في Aspose.PSD لـ Java
linktitle: تطبيق مرشحات غاوسي و وينر
second_title: Aspose.PSD جافا API
description: قم بتحسين معالجة صور Java الخاصة بك باستخدام Aspose.PSD. تعلم كيفية تطبيق مرشحات Gaussian وWiener خطوة بخطوة للحصول على نتائج مرئية مذهلة.
type: docs
weight: 10
url: /ar/java/image-processing/apply-gaussian-wiener-filters/
---
## مقدمة

مرحبًا بك في برنامجنا التعليمي الشامل حول تطبيق مرشحات Gaussian وWiener في Aspose.PSD لـ Java! في هذا الدليل، سنرشدك خلال عملية تحسين صورك باستخدام هذه المرشحات القوية. يوفر Aspose.PSD for Java مجموعة قوية من الميزات لمعالجة الصور، ومع تطبيق مرشحات Gaussian وWiener، يمكنك الحصول على صور أكثر سلاسة ودقة.

## المتطلبات الأساسية

قبل أن نتعمق في البرنامج التعليمي، تأكد من توفر المتطلبات الأساسية التالية:

- بيئة تطوير Java: تأكد من إعداد بيئة تطوير Java على جهازك.

- Aspose.PSD لمكتبة Java: قم بتنزيل وتثبيت Aspose.PSD لمكتبة Java. يمكنك العثور على رابط التحميل[هنا](https://releases.aspose.com/psd/java/).

## حزم الاستيراد

في مشروع Java الخاص بك، قم باستيراد الحزم اللازمة لـ Aspose.PSD. فيما يلي نموذج لبيان الاستيراد للبدء:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.imagefilters.filteroptions.GaussWienerFilterOptions;
import com.aspose.psd.imageoptions.GifOptions;
```

الآن، دعونا نقسم المثال إلى خطوات متعددة لتطبيق مرشحات Gaussian وWiener.

## الخطوة 1: تحميل الصورة

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

Image image = Image.load(sourceFile);
RasterImage rasterImage = (RasterImage)image;
```

في هذه الخطوة، نقوم بتحميل ملف صورة PSD من الدليل المحدد.

## الخطوة 2: التحقق من الصورة النقطية

```java
if (rasterImage == null) {
    return;
}
```

تأكد من أن الصورة المحملة هي RasterImage صالحة؛ وإلا فسيتم إنهاء العملية.

## الخطوة 3: تكوين خيارات التصفية

```java
GaussWienerFilterOptions options = new GaussWienerFilterOptions(12, 3);
options.setGrayscale(true);
```

قم بإنشاء مثيل لـ GaussWienerFilterOptions، وقم بتعيين حجم نصف القطر، والقيمة المتجانسة، وحدد ما إذا كنت تريد تطبيق المرشح بالتدرج الرمادي.

## الخطوة 4: تطبيق التصفية والحفظ

```java
rasterImage.filter(image.getBounds(), options);
String destName = dataDir + "gauss_wiener_out.gif";
image.save(destName, new GifOptions());
```

أخيرًا، قم بتطبيق مرشحات Gaussian وWiener التي تم تكوينها على RasterImage واحفظ الصورة الناتجة بتنسيق GIF.

## خاتمة

تهانينا! لقد تعلمت بنجاح كيفية تطبيق مرشحات Gaussian وWiener باستخدام Aspose.PSD لـ Java. قم بتجربة معلمات مختلفة لتحقيق تحسينات الصورة المطلوبة.

## الأسئلة الشائعة

### س1: هل يمكنني تطبيق هذه المرشحات على الصور بتنسيقات أخرى غير PSD؟

A1: نعم، يدعم Aspose.PSD for Java تنسيقات صور متنوعة تتجاوز PSD.

### س2: هل هناك أي قيود في الإصدار التجريبي من Aspose.PSD لـ Java؟

ج2: الإصدار التجريبي له قيود، ويمكنك استكشاف الإمكانيات الكاملة من خلال الحصول على ترخيص صالح.

### س3: كيف يمكنني الحصول على دعم Aspose.PSD لـ Java؟

 ج3: قم بزيارة[منتدى Aspose.PSD](https://forum.aspose.com/c/psd/34) لدعم المجتمع والمناقشات.

### س4: هل هناك ترخيص مؤقت متاح لأغراض الاختبار؟

 ج4: نعم، يمكنك الحصول على ترخيص مؤقت[هنا](https://purchase.aspose.com/temporary-license/).

### س5: أين يمكنني العثور على الوثائق التفصيلية لـ Aspose.PSD لـ Java؟

 ج5: راجع[توثيق](https://reference.aspose.com/psd/java/) للحصول على معلومات متعمقة.