---
date: 2026-09-08
description: تعلم كيفية java graphics draw line في ملفات PSD باستخدام Aspose.PSD for
  Java. يوضح هذا الدليل كيفية draw lines java بخطوات واضحة وأمثلة على الشيفرة.
keywords:
- java graphics draw line
- draw lines java
- how to draw lines java
lastmod: 2026-09-08
linktitle: رسم الخطوط في Java
og_description: اكتشف كيفية java graphics draw line في Java باستخدام Aspose.PSD. اتبع
  تعليمات خطوة بخطوة لرسم خطوط java في ملفات PSD بسرعة.
og_image_alt: Screenshot of Java code drawing lines in a PSD file using Aspose.PSD
og_title: كيفية java graphics draw line في Java مع Aspose.PSD
schemas:
- author: Aspose
  dateModified: '2026-09-08'
  description: Learn how to java graphics draw line in PSD files using Aspose.PSD
    for Java. This guide shows draw lines java with clear steps and code examples.
  headline: How to java graphics draw line in Java
  type: TechArticle
- questions:
  - answer: Aspose.PSD for Java.
    question: What library is required?
  - answer: java graphics draw line.
    question: Which primary keyword does this tutorial target?
  - answer: Yes – a free trial license is available.
    question: Do I need a license to try it?
  - answer: The library works on Windows, Linux, and macOS.
    question: Can I run this on any OS?
  - answer: About 10‑15 minutes for a basic line drawing.
    question: How long does the implementation take?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- java graphics
- Aspose.PSD
- PSD line drawing
- Java image processing
title: كيفية رسم خط باستخدام رسومات Java في Java
url: /ar/java/java-graphics-drawing/drawing-lines/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# رسم خطوط في جافا

## المقدمة
في هذا الدرس ستتعلم كيفية **java graphics draw line** في ملفات PSD باستخدام Aspose.PSD for Java. يسمح لك رسم الخطوط برمجياً بأتمتة إنشاء الرسومات، إضافة تعليقات توضيحية، أو إنشاء أصول تصميم دون فتح Photoshop. في نهاية الدليل ستكون قادرًا على رسم خطوط منقطة ومستقيمة باستخدام بضع أسطر من كود جافا.

## إجابات سريعة
- **ما المكتبة المطلوبة؟** Aspose.PSD for Java.  
- **ما الكلمة المفتاحية الأساسية التي يستهدفها هذا الدرس؟** java graphics draw line.  
- **هل أحتاج إلى ترخيص لتجربتها؟** نعم – ترخيص تجريبي مجاني متاح.  
- **هل يمكن تشغيلها على أي نظام تشغيل؟** المكتبة تعمل على Windows وLinux وmacOS.  
- **كم من الوقت تستغرق عملية التنفيذ؟** حوالي 10‑15 دقيقة لرسم خط أساسي.

## ما هو java graphics draw line؟
المصطلح `java graphics draw line` يصف عملية استخدام واجهات برمجة رسومات مبنية على جافا لتصوير أشكال الخط المستقيم على لوحة صورة. في هذا الدرس توفر مكتبة Aspose.PSD الفئة `Graphics`، التي تقدم طريقة `drawLine` التي تستقبل `Pen` وقيم إحداثية لإنتاج الخط.

## لماذا نستخدم Aspose.PSD لرسم الخطوط؟
توفر Aspose.PSD محركًا قويًا وفعالًا في الذاكرة لمعالجة ملفات Photoshop مباشرةً من كود جافا. تدعم أكثر من 70 تنسيقًا للصور والوثائق، ويمكنها التعامل مع ملفات PSD تصل إلى 2 GB دون تحميلها بالكامل، وتقدم عمليات رسم عالية الأداء، مما يجعلها مثالية للمعالجة الدفعية وتوليد الرسومات تلقائيًا.

## المتطلبات المسبقة
- معرفة أساسية بلغة برمجة جافا.  
- وجود JDK (Java Development Kit) مثبت على نظامك.  
- مكتبة Aspose.PSD for Java تم تنزيلها وإعدادها في بيئة التطوير الخاصة بك.

## استيراد الحزم
الاستيرادات التالية تجلب الفئات المطلوبة من Aspose.PSD لإنشاء الصور، ومعالجة الرسومات، وإدارة الألوان.
```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import static com.aspose.psd.GraphicsUnit.Point;
import com.aspose.psd.Image;
import com.aspose.psd.Pen;
import com.aspose.psd.Point;
import com.aspose.psd.brushes.SolidBrush;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.BmpOptions;
```

