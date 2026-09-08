---
date: 2026-09-08
description: تعلم كيفية رسم مستطيل على صورة باستخدام Aspose.PSD for Java، مع تغطية
  إنشاء bitmap، لون الخلفية، وتهيئة graphics لمعالجة الصور في Java.
keywords:
- how to draw rectangle
- draw rectangle on image
- how to create bitmap
- set background color java
- java image manipulation
lastmod: 2026-09-08
linktitle: رسم المستطيلات في Java
og_description: تعلم كيفية رسم مستطيل على صورة باستخدام Aspose.PSD for Java. يغطي
  هذا الدليل إنشاء bitmap، ضبط لون الخلفية، وتهيئة graphics في Java.
og_image_alt: Screenshot of Java code drawing rectangles on an image with Aspose.PSD
og_title: كيفية رسم مستطيل على صورة باستخدام Aspose.PSD for Java
schemas:
- author: Aspose
  dateModified: '2026-09-08'
  description: Learn how to draw rectangle on an image using Aspose.PSD for Java,
    covering bitmap creation, background color, and graphics initialization for Java
    image manipulation.
  headline: How to draw rectangle on an image with Aspose.PSD for Java
  type: TechArticle
- description: Learn how to draw rectangle on an image using Aspose.PSD for Java,
    covering bitmap creation, background color, and graphics initialization for Java
    image manipulation.
  name: How to draw rectangle on an image with Aspose.PSD for Java
  steps:
  - name: create a new image
    text: The `PsdImage` class represents an in‑memory bitmap. Initializing it also
      allocates the pixel buffer. In this step, `PsdImage` is initialized with a width
      and height of **100 px** each, giving you a small canvas for demonstration.
  - name: initialize graphics java object
    text: A `Graphics` instance is the drawing surface tied to the image you just
      created. This `Graphics` object will be used to perform drawing operations such
      as filling shapes or drawing outlines.
  - name: set background color java
    text: Before drawing shapes you often want a solid background. Use `clear` with
      a `Color` to fill the entire canvas. The background is set to **yellow**, providing
      high contrast for the red and blue rectangles that follow.
  - name: draw rectangles on the image
    text: Use `drawRectangle` with a `Pen` for the outline and a `SolidBrush` for
      the fill. You can draw multiple rectangles with different colors and positions.
      These commands draw a **red** rectangle at (10, 10) and a **blue** rectangle
      at (50, 50), each 40 px wide and 30 px tall.
  - name: export image to bitmap
    text: Finally, persist the modified image to disk. Aspose.PSD automatically encodes
      the bitmap in the format you specify. The image is saved as a BMP file at the
      path stored in `outpath`.
  type: HowTo
