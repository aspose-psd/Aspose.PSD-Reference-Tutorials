---
title: قم بإجراء رسم بسيط باستخدام Aspose.PSD لـ Java
linktitle: تنفيذ رسم بسيط
second_title: Aspose.PSD جافا API
description: تعرف على كيفية رسم الأشكال في ملفات PSD باستخدام Aspose.PSD لـ Java. يغطي هذا الدليل خطوة بخطوة إنشاء الطبقات وإضافتها والرسم باستخدام أمثلة التعليمات البرمجية.
type: docs
weight: 10
url: /ar/java/basic-image-operations/simple-drawing/
---
## مقدمة

مرحبًا بك في هذا الدليل التفصيلي خطوة بخطوة حول إجراء رسم بسيط باستخدام Aspose.PSD لـ Java! في هذا البرنامج التعليمي، سوف نستكشف أساسيات إنشاء مستند PSD جديد، وإضافة الطبقات، ورسم الأشكال بألوان مختلفة. Aspose.PSD for Java هي مكتبة قوية تمكنك من التعامل مع ملفات PSD برمجياً، مما يوفر وظائف واسعة النطاق لمهام تصميم الرسومات.

## المتطلبات الأساسية

قبل الغوص في البرنامج التعليمي، تأكد من توفر المتطلبات الأساسية التالية:

- تم تثبيت Java Development Kit (JDK) على جهازك.
- Aspose.PSD لمكتبة جافا. يمكنك تنزيله من[Aspose.PSD لتوثيق جافا](https://reference.aspose.com/psd/java/).

## حزم الاستيراد

للبدء، قم باستيراد الحزم الضرورية إلى مشروع Java الخاص بك. قم بتضمين الكود التالي في بداية ملف Java الخاص بك:

```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Pen;
import com.aspose.psd.Rectangle;
import com.aspose.psd.brushes.SolidBrush;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
```

## الخطوة 1: إنشاء مستند جديد

لنبدأ بإنشاء مستند PSD جديد بعرض وارتفاع محددين:

```java
//ExStart: إنشاء مستند
String outputDir = "Your Document Directory";
String outPsdFilePath = outputDir + "output.psd";
int width = 100;
int height = 100;

PsdImage image = new PsdImage(width, height);
//ExEnd: إنشاء مستند
```

## الخطوة 2: إضافة طبقة

الآن، دعونا نضيف طبقة إلى المستند باستخدام مُنشئ no-argument:

```java
//ExStart:AddLayer
Layer layer = new Layer();
layer.setBottom(height);
layer.setRight(width);
image.addLayer(layer);
//ExEnd:AddLayer
```

## الخطوة 3: رسم الأشكال

في هذه الخطوة، سوف نستخدم فئة الرسومات لرسم الأشكال على الطبقة التي تم إنشاؤها:

### ارسم مستطيلاً باللون الأصفر

```java
//ExStart: رسم مستطيل باللون الأصفر
Graphics graphic = new Graphics(layer);
graphic.clear(Color.getYellow());
//النهاية: رسم مستطيل باللون الأصفر
```

### ارسم مستطيلًا أحمر

```java
//ExStart: DrawRedRectangle
graphic.drawRectangle(new Pen(Color.getRed()), new Rectangle(30, 10, 40, 80));
//ExEnd: DrawRedRectangle
```

### ارسم مستطيلًا أزرقًا

```java
//ExStart: رسم المستطيل الأزرق
graphic.drawRectangle(new Pen(new SolidBrush(Color.getBlue())), new Rectangle(10, 30, 80, 40));
//النهاية: رسم المستطيل الأزرق
```

## الخطوة 4: حفظ التغييرات

أخيرًا، احفظ نسخة من ملف PSD الذي تم تحميله بما في ذلك التغييرات:

```java
//ExStart: حفظ التغييرات
image.save(outPsdFilePath);
//انتهاء: حفظ التغييرات
```

## خاتمة

تهانينا! لقد قمت بنجاح بتنفيذ رسم بسيط باستخدام Aspose.PSD لـ Java. تناول هذا البرنامج التعليمي إنشاء مستند جديد وإضافة طبقات ورسم مستطيلات بألوان مختلفة. لا تتردد في استكشاف المزيد من الميزات المتقدمة التي تقدمها المكتبة لتلبية احتياجات التصميم الجرافيكي الخاصة بك.

## الأسئلة الشائعة

### س1: هل يمكنني استخدام Aspose.PSD لـ Java لمعالجة ملفات PSD الموجودة؟

ج1: نعم، يوفر Aspose.PSD for Java وظائف شاملة لتحرير ملفات PSD الموجودة ومعالجتها.

### س2: أين يمكنني العثور على دعم لـ Aspose.PSD لـ Java؟

 ج2: يمكنك زيارة[Aspose.PSD لمنتدى جافا](https://forum.aspose.com/c/psd/34) لأية استفسارات متعلقة بالدعم.

### س3: هل هناك نسخة تجريبية مجانية متاحة لـ Aspose.PSD لـ Java؟

 ج3: نعم، يمكنك الوصول إلى الإصدار التجريبي المجاني[هنا](https://releases.aspose.com/).

### س4: كيف يمكنني شراء ترخيص Aspose.PSD لـ Java؟

 ج4: يمكنك شراء ترخيص من[صفحة شراء Aspose.PSD](https://purchase.aspose.com/buy).

### س5: هل التراخيص المؤقتة متاحة لـ Aspose.PSD لـ Java؟

 ج5: نعم، يمكنك الحصول على ترخيص مؤقت من[هنا](https://purchase.aspose.com/temporary-license/).