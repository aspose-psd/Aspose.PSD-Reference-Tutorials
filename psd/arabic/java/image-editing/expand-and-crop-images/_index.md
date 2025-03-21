---
title: قم بتوسيع الصور واقتصاصها باستخدام Aspose.PSD لـ Java
linktitle: توسيع واقتصاص الصور
second_title: Aspose.PSD جافا API
description: تعرف على كيفية توسيع الصور واقتصاصها في Java باستخدام Aspose.PSD. دليل خطوة بخطوة لمعالجة الصور بكفاءة.
weight: 18
url: /ar/java/image-editing/expand-and-crop-images/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# قم بتوسيع الصور واقتصاصها باستخدام Aspose.PSD لـ Java

## مقدمة

في هذا البرنامج التعليمي، سنستكشف كيفية استخدام Aspose.PSD لـ Java لتوسيع الصور واقتصاصها بكفاءة. Aspose.PSD هي مكتبة قوية توفر مجموعة واسعة من الميزات للعمل مع ملفات PSD في تطبيقات Java. في هذا الدليل، سنغطي المتطلبات الأساسية اللازمة، واستيراد الحزم، وتقسيم كل خطوة مع شرح مفصل.

## المتطلبات الأساسية

قبل أن نتعمق في البرنامج التعليمي، تأكد من توفر المتطلبات الأساسية التالية:

1. بيئة تطوير Java: تأكد من تثبيت Java على نظامك.

2.  مكتبة Aspose.PSD: قم بتنزيل وتثبيت مكتبة Aspose.PSD. يمكنك العثور على المكتبة[هنا](https://releases.aspose.com/psd/java/).

## حزم الاستيراد

الآن بعد أن قمت بتنظيم متطلباتك الأساسية، قم باستيراد الحزم اللازمة لبدء العمل مع Aspose.PSD لـ Java. أضف الأسطر التالية إلى كود Java الخاص بك:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;
import com.aspose.psd.Rectangle;

import com.aspose.psd.imageoptions.JpegOptions;
```

توفر هذه الحزم الفئات والأساليب الأساسية لمعالجة الصور باستخدام Aspose.PSD.

## الخطوة 1: قم بتعيين دليل المستندات الخاص بك

ابدأ بتعيين الدليل الذي يوجد به ملف PSD الخاص بك. استبدل "دليل المستندات الخاص بك" بالمسار الفعلي.

```java
String dataDir = "Your Document Directory";
```

## الخطوة 2: تحديد مسارات المصدر والوجهة

حدد ملف PSD المصدر والمسار الوجهة لصورة الإخراج.

```java
String sourceFile = dataDir + "example1.psd";
String destName = dataDir + "jpeg_out.jpg";
```

## الخطوة 3: تحميل الصورة وتخزينها مؤقتًا

 قم بتحميل ملف PSD إلى ملف`RasterImage` الكائن وتخزين بياناته مؤقتًا.

```java
RasterImage rasterImage = (RasterImage)Image.load(sourceFile);
rasterImage.cacheData();
```

## الخطوة 4: إنشاء مستطيل للاقتصاص

 إنشاء مثيل أ`Rectangle` الكائن وتحديد إحداثيات X وY وعرضه وارتفاعه. سيحدد هذا المستطيل المنطقة التي تم اقتصاصها.

```java
Rectangle destRect = new Rectangle(-200, -200, 300, 300);
```

## الخطوة 5: احفظ الصورة التي تم اقتصاصها

 احفظ الصورة التي تم اقتصاصها باستخدام المستطيل المحدد و`JpegOptions` فصل.

```java
rasterImage.save(destName, new JpegOptions(), destRect);
```

تهانينا! لقد نجحت في توسيع الصورة واقتصاصها باستخدام Aspose.PSD لـ Java.

## خاتمة

في هذا البرنامج التعليمي، استكشفنا عملية توسيع الصور واقتصاصها باستخدام مكتبة Aspose.PSD لـ Java. بفضل ميزاته القوية، يعمل Aspose.PSD على تبسيط مهام معالجة الصور، مما يجعله خيارًا ممتازًا لمطوري Java.

## الأسئلة الشائعة

### س1: هل Aspose.PSD متوافق مع إصدارات Java المختلفة؟

ج1: نعم، يدعم Aspose.PSD إصدارات Java المختلفة، مما يضمن التوافق مع نطاق واسع من بيئات التطوير.

### س2: هل يمكنني استخدام Aspose.PSD للمشاريع التجارية؟

ج2: بالتأكيد، يوفر Aspose.PSD تراخيص تجارية للمطورين، مما يسمح باستخدامه في كل من المشاريع الشخصية والتجارية.

### س3: هل هناك أي قيود على تنسيقات ملفات الصور المدعومة؟

 A3: يدعم Aspose.PSD مجموعة متنوعة من تنسيقات ملفات الصور، بما في ذلك PSD وJPEG وPNG والمزيد. الرجوع إلى[الوثائق](https://reference.aspose.com/psd/java/) للحصول على قائمة كاملة.

### س4: كيف يمكنني الحصول على الدعم للاستعلامات المتعلقة بـ Aspose.PSD؟

 ج4: قم بزيارة[منتدى Aspose.PSD](https://forum.aspose.com/c/psd/34) لطلب المساعدة من المجتمع أو فريق دعم Aspose.

### س5: هل هناك نسخة تجريبية مجانية متاحة؟

 ج5: نعم، يمكنك استكشاف Aspose.PSD من خلال النسخة التجريبية المجانية. قم بتنزيله[هنا](https://releases.aspose.com/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