## الخطوة 1: إعداد مشروعك
ابدأ بإنشاء مشروع جافا جديد في بيئة التطوير المتكاملة (IDE) وإضافة Aspose.PSD for Java إلى تبعياتك. يمكنك تنزيل المكتبة من [Aspose.PSD for Java Download](https://releases.aspose.com/psd/java/).

## الخطوة 2: تهيئة صورة PSD
الفئة `PsdImage` تمثل مستند Photoshop وتتيح لك إنشاء لوحة PSD فارغة جديدة بالأبعاد المحددة.
```java
String dataDir = "Your Document Directory";
String outpath = dataDir + "Lines.psd";
Image image = new PsdImage(100, 100);
```

## الخطوة 3: تهيئة كائن الرسومات
`Graphics` هي الفئة الأساسية في Aspose.PSD لرسم الأشكال والنصوص والخطوط على لوحة PSD.  
أنشئ نسخة من فئة Graphics وامسح سطح الرسومات:
```java
Graphics graphic = new Graphics(image);
graphic.clear(Color.getYellow());
```

## كيف نرسم خطًا باستخدام java graphics draw line في جافا؟
حمّل أو أنشئ لوحة PSD، احصل على كائن `Graphics` الخاص بها، واستدعِ طريقة `drawLine` مع `Pen` مُكوَّن. هذه الطريقة ذات الاستدعاء الواحد ترسم خطًا مستقيمًا فورًا، مع معالجة مضادة للتعرج ومزج الألوان تلقائيًا. يمكنك تكرار الاستدعاء بإحداثيات مختلفة لإنشاء خطوط متعددة.

## الخطوة 4: رسم خطوط منقطة مائلة
كائن `Pen` يحدد لون الخط وعرضه ونمطه المتقطع، ويتم تمريره إلى طريقة `drawLine` لرسم الخط.
```java
graphic.drawLine(new Pen(Color.getBlue()), 9, 9, 90, 90);
graphic.drawLine(new Pen(Color.getBlue()), 9, 90, 90, 9);
```

## الخطوة 5: رسم خطوط مستمرة
`SolidBrush` يوفر لون تعبئة صلبة للقلم، مما يتيح لك تعيين لون الخط بسهولة.
```java
graphic.drawLine(new Pen(new SolidBrush(Color.getRed())), new Point(9, 9), new Point(9, 90));
graphic.drawLine(new Pen(new SolidBrush(Color.getAqua())), new Point(9, 90), new Point(90, 90));
graphic.drawLine(new Pen(new SolidBrush(Color.getBlack())), new Point(90, 90), new Point(90, 9));
graphic.drawLine(new Pen(new SolidBrush(Color.getWhite())), new Point(90, 9), new Point(9, 9));
```

## الخطوة 6: حفظ الصورة
استدعاء طريقة `save` على كائن `Image` يكتب ملف PSD المعدل إلى المسار المحدد على القرص.
```java
image.save(outpath);
```

## الخلاصة
باتباع هذه الخطوات، قمت برسم خطوط بنجاح داخل ملف PSD باستخدام Aspose.PSD for Java. يغطي هذا الدرس تهيئة صورة PSD، إعداد الرسومات، رسم أنواع مختلفة من الخطوط، وحفظ الصورة الناتجة. لديك الآن أساس قوي لأتمتة إنشاء الرسومات في جافا.

## الأسئلة المتكررة
### ما هو Aspose.PSD for Java؟
Aspose.PSD for Java هي مكتبة جافا قوية للعمل مع ملفات PSD برمجيًا.

### أين يمكنني العثور على الوثائق الخاصة بـ Aspose.PSD for Java؟
يمكنك العثور على الوثائق في صفحة مرجع API لجافا الخاصة بـ Aspose.PSD [Aspose.PSD Java API reference](https://reference.aspose.com/psd/java/).

### هل يمكنني تجربة Aspose.PSD for Java قبل الشراء؟
نعم، يمكنك الحصول على تجربة مجانية من صفحة إصدارات Aspose [Aspose releases page](https://releases.aspose.com/).

### كيف أحصل على الدعم الفني لـ Aspose.PSD for Java؟
للحصول على الدعم الفني، زر [Aspose.PSD forum](https://forum.aspose.com/c/psd/34).

### أين يمكنني الحصول على ترخيص مؤقت لـ Aspose.PSD for Java؟
يمكنك الحصول على ترخيص مؤقت عبر بوابة شراء Aspose [Aspose temporary license page](https://purchase.aspose.com/temporary-license/).

---

**Last Updated:** 2026-09-08  
**Tested With:** Aspose.PSD for Java 24.12  
**Author:** Aspose

## الدروس ذات الصلة

- [تغيير حجم الصورة باستخدام Aspose.PSD for Java – رسم الأشكال والعمليات الأساسية على الصورة](/psd/java/basic-image-operations/)
- [رسم وحفظ مستطيل في PSD باستخدام Aspose.PSD for Java](/psd/java/basic-image-operations/simple-drawing/)
- [إضافة توقيع إلى الصورة – رسم الصورة على لوحة باستخدام Aspose.PSD for Java](/psd/java/advanced-image-effects/add-signature-to-image/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}