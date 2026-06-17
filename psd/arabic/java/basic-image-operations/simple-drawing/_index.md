---
date: 2026-06-13
description: تعلم كيفية رسم مستطيل في ملفات PSD باستخدام Aspose.PSD for Java. يوضح
  هذا الدليل step‑by‑step code، إضافة layers، server‑side image processing ورسم shape
  drawing.
keywords:
- how to draw rectangle
- how to create psd
- java graphics draw rectangle
- server side image processing
- add layer to psd
linktitle: تنفيذ رسم بسيط
schemas:
- author: Aspose
  dateModified: '2026-06-13'
  description: Learn how to draw rectangle in PSD files using Aspose.PSD for Java.
    This guide shows step‑by‑step code, adding layers, server‑side image processing
    and shape drawing.
  headline: How to Draw Rectangle in PSD with Aspose.PSD for Java
  type: TechArticle
- questions:
  - answer: Yes, the `Graphics` class also supports drawing ellipses, lines, and custom
      paths via the `drawPath` method.
    question: Can I draw other shapes besides rectangles?
  - answer: Absolutely; you can use `SolidBrush` with an ARGB color to include alpha
      transparency, enabling semi‑transparent overlays.
    question: Does Aspose.PSD support transparency in drawn shapes?
  - answer: Yes, each `Layer` object has a `setOpacity` method that accepts a value
      from 0 to 255, allowing fine‑grained control over layer transparency.
    question: Is it possible to edit the opacity of a layer?
  - answer: Use `PsdImage image = (PsdImage)Image.load("path/to/file.psd");` before
      manipulating layers. The loaded image retains all original layers and masks.
    question: How do I load an existing PSD file instead of creating a new one?
  type: FAQPage
second_title: Aspose.PSD Java API
title: كيفية رسم مستطيل في PSD باستخدام Aspose.PSD for Java
url: /ar/java/basic-image-operations/simple-drawing/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# كيفية رسم مستطيل في PSD باستخدام Aspose.PSD للـ Java

## المقدمة

في هذا الدرس ستكتشف **كيفية رسم مستطيل** داخل ملف Photoshop PSD باستخدام مكتبة Aspose.PSD للـ Java النقية. سواءً كنت تبني خط أنابيب أصول من جانب الخادم، أو تقوم بأتمتة إنشاء الصور المصغرة، أو تضيف رسومات ديناميكية إلى تصاميم موجودة، فإن الخطوات أدناه تمنحك حلاً كاملاً وجاهزًا للإنتاج. سنغطي إنشاء مستند PSD جديد، إضافة طبقة، مسح الخلفية، وأخيرًا رسم مستطيلين أحمر وأزرق—كل ذلك دون الحاجة لتشغيل Photoshop.

## إجابات سريعة
- **ما هو الصنف الأساسي لإنشاء ملف PSD؟** `PsdImage`
- **ما هي الطريقة التي تمسح لون خلفية الطبقة؟** `Graphics.clear(Color)`
- **كيف ترسم مستطيلًا أحمر؟** `graphic.drawRectangle(new Pen(Color.getRed()), new Rectangle(...))`
- **هل أحتاج إلى ترخيص للتطوير؟** نسخة تجريبية مجانية تعمل للاختبار؛ الترخيص مطلوب للإنتاج.
- **هل يمكنني تعديل ملفات PSD الموجودة باستخدام نفس الـ API؟** نعم، Aspose.PSD يدعم تحرير PSD بالكامل.

## ما هو رسم مستطيل أحمر في ملف PSD؟

يعني رسم مستطيل أحمر استخدام كائن `Graphics` لتصيير شكل مستطيل مملوء أو محدد باللون الأحمر على طبقة محددة من صورة PSD. هذه العملية شائعة لتسليط الضوء على مناطق، إنشاء نواقل مؤقتة، أو إضافة رسومات بسيطة برمجيًا.

## لماذا تستخدم Aspose.PSD للـ Java لمعالجة ملفات PSD؟

يدعم Aspose.PSD للـ Java **أكثر من 50 تنسيقًا للإدخال والإخراج**، ويمكنه معالجة ملفات PSD متعددة المئات من الصفحات دون تحميل الملف بالكامل إلى الذاكرة، ويعمل على أي منصة تدعم Java 8 أو أعلى. محرك معالجة الصور من جانب الخادم يلغي الحاجة إلى Photoshop، يقلل من تكاليف الترخيص، ويمكن من سير عمل آلي يتعامل مع ما يصل إلى **10 GB** من بيانات الصور في الساعة على جهاز افتراضي بسيط.

## المتطلبات المسبقة

