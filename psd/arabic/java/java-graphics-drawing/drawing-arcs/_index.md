---
date: 2026-09-03
description: تعلم كيفية java graphics draw arc باستخدام Aspose.PSD for Java. دليل
  خطوة بخطوة مع مقتطفات شفرة لإنشاء أقواس في ملفات PSD.
keywords:
- java graphics draw arc
- how to draw arcs java
- Aspose.PSD arc drawing
lastmod: 2026-09-03
linktitle: رسم أقواس في Java
og_description: تعلم كيفية java graphics draw arc مع Aspose.PSD for Java. يوضح هذا
  البرنامج التعليمي المتطلبات المسبقة، خطوات الشفرة، ونصائح لإنشاء أقواس في ملفات
  PSD.
og_image_alt: Screenshot of a Java program drawing an arc using Aspose.PSD
og_title: كيفية java graphics draw arc في Java – دليل Aspose.PSD
schemas:
- author: Aspose
  dateModified: '2026-09-03'
  description: Learn how to java graphics draw arc using Aspose.PSD for Java. Step‑by‑step
    guide with code snippets for creating arcs in PSD files.
  headline: How to java graphics draw arc in Java
  type: TechArticle
- description: Learn how to java graphics draw arc using Aspose.PSD for Java. Step‑by‑step
    guide with code snippets for creating arcs in PSD files.
  name: How to java graphics draw arc in Java
  steps:
  - name: set up your Java project
    text: Create a new Java project in your favourite IDE and add the Aspose.PSD JAR
      to the build path. Ensure the JAR is referenced correctly so the compiler can
      locate the library classes.
  - name: import required packages
    text: 'To begin, import the necessary packages from Aspose.PSD for Java: The `Pen`
      class defines the colour, width, and style of the line used to draw the arc.
      These imports expose the `PsdImage`, `Graphics`, `Pen`, and colour classes needed
      for arc drawing.'
  - name: initialise image and graphics objects
    text: 'Create an instance of `PsdImage` and obtain a `Graphics` object to draw
      on: Replace `"Your Document Directory"` with the folder where you want the output
      files saved.'
  - name: define arc parameters
    text: 'Set the geometry and style of the arc—its bounding rectangle, start angle,
      sweep angle, colour, and thickness: Adjust the values to match the visual design
      you need; for example, a 200 px radius arc starting at 45° and sweeping 270°.'
  - name: draw the arc and save the image
    text: 'Invoke `drawArc` on the `Graphics` object and persist the PSD (or export
      to another format): The `drawArc` method of the `Graphics` class renders an
      arc defined by a bounding rectangle, start angle, and sweep angle using the
      specified `Pen`. The snippet draws the arc on the canvas and saves it as a '
  type: HowTo
- questions:
  - answer: Yes, the library can draw rectangles, ellipses, lines, polygons, and custom
      paths using the same `Graphics` API.
    question: Can Aspose.PSD for Java handle other shapes besides arcs?
  - answer: Create a `Pen` with the desired `Color` and width, then pass that `Pen`
      instance to `drawArc`.
    question: How do I change the arc colour and thickness?
  - answer: Absolutely. Aspose.PSD supports PNG, JPEG, TIFF, GIF and many more – just
      change the file extension in the `save` method.
    question: Is it possible to export the PSD to a format other than BMP?
  - answer: Visit the [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) for tutorials,
      code samples, and assistance from other developers.
    question: Where can I find more examples and community support?
  - answer: Yes, it can process files up to 2 GB and render arcs without loading the
      entire document into memory, thanks to its streaming architecture.
    question: Does the library work with large PSD files?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- java graphics
- Aspose.PSD
- arc drawing
- PSD manipulation
title: كيفية رسم قوس باستخدام java graphics في Java
url: /ar/java/java-graphics-drawing/drawing-arcs/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# كيفية رسم قوس Java graphics في Java

## مقدمة
في هذا الدرس ستكتشف كيفية **java graphics draw arc** باستخدام مكتبة Aspose.PSD for Java. رسم الأقواس برمجياً هو طلب شائع للمكونات UI المخصصة، تصورات البيانات، والتقارير الغنية بالرسومات. تمنحك Aspose.PSD for Java تحكمًا كاملاً في ملفات PSD (Photoshop Document)، مما يتيح لك إنشاء وتعديل وتصدير الصور دون الحاجة إلى تثبيت Photoshop.

