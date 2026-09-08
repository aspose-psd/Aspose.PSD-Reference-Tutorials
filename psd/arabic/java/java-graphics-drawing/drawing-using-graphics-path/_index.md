---
date: 2026-09-08
description: تعلم كيفية إنشاء صورة باستخدام فئة Graphics Path في Aspose.PSD بلغة Java.
  يوضح لك هذا الدليل step‑by‑step كيفية إضافة النصوص والأشكال ومسح خلفية الصورة بكفاءة.
keywords:
- how to create image
- add text image java
- clear image background java
lastmod: 2026-09-08
linktitle: كيفية إنشاء صورة باستخدام Graphics Path في Java
og_description: تعلم كيفية إنشاء صورة باستخدام Aspose.PSD في Java. يغطي هذا البرنامج
  التعليمي إضافة النصوص والأشكال ومسح خلفية الصورة باستخدام فئة Graphics Path.
og_image_alt: Screenshot of Java code creating an image with graphics path using Aspose.PSD
og_title: كيفية إنشاء صورة باستخدام Graphics Path في Java مع Aspose.PSD
schemas:
- author: Aspose
  dateModified: '2026-09-08'
  description: Learn how to create image with Aspose.PSD's Graphics Path class in
    Java. This step‑by‑step guide shows you how to add text, shapes, and clear image
    background efficiently.
  headline: How to create image using Graphics Path in Java
  type: TechArticle
- description: Learn how to create image with Aspose.PSD's Graphics Path class in
    Java. This step‑by‑step guide shows you how to add text, shapes, and clear image
    background efficiently.
  name: How to create image using Graphics Path in Java
  steps:
  - name: '**Java Development Kit (JDK)** – a stable JDK 11+ installed. Download it
      from [Oracle’s site](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).'
    text: '**Java Development Kit (JDK)** – a stable JDK 11+ installed. Download it
      from [Oracle’s site](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).'
  - name: '**Aspose.PSD for Java library** – obtain the latest JAR from [here](https://releases.aspose.com/psd/java/)
      and add it to your project’s classpath.'
    text: '**Aspose.PSD for Java library** – obtain the latest JAR from [here](https://releases.aspose.com/psd/java/)
      and add it to your project’s classpath.'
  - name: '**IDE** – any Java IDE such as Eclipse, IntelliJ IDEA, or VS Code.'
    text: '**IDE** – any Java IDE such as Eclipse, IntelliJ IDEA, or VS Code.'
  type: HowTo
