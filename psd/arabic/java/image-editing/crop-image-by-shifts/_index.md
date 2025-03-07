---
title: قص الصورة عن طريق التحولات في Aspose.PSD لجافا
linktitle: اقتصاص الصورة عن طريق التحولات
second_title: Aspose.PSD جافا API
description: اقتصاص الصور الرئيسي باستخدام Aspose.PSD لـ Java. برنامج تعليمي شامل لمعالجة الصور بسلاسة.
weight: 16
url: /ar/java/image-editing/crop-image-by-shifts/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# قص الصورة عن طريق التحولات في Aspose.PSD لجافا

## مقدمة

في عالم معالجة الصور المستندة إلى Java، يبرز Aspose.PSD كأداة قوية لمعالجة الصور وتحسينها بأقصى قدر من الدقة. إحدى الميزات الرئيسية التي تميز Aspose.PSD هي قدرته على إجراء قص الصورة بسلاسة. في هذا البرنامج التعليمي، سوف نتعمق في فن قص الصور باستخدام Aspose.PSD لـ Java. وفي النهاية، ستكون مجهزًا بالمهارات اللازمة لاقتصاص الصور بسهولة وفقًا لمواصفاتك.

## المتطلبات الأساسية

قبل أن نبدأ هذه الرحلة المثيرة، دعونا نتأكد من أن لديك المتطلبات الأساسية اللازمة:

### مجموعة تطوير جافا (JDK)

 تأكد من تثبيت أحدث إصدار من JDK على نظامك. يمكنك تنزيله من[هنا](https://www.oracle.com/java/technologies/javase-downloads.html).

### Aspose.PSD لمكتبة جافا

 للبدء، ستحتاج إلى الحصول على Aspose.PSD لمكتبة Java. توجه إلى[صفحة التحميل](https://releases.aspose.com/psd/java/) والاستيلاء على أحدث نسخة.

### بيئة التطوير المتكاملة (IDE)

اختر Java IDE المفضل لديك، مثل Eclipse أو IntelliJ، للاستمتاع بتجربة برمجة سلسة.

## حزم الاستيراد

في مشروع Java الخاص بك، قم باستيراد الحزم اللازمة لبدء عملية اقتصاص الصورة:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.imageoptions.JpegOptions;
```

الآن، دعونا نقسم عملية اقتصاص الصورة باستخدام Aspose.PSD لـ Java إلى سلسلة من الخطوات البسيطة:

## الخطوة 1: تحميل الصورة

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// قم بتحميل صورة موجودة في مثيل لفئة RasterImage
RasterImage rasterImage = (RasterImage)Image.load(sourceFile);
```

## الخطوة 2: تخزين بيانات الصورة مؤقتًا

قبل الاقتصاص، يُنصح بتخزين بيانات الصورة مؤقتًا لتحسين الأداء:

```java
if (!rasterImage.isCached()) {
  rasterImage.cacheData();
}
```

## الخطوة 3: تحديد قيم التحول

حدد قيم التحول لجميع الجوانب الأربعة للصورة:

```java
int leftShift = 10;
int rightShift = 10;
int topShift = 10;
int bottomShift = 10;
```

## الخطوة 4: تطبيق الاقتصاص

 استنادًا إلى قيم الإزاحة المحددة، قم بتطبيق الاقتصاص على الصورة باستخدام الزر`crop` طريقة:

```java
rasterImage.crop(leftShift, rightShift, topShift, bottomShift);
```

## الخطوة 5: حفظ النتائج

احفظ الصورة التي تم اقتصاصها على القرص بالتنسيق المطلوب، في هذه الحالة، JPEG:

```java
String destName = dataDir + "CroppingByShifts_out.jpg";
rasterImage.save(destName, new JpegOptions());
```

تهانينا! لقد نجحت في اقتصاص صورة باستخدام Aspose.PSD لـ Java.

## خاتمة

في هذا البرنامج التعليمي، استكشفنا تعقيدات اقتصاص الصور باستخدام Aspose.PSD لـ Java. بفضل هذه المعرفة، يمكنك الآن دمج ميزة اقتصاص الصور بسلاسة في مشاريع Java الخاصة بك، مما يضيف لمسة من البراعة إلى قدرات معالجة الصور لديك.

## الأسئلة الشائعة

### س1: هل Aspose.PSD متوافق مع جميع تنسيقات الصور؟

ج1: نعم، يدعم Aspose.PSD نطاقًا واسعًا من تنسيقات الصور، مما يضمن تعدد الاستخدامات في مشروعاتك.

### س2: هل يمكنني تطبيق عمليات قص متعددة على نفس الصورة؟

ج2: بالتأكيد، يمكنك إجراء عمليات اقتصاص متعددة بالتسلسل على نفس الصورة.

### س3: هل يوجد منتدى مجتمعي لدعم Aspose.PSD؟

 ج3: نعم، يمكنك العثور على الدعم والتفاعل مع المجتمع على[منتدى Aspose.PSD](https://forum.aspose.com/c/psd/34).

### س4: كيف يمكنني الحصول على ترخيص مؤقت لـ Aspose.PSD؟

 ج4: زيارة[هنا](https://purchase.aspose.com/temporary-license/) للحصول على ترخيص مؤقت.

### س 5: هل هناك أية مشاريع نموذجية تعرض وظائف Aspose.PSD؟

 ج5: استكشف الوثائق والأمثلة في[وثائق جافا Aspose.PSD](https://reference.aspose.com/psd/java/).

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
