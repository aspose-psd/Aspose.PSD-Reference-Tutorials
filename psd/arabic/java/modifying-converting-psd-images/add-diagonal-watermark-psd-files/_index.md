---
title: أضف علامة مائية قطرية إلى ملفات PSD باستخدام Java
linktitle: أضف علامة مائية قطرية إلى ملفات PSD باستخدام Java
second_title: Aspose.PSD جافا API
description: تعرف على كيفية إضافة علامة مائية قطرية بسهولة إلى ملفات PSD باستخدام Java مع Aspose.PSD. دليل خطوة بخطوة لتحسين صورك بثقة.
weight: 12
url: /ar/java/modifying-converting-psd-images/add-diagonal-watermark-psd-files/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# أضف علامة مائية قطرية إلى ملفات PSD باستخدام Java

## مقدمة
في عالمنا الرقمي اليوم، يمكن أن يؤدي الحصول على مظهر مرئي مذهل إلى إحداث فرق كبير. سواء كنت مصممًا يتطلع إلى حماية عملك أو مسوقًا يرغب في إضافة علامة تجارية إلى الصور، فإن تطبيق العلامة المائية أمر ضروري. في هذا البرنامج التعليمي، سنستكشف كيفية إضافة علامة مائية قطرية إلى ملفات PSD باستخدام Java بمساعدة Aspose.PSD، وهي مكتبة قوية لمعالجة ملفات PSD.
## المتطلبات الأساسية
قبل أن ننتقل إلى جزء البرمجة المثير، ستحتاج إلى التأكد من إعداد بعض الأشياء:
### 1. بيئة تطوير جافا
 تأكد من تثبيت Java على جهازك. يمكنك تنزيل أحدث إصدار من[موقع جافا](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).
