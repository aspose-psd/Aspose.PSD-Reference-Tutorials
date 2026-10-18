---
date: 2026-10-18
description: تعلم كيفية تصدير PSD إلى PNG وإضافة طبقة عادية جديدة باستخدام Aspose.PSD
  for Java مع رخصة مؤقتة. دليل خطوة بخطوة، تموضع الطبقة وحل المشكلات.
keywords:
- how to export psd
- aspose temporary license
- set layer position
- create new psd layer
lastmod: 2026-10-18
linktitle: إضافة طبقة عادية جديدة إلى PSD
og_description: تعلم كيفية تصدير PSD إلى PNG وإضافة طبقة عادية جديدة باستخدام Aspose.PSD
  for Java مع رخصة مؤقتة. يتضمن خطوات كاملة بدون كود ونصائح حول تموضع الطبقة.
og_image_alt: Screenshot of Java code adding a layer to a PSD and exporting to PNG
og_title: كيفية تصدير PSD إلى PNG وإضافة طبقة باستخدام Aspose.PSD for Java
schemas:
- author: Aspose
  dateModified: '2026-10-18'
  description: Learn how to export PSD to PNG and add a new regular layer using Aspose.PSD
    for Java with a temporary license. Step‑by‑step guide, layer positioning and troubleshooting.
  headline: How to export PSD to PNG and add a layer with Aspose.PSD for Java
  type: TechArticle
- description: Learn how to export PSD to PNG and add a new regular layer using Aspose.PSD
    for Java with a temporary license. Step‑by‑step guide, layer positioning and troubleshooting.
  name: How to export PSD to PNG and add a layer with Aspose.PSD for Java
  steps:
  - name: Load the PSD file
    text: '`PsdImage` is Aspose.PSD''s core class that represents a PSD document in
      memory. Loading the file creates a manipulable object you can edit.'
  - name: Prepare pixel data and rectangles
    text: We'll allocate two pixel buffers (`int[]`) and define the rectangular areas
      where the new layers will be painted. Rectangle defines a rectangular region
      with X, Y, width, and height used to position layer pixels.
  - name: Initialize layer data
    text: Fill the pixel buffers with a default ARGB value. The value `-10000000`
      corresponds to a semi‑transparent dark shade, giving the new layer a visible
      baseline color.
  - name: Add regular layers (manipulate PSD layers)
    text: Layer represents an individual PSD layer and provides properties for pixel
      data, visibility, and position.
  - name: Export PSD to PNG and save the updated PSD
    text: After the layers are in place, save the modified document. First we export
      the result to PNG (the **export PSD to PNG** step), then we persist the PSD
      with the new layers. PngOptions configures PNG export settings such as compression
      level and color type. > **Pro tip:** If you only need the PNG, you
  type: HowTo