- questions:
  - answer: Aspose.PSD is a Java library that enables you to create, edit, and convert
      Photoshop (PSD) files and other raster formats without requiring Photoshop.
    question: What is Aspose.PSD?
  - answer: Yes – the library supports **50+** formats, including PNG, JPEG, BMP,
      TIFF, and GIF.
    question: Can I work with formats other than PSD?
  - answer: Yes, you can access a free trial of Aspose.PSD [here](https://releases.aspose.com/).
    question: Is a trial version available?
  - answer: You can purchase Aspose.PSD from [here](https://purchase.aspose.com/buy).
    question: How do I purchase a license?
  - answer: You can seek support and discussions on [Aspose’s forum](https://forum.aspose.com/c/psd/34).
    question: Where can I get support?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- graphics path
- Aspose.PSD
- Java image processing
title: كيفية إنشاء صورة باستخدام Graphics Path في Java
url: /ar/java/java-graphics-drawing/drawing-using-graphics-path/
weight: 19
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# كيفية إنشاء صورة باستخدام Graphics Path في Java

## مقدمة
في هذا الدرس ستتعلم **كيفية إنشاء صورة** برمجياً باستخدام فئة **Graphics Path** القوية المقدمة من Aspose.PSD for Java. سواء كنت بحاجة إلى رسم أشكال مخصصة، أو تضمين نص، أو مسح خلفية الصورة، فإن الدليل خطوة بخطوة أدناه يوضح لك بالضبط كيفية تحقيق نتائج احترافية في بضع أسطر من الشيفرة فقط.

## إجابات سريعة
- **أي مكتبة تتعامل مع الرسم المعقد؟** فئة Graphics Path الخاصة بـ Aspose.PSD for Java.  
- **هل يمكنني إضافة نص إلى الصورة؟** نعم – استخدم طريقة `GraphicsPath.addString`.  
- **هل يدعم مسح الخلفية؟** بالتأكيد، املأ المسار بفرشاة شفافة.  
- **ما إصدار Java المطلوب؟** JDK 11 أو أحدث.  
- **هل أحتاج إلى ترخيص للإنتاج؟** يلزم ترخيص تجاري؛ يتوفر نسخة تجريبية مجانية.

## ما هي فئة Graphics Path؟
فئة `GraphicsPath` هي الكائن الأساسي في Aspose.PSD لتحديد تعليمات الرسم القائمة على المتجهات. تتيح لك تكوين الأشكال والنصوص والملء في مسار واحد قابل لإعادة الاستخدام يمكن عرضه على أي صورة. من خلال بناء مسار يمكنك تطبيق الأقلام، والفرش، والتحويلات في تمريرة عرض واحدة، مما يحسن الأداء ويحافظ على تنظيم منطق الرسم.

## لماذا نستخدم Graphics Path لإضافة نص إلى صورة Java ومسح خلفية الصورة Java؟
يدعم Aspose.PSD **أكثر من 50 تنسيق صورة** (بما في ذلك PSD، PNG، JPEG، BMP) ويمكنه معالجة ملفات تصل إلى **2 GB** دون تحميل المستند بالكامل في الذاكرة. يتيح لك استخدام Graphics Path دمج الرسم، وضع النص، ومسح الخلفية في عملية واحدة عالية الأداء، مما يقلل استهلاك الذاكرة بنسبة تصل إلى **30 %** مقارنةً بالنهج القائم على الرستر فقط.

## المتطلبات المسبقة
قبل البدء، تأكد من وجود ما يلي:

1. **Java Development Kit (JDK)** – JDK 11+ ثابت مثبت. قم بتنزيله من [Oracle’s site](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).  
2. **Aspose.PSD for Java library** – احصل على أحدث ملف JAR من [here](https://releases.aspose.com/psd/java/) وأضفه إلى مسار الفئات في مشروعك.  
3. **IDE** – أي بيئة تطوير Java مثل Eclipse أو IntelliJ IDEA أو VS Code.

مع توفر هذه المتطلبات، أنت جاهز لبدء إنشاء الصور.

## استيراد الحزم
للعمل مع الرسومات، استورد المساحات الاسمية المطلوبة:

```java
import com.aspose.psd.Color;
import com.aspose.psd.Figure;
import com.aspose.psd.Font;
import com.aspose.psd.Graphics;
import com.aspose.psd.GraphicsPath;
import com.aspose.psd.HatchStyle;
import com.aspose.psd.Pen;
import com.aspose.psd.RectangleF;
import com.aspose.psd.StringFormat;
import com.aspose.psd.brushes.HatchBrush;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.shapes.EllipseShape;
import com.aspose.psd.shapes.RectangleShape;
import com.aspose.psd.shapes.TextShape;
```

تُظهر هذه الاستيرادات فئات الرسم، والفرشاة، والقلم الأساسية المطلوبة لمعالجة الصور.

## كيفية إنشاء صورة باستخدام Graphics Path في Java؟
أنشئ لوحة قماش رستر جديدة، واربط كائن `Graphics`، وحضر سطح الرسم. تُعد هذه الخطوة الوحيدة إعداد لوحة bitmap بحجم **500 × 500 بكسل** جاهزة للعرض المتجهي. تكون اللوحة في البداية شفافة، مما يتيح لك ملؤها لاحقًا بأي لون خلفية أو نمط تختاره، وهو أمر أساسي لسيناريوهات مسح خلفية الصورة.

```java
PsdImage image = new PsdImage(500, 500);
Graphics graphics = new Graphics(image);
graphics.clear(Color.getWhite());
```

## الخطوة 1: تهيئة الصورة والرسومات
هنا نقوم بإنشاء كائن `PsdImage` (500 × 500) ونحصل على سياق `Graphics` الخاص به.  
`PsdImage` يمثل صورة رسترية في الذاكرة يمكن لـ Aspose.PSD تعديلها وحفظها بالعديد من الصيغ.  
`Graphics` يوفر طرق رسم تُظهر الأشكال، والنصوص، والمسارات على `PsdImage`.

## الخطوة 2: إنشاء وتكوين مسار الرسومات
بعد ذلك، نبني `GraphicsPath` يحتوي على دائرة، ومستطيل، وعلامة نصية.  
`GraphicsPath` هو حاوية للأشكال الهندسية؛ يمكنك إضافة أشكال، خطوط، وسلاسل نصية إليه قبل العرض.

```java
GraphicsPath graphicspath = new GraphicsPath();
Figure figure = new Figure();
figure.addShape(new EllipseShape(new RectangleF(0, 0, 499, 499)));
figure.addShape(new RectangleShape(new RectangleF(0, 0, 499, 499)));
figure.addShape(new TextShape("Aspose.PSD", new RectangleF(170, 225, 170, 100), new TextFont("Arial", 20), StringFormat.getGenericTypographic()));
Figure[] fig = { figure };
graphicspath.addFigures(fig);
```

### إضافة نص إلى الصورة (add text image java)
طريقة `addString` في `GraphicsPath` تضع النص المحدد عند الإحداثيات المعطاة باستخدام الخط والفرشاة المزوّدين. هذه هي الطريقة الأكثر موثوقية لتضمين نص واضح وقابل للتكبير داخل مسار المتجه.

## الخطوة 3: رسم وتعبئة المسار
الآن نقوم بعرض المسار باستخدام قلم أزرق وتعبئته بفرشاة مخطط عمودي، وهو ما يوضح أيضًا كيفية **مسح خلفية الصورة java** عن طريق ملء نمط شفاف إذا رغبت. يحدد `Pen` نمط الحد، بينما تُنشئ `HatchBrush` تعبئة بنمط.

```java
graphics.drawPath(new Pen(Color.getBlue()), graphicspath);
HatchBrush hatchbrush = new HatchBrush();
hatchbrush.setBackgroundColor(Color.getBrown());
hatchbrush.setForegroundColor(Color.getBlue());
hatchbrush.setHatchStyle(HatchStyle.Vertical);
graphics.fillPath(hatchbrush, graphicspath);
```

## الخطوة 4: حفظ الصورة
أخيرًا، احفظ الصورة المركبة إلى القرص بتنسيق PNG (أو أي من الصيغ الـ 50+ المدعومة). تحدد طريقة `save` نوع ملف الإخراج بناءً على امتداد الملف الذي تقدمه.

```java
String dataDir = "Your Document Directory";
image.save(dataDir + "DrawingUsingGraphicsPath_output.psd");
```

## المشكلات الشائعة والحلول
- **المسار غير مرئي** – تأكد من أن لون القلم يتباين مع فرشاة التعبئة.  
- **النص يظهر ضبابيًا** – استخدم صورة ذات دقة أعلى أو خط TrueType ب DPI كافٍ.  
- **أخطاء نفاد الذاكرة على ملفات كبيرة** – فعّل `PsdImageOptions.setUseMemoryCache(true)` لتدفق البيانات بدلاً من تحميلها بالكامل.

## الأسئلة المتكررة

**س: ما هو Aspose.PSD؟**  
ج: Aspose.PSD هي مكتبة Java تمكنك من إنشاء وتحرير وتحويل ملفات Photoshop (PSD) وغيرها من صيغ الرستر دون الحاجة إلى Photoshop.

**س: هل يمكنني العمل مع صيغ غير PSD؟**  
ج: نعم – تدعم المكتبة **أكثر من 50** صيغة، بما في ذلك PNG، JPEG، BMP، TIFF، و GIF.

**س: هل تتوفر نسخة تجريبية؟**  
ج: نعم، يمكنك الوصول إلى نسخة تجريبية مجانية من Aspose.PSD [here](https://releases.aspose.com/).

**س: كيف يمكنني شراء ترخيص؟**  
ج: يمكنك شراء Aspose.PSD من [here](https://purchase.aspose.com/buy).

**س: أين يمكنني الحصول على الدعم؟**  
ج: يمكنك طلب الدعم والمناقشات على [Aspose’s forum](https://forum.aspose.com/c/psd/34).

## الخلاصة
باتباع هذا الدليل، أصبحت الآن تعرف **كيفية إنشاء صورة** بملفات تحتوي على أشكال متجهية معقدة، نص مدمج، وخلفيات شفافة باستخدام فئة Graphics Path في Aspose.PSD. جرّب أقلامًا وفرشًا وهندسات مسار مختلفة لبناء رسومات أغنى للألعاب، عناصر واجهة المستخدم، أو إنشاء تقارير تلقائية.

---

**آخر تحديث:** 2026-09-08  
**تم الاختبار مع:** Aspose.PSD for Java 24.11  
**المؤلف:** Aspose

## دروس ذات صلة

- [إنشاء صورة PSD في Java عن طريق تعيين المسار باستخدام Aspose.PSD](/psd/java/image-editing/create-image-by-setting-path/)
- [تغيير حجم الصورة باستخدام Aspose.PSD for Java – رسم الأشكال والعمليات الأساسية على الصورة](/psd/java/basic-image-operations/)
- [إضافة توقيع إلى الصورة – رسم الصورة على لوحة قماش باستخدام Aspose.PSD for Java](/psd/java/advanced-image-effects/add-signature-to-image/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}