### 2. مكتبة Aspose.PSD
 للعمل مع ملفات PSD، ستحتاج إلى مكتبة Aspose.PSD. يمكنك تنزيله من[صفحة التنزيلات Aspose](https://releases.aspose.com/psd/java/)اعتمادًا على بنية مشروعك، ربما تستخدم Maven أو أي أداة أخرى لإدارة التبعية، لذا لا تتردد في دمجها وفقًا لاحتياجاتك.
### 3. الفهم الأساسي لجافا
سيساعدك الفهم القوي لـ Java على متابعة هذا البرنامج التعليمي بسلاسة. تأكد من أنك مرتاح للفئات والكائنات والتعامل الأساسي مع الملفات في Java.
### 4. إعداد IDE
استخدم أي بيئة تطوير متكاملة (IDE) مثل IntelliJ IDEA أو Eclipse أو NetBeans للبرمجة. إنه يجعل البرمجة أسهل بكثير، ألا تعتقد ذلك؟
## حزم الاستيراد
لمعالجة ملفات PSD، ستحتاج إلى استيراد حزم معينة من Aspose.PSD. فيما يلي الحزم التي تحتاج إلى تضمينها في الجزء العلوي من ملف Java الخاص بك:
```java
import com.aspose.psd.Color;
import com.aspose.psd.Font;
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;
import com.aspose.psd.Matrix;
import com.aspose.psd.PointF;
import com.aspose.psd.RectangleF;
import com.aspose.psd.StringAlignment;
import com.aspose.psd.StringFormat;
import com.aspose.psd.brushes.SolidBrush;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PngOptions;
```
الآن بعد أن قمنا بفرز متطلباتنا الأساسية واستيراد الحزم الضرورية، فلنستعرض خطوات إضافة علامة مائية قطرية إلى ملف PSD.
## الخطوة 1: إعداد الدليل الخاص بك
```java
String dataDir = "Your Document Directory";
```
أولاً، ستحتاج إلى تحديد الدليل الذي توجد به ملفات PSD الخاصة بك. سيكون هذا الدليل هو نقطة البداية لتحميل الصورة. لذا استبدل`"Your Document Directory"` بالمسار الفعلي الذي يوجد به ملف PSD الخاص بك.
## الخطوة 2: قم بتحميل ملف PSD
```java
PsdImage psdImage = (PsdImage)Image.load(dataDir + "layers.psd");
```
 الآن، سنقوم بتحميل ملف PSD الذي تريد العمل به. ال`Image.load` يقرأ الأسلوب الملف ويلقيه في ملف`PsdImage` هدف. تأكد من تقديم الاسم الدقيق لملف PSD الخاص بك، وهو في هذه الحالة`"layers.psd"`.
## الخطوة 3: إنشاء كائن رسومي
```java
Graphics graphics = new Graphics(psdImage);
```
 في هذه الخطوة نقوم بإنشاء`Graphics` كائن يسمح لنا بإجراء عمليات الرسم على الصورة المحملة. فكر في الأمر كتجهيز لوحة قماشية حيث يمكننا رسم علامتنا المائية.
## الخطوة 4: إنشاء خط للعلامة المائية
```java
Font font = new Font("Arial", 20.0f);
```
هنا، نحدد نمط الخط وحجم نص العلامة المائية لدينا. في هذه الحالة، اخترنا Arial بحجم 20. لا تتردد في اختيار أي خط مثبت على نظامك - أضف بعض الإثارة إلى الأمور!
## الخطوة 5: إنشاء فرشاة للعلامة المائية
```java
SolidBrush brush = new SolidBrush(Color.fromArgb(50, 128, 128, 128));
```
 بعد ذلك، نقوم بإنشاء`SolidBrush` الكائن الذي سوف لون العلامة المائية لدينا. ال`Color.fromArgb`تأخذ الطريقة أربعة معلمات: ألفا، والأحمر، والأخضر، والأزرق. تتحكم قيمة ألفا في الشفافية (0 شفاف بالكامل و255 معتم بالكامل). لقد قمنا بضبطه على 50 للحصول على تأثير شبه شفاف لطيف.
## الخطوة 6: إعداد مصفوفة التحويل
```java
graphics.setTransform(new Matrix());
graphics.getTransform().rotateAt(45, new PointF(psdImage.getWidth() / 2, psdImage.getHeight() / 2));
```
 هذا هو المكان الذي يحدث فيه السحر! نقوم بإنشاء مصفوفة تحويل لتدوير العلامة المائية. ال`rotateAt` تأخذ الدالة معلمتين: الزاوية (45 درجة للحصول على مظهر قطري) والنقطة التي سيتم التدوير حولها (وهي مركز الصورة في حالتنا).
## الخطوة 7: تحديد محاذاة السلسلة
```java
StringFormat sf = new StringFormat();
sf.setAlignment(StringAlignment.Center);
```
 نحن بحاجة للتأكد من أن العلامة المائية لدينا تتمحور. ال`StringFormat` يساعدنا class في ذلك، حيث يقوم بمحاذاة النص بشكل مثالي في وسط الصورة. ففي النهاية، من يحب المواضع الفوضوية؟
## الخطوة 8: ارسم العلامة المائية
```java
graphics.drawString("Some watermark text", font, brush, new RectangleF(0, psdImage.getHeight() / 2, psdImage.getWidth(), psdImage.getHeight() / 2), sf);
```
 الآن، حان الوقت لرسم العلامة المائية فعليًا! باستخدام`drawString`الطريقة، نحدد محتوى العلامة المائية الخاصة بنا (لا تتردد في تخصيص النص)، والخط، والفرشاة، والمنطقة التي نريد رسمها فيها، وإعدادات المحاذاة. سيتم تطبيق العلامة المائية الخاصة بك باستخدام المعلمات التي وضعناها في المستطيل!
## الخطوة 9: احفظ الصورة
```java
psdImage.save(dataDir + "AddDiagnolWatermark_output.png", new PngOptions());
```
 وأخيرا، نقوم بحفظ الصورة المعدلة لدينا. وهنا نقوم بتصديره كملف PNG. تأكد من إعطاء ملف الإخراج الخاص بك اسمًا فريدًا حتى لا يحل محل أي ملفات موجودة. ال`PngOptions` يساعد الفصل على تحديد تنسيق الصورة.
## خاتمة
وبهذه الطريقة، تكون قد نجحت في إضافة علامة مائية قطرية إلى ملف PSD الخاص بك باستخدام Java! إنها عملية واضحة ومباشرة، ولكنها يمكن أن ترفع مستوى احترافية صورك بشكل كبير. سواء كنت تحمي عملك الفني أو تروج لعلامتك التجارية، فإن العلامة المائية هي حل بسيط ولكنه فعال.

## الأسئلة الشائعة
### ما هو Aspose.PSD؟
Aspose.PSD هي مكتبة Java تُستخدم للعمل مع ملفات PSD ومعالجتها دون الحاجة إلى Adobe Photoshop.
### هل يمكنني استخدام خطوط أخرى للعلامة المائية؟
نعم، يمكنك اختيار أي خط مثبت على نظامك لوضع العلامة المائية.
### هل هناك طريقة لتخصيص شفافية العلامة المائية؟
قطعاً! يمكنك ضبط قيمة ألفا في SolidBrush لتغيير الشفافية.
### هل يمكنني إضافة علامات مائية متعددة؟
 نعم يمكنك الاتصال بالرقم`drawString` الطريقة عدة مرات مع معلمات مختلفة لإضافة المزيد من العلامات المائية.
### أين يمكنني العثور على مزيد من المعلومات حول Aspose.PSD؟
 يمكنك التحقق من الوثائق[هنا](https://reference.aspose.com/psd/java/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