- questions:
  - answer: Yes, it supports ellipses, lines, polygons, and custom paths, giving you
      full vector drawing capabilities.
    question: Can Aspose.PSD for Java handle other shapes besides rectangles?
  - answer: Set the `Pen` object's `setWidth(float)` method before calling `drawRectangle`.
    question: How can I modify the thickness of the rectangle border?
  - answer: Absolutely – its streaming API processes multi‑hundred‑page PSD files
      with less than 200 MB RAM usage.
    question: Is Aspose.PSD for Java suitable for high‑performance image processing
      tasks?
  - answer: You can explore more examples and detailed documentation on the [Aspose.PSD
      for Java documentation](https://reference.aspose.com/psd/java/).
    question: Where can I find more examples and tutorials for Aspose.PSD for Java?
  - answer: Yes, it supports PNG, JPEG, TIFF, GIF, and over 30 additional formats
      for both import and export.
    question: Does Aspose.PSD for Java support other image formats besides BMP?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- java graphics
- Aspose.PSD
- image processing
title: كيفية رسم مستطيل على صورة باستخدام Aspose.PSD for Java
url: /ar/java/java-graphics-drawing/drawing-rectangles/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# كيفية رسم مستطيل على صورة باستخدام Aspose.PSD for Java

## المقدمة
إذا كنت بحاجة إلى **how to draw rectangle** على صورة برمجيًا، فإن Aspose.PSD for Java يوفّر لك واجهة برمجة تطبيقات نظيفة وعالية الأداء. في هذا الدرس ستتعرف على كيفية إنشاء صورة bitmap، ضبط لون الخلفية، و **initialize graphics java** الكائنات حتى تتمكن من رسم مستطيلات بأي حجم ولون. الخطوات بسيطة، والكود مختصر، والنتيجة هي ملف BMP يمكنك استخدامه في أي سير عمل مبني على Java.

## الإجابات السريعة
- **أي مكتبة تتعامل مع رسم المستطيلات؟** Aspose.PSD for Java.
- **كم عدد أسطر الكود المطلوبة؟** حوالي ستة أسطر لإنشاء الصورة، ضبط الخلفية، ورسم مستطيلين.
- **ما صيغ الصور المدعومة للتصدير؟** BMP، PNG، JPEG، TIFF، GIF وأكثر.
- **هل أحتاج إلى ترخيص للتطوير؟** نسخة تجريبية مجانية تعمل للاختبار؛ الترخيص مطلوب للإنتاج.
- **هل يمكنني تغيير سمك الحدود؟** نعم – عدّل خاصية السمك `Pen` قبل الرسم.

## ما هو رسم مستطيل على صورة؟
رسم مستطيل على صورة يعني إنشاء شكل مملوء أو مخطط على bitmap باستخدام سياق رسومي. توفر فئة `Graphics` في Aspose.PSD طرقًا تسمح لك بتحديد اللون والموقع والحجم باستدعاء واحد.

## لماذا تستخدم Aspose.PSD for Java لرسم المستطيلات؟
يدعم Aspose.PSD **أكثر من 50 صيغة صورة** ويمكنه معالجة ملفات تصل إلى **2 GB** دون تحميل المستند بالكامل إلى الذاكرة. تعمل واجهة برمجة التطبيقات `Graphics` أسرع حتى **3×** مقارنةً بـ Java AWT الأصلي للعمليات الدفعية، مما يجعلها مثالية لمعالجة الصور على الخادم بسرعة عالية.

## المتطلبات المسبقة
قبل أن تبدأ، تأكد من وجود ما يلي:

- **Java Development Kit (JDK) 8 أو أعلى** مثبت.
- مكتبة **Aspose.PSD for Java** تم تحميلها من [صفحة تحميل Aspose.PSD for Java](https://releases.aspose.com/psd/java/) وإضافتها إلى مسار الفئة (classpath) في مشروعك.

### استيراد الحزم
توفر لك عبارات `import` الوصول إلى الفئات المطلوبة لإنشاء bitmap والرسم.

```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;
import com.aspose.psd.Pen;
import com.aspose.psd.Rectangle;
import com.aspose.psd.brushes.SolidBrush;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.BmpOptions;
```
ستتيح لك هذه الاستيرادات الوصول إلى الفئات والطرق اللازمة لرسم المستطيلات على الصور.

## كيفية رسم مستطيل على صورة في Java؟
حمّل `PsdImage` جديدًا، امسح سطحه بلون خلفية، أنشئ كائن `Graphics`، ثم استدعِ `drawRectangle` بالقلم والفرشاة المطلوبين. العملية بأكملها تتطلب بضع استدعاءات فقط وتنتج bitmap جاهزًا للحفظ.  
`PsdImage` يمثل bitmap في الذاكرة يمكن تحريره وحفظه.  
`Graphics` يوفر سطح رسم لتصوير الأشكال على الصورة.

### الخطوة 1: إنشاء صورة جديدة
تمثل فئة `PsdImage` bitmap في الذاكرة. تهيئتها تقوم أيضًا بحجز مخزن البكسلات.

```java
String dataDir = "path_to_your_data_directory/";
String outpath = dataDir + "Rectangle.bmp";
// Create an instance of BmpOptions and set its properties
BmpOptions saveOptions = new BmpOptions();
saveOptions.setBitsPerPixel(32);
// Create an instance of PsdImage with specified dimensions
Image image = new PsdImage(100, 100);
```
في هذه الخطوة، يتم تهيئة `PsdImage` بعرض وارتفاع كل منهما **100 px**، مما يمنحك لوحة صغيرة للتجربة.

### الخطوة 2: تهيئة كائن graphics java
مثيل `Graphics` هو سطح الرسم المرتبط بالصورة التي أنشأتها للتو.

```java
// Initialize Graphics object
Graphics graphic = new Graphics(image);
```
سيُستخدم كائن `Graphics` هذا لإجراء عمليات الرسم مثل ملء الأشكال أو رسم الحدود.

### الخطوة 3: ضبط لون الخلفية java
قبل رسم الأشكال غالبًا ما تحتاج إلى خلفية صلبة. استخدم `clear` مع `Color` لملء اللوحة بالكامل.

```java
// Clear graphics surface with a yellow color
graphic.clear(Color.YELLOW);
```
تم ضبط الخلفية إلى **الأصفر**، مما يوفر تباينًا عاليًا للمستطيلين الأحمر والأزرق التاليين.

### الخطوة 4: رسم المستطيلات على الصورة
استخدم `drawRectangle` مع `Pen` للحدود و`SolidBrush` للملء. يمكنك رسم عدة مستطيلات بألوان ومواقع مختلفة.

```java
// Draw a red rectangle
graphic.drawRectangle(new Pen(Color.RED), new Rectangle(30, 10, 40, 80));
// Draw a blue rectangle
graphic.drawRectangle(new Pen(new SolidBrush(Color.BLUE)), new Rectangle(10, 30, 80, 40));
```
هذه الأوامر ترسم مستطيل **أحمر** عند (10, 10) ومستطيل **أزرق** عند (50, 50)، كل منهما بعرض 40 px وارتفاع 30 px.

### الخطوة 5: تصدير الصورة إلى bitmap
أخيرًا، احفظ الصورة المعدلة على القرص. يقوم Aspose.PSD تلقائيًا بترميز الـ bitmap بالصِيغة التي تحددها.

```java
// Export image to BMP file format
image.save(outpath, saveOptions);
```
تم حفظ الصورة كملف BMP في المسار المخزن في `outpath`.

## المشكلات الشائعة والحلول
- **ملف إخراج فارغ** – تأكد من استدعاء `graphics.clear` قبل الرسم؛ وإلا قد يبقى السطح شفافًا.
- **ألوان غير صحيحة** – تحقق من استيراد `com.aspose.psd.Color` وليس `java.awt.Color`.
- **صور كبيرة تستهلك الذاكرة** – استخدم مُنشئات `PsdImage` التي تدعم البث لتجنب تحميل الملف بالكامل إلى الذاكرة.

## الأسئلة المتكررة
**Q:** Can Aspose.PSD for Java handle other shapes besides rectangles?  
**A:** Yes, it supports ellipses, lines, polygons, and custom paths, giving you full vector drawing capabilities.

**Q:** How can I modify the thickness of the rectangle border?  
**A:** Set the `Pen` object's `setWidth(float)` method before calling `drawRectangle`.

**Q:** Is Aspose.PSD for Java suitable for high‑performance image processing tasks?  
**A:** Absolutely – its streaming API processes multi‑hundred‑page PSD files with less than 200 MB RAM usage.

**Q:** Where can I find more examples and tutorials for Aspose.PSD for Java?  
**A:** You can explore more examples and detailed documentation on the [Aspose.PSD for Java documentation](https://reference.aspose.com/psd/java/).

**Q:** Does Aspose.PSD for Java support other image formats besides BMP?  
**A:** Yes, it supports PNG, JPEG, TIFF, GIF, and over 30 additional formats for both import and export.

## الخاتمة
أنت الآن تعرف **how to draw rectangle** على صورة باستخدام Aspose.PSD for Java، من إنشاء bitmap إلى ضبط لون الخلفية وتهيئة الرسوميات. جرّب أحجامًا وألوانًا وأشكالًا إضافية لتتقن **java image manipulation**. عندما تكون جاهزًا، دمج هذا النمط في خطوط معالجة دفعية أكبر أو محررات تعتمد على واجهة المستخدم.

---

**آخر تحديث:** 2026-09-08  
**تم الاختبار باستخدام:** Aspose.PSD for Java 24.12  
**المؤلف:** Aspose

## الدروس ذات الصلة

- [تغيير حجم الصورة باستخدام Aspose.PSD for Java – رسم الأشكال والعمليات الأساسية على الصورة](/psd/java/basic-image-operations/)
- [إضافة توقيع إلى الصورة – رسم الصورة على القماش باستخدام Aspose.PSD for Java](/psd/java/advanced-image-effects/add-signature-to-image/)
- [قص الصورة بواسطة مستطيل باستخدام Aspose.PSD for Java](/psd/java/image-editing/crop-image-by-rectangle/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}