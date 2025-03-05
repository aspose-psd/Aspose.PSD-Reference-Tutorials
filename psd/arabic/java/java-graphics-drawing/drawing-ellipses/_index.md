---
title: رسم القطع الناقص في جافا
linktitle: رسم القطع الناقص في جافا
second_title: Aspose.PSD جافا API
description: تعرف على كيفية رسم الأشكال البيضاوية في Java باستخدام Aspose.PSD لتصميم رسومي دقيق ومعالجة الصور. إتقان الدروس خطوة بخطوة.
type: docs
weight: 15
url: /ar/java/java-graphics-drawing/drawing-ellipses/
---
## مقدمة
في هذا البرنامج التعليمي، ستتعلم كيفية رسم الأشكال البيضاوية باستخدام Aspose.PSD لـ Java. Aspose.PSD هي مكتبة قوية تسمح لمطوري Java بالعمل مع ملفات PSD ومعالجة الصور بسهولة. يعد رسم الأشكال مثل القطع الناقص مهمة أساسية في معالجة الصور والتصميم الجرافيكي. باتباع هذا الدليل، ستكتسب خبرة عملية في إنشاء علامات الحذف برمجيًا باستخدام Aspose.PSD.
## المتطلبات الأساسية
قبل أن تبدأ، تأكد من أن لديك ما يلي:
- المعرفة الأساسية ببرمجة جافا.
- JDK (Java Development Kit) مثبت على نظامك.
- بيئة التطوير المتكاملة (IDE) مثل IntelliJ IDEA أو Eclipse.
-  Aspose.PSD لمكتبة جافا. يمكنك تنزيله من[هنا](https://releases.aspose.com/psd/java/).
## حزم الاستيراد
أولاً، تحتاج إلى استيراد الحزم الضرورية من Aspose.PSD:
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
## الخطوة 1: قم بإعداد مشروع Java الخاص بك
قبل البدء في البرمجة، تأكد من إعداد مشروع Java الخاص بك بشكل صحيح مع تضمين Aspose.PSD باعتباره تبعية.
## الخطوة 2: إنشاء مثيل لـ PsdImage
قم بتهيئة مثيل جديد لـ PsdImage بالعرض والارتفاع المطلوبين.
```java
Image image = new PsdImage(100, 100);
```
## الخطوة 3: تهيئة كائن الرسومات
قم بإنشاء وتهيئة مثيل للرسومات للعمل مع الصورة.
```java
Graphics graphics = new Graphics(image);
```
## الخطوة 4: قم بمسح سطح الرسومات
قبل الرسم، قم بمسح سطح الرسومات بلون محدد (اختياري).
```java
graphics.clear(Color.getYellow());
```
## الخطوة 5: ارسم شكلًا بيضاويًا منقطًا
استخدم كائن القلم ذو اللون الأحمر وارسم شكلًا ناقصًا منقطًا داخل مستطيل محدد.
```java
graphics.drawEllipse(new Pen(Color.getRed()), new Rectangle(30, 10, 40, 80));
```
## الخطوة 6: ارسم شكلًا ناقصًا مستمرًا
قم بإنشاء كائن القلم باستخدام فرشاة زرقاء صلبة وارسم شكلًا ناقصًا مستمرًا داخل مستطيل آخر.
```java
graphics.drawEllipse(new Pen(new SolidBrush(Color.getBlue())), new Rectangle(10, 30, 80, 40));
```
## الخطوة 7: احفظ الصورة
وأخيرًا، احفظ الصورة التي تم إنشاؤها بتنسيق BMP في المسار المحدد.
```java
String outputPath = "Your Document Directory/Ellipse.bmp";
BmpOptions saveOptions = new BmpOptions();
saveOptions.setBitsPerPixel(32);
image.save(outputPath, saveOptions);
```

## خاتمة
تهانينا! لقد تعلمت بنجاح كيفية رسم علامات الحذف برمجياً باستخدام Aspose.PSD لـ Java. يغطي هذا البرنامج التعليمي إعداد مشروعك، وتهيئة الرسومات، ورسم علامات الحذف المنقطة والمستمرة، وحفظ الصورة الناتجة. يمكنك الآن دمج هذه التقنيات في تطبيقات Java الخاصة بك لمختلف مهام التصميم الجرافيكي ومعالجة الصور.
## الأسئلة الشائعة
### هل يمكنني استخدام Aspose.PSD مجانًا؟
يقدم Aspose.PSD نسخة تجريبية مجانية، مما يسمح لك بتقييم ميزاته قبل الشراء.
### أين يمكنني العثور على المزيد من الأمثلة والوثائق؟
 يزور[وثائق Aspose.PSD](https://reference.aspose.com/psd/java/) للحصول على أدلة وأمثلة شاملة.
### كيف يمكنني الحصول على تراخيص مؤقتة لـ Aspose.PSD؟
 يمكن الحصول على التراخيص المؤقتة من[Aspose.PSD الترخيص المؤقت](https://purchase.aspose.com/temporary-license/).
### ما هي التنسيقات التي يمكن لـ Aspose.PSD حفظ الصور بها؟
يدعم Aspose.PSD حفظ الصور بتنسيقات مختلفة بما في ذلك BMP وPNG وJPEG وPSD.
### هل Aspose.PSD مناسب للاستخدام المؤسسي؟
نعم، تم تصميم Aspose.PSD لمهام معالجة الصور الاحترافية وعلى مستوى المؤسسات.