---
date: 2026-09-08
description: تعلم كيفية رسم منحنيات Bezier في Java باستخدام Aspose.PSD للـ Java. اتبع
  step‑by‑step instructions، prerequisites، و code‑free examples.
keywords:
- how to draw bezier
- how to use pen
- bezier curve example java
- java graphics draw curve
lastmod: 2026-09-08
linktitle: رسم منحنيات Bezier في Java
og_description: كيفية رسم منحنيات Bezier في Java باستخدام Aspose.PSD. يغطي هذا الدليل
  prerequisites، step‑by‑step drawing، ونصائح لل high‑resolution images.
og_image_alt: Screenshot of a Java application rendering a Bezier curve with Aspose.PSD
og_title: كيفية رسم منحنيات Bezier في Java باستخدام مكتبة Aspose.PSD
schemas:
- author: Aspose
  dateModified: '2026-09-08'
  description: Learn how to draw bezier curves in Java using Aspose.PSD for Java.
    Follow step‑by‑step instructions, prerequisites, and code‑free examples.
  headline: How to draw bezier curves in Java with Aspose.PSD library
  type: TechArticle
- description: Learn how to draw bezier curves in Java using Aspose.PSD for Java.
    Follow step‑by‑step instructions, prerequisites, and code‑free examples.
  name: How to draw bezier curves in Java with Aspose.PSD library
  steps:
  - name: create an image instance
    text: 'The `PsdImage` class is Aspose.PSD''s top‑level object that represents
      a single PSD file in memory. First, you need to create an instance of the `PsdImage`
      class, which represents a PSD image in memory. Explanation: - `PsdImage` is
      instantiated with width and height parameters (100 × 100 pixels in th'
  - name: initialize graphics context
    text: 'The `Graphics` class provides drawing capabilities on a `PsdImage`. Next,
      initialize an instance of the `Graphics` class to perform drawing operations
      on the image. Explanation: - `Graphics` object is initialized with the `image`
      instance, allowing drawing operations.'
  - name: clear the graphics surface
    text: 'The `clear()` method sets the background colour of the graphics surface.
      Clear the graphics surface using a specific background colour, here `Color.getYellow()`.
      Explanation: - `clear()` method sets the background colour of the graphics surface.'
  - name: initialize pen for drawing
    text: 'The `Pen` object defines stroke attributes such as colour and width. Set
      up a `Pen` object with properties like colour and width to define how the curve
      will be drawn. Explanation: - `Pen` is initialized with black colour and 3‑pixel
      width.'
  - name: define bezier curve parameters
    text: 'Control points determine the curvature. Specify the control points and
      end points for the Bezier curve. Explanation: - `startX`, `startY`: Starting
      point of the curve. - `controlX1`, `controlY1`: First control point. - `controlX2`,
      `controlY2`: Second control point. - `endX`, `endY`: Ending point of'
  - name: draw the bezier curve
    text: 'The `drawBezier()` method renders the curve using the supplied `Pen` and
      points. Use the `drawBezier()` method to draw the Bezier curve onto the image
      using the previously defined `Pen` and control points. Explanation: - `drawBezier()`
      method draws the curve with specified parameters using the `blac'
  - name: save the image
    text: Saving the image persists the drawing to disk. Save the drawn image to a
      BMP file format.
  type: HowTo
- questions:
  - answer: Yes, repeat the `drawBezier()` call inside a loop, updating the control
      points for each curve.
    question: Can I draw multiple Bezier curves in the same image?
  - answer: Modify the `Pen` object's colour property (`Color.getBlack()` in the example)
      before invoking `drawBezier()`.
    question: How can I change the colour of the Bezier curve?
  - answer: Yes, Aspose.PSD for Java supports high‑resolution images with efficient
      memory management, handling files larger than 500 MB without loading the entire
      file into memory.
    question: Is Aspose.PSD for Java suitable for high‑resolution images?
  - answer: Yes, Aspose.PSD for Java supports exporting to PNG, JPEG, TIFF, and many
      other raster formats.
    question: Can I export the image to formats other than BMP?
  - answer: Visit the [Aspose.PSD for Java documentation](https://reference.aspose.com/psd/java/)
      for comprehensive guides and code samples.
    question: Where can I find more examples and documentation?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- drawing bezier
- Aspose.PSD
- Java graphics
- curve drawing
title: كيفية رسم منحنيات Bezier في Java باستخدام مكتبة Aspose.PSD
url: /ar/java/java-graphics-drawing/drawing-bezier-curves/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# كيفية رسم منحنيات بيزييه في Java باستخدام مكتبة Aspose.PSD

## مقدمة
إذا كنت بحاجة إلى معرفة **كيفية رسم أشكال بيزييه** في تطبيق Java لسطح المكتب أو الخادم، فإن Aspose.PSD for Java يوفر لك واجهة برمجة تطبيقات نظيفة وفعّالة في استهلاك الذاكرة. في هذا الدرس ستتعرف على الخطوات الدقيقة لإنشاء لوحة PSD، وتكوين قلم الرسم، وتعريف نقاط التحكم، ورسم منحنى بيزييه سلس—كل ذلك دون كتابة أي كود منخفض المستوى لمعالجة البكسلات.

## إجابات سريعة
- **ما المكتبة التي تتعامل مع الرسم؟** Aspose.PSD for Java.
- **كم عدد أسطر الكود المطلوبة؟** حوالي عشر عبارات مختصرة.
- **هل يمكنني تغيير لون المنحنى؟** نعم، عن طريق تعديل خاصية اللون في `Pen`.
- **هل يدعم الإخراج عالي الدقة؟** نعم، حتى ملفات بحجم 500 ميغابايت دون تحميل كامل للذاكرة.
- **هل أحتاج إلى ترخيص تجاري؟** النسخة التجريبية المجانية تكفي للتطوير؛ الترخيص مطلوب للإنتاج.

## ما هو منحنى بيزييه؟
منحنى بيزييه هو خط أملس معرف رياضياً يتم التحكم فيه بواسطة نقطتين أو أكثر. يُستخدم على نطاق واسع في الرسومات المتجهية، والرسوم المتحركة، وتصميم واجهات المستخدم لإنشاء أشكال أنيقة وقابلة للتوسع. يتحدد شكل المنحنى بنقطة البداية، نقطة النهاية، ونقطة أو أكثر من نقاط التحكم التي تؤثر على انحنائه، مما يسمح للمصممين بنمذجة مسارات معقدة باستخدام معلمات بسيطة.

## لماذا نستخدم Aspose.PSD لرسم منحنيات بيزييه؟
يدعم Aspose.PSD **أكثر من 30 صيغة صورة** ويمكنه معالجة **ملفات PSD مئات الصفحات** دون تحميل المستند بالكامل إلى الذاكرة. طريقة `drawBezier()` في المكتبة تتعامل تلقائيًا مع مضاد التعرج وإدارة الألوان، مما يقدم نتائج دقيقة على مستوى البكسل في أقل من ثانية للوح قياسي بحجم 100 × 100.

## المتطلبات المسبقة
1. **Java Development Kit (JDK)** – أي نسخة حديثة (8 أو أحدث) مثبتة ومُكوَّنة.
2. **Aspose.PSD for Java JAR** – قم بتحميل مكتبة Aspose.PSD for Java من [Aspose.PSD Java download](https://releases.aspose.com/psd/java/) وأضفها إلى مسار الفئات (classpath) في مشروعك.
3. **بيئة التطوير المتكاملة (IDE)** – مثل Eclipse أو IntelliJ IDEA أو NetBeans، مُعدّة مع JDK.

## استيراد الحزم
الاستيرادات التالية تجلب فئات Aspose.PSD المطلوبة لإنشاء الصور والرسم.
```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;
import com.aspose.psd.Pen;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.BmpOptions;
```

## كيف ترسم منحنيات بيزييه في Java؟
حمّل صورة `PsdImage` فارغة، أنشئ كائن `Graphics`، قم بتكوين `Pen`، حدد نقاط البداية، التحكم، والنهاية، استدعِ `drawBezier()`، وأخيرًا احفظ الصورة. هذه السلسلة تنتج منحنىً أملسًا باستدعاء طريقة واحدة ولا تتطلب حسابات يدوية للبكسلات.

### الخطوة 1: إنشاء نسخة صورة
فئة `PsdImage` هي الكائن الأعلى مستوى في Aspose.PSD الذي يمثل ملف PSD واحد في الذاكرة. أولاً، تحتاج إلى إنشاء نسخة من فئة `PsdImage`، التي تمثل صورة PSD في الذاكرة.
```java
String dataDir = "Your Document Directory";
Image image = new PsdImage(100, 100);
```
شرح:
- `PsdImage` يتم إنشاؤه بمعاملات العرض والارتفاع (100 × 100 بكسل في هذا المثال).

### الخطوة 2: تهيئة سياق الرسومات
فئة `Graphics` توفر إمكانيات الرسم على `PsdImage`. بعد ذلك، قم بتهيئة نسخة من فئة `Graphics` لتنفيذ عمليات الرسم على الصورة.
```java
Graphics graphics = new Graphics(image);
```
شرح:
- كائن `Graphics` يتم تهيئته باستخدام نسخة `image`، مما يسمح بعمليات الرسم.

### الخطوة 3: مسح سطح الرسومات
طريقة `clear()` تضبط لون خلفية سطح الرسومات. امسح سطح الرسومات باستخدام لون خلفية محدد، هنا `Color.getYellow()`.
```java
graphics.clear(Color.getYellow());
```
شرح:
- طريقة `clear()` تضبط لون خلفية سطح الرسومات.

### الخطوة 4: تهيئة القلم للرسم
كائن `Pen` يحدد خصائص الخط مثل اللون والعرض. قم بإعداد كائن `Pen` بخصائص مثل اللون والعرض لتحديد كيفية رسم المنحنى.
```java
Pen blackPen = new Pen(Color.getBlack(), 3);
```
شرح:
- `Pen` يتم تهيئته باللون الأسود وعرض 3 بكسل.

### الخطوة 5: تعريف معلمات منحنى بيزييه
نقاط التحكم تحدد الانحناء. حدد نقاط التحكم ونقاط النهاية لمنحنى بيزييه.
```java
float startX = 10, startY = 25;
float controlX1 = 20, controlY1 = 5;
float controlX2 = 55, controlY2 = 10;
float endX = 90, endY = 25;
```
شرح:
- `startX`، `startY`: نقطة بداية المنحنى.  
- `controlX1`، `controlY1`: نقطة التحكم الأولى.  
- `controlX2`، `controlY2`: نقطة التحكم الثانية.  
- `endX`، `endY`: نقطة نهاية المنحنى.

### الخطوة 6: رسم منحنى بيزييه
طريقة `drawBezier()` ترسم المنحنى باستخدام `Pen` والنقاط المقدمة. استخدم طريقة `drawBezier()` لرسم منحنى بيزييه على الصورة باستخدام `Pen` ونقاط التحكم المحددة مسبقًا.
```java
graphics.drawBezier(blackPen, startX, startY, controlX1, controlY1, controlX2, controlY2, endX, endY);
```
شرح:
- طريقة `drawBezier()` ترسم المنحنى بالمعلمات المحددة باستخدام `blackPen`.

### الخطوة 7: حفظ الصورة
حفظ الصورة يثبت الرسم على القرص. احفظ الصورة المرسومة بصيغة ملف BMP.
```java
String outpath = dataDir + "Bezier.bmp";
BmpOptions saveOptions = new BmpOptions();
image.save(outpath, saveOptions);
```

## المشكلات الشائعة والحلول
- **المنحنى يبدو مسطحًا** – تأكد من أن نقاط التحكم ليست على خط مستقيم مع نقطتي البداية والنهاية. قم بإزاحتها قليلاً لإنشاء انحناء.  
- **اللون لا يتغير** – تأكد من تعديل لون `Pen` قبل استدعاء `drawBezier()`.  
- **أخطاء نفاد الذاكرة على اللوحات الكبيرة** – استخدم مُنشئات `PsdImage` التي تتيح البث، أو قسّم الرسم إلى بلاطات.

## الأسئلة المتكررة

**س: هل يمكنني رسم عدة منحنيات بيزييه في نفس الصورة؟**  
ج: نعم، كرّر استدعاء `drawBezier()` داخل حلقة، مع تحديث نقاط التحكم لكل منحنى.

**س: كيف يمكنني تغيير لون منحنى بيزييه؟**  
ج: عدّل خاصية اللون لكائن `Pen` (`Color.getBlack()` في المثال) قبل استدعاء `drawBezier()`.

**س: هل Aspose.PSD for Java مناسب للصور عالية الدقة؟**  
ج: نعم، يدعم Aspose.PSD for Java الصور عالية الدقة مع إدارة فعّالة للذاكرة، ويتعامل مع ملفات أكبر من 500 ميغابايت دون تحميل الملف بالكامل إلى الذاكرة.

**س: هل يمكنني تصدير الصورة إلى صيغ غير BMP؟**  
ج: نعم، يدعم Aspose.PSD for Java التصدير إلى PNG، JPEG، TIFF، والعديد من صيغ الرسوم النقطية الأخرى.

**س: أين يمكنني العثور على المزيد من الأمثلة والوثائق؟**  
ج: زر [وثائق Aspose.PSD for Java](https://reference.aspose.com/psd/java/) للحصول على أدلة شاملة وعينات كود.

---

**آخر تحديث:** 2026-09-08  
**تم الاختبار مع:** Aspose.PSD for Java 24.11  
**المؤلف:** Aspose

## دروس ذات صلة

- [تغيير حجم الصورة باستخدام Aspose.PSD for Java – رسم الأشكال والعمليات الأساسية على الصورة](/psd/java/basic-image-operations/)
- [رسم وحفظ مستطيل في PSD باستخدام Aspose.PSD for Java](/psd/java/basic-image-operations/simple-drawing/)
- [كيفية تغيير لون الحد في Java باستخدام Aspose.PSD](/psd/java/advanced-image-effects/add-stroke-layer-color/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}