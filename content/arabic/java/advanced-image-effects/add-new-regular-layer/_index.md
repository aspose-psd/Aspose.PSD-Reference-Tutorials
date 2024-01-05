---
title: أضف طبقة عادية جديدة إلى PSD باستخدام Aspose.PSD لـ Java
linktitle: أضف طبقة عادية جديدة إلى PSD
second_title: Aspose.PSD جافا API
description: تعرف على كيفية إضافة طبقة عادية جديدة إلى ملفات PSD باستخدام Aspose.PSD لـ Java. اتبع دليلنا خطوة بخطوة لمعالجة ملفات PSD بسلاسة.
type: docs
weight: 11
url: /ar/java/advanced-image-effects/add-new-regular-layer/
---
## مقدمة

مرحبًا بك في هذا البرنامج التعليمي الشامل حول استخدام Aspose.PSD لـ Java لإضافة طبقة عادية جديدة إلى ملف PSD. Aspose.PSD هي مكتبة Java قوية تتيح للمطورين التعامل مع ملفات PSD والعمل معها بكفاءة. في هذا البرنامج التعليمي، سنرشدك خلال عملية إضافة طبقة عادية جديدة إلى ملف PSD، مع تقديم خطوات تفصيلية وأمثلة على التعليمات البرمجية.

## المتطلبات الأساسية

قبل الغوص في البرنامج التعليمي، تأكد من توفر المتطلبات الأساسية التالية:

- بيئة تطوير Java: تأكد من إعداد بيئة تطوير Java على نظامك.
-  مكتبة Aspose.PSD: قم بتنزيل وتثبيت Aspose.PSD لمكتبة Java. يمكنك العثور على المكتبة[هنا](https://releases.aspose.com/psd/java/).

## حزم الاستيراد

للبدء، قم باستيراد الحزم الضرورية إلى مشروع Java الخاص بك. تعتبر هذه الحزم ضرورية للعمل مع وظائف Aspose.PSD. قم بتضمين الأسطر التالية في بداية ملف Java الخاص بك:

```java
import com.aspose.psd.Image;
import com.aspose.psd.Rectangle;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.imageoptions.PsdOptions;
```

## الخطوة 1: تحميل ملف PSD

قم بتحميل ملف PSD الذي تريد تحريره باستخدام الكود التالي:

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "OneLayer.psd";
PsdImage im = (PsdImage)Image.load(sourceFileName);
```

## الخطوة 2: إعداد صفائف البيانات والمستطيلات

قم بإعداد صفيفين int وكائنين مستطيلين كما يلي:

```java
int[] data1 = new int[2500];
int[] data2 = new int[2500];
Rectangle rect1 = new Rectangle(0, 0, 50, 50);
Rectangle rect2 = new Rectangle(0, 0, 100, 25);
```

## الخطوة 3: تهيئة بيانات الطبقة

تهيئة صفائف البيانات بقيمة افتراضية:

```java
for (int i = 0; i < 2500; i++) {
    data1[i] = -10000000;
    data2[i] = -10000000;
}
```

## الخطوة 4: إضافة طبقات عادية

أضف طبقتين عاديتين إلى صورة PSD:

```java
Layer layer1 = im.addRegularLayer();
layer1.setLeft(25);
layer1.setTop(25);
layer1.setRight(75);
layer1.setBottom(75);
layer1.saveArgb32Pixels(rect1, data1);

Layer layer2 = im.addRegularLayer();
layer2.setLeft(25);
layer2.setTop(150);
layer2.setRight(1255);
layer2.setBottom(175);
layer2.saveArgb32Pixels(rect2, data2);
```

## الخطوة 5: حفظ PSD و PNG

احفظ ملف PSD المعدل وملف PNG إضافيًا:

```java
im.save(exportPath, new PsdOptions());
im.save(exportPathPng, new PngOptions());
```

تهانينا! لقد نجحت في إضافة طبقة عادية جديدة إلى ملف PSD باستخدام Aspose.PSD لـ Java.

## خاتمة

في هذا البرنامج التعليمي، قمنا بتغطية عملية إضافة طبقة عادية جديدة إلى ملف PSD باستخدام Aspose.PSD لـ Java. تعمل هذه المكتبة القوية على تبسيط معالجة PSD، مما يجعلها في متناول مطوري Java. قم بتجربة معلمات ووظائف مختلفة لاستكشاف الإمكانات الكاملة لـ Aspose.PSD.

## الأسئلة الشائعة

### س1: هل Aspose.PSD متوافق مع Java 8؟

A1: نعم، يدعم Aspose.PSD Java 8 والإصدارات الأحدث.

### س2: هل يمكنني تطبيق التحويلات على الطبقات المضافة؟

ج2: بالتأكيد! يوفر Aspose.PSD مجموعة من خيارات التحويل للطبقات.

### س3: أين يمكنني العثور على وثائق Aspose.PSD إضافية؟

 ج3: يمكنك الرجوع إلى الوثائق[هنا](https://reference.aspose.com/psd/java/).

### س4: كيف يمكنني الحصول على ترخيص مؤقت لـ Aspose.PSD؟

 ج4: زيارة[هذا الرابط](https://purchase.aspose.com/temporary-license/) لخيارات الترخيص المؤقت.

### س5: هل هناك أية منتديات مجتمعية لدعم Aspose.PSD؟

 ج5: نعم، يمكنك العثور على الدعم والمناقشات[هنا](https://forum.aspose.com/c/psd/34).