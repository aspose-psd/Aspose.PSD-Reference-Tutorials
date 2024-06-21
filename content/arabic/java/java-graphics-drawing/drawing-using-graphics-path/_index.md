---
title: الرسم باستخدام مسار الرسومات في جافا
linktitle: الرسم باستخدام مسار الرسومات في جافا
second_title: Aspose.PSD جافا API
description: تعرف على كيفية إنشاء رسومات معقدة في Java باستخدام فئة مسار الرسومات الخاصة بـ Aspose.PSD. يرشدك هذا البرنامج التعليمي خلال كل خطوة لإنشاء صور مذهلة.
type: docs
weight: 19
url: /ar/java/java-graphics-drawing/drawing-using-graphics-path/
---
## مقدمة
يمكن أن يكون إنشاء الصور ومعالجتها برمجيًا مهمة مثيرة لمطوري Java، خاصة عند استخدام مكتبات مثل Aspose.PSD. في هذا البرنامج التعليمي، سوف نتعمق في عملية رسم الرسومات المعقدة باستخدام فئة Graphics Path في Java باستخدام Aspose.PSD.
## المتطلبات الأساسية
قبل أن ننتقل إلى الجزء الخاص بالبرمجة، تأكد من أن لديك المتطلبات الأساسية التالية:
1.  Java Development Kit (JDK): إصدار ثابت من JDK مثبت على جهازك. يمكنك تنزيله من[موقع أوراكل](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).
2.  Aspose.PSD لمكتبة Java: قم بتنزيل Aspose.PSD لمكتبة Java من[هنا](https://releases.aspose.com/psd/java/). بعد التنزيل، أضف ملف JAR إلى مسار الفصل الخاص بمشروعك.
3. بيئة التطوير المتكاملة (IDE): سواء كان Eclipse أو IntelliJ IDEA أو أي برنامج آخر، فأنت بحاجة إلى IDE لكتابة تعليمات Java البرمجية وتشغيلها.
مع توفر هذه المتطلبات الأساسية، دعنا نستكشف كيفية إنشاء صور جذابة بصريًا باستخدام فئة مسار الرسومات.
## حزم الاستيراد
للبدء، تحتاج إلى استيراد الحزم الضرورية:
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
import com.aspose.psd.examples.Utils.Utils;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.shapes.EllipseShape;
import com.aspose.psd.shapes.RectangleShape;
import com.aspose.psd.shapes.TextShape;
```
توفر هذه الواردات إمكانية الوصول إلى الوظائف الأساسية اللازمة لإنشاء الصور ومعالجتها باستخدام Aspose.PSD.
## الخطوة 1: تهيئة الصورة والرسومات
للبدء، لنقم بإعداد صورة جديدة وتهيئة كائن رسومي:
```java
PsdImage image = new PsdImage(500, 500);
Graphics graphics = new Graphics(image);
graphics.clear(Color.getWhite());
```
هنا، نقوم بإنشاء صورة بحجم 500 × 500 بكسل وكائن رسومي للرسم.
## الخطوة 2: إنشاء مسار الرسومات وتكوينه
 بعد ذلك، نقوم بإنشاء`GraphicsPath` كائن لتحديد مسار الرسم:
```java
GraphicsPath graphicspath = new GraphicsPath();
Figure figure = new Figure();
figure.addShape(new EllipseShape(new RectangleF(0, 0, 499, 499)));
figure.addShape(new RectangleShape(new RectangleF(0, 0, 499, 499)));
figure.addShape(new TextShape("Aspose.PSD", new RectangleF(170, 225, 170, 100), new TextFont("Arial", 20), StringFormat.getGenericTypographic()));
Figure[] fig = { figure };
graphicspath.addFigures(fig);
```
في هذه الخطوة، نقوم بإضافة دائرة ومستطيل وتسمية نصية إلى الشكل الخاص بنا ثم نضيف هذا الشكل إلى مسار الرسومات لدينا.
## الخطوة 3: ارسم المسار واملأه
الآن بعد أن حددنا المسار، يمكننا رسمه وتعبئته:
```java
graphics.drawPath(new Pen(Color.getBlue()), graphicspath);
HatchBrush hatchbrush = new HatchBrush();
hatchbrush.setBackgroundColor(Color.getBrown());
hatchbrush.setForegroundColor(Color.getBlue());
hatchbrush.setHatchStyle(HatchStyle.Vertical);
graphics.fillPath(hatchbrush, graphicspath);
```
في هذه الخطوة، نرسم المسار باستخدام قلم أزرق ونملأه بنمط التظليل الرأسي باستخدام فرشاة التظليل.
## الخطوة 4: احفظ الصورة
وأخيرا، احفظ الصورة في ملف:
```java
String dataDir = "Your Document Directory";
image.save(dataDir + "DrawingUsingGraphicsPath_output.psd");
```
مع هذه الخطوة الأخيرة، اكتمل إنشاء الصورة باستخدام مسار الرسومات.
## خاتمة
يعد إنشاء صور معقدة باستخدام فئة Graphics Path باستخدام Aspose.PSD أمرًا قويًا وجذابًا. باتباع هذا الدليل، يمكنك توسيع إمكانيات تطبيق Java الخاص بك في التصميم الرسومي.
## الأسئلة الشائعة
### ما هو Aspose.PSD؟
Aspose.PSD هي مكتبة تتيح للمطورين العمل مع ملفات Photoshop ومعالجة طبقات الصور برمجيًا.
### هل يمكنني استخدام Aspose.PSD لتنسيقات أخرى غير PSD؟
اعتبارًا من هذا الدليل، يتعامل Aspose.PSD بشكل خاص مع ملفات PSD ولكنه يقدم امتدادات للتعامل مع تنسيقات الصور المختلفة.
### هل يتوفر إصدار تجريبي لـ Aspose.PSD؟
 نعم، يمكنك الوصول إلى النسخة التجريبية المجانية من Aspose.PSD.[هنا](https://releases.aspose.com/).
### كيف يمكنني شراء Aspose.PSD؟
 يمكنك شراء Aspose.PSD من[هنا](https://purchase.aspose.com/buy).
### أين يمكنني الحصول على الدعم لـ Aspose.PSD؟
يمكنك طلب الدعم والمناقشات حول[منتدى Aspose](https://forum.aspose.com/c/psd/34).