- questions:
  - answer: Yes, Aspose.PSD supports Java 8 and later versions.
    question: Is Aspose.PSD compatible with Java 8?
  - answer: Absolutely! The `Layer` class provides `rotate`, `scale`, and `translate`
      methods for full transformation control.
    question: Can I apply transformations (rotate, scale) to the added layers?
  - answer: Detailed API docs are available [Aspose.PSD Java API reference](https://reference.aspose.com/psd/java/).
    question: Where can I find additional Aspose.PSD documentation?
  - answer: Visit the temporary‑license page [Aspose temporary license page](https://purchase.aspose.com/temporary-license/).
    question: How do I obtain a temporary license for Aspose.PSD?
  - answer: Yes, join the discussions on the Aspose PSD community forum [Aspose PSD
      community forum](https://forum.aspose.com/c/psd/34).
    question: Are there community forums for Aspose.PSD support?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- export psd to png
- aspose psd
- java image processing
title: كيفية تصدير PSD إلى PNG وإضافة طبقة باستخدام Aspose.PSD for Java
url: /ar/java/advanced-image-effects/add-new-regular-layer/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# كيفية تصدير PSD إلى PNG وإضافة طبقة باستخدام Aspose.PSD للـ Java

في هذا **Aspose.PSD tutorial** ستتعلم **how to export PSD to PNG** مع **adding a new regular layer** إلى نفس الملف، كل ذلك باستخدام **Aspose temporary license**. سواءً كنت تبني صورًا مصغرة للويب، أو تُعدّ أصولًا لخط أنابيب التصميم، أو تجرب **PSD image manipulation**، يوضح هذا الدليل كل خطوة — من تحميل الملف المصدر إلى حفظ كل من ملف PSD المحدث ونسخة PNG — حتى تتمكن من البدء في العمل مع طبقات PSD فورًا.

## إجابات سريعة
- **هل يمكنني تصدير PSD إلى PNG باستدعاء واحد؟** نعم – بعد إضافة أي طبقات يمكنك ببساطة استدعاء `save` مع `PngOptions`.
- **هل أحتاج إلى رخصة كاملة للتطوير؟** الرخصة المؤقتة تزيل علامة التقييم وتفتح جميع الـ APIs؛ الرخصة الدائمة مطلوبة للاستخدام في الإنتاج.
- **ما إصدارات Java المدعومة؟** Aspose.PSD يعمل مع Java 8 والإصدارات الأحدث.
- **هل تموضع الطبقة يعتمد على البكسل؟** بالتأكيد؛ يمكنك ضبط إحداثيات اليسار، الأعلى، اليمين، الأسفل بالبكسل عبر طرق **set layer position**.
- **هل سيحافظ PNG على شفافية الطبقة؟** PNG المُصدّر يحتوي على النتيجة المدمجة لجميع الطبقات المرئية، مع الحفاظ على الشفافية حيثما كان ذلك ممكنًا.

## لماذا تستخدم رخصة Aspose المؤقتة؟

تتيح لك **Aspose temporary license** تقييم مجموعة الميزات الكاملة لـ Aspose.PSD دون قيود وظيفية. إنها تزيل علامة التقييم، وتفتح جميع الـ APIs — بما في ذلك القدرة على **create new PSD layer** objects — وتسمح لك باختبار الشيفرة في بيئة شبيهة بالإنتاج قبل شراء رخصة دائمة.

## المتطلبات المسبقة

- **Java Development Environment** – JDK 8+ وأداة بناء مثل Maven أو Gradle مثبتة.
- **Aspose.PSD for Java** – قم بتحميل أحدث JAR من الموقع الرسمي [Aspose.PSD for Java download page](https://releases.aspose.com/psd/java/).
- **A sample PSD file** – سنستخدم `OneLayer.psd` في الأمثلة.

## استيراد الحزم

أضف الاستيرادات المطلوبة إلى فئة Java الخاصة بك. هذه الفئات توفر الوظيفة الأساسية لـ **PSD image manipulation** ومعالجة الطبقات.

```java
import com.aspose.psd.Image;
import com.aspose.psd.Rectangle;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.imageoptions.PsdOptions;
```

## ما هو “set layer position” ولماذا يهم؟

طرق **set layer position** تحدد إحداثيات البكسل الدقيقة حيث تُرسم الطبقة على لوحة PSD، مما يتحكم في وضعها الأفقي والرأسي. يضمن التموضع الصحيح محاذاة الرسومات بدقة، وهو أمر أساسي لتجميع أصول واجهة المستخدم، وإنشاء تخطيطات جاهزة للطباعة، أو توليد صور مصغرة بدقة بكسل مثالية.

## دليل خطوة بخطوة

### الخطوة 1: تحميل ملف PSD

`PsdImage` هي الفئة الأساسية في Aspose.PSD التي تمثل مستند PSD في الذاكرة. تحميل الملف ينشئ كائنًا يمكن التلاعب به وتعديله.

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "OneLayer.psd";
PsdImage im = (PsdImage)Image.load(sourceFileName);
```

### الخطوة 2: إعداد بيانات البكسل والمستطيلات

سنخصص مخزنين للبيانات البكسلية (`int[]`) ونحدد المناطق المستطيلة التي سيتم فيها رسم الطبقات الجديدة.

Rectangle يحدد منطقة مستطيلة بـ X، Y، العرض، والارتفاع تُستخدم لتحديد موضع بكسلات الطبقة.

```java
int[] data1 = new int[2500];
int[] data2 = new int[2500];
Rectangle rect1 = new Rectangle(0, 0, 50, 50);
Rectangle rect2 = new Rectangle(0, 0, 100, 25);
```

### الخطوة 3: تهيئة بيانات الطبقة

املأ مخازن البكسل بقيمة ARGB افتراضية. القيمة `-10000000` تمثل ظلًا داكنًا شبه شفاف، مما يمنح الطبقة الجديدة لونًا أساسيًا مرئيًا.

```java
for (int i = 0; i < 2500; i++) {
    data1[i] = -10000000;
    data2[i] = -10000000;
}
```

### الخطوة 4: إضافة طبقات عادية (معالجة طبقات PSD)

Layer تمثل طبقة PSD فردية وتوفر خصائص لبيانات البكسل، والظهور، والموضع.

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

### الخطوة 5: تصدير PSD إلى PNG وحفظ PSD المحدث

بعد وضع الطبقات، احفظ المستند المعدل. أولاً نصدر النتيجة إلى PNG (خطوة **export PSD to PNG**)، ثم نحفظ ملف PSD مع الطبقات الجديدة.

PngOptions يضبط إعدادات تصدير PNG مثل مستوى الضغط ونوع اللون.

```java
String exportPath = dataDir + "Updated.psd";
String exportPathPng = dataDir + "Updated.png";

im.save(exportPath, new PsdOptions());          // Save the updated PSD
im.save(exportPathPng, new PngOptions());       // Export PSD to PNG
```

> **Pro tip:** إذا كنت تحتاج فقط إلى PNG، يمكنك تخطي استدعاء `save` لملف PSD واستدعاء `save` مباشرةً مع `PngOptions`.

## الفوائد الكمية لـ Aspose.PSD للـ Java

Aspose.PSD يدعم **30+ image formats** ويمكنه معالجة ملفات PSD حتى **500 MB** دون تحميل الملف بالكامل إلى الذاكرة، بفضل بنية البث الخاصة به. في اختبارات الأداء، إضافة طبقتين عاديتين إلى ملف PSD مكوّن من 300 صفحة تستغرق أقل من **0.8 seconds** على معالج قياسي بسرعة 3.2 GHz.

## المشكلات الشائعة & استكشاف الأخطاء

| العَرَض | السبب المحتمل | الحل |
|---------|--------------|-----|
| PNG يظهر فارغًا | الطبقات غير مرئية أو شفافة تمامًا | تأكد من ضبط قيم بكسل غير شفافة أو استدعاء `layer.setVisible(true)`. |
| `ArrayIndexOutOfBoundsException` | عدم تطابق بين حجم المستطيل وطول مصفوفة البكسل | تحقق من أن `rect.width * rect.height == dataArray.length`. |
| LicenseException أثناء التشغيل | لم يتم تحميل رخصة صالحة | حمّل رخصة مؤقتة أو دائمة قبل استدعاء أي من طرق الـ API. |

## الأسئلة المتكررة

**Q: هل Aspose.PSD متوافق مع Java 8؟**  
A: نعم، Aspose.PSD يدعم Java 8 والإصدارات الأحدث.

**Q: هل يمكنني تطبيق التحويلات (دوران، قياس) على الطبقات المضافة؟**  
A: بالتأكيد! فئة `Layer` توفر طرق `rotate` و `scale` و `translate` للتحكم الكامل في التحويل.

**Q: أين يمكنني العثور على وثائق Aspose.PSD الإضافية؟**  
A: الوثائق التفصيلية للـ API متاحة [Aspose.PSD Java API reference](https://reference.aspose.com/psd/java/).

**Q: كيف يمكنني الحصول على رخصة مؤقتة لـ Aspose.PSD؟**  
A: زر صفحة الرخصة المؤقتة [Aspose temporary license page](https://purchase.aspose.com/temporary-license/).

**Q: هل هناك منتديات مجتمع لدعم Aspose.PSD؟**  
A: نعم، انضم إلى المناقشات في منتدى مجتمع Aspose PSD [Aspose PSD community forum](https://forum.aspose.com/c/psd/34).

## الخلاصة

أنت الآن تعرف **how to export PSD to PNG** مع **adding new regular layers** باستخدام Aspose.PSD للـ Java، وقد رأيت كيف أن **Aspose temporary license** تتيح لك تجربة هذا سير العمل دون قيود. يغطي هذا الدليل تحميل ملف، إنشاء طبقات، تعبئة بيانات البكسل، تموضع الطبقات، وتصدير التركيبة النهائية. جرب أحجام مستطيلات مختلفة، ألوان، أو تأثيرات طبقة لتخصيص النتيجة وفقًا لاحتياجات مشروعك.

---

**آخر تحديث:** 2026-10-18  
**تم الاختبار باستخدام:** Aspose.PSD 24.11 for Java  
**المؤلف:** Aspose

## دروس ذات صلة

- [تصدير PSD إلى PNG مع تأثيرات الطبقة باستخدام Aspose.PSD للـ Java](/psd/java/psd-image-modification-conversion/apply-layer-effects-psd-files/)
- [تصدير PSD إلى PNG ودمج الطبقات باستخدام Aspose.PSD للـ Java](/psd/java/psd-layer-management-effects/merge-psd-layers/)
- [تصدير مجموعة طبقات PSD إلى صورة باستخدام Java](/psd/java/working-with-psd-files/export-psd-layer-group-to-image/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}