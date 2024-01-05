---
title: قص الصورة حسب المستطيل في Aspose.PSD لـ Java
linktitle: اقتصاص الصورة بواسطة المستطيل
second_title: Aspose.PSD جافا API
description: اكتشف إمكانات قص الصور السلسة في Java باستخدام Aspose.PSD. اتبع دليلنا خطوة بخطوة لاقتصاص الصور بسهولة باستخدام Aspose.PSD لـ Java.
type: docs
weight: 15
url: /ar/java/image-editing/crop-image-by-rectangle/
---
## مقدمة

في عالم تطوير Java، تعد معالجة الصور مهمة شائعة، ويوفر Aspose.PSD for Java حلاً قويًا لمعالجة الصور. في هذا البرنامج التعليمي، سنرشدك خلال عملية اقتصاص صورة بواسطة مستطيل باستخدام Aspose.PSD لـ Java. اتبع الخطوات أدناه لتحقيق ذلك بكل سهولة.

## المتطلبات الأساسية

قبل الغوص في البرنامج التعليمي، تأكد من توفر المتطلبات الأساسية التالية:

- تم تثبيت Java Development Kit (JDK) على جهازك.
-  Aspose.PSD لمكتبة جافا. يمكنك تنزيله من[موقع إلكتروني](https://releases.aspose.com/psd/java/).

## حزم الاستيراد

تأكد من تضمين الحزم الضرورية في مشروع Java الخاص بك للاستفادة من إمكانيات Aspose.PSD لـ Java. أضف عبارات الاستيراد التالية في بداية ملف Java الخاص بك:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;
import com.aspose.psd.Rectangle;

import com.aspose.psd.imageoptions.JpegOptions;
```

الآن، دعنا نقسم العملية إلى خطوات متعددة لإرشادك خلال قص الصورة بواسطة مستطيل باستخدام Aspose.PSD لـ Java.

## الخطوة 1: قم بإعداد دليل المستندات الخاص بك

```java
String dataDir = "Your Document Directory";
```

 يستبدل`"Your Document Directory"` بالمسار الفعلي حيث يوجد ملف PSD الخاص بك.

## الخطوة 2: تحديد ملفات المصدر والوجهة

```java
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "CroppingByRectangle_out.jpg";
```

حدد المسارات لملف PSD المصدر وملف JPEG الوجهة.

## الخطوة 3: تحميل الصورة وتخزينها مؤقتًا

```java
RasterImage rasterImage = (RasterImage)Image.load(sourceFile);

if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

 قم بتحميل صورة PSD إلى ملف`RasterImage` المثيل وتخزين البيانات الخاصة به.

## الخطوة 4: إنشاء وتعريف مستطيل المحاصيل

```java
Rectangle rectangle = new Rectangle(20, 20, 20, 20);
```

 إنشاء مثيل لـ`Rectangle` الفئة بالحجم المطلوب للاقتصاص.

## الخطوة 5: قص الصورة وحفظها

```java
rasterImage.crop(rectangle);
rasterImage.save(destName, new JpegOptions());
```

قم بإجراء عملية الاقتصاص باستخدام المستطيل المحدد واحفظ النتائج كملف JPEG.

كرر هذه الخطوات حسب الحاجة، واضبط المعلمات وفقًا لمتطلباتك المحددة.

## خاتمة

في هذا البرنامج التعليمي، مررنا بعملية قص صورة بمستطيل باستخدام Aspose.PSD لـ Java. باتباع هذه الخطوات، يمكنك بسهولة دمج إمكانات معالجة الصور القوية في تطبيقات Java الخاصة بك.

## الأسئلة الشائعة

### س1: هل يمكنني استخدام Aspose.PSD لـ Java مع أطر عمل Java الأخرى؟

ج1: نعم، يمكن دمج Aspose.PSD for Java مع أطر عمل Java المختلفة، مما يوفر المرونة في مشاريع التطوير الخاصة بك.

### س2: هل هناك نسخة تجريبية مجانية متاحة لـ Aspose.PSD لـ Java؟

 ج2: نعم، يمكنك الوصول إلى النسخة التجريبية المجانية[هنا](https://releases.aspose.com/).

### س3: أين يمكنني العثور على دعم أو مساعدة إضافية؟

 ج3: قم بزيارة[منتدى Aspose.PSD](https://forum.aspose.com/c/psd/34) لدعم المجتمع والمناقشات.

### س4: كيف يمكنني الحصول على ترخيص مؤقت لـ Aspose.PSD لـ Java؟

 ج4: يمكنك الحصول على ترخيص مؤقت[هنا](https://purchase.aspose.com/temporary-license/).

### س5: ما هي تنسيقات الصور المدعومة للاقتصاص في Aspose.PSD لـ Java؟

ج5: يدعم Aspose.PSD for Java تنسيقات صور متنوعة، بما في ذلك PSD وPNG وJPEG والمزيد.