## إجابات سريعة
- **أي مكتبة تدعم رسم الأقواس في Java؟** Aspose.PSD for Java.
- **هل أحتاج إلى ترخيص للاستخدام الإنتاجي؟** نعم، يلزم ترخيص تجاري للنشر غير التجريبي.
- **ما هي صيغ الملفات التي يمكنني التصدير إليها؟** BMP، PNG، JPEG، TIFF، GIF والمزيد.
- **هل يمكنني تغيير سمك القوس ولونه؟** نعم، عبر كائن `Pen` الممرّر إلى `drawArc`.
- **هل API متوافق مع Java 8 وما بعده؟** متوافق بالكامل مع Java 8‑21.

## ما هو Java graphics draw arc؟
`java graphics draw arc` يشير إلى عملية رسم مقطع خط منحني—قوس—على سطح رسومي باستخدام APIs الرسم في Java. في سياق Aspose.PSD، يتم تنفيذ العملية على كائن `Graphics` الذي يمثل طبقة داخل ملف PSD.

## لماذا تستخدم Aspose.PSD for Java لرسم الأقواس؟
يدعم Aspose.PSD **أكثر من 50** صيغة صورة ومستند، ويمكنه التعامل مع ملفات PSD بحجم **حتى 2 GB**، ويعالج مستندات مئات الصفحات دون تحميل الملف بالكامل إلى الذاكرة. هذا الأداء القابل للقياس يجعلها مثالية لتوليد الرسومات على الخادم حيث السرعة واستخدام الذاكرة مهمان.

