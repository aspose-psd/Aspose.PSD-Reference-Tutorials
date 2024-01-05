---
title: تغيير الحجم باستخدام تغيير حجم النوع في Aspose.PSD لـ Java
linktitle: تغيير الحجم مع تغيير حجم نوع التعداد
second_title: Aspose.PSD جافا API
description: تغيير حجم الصورة الرئيسية في Java باستخدام Aspose.PSD. دليل خطوة بخطوة باستخدام Resize Type Enumeration.
type: docs
weight: 18
url: /ar/java/advanced-image-manipulation/resizing-with-resize-type-enumeration/
---
## مقدمة

في مشهد تطوير Java الدائم التطور، تعد المعالجة الفعالة للصور جانبًا حاسمًا غالبًا ما يتعامل معه المطورون. يظهر Aspose.PSD for Java كحل قوي، حيث يوفر تجربة سلسة لتغيير حجم الصور مع ميزة إضافية تتمثل في Resize Type Enumeration. في هذا البرنامج التعليمي، سوف نتعمق في تعقيدات تغيير حجم الصور باستخدام Aspose.PSD لـ Java، مع تفصيل كل خطوة لضمان الفهم الشامل.

## المتطلبات الأساسية

قبل الشروع في هذا البرنامج التعليمي، تأكد من توفر المتطلبات الأساسية التالية:

1. بيئة تطوير Java: تأكد من إعداد بيئة تطوير Java على جهازك.

2. مكتبة Aspose.PSD: قم بتنزيل وتثبيت مكتبة Aspose.PSD من ملف[موقع إلكتروني](https://releases.aspose.com/psd/java/).

3.  نموذج ملف PSD: احصل على نموذج ملف PSD جاهز للتجربة. يمكنك استخدام ال[Sample.psd](ملف Document Directory/sample.psd) لهذا البرنامج التعليمي.

## حزم الاستيراد

للبدء، قم باستيراد الحزم الضرورية إلى مشروع Java الخاص بك:

```java
import com.aspose.psd.Image;
import com.aspose.psd.ResizeType;

import com.aspose.psd.imageoptions.JpegOptions;
```

## الخطوة 1: تحميل الصورة

 ابدأ بتحميل صورة موجودة في مثيل`RasterImage` فصل. استخدم مقتطف الكود التالي:

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// قم بتحميل صورة موجودة في مثيل لفئة RasterImage
Image image = Image.load(sourceFile);
```

## الخطوة 2: تغيير حجم الصورة

الآن، قم بتغيير حجم الصورة المحملة باستخدام Resize Type Enumeration. في هذا المثال، نستخدم طريقة Lanczos Resample:

```java
image.resize(300, 300, ResizeType.LanczosResample);
```

## الخطوة 3: احفظ الصورة التي تم تغيير حجمها

بعد تغيير الحجم، احفظ الصورة بالأبعاد المحددة ونوع تغيير الحجم المختار. وهنا نقوم بحفظه كملف JPEG:

```java
String destName = dataDir + "ResizingwithResizeTypeEnumeration_out.jpg";
image.save(destName, new JpegOptions());
```

وهناك لديك! لقد قمت بتغيير حجم الصورة بنجاح باستخدام Resize Type Enumeration في Aspose.PSD لـ Java.

في الختام، يوفر Aspose.PSD for Java منصة قوية لمعالجة الصور، ويضيف Resize Type Enumeration طبقة من المرونة إلى هذه العملية. سواء كنت تعمل على مشروع صغير أو تطبيق واسع النطاق، فإن إتقان هذه الخطوات سيمكنك من التعامل مع تغيير حجم الصورة بسلاسة.

## الأسئلة الشائعة

### س1: هل Aspose.PSD for Java مناسب لكل من المشاريع الصغيرة والكبيرة الحجم؟

ج1: بالتأكيد! تم تصميم Aspose.PSD for Java لتلبية احتياجات المشاريع بجميع أحجامها، مما يوفر قابلية التوسع والكفاءة.

### س2: هل يمكنني استخدام نوع تغيير حجم مختلف غير Lanczos Resample؟

ج2: نعم، يوفر Aspose.PSD for Java أنواعًا مختلفة لتغيير الحجم، مثل أقرب جار وBicubic والمزيد. استكشف الوثائق للحصول على قائمة شاملة.

### س3: أين يمكنني العثور على دعم إضافي لـ Aspose.PSD لـ Java؟

 ج3: لأية استفسارات أو مساعدة، قم بزيارة[منتدى Aspose.PSD](https://forum.aspose.com/c/psd/34).

### س4: هل هناك نسخة تجريبية مجانية متاحة لـ Aspose.PSD لـ Java؟

 ج4: نعم، يمكنك الوصول إلى نسخة تجريبية مجانية[هنا](https://releases.aspose.com/).

### س5: كيف يمكنني الحصول على ترخيص مؤقت لـ Aspose.PSD لـ Java؟

 ج5: للحصول على ترخيص مؤقت قم بزيارة[هذا الرابط](https://purchase.aspose.com/temporary-license/).