- مجموعة تطوير جافا (JDK) 8 أو أحدث مثبتة على جهازك.  
- مكتبة Aspose.PSD للـ Java. يمكنك تنزيلها من [توثيق Aspose.PSD للـ Java](https://reference.aspose.com/psd/java/).

## استيراد الحزم

جمل `import` تجلب الأصناف المطلوبة إلى النطاق حتى تتمكن من العمل مع صور PSD، الطبقات، الألوان والرسومات.

الصنف `PsdImage` هو الكائن الأعلى مستوى في Aspose.PSD الذي يمثل ملف PSD واحد في الذاكرة.  
`Graphics` يوفر بدائيات الرسم مثل الخطوط، المستطيلات والبيضاوي.  
`Color` و `Pen` يتيحان لك تحديد ألوان الخط وسمكه.  
الصنف `Layer` يمثل طبقة صورة فردية داخل مستند PSD.  
الصنف `Rectangle` يحدد موقع وحجم المنطقة المستطيلة المستخدمة في عمليات الرسم.  
الصنف `SolidBrush` يملأ الأشكال بلون صلب.

## ما هي الخطوة الأولى لإنشاء مستند PSD؟

تقوم بإنشاء كائن `PsdImage` بتوفير عرض وارتفاع القماش بالبكسل، مما ينشئ هيكل ملف PSD فارغ. بعد إعداد أي طبقات أو خلفية أولية، استدعِ طريقة `save` مع مسار ملف لكتابة المستند إلى القرص. هذا يجهز الصورة لعمليات التحرير اللاحقة.

## الخطوة 1: إنشاء مستند جديد

أولاً، أنشئ مستند PSD جديد بالحجم المطلوب للقماش. سيستضيف هذا المستند الطبقة التي سنرسم عليها.

```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Pen;
import com.aspose.psd.Rectangle;
import com.aspose.psd.brushes.SolidBrush;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
```

## كيف تضيف طبقة فارغة جديدة إلى صورة PSD؟

أولاً، أنشئ كائن `Layer` جديد بنفس العرض والارتفاع للـ `PsdImage` الأصلية. ثم أضف هذه الطبقة إلى مجموعة `Layers` الخاصة بالصورة باستخدام طريقة `add`. بمجرد أن تصبح الطبقة جزءًا من الصورة، احصل على كائن `Graphics` الخاص بها لأداء عمليات الرسم؛ بدون هذه الخطوة لن تظهر الرسومات.

## الخطوة 2: إضافة طبقة

بعد ذلك، أضف طبقة فارغة جديدة تمتد عبر كامل عرض وارتفاع الصورة. الطبقات ضرورية لفصل عمليات الرسم.

```java
//ExStart:CreateDocument
String outputDir = "Your Document Directory";
String outPsdFilePath = outputDir + "output.psd";
int width = 100;
int height = 100;

PsdImage image = new PsdImage(width, height);
//ExEnd:CreateDocument
```

## ما هو هدف مسح لون خلفية الطبقة؟

استدعاء `Graphics.clear` بلون `Color` محدد يملأ الطبقة بالكامل بذلك اللون، مما يعيد تعيين جميع بيانات البكسل. يضمن ذلك إزالة أي محتوى سابق وأن تبدأ الطبقة من خلفية معروفة، مما يجنب الشفافية غير المتوقعة أو خلط الألوان عند فتح أو تحرير PSD لاحقًا في Photoshop.

## الخطوة 3: رسم الأشكال

سنستخدم الصنف `Graphics` للتلاعب ببيانات بكسل الطبقة. أدناه ثلاثة أمثلة توضح مسح الخلفية ورسم مستطيلات بألوان مختلفة.

### مسح لون الطبقة (تعيين الخلفية إلى أصفر)

```java
//ExStart:AddLayer
Layer layer = new Layer();
layer.setBottom(height);
layer.setRight(width);
image.addLayer(layer);
//ExEnd:AddLayer
```

### رسم مستطيل أحمر (التركيز الأساسي)

```java
//ExStart:DrawRectangleYellow
Graphics graphic = new Graphics(layer);
graphic.clear(Color.getYellow());
//ExEnd:DrawRectangleYellow
```

### رسم مستطيل أزرق (مثال إضافي)

```java
//ExStart:DrawRedRectangle
graphic.drawRectangle(new Pen(Color.getRed()), new Rectangle(30, 10, 40, 80));
//ExEnd:DrawRedRectangle
```

## كيف تحفظ ملف PSD المعدل على القرص؟

استخدم طريقة `save` على كائن `PsdImage`، مع تمرير مسار الملف الكامل واختيارياً تحديد تنسيق الصورة المطلوب (PSD هو الافتراضي). هذا يكتب جميع الطبقات، الأقنعة، وأوامر الرسم في ملف PSD واحد يتوافق مع مواصفات Photoshop، مما يسمح بفتحه دون تحذيرات.

## الخطوة 4: حفظ التغييرات

أخيرًا، اكتب صورة PSD المعدلة إلى القرص. سيحتوي الملف على الطبقة الجديدة والأشكال المرسومة.

```java
//ExStart:DrawBlueRectangle
graphic.drawRectangle(new Pen(new SolidBrush(Color.getBlue())), new Rectangle(10, 30, 80, 40));
//ExEnd:DrawBlueRectangle
```

## مشكلات شائعة وحلول

- **الطبقة غير مرئية بعد الرسم:** تأكد من إضافة الطبقة إلى الصورة **قبل** إنشاء كائن `Graphics`. يجب أن تكون سطح الرسم مرتبطًا بطبقة صالحة.
- **الألوان تظهر غير صحيحة:** تحقق من أنك تستخدم `Color.getRed()` (أو `Color.getBlue()`) بدلاً من إنشاء قيمة RGB مخصصة تتجاوز النطاق 0‑255.
- **الملف غير محفوظ:** تأكد من وجود مسار `outputDir` وأن التطبيق يمتلك أذونات الكتابة. على لينكس، قد تحتاج إلى تعديل ملكية المجلد أو استخدام `Files.createDirectories`.
- **تباطؤ الأداء على ملفات كبيرة:** استخدم `setLoadOptions` في `PsdImage` لتحميل القنوات المطلوبة فقط، مما يقلل استهلاك الذاكرة لملفات PSD أكبر من 200 MB.

## الأسئلة المتكررة

**س1: هل يمكنني استخدام Aspose.PSD للـ Java لتعديل ملفات PSD الموجودة؟**  
ج1: نعم، Aspose.PSD للـ Java يوفر وظائف واسعة لتحرير وتعديل ملفات PSD الموجودة، بما في ذلك إعادة ترتيب الطبقات، تعديل الأقنعة والرسم المتجهي.

**س2: أين يمكنني العثور على دعم Aspose.PSD للـ Java؟**  
ج2: يمكنك زيارة [منتدى Aspose.PSD للـ Java](https://forum.aspose.com/c/psd/34) للحصول على مساعدة من المجتمع وردود رسمية من Aspose.

**س3: هل هناك نسخة تجريبية مجانية متاحة لـ Aspose.PSD للـ Java؟**  
ج3: نعم، يمكنك الوصول إلى النسخة التجريبية المجانية [من هنا](https://releases.aspose.com/). تشمل التجربة جميع الميزات لكنها تضيف علامة مائية إلى الملفات المحفوظة.

**س4: كيف يمكنني شراء ترخيص لـ Aspose.PSD للـ Java؟**  
ج4: يمكنك شراء ترخيص من [صفحة شراء Aspose.PSD](https://purchase.aspose.com/buy). تشمل خيارات الترخيص الدائم، الاشتراك، وترخيص المواقع.

**س5: هل تتوفر تراخيص مؤقتة لـ Aspose.PSD للـ Java؟**  
ج5: نعم، يمكنك الحصول على ترخيص مؤقت من [هنا](https://purchase.aspose.com/temporary-license/).

## أسئلة متكررة إضافية

**س: هل يمكنني رسم أشكال أخرى غير المستطيلات؟**  
ج: نعم، الصنف `Graphics` يدعم أيضًا رسم البيضاوي، الخطوط، والمسارات المخصصة عبر طريقة `drawPath`.

**س: هل يدعم Aspose.PSD الشفافية في الأشكال المرسومة؟**  
ج: بالتأكيد؛ يمكنك استخدام `SolidBrush` مع لون ARGB لتضمين شفافية ألفا، مما يتيح طبقات نصف شفافة.

**س: هل يمكن تعديل شفافية طبقة؟**  
ج: نعم، كل كائن `Layer` يحتوي على طريقة `setOpacity` التي تقبل قيمة من 0 إلى 255، مما يسمح بتحكم دقيق في شفافية الطبقة.

**س: كيف أحمل ملف PSD موجود بدلاً من إنشاء ملف جديد؟**  
ج: استخدم `PsdImage image = (PsdImage)Image.load("path/to/file.psd");` قبل تعديل الطبقات. الصورة المحملة تحتفظ بجميع الطبقات والأقنعة الأصلية.

## الخاتمة

لقد أتقنت الآن **كيفية رسم مستطيل** داخل ملف PSD والتعامل مع الطبقات باستخدام Aspose.PSD للـ Java. من خلال إنشاء مستند، إضافة طبقة، مسح خلفيتها، والرسم باستخدام واجهة `Graphics`، يمكنك أتمتة عدد لا يحصى من مهام التصميم على جانب الخادم. جرب أقلامًا وفرشًا وتأثيرات طبقة مختلفة لتوسيع هذا الأساس إلى خطوط إنتاج صور متكاملة.

```java
//ExStart:SaveChanges
image.save(outPsdFilePath);
//ExEnd:SaveChanges
```

{{< blocks/products/products-backtop-button >}}

## دروس ذات صلة

- [كيفية رسم الأشكال Java – عمليات الصورة الأساسية](/psd/java/basic-image-operations/)
- [تغيير الحجم ببساطة مع Aspose.PSD – مكتبة معالجة صور Java](/psd/java/basic-image-operations/simple-resizing/)
- [قص صورة بمستطيل في Aspose.PSD للـ Java](/psd/java/image-editing/crop-image-by-rectangle/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

**آخر تحديث:** 2026-06-13  
**تم الاختبار مع:** Aspose.PSD for Java 24.12 (أحدث نسخة عند كتابة هذا المقال)  
**المؤلف:** Aspose