---
date: 2026-09-28
description: تعلم كيفية رسم ellipse في Java باستخدام Aspose.PSD، الدليل الرائد لمعالجة
  الصور في Java لإنشاء ellipses وأشكال أخرى.
keywords:
- how to draw ellipse
- draw shapes java
- java image processing tutorial
- create ellipse image
- draw ellipses java
lastmod: 2026-09-28
linktitle: رسم Ellipses في Java
og_description: تعلم كيفية رسم ellipse في Java باستخدام Aspose.PSD، الدليل المتقدم
  لمعالجة الصور في Java الذي يتيح لك إنشاء ellipses، ورسم الأشكال، وإنشاء صور bitmap
  بكفاءة.
og_image_alt: Guide showing how to draw an ellipse in Java with Aspose.PSD
og_title: كيفية رسم ellipse في Java باستخدام مكتبة Aspose.PSD
schemas:
- author: Aspose
  dateModified: '2026-09-28'
  description: Learn how to draw ellipse in Java using Aspose.PSD, the leading Java
    image processing tutorial for creating ellipses and other shapes.
  headline: How to draw ellipse in Java using Aspose.PSD library
  type: TechArticle
- questions:
  - answer: Aspose.PSD offers a fully functional trial that lets you evaluate all
      features before purchasing a license.
    question: Can I use Aspose.PSD for free?
  - answer: Visit [Aspose.PSD Documentation](https://reference.aspose.com/psd/java/)
      for comprehensive guides, API references, and sample projects.
    question: Where can I find more examples and documentation?
  - answer: Temporary licenses are available through the Aspose portal at [Aspose.PSD
      Temporary License](https://purchase.aspose.com/temporary-license/).
    question: How do I obtain a temporary license for testing?
  - answer: It supports BMP, PNG, JPEG, TIFF, GIF, and native PSD among others.
    question: What image formats can Aspose.PSD export to?
  - answer: Yes, the library is designed for high‑throughput server environments and
      includes features such as multi‑threaded processing and memory‑efficient streaming.
    question: Is Aspose.PSD suitable for enterprise‑level workloads?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- draw ellipse
- Aspose.PSD
- Java graphics
- image processing
title: كيفية رسم ellipse في Java باستخدام مكتبة Aspose.PSD
url: /ar/java/java-graphics-drawing/drawing-ellipses/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# كيفية رسم القطع الناقص في Java باستخدام مكتبة Aspose.PSD

## مقدمة
في هذا الدرس ستتعلم **كيفية رسم القطع الناقص** في Java باستخدام مكتبة Aspose.PSD. Aspose.PSD for Java هي API قوية تتيح لك إنشاء وتحرير وتصدير ملفات PSD دون الحاجة إلى Adobe Photoshop. رسم الأشكال مثل القطع الناقصة هو مهارة أساسية لأي مشروع معالجة صور Java، وهذا الدليل يرافقك في كل خطوة — من إعداد المشروع إلى حفظ الصورة النقطية النهائية.

## إجابات سريعة
- **ما هي المكتبة الأفضل لرسم القطع الناقصة في Java؟** Aspose.PSD for Java.
- **كم عدد أسطر الكود المطلوبة؟** حوالي عشر أسطر بالإضافة إلى بعض عبارات الإعداد.
- **هل أحتاج إلى ترخيص للتطوير؟** النسخة التجريبية المجانية تعمل للاختبار؛ يلزم ترخيص تجاري للإنتاج.
- **هل يمكنني تصدير إلى BMP أو PNG أو JPEG؟** نعم، Aspose.PSD يدعم BMP و PNG و JPEG و PSD.
- **هل API متوافق مع Java 8 والإصدارات الأحدث؟** مدعوم بالكامل على Java 8‑21.

## ما هو Aspose.PSD for Java؟
Aspose.PSD for Java هي مكتبة Java صافية تمكّن من إنشاء ومعالجة وتحويل ملفات Photoshop PSD برمجيًا. تدعم أكثر من 100 صيغة صورة ويمكنها التعامل مع ملفات تصل إلى 2 GB دون تحميل المستند بالكامل في الذاكرة.

## لماذا تستخدم Aspose.PSD لرسم القطع الناقص؟
Aspose.PSD تقدم أداءً عاليًا، حيث تعالج المستندات متعددة الصفحات في ثوانٍ، وتدعم أكثر من 100 صيغة إدخال وإخراج مثل BMP و PNG و JPEG و PSD. تعمل بالكامل في Java، مما يلغي الحاجة إلى Photoshop الأصلي ويجعلها مثالية لأنابيب CI/CD والخدمات السحابية.

## المتطلبات المسبقة
- معرفة أساسية ببرمجة Java.
- JDK 8 أو أحدث مثبت.
- بيئة تطوير متكاملة (IDE) مثل IntelliJ IDEA أو Eclipse.
- مكتبة Aspose.PSD for Java. يمكنك تنزيلها من [صفحة تنزيل Aspose.PSD for Java](https://releases.aspose.com/psd/java/).

## استيراد الحزم
أولاً، استورد الفئات التي ستحتاجها من مساحة الاسم Aspose.PSD.

## كيفية رسم القطع الناقص في Java؟
حمّل مكتبة Aspose.PSD، أنشئ لوحة قماشية فارغة من نوع PsdImage، احصل على كائن Graphics، يمكنك اختيارياً مسح الخلفية، ثم استخدم كائنات Pen بالألوان والأنماط المطلوبة لرسم القطع الناقصة داخل حدود Rectangle. أخيرًا، احفظ الصورة بصيغة BMP أو PNG أو JPEG. عادةً ما يتطلب هذا العملية أقل من 15 سطرًا من الكود.

## الخطوة 1: إعداد مشروع Java الخاص بك
قبل البدء بالبرمجة، تأكد من أن مشروعك يتضمن ملف JAR الخاص بـ Aspose.PSD كاعتماد Maven/Gradle أو يضيف الـ JAR إلى مسار الفئات (classpath).

## الخطوة 2: إنشاء مثيل من PsdImage
PsdImage تمثل مستند Photoshop في الذاكرة وتوفر لوحة قماشية للرسم.

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

## الخطوة 3: تهيئة كائن graphics
Graphics توفر طرق رسم لتصوير الأشكال على سطح الصورة.

```java
Image image = new PsdImage(100, 100);
```

## الخطوة 4: مسح سطح graphics
يمكنك اختيارياً مسح اللوحة بلون خلفية لضمان منطقة رسم نظيفة.

```java
Graphics graphics = new Graphics(image);
```

## الخطوة 5: رسم قطع ناقص منقط
Pen يحدد اللون والنمط للحد الخارجي المستخدم عند رسم الأشكال.

```java
graphics.clear(Color.getYellow());
```

## الخطوة 6: رسم قطع ناقص مستمر
Pen مع فرشاة زرقاء صلبة يخلق حدًا مستمرًا للقطع الناقص الثاني.

```java
graphics.drawEllipse(new Pen(Color.getRed()), new Rectangle(30, 10, 40, 80));
```

## الخطوة 7: حفظ الصورة
BmpOptions يحدد إعدادات صيغة BMP لحفظ الصورة.

```java
graphics.drawEllipse(new Pen(new SolidBrush(Color.getBlue())), new Rectangle(10, 30, 80, 40));
```

```java
String outputPath = "Your Document Directory/Ellipse.bmp";
BmpOptions saveOptions = new BmpOptions();
saveOptions.setBitsPerPixel(32);
image.save(outputPath, saveOptions);
```

## المشكلات الشائعة والحلول
- **الصورة تظهر فارغة:** تأكد من أنك استدعيت `graphics.clear()` بلون مرئي قبل الرسم.
- **القطع الناقص يبدو مشوّهًا:** تحقق من أن أبعاد `Rectangle` تتطابق مع نسبة أبعاد الصورة.
- **أخطاء نفاد الذاكرة في الملفات الكبيرة:** استخدم API البث الخاص بـ `PsdImage` لمعالجة أقسام الملف بدلاً من تحميل المستند بالكامل.

## الأسئلة المتكررة

**س: هل يمكنني استخدام Aspose.PSD مجانًا؟**  
ج: Aspose.PSD تقدم نسخة تجريبية كاملة الوظائف تتيح لك تقييم جميع الميزات قبل شراء الترخيص.

**س: أين يمكنني العثور على المزيد من الأمثلة والوثائق؟**  
ج: زر [Aspose.PSD Documentation](https://reference.aspose.com/psd/java/) للحصول على أدلة شاملة، مراجع API، ومشاريع مثال.

**س: كيف أحصل على ترخيص مؤقت للاختبار؟**  
ج: التراخيص المؤقتة متاحة عبر بوابة Aspose على [Aspose.PSD Temporary License](https://purchase.aspose.com/temporary-license/).

**س: ما هي صيغ الصور التي يمكن لـ Aspose.PSD تصديرها؟**  
ج: يدعم BMP و PNG و JPEG و TIFF و GIF و PSD الأصلي وغيرها.

**س: هل Aspose.PSD مناسبة لأعباء العمل على مستوى المؤسسات؟**  
ج: نعم، تم تصميم المكتبة لبيئات الخوادم عالية الإنتاجية وتشمل ميزات مثل المعالجة متعددة الخيوط والبث الفعال للذاكرة.

## الخلاصة
أصبح لديك الآن مثال كامل من البداية إلى النهاية **كيفية رسم القطع الناقص** في Java باستخدام Aspose.PSD. من خلال إعداد `PsdImage`، واستخدام API `Graphics`، وتكوين كائنات `Pen`، يمكنك رسم كل من القطع الناقصة المنقطة والصلبة وحفظ النتيجة بأي من صيغ البت ماب المدعومة. دمج هذه الخطوات في تطبيقاتك الخاصة لتوليد رسومات ديناميكية، صور مصغرة، أو عناصر واجهة مستخدم مخصصة دون الاعتماد على محررات رسومات خارجية.

---

**Last Updated:** 2026-09-28  
**Tested With:** Aspose.PSD for Java 24.12  
**Author:** Aspose

## دروس ذات صلة

- [رسم وحفظ مستطيل في PSD باستخدام Aspose.PSD for Java](/psd/java/basic-image-operations/simple-drawing/)
- [تغيير حجم الصورة باستخدام Aspose.PSD for Java – رسم الأشكال وعمليات الصورة الأساسية](/psd/java/basic-image-operations/)
- [إضافة توقيع إلى الصورة – رسم الصورة على اللوحة باستخدام Aspose.PSD for Java](/psd/java/advanced-image-effects/add-signature-to-image/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}