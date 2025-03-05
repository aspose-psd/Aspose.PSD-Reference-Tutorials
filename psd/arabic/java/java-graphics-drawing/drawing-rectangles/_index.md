---
title: رسم المستطيلات في جافا
linktitle: رسم المستطيلات في جافا
second_title: Aspose.PSD جافا API
description: تعلم كيفية رسم المستطيلات على الصور باستخدام Aspose.PSD لـ Java. يرشد هذا البرنامج التعليمي مطوري Java خطوة بخطوة. مثالية لمهام معالجة الصور.
type: docs
weight: 17
url: /ar/java/java-graphics-drawing/drawing-rectangles/
---
## مقدمة
في عالم تطوير Java، تعد معالجة الصور وإنشاءها برمجيًا متطلبًا شائعًا عبر التطبيقات المختلفة. إحدى هذه المهام التي تتم مواجهتها غالبًا هي رسم أشكال مثل المستطيلات على الصور. يوفر Aspose.PSD for Java مجموعة قوية من الأدوات والوظائف لإنجاز ذلك بكفاءة. سيرشدك هذا البرنامج التعليمي خلال عملية رسم المستطيلات على الصورة باستخدام Aspose.PSD لـ Java، خطوة بخطوة.
## المتطلبات الأساسية
قبل الغوص في البرنامج التعليمي، تأكد من إعداد المتطلبات الأساسية التالية:
### بيئة تطوير جافا
تأكد من تثبيت Java Development Kit (JDK) على نظامك، ويفضل JDK 8 أو أعلى.
### Aspose.PSD لجافا
 يجب أن يكون لديك Aspose.PSD لمكتبة Java. يمكنك تنزيله من[Aspose.PSD لصفحة تنزيل Java](https://releases.aspose.com/psd/java/) واتبع تعليمات التثبيت المتوفرة في وثائقها.
## حزم الاستيراد
للبدء، قم باستيراد حزم Aspose.PSD اللازمة لـ Java إلى ملف Java الخاص بك:
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
ستسمح لك هذه الواردات بالوصول إلى الفئات والأساليب اللازمة لرسم المستطيلات على الصور.
## الخطوة 1: إنشاء صورة جديدة
 أولاً، قم بإنشاء مثيل جديد لـ`PsdImage` فئة ذات عرض وارتفاع محددين.
```java
String dataDir = "path_to_your_data_directory/";
String outpath = dataDir + "Rectangle.bmp";
// قم بإنشاء مثيل BmpOptions وقم بتعيين خصائصه
BmpOptions saveOptions = new BmpOptions();
saveOptions.setBitsPerPixel(32);
// قم بإنشاء مثيل PsdImage بأبعاد محددة
Image image = new PsdImage(100, 100);
```
 في هذه الخطوة،`PsdImage` تتم تهيئته بعرض وارتفاع 100 بكسل لكل منهما.
## الخطوة 2: تهيئة كائن الرسومات
 بعد ذلك، قم بتهيئة أ`Graphics` كائن باستخدام`image` تم إنشاؤها في الخطوة السابقة.
```java
// تهيئة كائن الرسومات
Graphics graphic = new Graphics(image);
```
 هذا`Graphics`سيتم استخدام الكائن لإجراء عمليات الرسم على الصورة.
## الخطوة 3: مسح سطح الرسومات
قم بمسح السطح الرسومي للصورة باستخدام لون محدد.
```java
// سطح رسومات واضح باللون الأصفر
graphic.clear(Color.YELLOW);
```
يؤدي هذا إلى تعيين خلفية الصورة إلى اللون الأصفر.
## الخطوة 4: رسم المستطيلات
الآن، ارسم مستطيلات على الصورة باستخدام ألوان وأبعاد مختلفة.
```java
// ارسم مستطيلاً أحمر
graphic.drawRectangle(new Pen(Color.RED), new Rectangle(30, 10, 40, 80));
// ارسم مستطيلًا أزرقًا
graphic.drawRectangle(new Pen(new SolidBrush(Color.BLUE)), new Rectangle(10, 30, 80, 40));
```
تقوم هذه الأوامر برسم مستطيلات بألوان محددة (أحمر وأزرق) ومواضع على الصورة.
## الخطوة 5: تصدير الصورة
وأخيرا، احفظ الصورة المعدلة بتنسيق ملف BMP.
```java
// تصدير الصورة إلى تنسيق ملف BMP
image.save(outpath, saveOptions);
```
 يؤدي هذا إلى حفظ الصورة ذات المستطيلات المرسومة في ملف BMP المحدد بواسطة`outpath`.

## خاتمة
يعد رسم المستطيلات برمجيًا على الصور في Java باستخدام Aspose.PSD لـ Java أمرًا سهلاً باستخدام الأدوات والمكتبات المناسبة. باتباع هذا البرنامج التعليمي، تعلمت كيفية تهيئة الصورة ومعالجة الكائنات الرسومية ورسم الأشكال وحفظ الصورة المعدلة في ملف. ستؤدي تجربة الأشكال والألوان والأبعاد المختلفة إلى تحسين فهمك لمعالجة الصور في Java.
## الأسئلة الشائعة
### هل يستطيع Aspose.PSD لـ Java التعامل مع الأشكال الأخرى إلى جانب المستطيلات؟
يدعم Aspose.PSD for Java رسم أشكال مختلفة مثل علامات الحذف والخطوط والمضلعات بالإضافة إلى المستطيلات.
### كيف يمكنني تعديل سمك حدود المستطيل؟
 يمكنك ضبط سمك حدود المستطيل عن طريق ضبط`Pen` خاصية سمك.
### هل Aspose.PSD for Java مناسب لمهام معالجة الصور عالية الأداء؟
نعم، تم تصميم Aspose.PSD for Java لمعالجة الصور عالية الأداء مع ميزات شاملة لكل من العمليات البسيطة والمعقدة.
### أين يمكنني العثور على المزيد من الأمثلة والبرامج التعليمية لـ Aspose.PSD لـ Java؟
 يمكنك استكشاف المزيد من الأمثلة والوثائق التفصيلية على[Aspose.PSD لوثائق جافا](https://reference.aspose.com/psd/java/).
### هل يدعم Aspose.PSD for Java تنسيقات الصور الأخرى إلى جانب BMP؟
نعم، يدعم Aspose.PSD for Java مجموعة واسعة من تنسيقات الصور بما في ذلك PNG، وJPEG، وTIFF، وGIF.