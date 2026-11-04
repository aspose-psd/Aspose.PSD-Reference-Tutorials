---
date: 2026-11-04
description: تعلم كيفية استخدام Aspose.PSD for Java لتطبيق invert adjustment layer،
  ومعالجة صور PSD دفعيًا، وإنشاء ملفات PSD ذات الصورة السلبية.
keywords:
- how to use aspose
- batch process psd images
- create negative image psd
- image processing java library
- apply multiple adjustment layers
lastmod: 2026-11-04
linktitle: Invert Adjustment Layer
og_description: كيفية استخدام Aspose.PSD for Java لإضافة invert adjustment layer،
  ومعالجة صور PSD دفعيًا، وإنشاء صورة سلبية بصيغة PSD. اتبع الدليل خطوة بخطوة.
og_image_alt: Screenshot showing Aspose.PSD Java code adding an invert adjustment
  layer
og_title: كيفية استخدام Aspose.PSD لإضافة invert adjustment layer في Java
schemas:
- author: Aspose
  dateModified: '2026-11-04'
  description: Learn how to use Aspose.PSD for Java to apply an invert adjustment
    layer, batch process PSD images, and create negative image PSD files.
  headline: How to use Aspose.PSD to add an invert adjustment layer in Java
  type: TechArticle
- questions:
  - answer: Yes, it supports Java 6.0 and later, including Java 8, 11, and 17.
    question: Is Aspose.PSD compatible with all Java versions?
  - answer: Absolutely. After adding the invert layer you can call `addBrightnessAdjustmentLayer()`,
      `addHueSaturationAdjustmentLayer()`, etc., to stack effects.
    question: Can I apply multiple adjustment layers in a single operation?
  - answer: The complete documentation is available [Aspose.PSD Java API reference](https://reference.aspose.com/psd/java/).
    question: Where can I find the full API reference?
  - answer: Yes, you can download a trial version [Aspose.PSD trial download](https://releases.aspose.com/).
    question: Is there a free trial for Aspose.PSD?
  - answer: Request a temporary license [temporary license request page](https://purchase.aspose.com/temporary-license/).
    question: How do I obtain a temporary license for testing?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- aspose psd
- java image processing
- invert adjustment layer
- batch psd processing
title: كيفية استخدام Aspose.PSD لإضافة invert adjustment layer في Java
url: /ar/java/advanced-image-manipulation/invert-adjustment-layer/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# كيفية استخدام Aspose.PSD لإضافة طبقة تعديل عكسية في Java

## مقدمة

إذا كنت تبحث عن مكتبة **image processing java library** قوية، فإن Aspose.PSD for Java هي واحدة من أكثر الخيارات مرونةً في السوق. في هذا البرنامج التعليمي ستتعرف على **كيفية استخدام Aspose** لإدراج **Invert Adjustment Layer** في ملف PSD، وتكديسه مع تعديلات أخرى، وحتى تشغيل العملية على عشرات الملفات. سواءً كنت تبني أداة معالجة دفعات، أو خدمة صور على الخادم، أو محرر صورة واحدة، فإن الخطوات أدناه ستنقلك من PSD المصدر إلى صورة سلبية قابلة للتحرير بالكامل في دقائق.

## إجابات سريعة

- **ماذا يفعل Invert Adjustment Layer؟** يقلب كل قيمة RGB في المنطقة المحددة، محولاً الصورة إلى سالب فوتوغرافي.  
- **أي مكتبة توفر هذه الميزة؟** Aspose.PSD، مكتبة **image processing java library** رائدة.  
- **هل يمكنني تكديسه مع تعديلات أخرى؟** نعم – يمكنك **apply multiple adjustment layers** مثل Brightness/Contrast، Hue/Saturation، وأكثر.  
- **هل أحتاج إلى ترخيص للتطوير؟** يتوفر إصدار تجريبي مجاني؛ الترخيص مطلوب للاستخدام في الإنتاج.  
- **كم من الوقت تستغرق عملية التنفيذ؟** عادةً أقل من 10 دقائق لحالة استخدام أساسية.  

## ما هو Invert Adjustment Layer؟

طبقة تعديل العكس هي تعديل غير مدمر يعكس قيم الألوان لكل بكسل تؤثر عليه. لأنها تقع فوق مجموعة الطبقات، يمكنك تبديل رؤيتها أو إعادة ترتيبها دون تعديل دائم لبيانات الصورة الأصلية. هذه هي أسرع طريقة لـ **create negative image PSD** أو الحصول على مظهر فيلم سالب كلاسيكي.

## لماذا تستخدم Aspose.PSD كمكتبة image processing java library الخاصة بك؟

Aspose.PSD يدعم **200+ PSD features**، يمكنه قراءة وكتابة ملفات Photoshop دون الحاجة إلى Photoshop، ويعالج مستندات متعددة المئات من الصفحات باستخدام أقل من 500 ميغابايت من ذاكرة الكومة. يعمل على أي بيئة تشغيل Java (Java 6+)، مما يجعله مثالياً لـ **batch process psd images** على خوادم Windows أو Linux أو macOS.

## المتطلبات المسبقة

قبل أن تبدأ، تأكد من أن لديك:

1. **Aspose.PSD for Java** – قم بتنزيل أحدث JAR من الموقع الرسمي [Aspose.PSD for Java download page](https://releases.aspose.com/psd/java/).  
2. **Java Development Kit** – JDK 6.0 أو أحدث مثبت ومُعد في `PATH` الخاص بك.  

الآن أنت جاهز لكتابة الشيفرة.

## استيراد الحزم

تمثل الفئة `PsdImage` مستند Photoshop كامل في الذاكرة، بينما توجد فئات طبقة التعديل في الحزمة `com.aspose.psd.layers.adjustments`.

الفئة `PsdImage` هي الكائن الأعلى المستوى في Aspose.PSD الذي يضم بنية ملف PSD وبيانات البكسل. استورد المساحات الاسمية، ثم ستكون قادرًا على تحميل وتحرير وحفظ ملفات PSD.

## الخطوة 1: إعداد دليل المستند

حدد المجلد الذي يحتوي على ملف PSD المصدر ومكان حفظ الناتج. استخدام المسارات المطلقة يتجنب `NullPointerException` عندما يتغير دليل العمل.

## الخطوة 2: تحميل ملف PSD

حمّل الملف المصدر في كائن `PsdImage`. هذا الكائن يحتفظ بالهيكل الكامل للطبقات في الذاكرة، مما يتيح تعديلات غير مدمرة.

توفر الفئة `PsdImage` طريقة ثابتة `load` تقرأ رأس الملف، تتحقق من صحة الصيغة، وتُنشئ تمثيلًا في الذاكرة جاهزًا للتلاعب.

## الخطوة 3: إضافة طبقة تعديل عكسية

استدعِ الطريقة المدمجة لإدراج Invert Adjustment Layer فوق مجموعة الطبقات الحالية. يمكنك لاحقًا إضافة المزيد من الطبقات (مثل Brightness، Hue) لـ **apply multiple adjustment layers** في سير عمل واحد.

`addInvertAdjustmentLayer()` يضيف Invert Adjustment Layer إلى مجموعة طبقات PSD.

## الخطوة 4: حفظ الناتج

احفظ ملف PSD المعدل إلى القرص.

`save()` يكتب ملف PSD، بما في ذلك جميع الطبقات والبيانات الوصفية، إلى المسار المحدد.

يستخدم الحفظ نفس طريقة `save` التي تكتب المستند بالكامل، بما في ذلك جميع طبقات التعديل، الأقنعة، والبيانات الوصفية، إلى الصيغة المحددة.

### ماذا حدث؟

تم تحميل ملف PSD إلى كائن `PsdImage`، وتم إنشاء `InvertAdjustmentLayer` وإضافته كأعلى طبقة، ثم تم حفظ المستند. هذه السلسلة تحافظ على بيانات الصورة الأصلية مع إضافة تأثير عكس غير مدمر يمكن تبديله أو إعادة ترتيبه لاحقًا.

لقد استخدمت الآن بنجاح Aspose.PSD، وهي **image processing java library**، لتعديل ملف PSD.

## كيفية معالجة صور PSD دفعةً باستخدام تعديل العكس؟

حمّل كل ملف داخل حلقة `for`، طبق نفس الخطوات، واستدعِ `save` لكل تكرار. نظرًا لأن Aspose.PSD يعالج الملفات بطريقة تدفقية، يمكنك التعامل مع **hundreds of PSDs** مع الحفاظ على استهلاك الذاكرة أقل من 300 ميغابايت عن طريق إعادة استخدام نفس كائن `PsdImage`.

## كيفية تحويل PSD إلى صورة سلبية؟

أضف Invert Adjustment Layer كأعلى عنصر واحفظ المستند – هذه العملية تعادل **convert PSD to negative**. يمكنك لاحقًا تعطيل أو حذف الطبقة للعودة إلى المظهر الأصلي دون إعادة تحميل الملف المصدر.

## المشكلات الشائعة والنصائح

| المشكلة | السبب | الحل |
|-------|-------|----------|
| **NullPointerException on `Image.load`** | مسار ملف غير صحيح أو ملف مفقود | تحقق من `dataDir` واسم الملف؛ استخدم مسارات مطلقة للاختبار |
| **ترتيب الطبقة ليس كما هو متوقع** | إضافة طبقات بعد الموجودة يغيّر التكديس | أدخل طبقة العكس قبل التعديلات الأخرى، أو أعد الترتيب عبر `psdImage.getLayers().move()` |
| **تباطؤ الأداء على ملفات PSD الكبيرة** | تحميل ملفات كبيرة جدًا إلى الذاكرة | زيادة مساحة كومة JVM (`-Xmx2g`) أو معالجة الملفات على دفعات باستخدام `psdImage.getPages().get(0).getResources().setMemoryOptimized(true)` |

## الأسئلة المتكررة

**س: هل Aspose.PSD متوافق مع جميع إصدارات Java؟**  
ج: نعم، يدعم Java 6.0 وما بعده، بما في ذلك Java 8، 11، و 17.

**س: هل يمكنني تطبيق طبقات تعديل متعددة في عملية واحدة؟**  
ج: بالتأكيد. بعد إضافة طبقة العكس يمكنك استدعاء `addBrightnessAdjustmentLayer()`, `addHueSaturationAdjustmentLayer()`، إلخ، لتكديس التأثيرات.

**س: أين يمكنني العثور على مرجع API الكامل؟**  
ج: الوثائق الكاملة متاحة [Aspose.PSD Java API reference](https://reference.aspose.com/psd/java/).

**س: هل هناك نسخة تجريبية مجانية لـ Aspose.PSD؟**  
ج: نعم، يمكنك تنزيل نسخة تجريبية [Aspose.PSD trial download](https://releases.aspose.com/).

**س: كيف أحصل على ترخيص مؤقت للاختبار؟**  
ج: اطلب ترخيصًا مؤقتًا [temporary license request page](https://purchase.aspose.com/temporary-license/).

**آخر تحديث:** 2026-11-04  
**تم الاختبار مع:** Aspose.PSD 24.12 for Java  
**المؤلف:** Aspose  









```java
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.psd.PsdImage;
```

```java
String dataDir = "Your Document Directory";
```

```java
String filePath = dataDir + "InvertStripes_before.psd";
String outputPath = dataDir + "InvertStripes_after.psd";

PsdImage im = (PsdImage)Image.load(filePath);
```

```java
im.addInvertAdjustmentLayer();
```

```java
im.save(outputPath);
```

## دروس ذات صلة

- [إضافة طبقة تعديل مستوى إلى ملفات PSD باستخدام Aspose.PSD for Java](/psd/java/modifying-converting-psd-images/add-level-adjustment-layer-psd/)
- [كيفية إضافة طبقة تعديل – خالط القنوات في PSD (Java)](/psd/java/modifying-converting-psd-images/add-channel-mixer-adjustment-layer-psd/)
- [كيفية تعديل PSD - إضافة طبقة تعديل المنحنيات باستخدام Java](/psd/java/modifying-converting-psd-images/add-curves-adjustment-layer-psd/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}