## المتطلبات المسبقة
1. **بيئة تطوير Java** – قم بتثبيت Java من [Oracle's website](https://www.oracle.com/java/).  
2. **مكتبة Aspose.PSD for Java** – قم بتنزيل أحدث JAR من [download page](https://releases.aspose.com/psd/java/). اتبع التعليمات المقدمة لإضافة الـ JAR إلى مسار الفئات (classpath) في مشروعك.

## كيفية رسم قوس Java graphics في Java؟
حمّل `PsdImage` جديدًا، احصل على سطح `Graphics` الخاص به، قم بتكوين `Pen` باللون والسُمك المطلوبين، ثم استدعِ `drawArc`. هذه السلسلة المختصرة تنشئ القوس وتحفظ النتيجة في سلسلة طريقة واحدة. من خلال تعديل المستطيل المحيط ومعلمات الزاوية يمكنك التحكم في الحجم والموقع ومسار القوس لتلبية متطلبات التصميم الخاصة بك.

### الخطوة 1: إعداد مشروع Java الخاص بك
أنشئ مشروع Java جديدًا في بيئة التطوير المتكاملة (IDE) المفضلة لديك وأضف ملف Aspose.PSD JAR إلى مسار البناء. تأكد من الإشارة إلى الـ JAR بشكل صحيح حتى يتمكن المترجم من العثور على فئات المكتبة.

### الخطوة 2: استيراد الحزم المطلوبة
لبدء، استورد الحزم اللازمة من Aspose.PSD for Java:
تحدد فئة `Pen` اللون والعرض والنمط للخط المستخدم لرسم القوس.
```java
import com.aspose.psd.Color;
import static com.aspose.psd.ColorAdjustType.Pen;
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;
import com.aspose.psd.Pen;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.BmpOptions;
```  
تُظهر هذه الاستيرادات فئات `PsdImage` و `Graphics` و `Pen` وفئات اللون المطلوبة لرسم القوس.

### الخطوة 3: تهيئة كائنات الصورة والرسومات
أنشئ نسخة من `PsdImage` واحصل على كائن `Graphics` للرسم عليه:
```java
String dataDir = "Your Document Directory";
// Initialize PsdImage object
PsdImage image = new PsdImage(100, 100);
// Initialize Graphics object and clear surface
Graphics graphics = new Graphics(image);
graphics.clear(Color.getYellow());
```  
استبدل `"Your Document Directory"` بالمجلد الذي تريد حفظ ملفات الإخراج فيه.

### الخطوة 4: تعريف معلمات القوس
حدد هندسة القوس ونمطه — المستطيل المحيط، زاوية البداية، زاوية المسح، اللون، والسُمك:
```java
int width = 100;
int height = 200;
int startAngle = 45;
int sweepAngle = 270;
```  
قم بتعديل القيم لتتناسب مع التصميم البصري الذي تحتاجه؛ على سبيل المثال، قوس نصف قطره 200 px يبدأ عند 45° ويمتد 270°.

### الخطوة 5: رسم القوس وحفظ الصورة
استدعِ `drawArc` على كائن `Graphics` واحفظ ملف PSD (أو صدّره إلى صيغة أخرى):
طريقة `drawArc` في فئة `Graphics` ترسم قوسًا معرفًا بمستطيل محيط، زاوية بداية، وزاوية مسح باستخدام الـ `Pen` المحدد.
```java
// Draw arc with specified Pen object (black color) and parameters
graphics.drawArc(new Pen(Color.getBlack()), 0, 0, width, height, startAngle, sweepAngle);
// Save the image in BMP format
String outputPath = dataDir + "Arc.bmp";
BmpOptions saveOptions = new BmpOptions();
saveOptions.setBitsPerPixel(32);
image.save(outputPath, saveOptions);
```  
المقتطف يرسم القوس على اللوحة ويحفظه كملف BMP. غيّر امتداد الملف في `outputPath` لتصديره إلى PNG أو JPEG أو TIFF.

## المشكلات الشائعة واستكشاف الأخطاء
- **وحدات الزاوية غير الصحيحة** – Aspose.PSD يتوقع الزوايا بالدرجات، وليس بالراديان. توفير الراديان سيؤدي إلى نتائج غير متوقعة.
- **سُمك القلم كبير جدًا** – الأقلام السميكة جدًا قد تتسبب في تجاوز القوس لحدود الصورة؛ قلل السُمك أو وسّع اللوحة.
- **مشكلات مسار الملف** – استخدم مسارات مطلقة أو تأكد من أن دليل العمل لديه أذونات كتابة لتجنب `IOException`.

## الأسئلة المتكررة

**س: هل يمكن لـ Aspose.PSD for Java التعامل مع أشكال أخرى غير الأقواس؟**  
ج: نعم، يمكن للمكتبة رسم المستطيلات، والبيضيات، والخطوط، والمتعددات، والمسارات المخصصة باستخدام نفس API `Graphics`.

**س: كيف يمكنني تغيير لون القوس وسُمكه؟**  
ج: أنشئ `Pen` بالـ `Color` والعرض المطلوبين، ثم مرّر تلك النسخة من `Pen` إلى `drawArc`.

**س: هل من الممكن تصدير ملف PSD إلى صيغة غير BMP؟**  
ج: بالتأكيد. يدعم Aspose.PSD PNG، JPEG، TIFF، GIF والعديد غيرها – فقط غيّر امتداد الملف في طريقة `save`.

**س: أين يمكنني العثور على المزيد من الأمثلة والدعم المجتمعي؟**  
ج: زر [منتدى Aspose.PSD](https://forum.aspose.com/c/psd/34) للحصول على دروس، عينات كود، ومساعدة من مطورين آخرين.

**س: هل تعمل المكتبة مع ملفات PSD الكبيرة؟**  
ج: نعم، يمكنها معالجة ملفات تصل إلى 2 GB ورسم الأقواس دون تحميل المستند بالكامل في الذاكرة، بفضل بنية البث الخاصة بها.

---

**آخر تحديث:** 2026-09-03  
**تم الاختبار مع:** Aspose.PSD for Java 24.11  
**المؤلف:** Aspose

## دروس ذات صلة

- [رسم وحفظ مستطيل في PSD باستخدام Aspose.PSD for Java](/psd/java/basic-image-operations/simple-drawing/)
- [تغيير حجم الصورة باستخدام Aspose.PSD for Java – رسم الأشكال والعمليات الأساسية على الصور](/psd/java/basic-image-operations/)
- [كيفية تغيير لون الحد في Java باستخدام Aspose.PSD](/psd/java/advanced-image-effects/add-stroke-layer-color/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}