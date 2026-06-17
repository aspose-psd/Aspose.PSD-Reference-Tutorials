---
date: 2026-03-04
description: تعلم كيفية إنشاء كائن رسومي في جافا وإضافة علامة مائية مائلة إلى ملفات
  PSD باستخدام Aspose.PSD. يغطي هذا الدليل خطوة بخطوة استخدام مكتبة العلامة المائية
  للصور في جافا.
linktitle: Add Diagonal Watermark to PSD Files with Java
second_title: Aspose.PSD Java API
title: إنشاء كائن رسومي في جافا – علامة مائية مائلة لملف PSD
url: /ar/java/modifying-converting-psd-images/add-diagonal-watermark-psd-files/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# إضافة علامة مائية مائلة إلى ملفات PSD باستخدام Java

## المقدمة
في هذا الدرس ستقوم **create graphics object java** وتستخدمه لإضافة علامة مائية مائلة إلى ملفات PSD. سواء كنت مصممًا تحمي أعمالك الفنية أو مسوّقًا يضع علامة تجارية على الصور، فإن العلامة المائية النظيفة يمكن أن تجعل عملك يبدو احترافيًا وآمنًا. سنستعرض كل خطوة مع شروحات واضحة، حتى تتمكن من تطبيق التقنية بسرعة في مشاريعك الخاصة.

## إجابات سريعة
- **ما المكتبة التي أحتاجها؟** Aspose.PSD for Java (مكتبة علامة مائية للصور java قوية).  
- **أي كلمة مفتاحية أساسية يغطيها هذا الدرس؟** create graphics object java.  
- **هل أحتاج إلى ترخيص؟** نسخة تجريبية مجانية تكفي للاختبار؛ يلزم الحصول على ترخيص تجاري للإنتاج.  
- **هل يمكنني تغيير نص العلامة المائية ونمطها؟** نعم – يمكنك تخصيص الخط، اللون، الشفافية، والدوران.  
- **ما صيغ الإخراج المدعومة؟** المثال يحفظ كـ PNG، لكن Aspose.PSD يمكنه التصدير إلى PSD، JPEG، BMP، وأكثر.

## ما هو كائن Graphics في Java؟
كائن **Graphics** يمثل سطح رسم لصورة. بإنشاء كائن رسومي، تحصل على وصول إلى طرق تتيح لك رسم النصوص، الأشكال، والعناصر البصرية الأخرى مباشرةً على البت ماب أو لوحة PSD. هذا هو المفهوم الأساسي وراء الكلمة المفتاحية **create graphics object java**.

## لماذا تستخدم Aspose.PSD للعلامات المائية؟
Aspose.PSD هي **java image watermark library** مخصصة تعمل دون الحاجة إلى Adobe Photoshop. تمنحك تحكمًا كاملًا في الطبقات، رسم النصوص، وتحويلات الصورة، مما يجعلها مثالية للمعالجة على الخادم أو للعمليات الدفعية.

## المتطلبات المسبقة
قبل الغوص في الكود، تأكد من توفر ما يلي:

### 1. بيئة تطوير Java
قم بتثبيت أحدث JDK من [Java website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).

### 2. مكتبة Aspose.PSD
حمّل المكتبة من [Aspose Downloads page](https://releases.aspose.com/psd/java/). أضف ملف JAR إلى مشروعك عبر Maven أو Gradle أو بإدراجه يدويًا في classpath.

### 3. فهم أساسي لـ Java
الإلمام بالصفوف، الكائنات، وملفات الإدخال/الإخراج سيساعدك على متابعة الشرح بسلاسة.

### 4. إعداد بيئة التطوير المتكاملة (IDE)
استخدم IntelliJ IDEA أو Eclipse أو NetBeans لتجربة برمجة مريحة.

## استيراد الحزم
للتعامل مع ملفات PSD، استورد الفئات المطلوبة من Aspose.PSD:

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

الآن بعد أن رتبنا المتطلبات المستندية واستوردنا الحزم اللازمة، دعنا نستعرض الخطوات لإضافة علامة مائية مائلة إلى ملف PSD.

## الخطوة 1: إعداد الدليل الخاص بك
```java
String dataDir = "Your Document Directory";
```
استبدل `"Your Document Directory"` بمسار المجلد الذي يحتوي على ملف PSD المصدر.

## الخطوة 2: تحميل ملف PSD
```java
PsdImage psdImage = (PsdImage)Image.load(dataDir + "layers.psd");
```
طريقة `Image.load` تقرأ الملف وتحوّله إلى `PsdImage` حتى نتمكن من العمل بالميزات الخاصة بـ PSD.

## الخطوة 3: إنشاء كائن Graphics
```java
Graphics graphics = new Graphics(psdImage);
```
هنا نقوم **create graphics object java** — السطح الذي سنرسم عليه العلامة المائية.

## الخطوة 4: إنشاء خط للعلامة المائية
```java
Font font = new Font("Arial", 20.0f);
```
اختر أي خط مثبت؛ الحجم يتحكم في بروز العلامة المائية.

## الخطوة 5: إنشاء فرشاة للعلامة المائية
```java
SolidBrush brush = new SolidBrush(Color.fromArgb(50, 128, 128, 128));
```
قيمة `alpha` (المعامل الأول) تحدد الشفافية. قيمة ألفا 50 تعطي مظهرًا خفيفًا شبه شفاف.

## الخطوة 6: إعداد مصفوفة التحويل
```java
graphics.setTransform(new Matrix());
graphics.getTransform().rotateAt(45, new PointF(psdImage.getWidth() / 2, psdImage.getHeight() / 2));
```
نقوم بتدوير سطح الرسم 45° حول مركز الصورة، مما يخلق التأثير المائل.

## الخطوة 7: تعريف محاذاة النص
```java
StringFormat sf = new StringFormat();
sf.setAlignment(StringAlignment.Center);
```
المحاذاة المركزية تضمن أن العلامة المائية توضع بشكل جميل في وسط المستطيل المدور.

## الخطوة 8: رسم العلامة المائية
```java
graphics.drawString("Some watermark text", font, brush, new RectangleF(0, psdImage.getHeight() / 2, psdImage.getWidth(), psdImage.getHeight() / 2), sf);
```
استبدل `"Some watermark text"` باسم علامتك التجارية أو إشعار حقوق النشر. المستطيل يحدد مكان رسم النص.

## الخطوة 9: حفظ الصورة
```java
psdImage.save(dataDir + "AddDiagnolWatermark_output.png", new PngOptions());
```
يتم حفظ الناتج كـ PNG، لكن يمكنك اختيار أي صيغة يدعمها Aspose.PSD.

## حالات الاستخدام الشائعة
- **حماية العلامة التجارية:** أضف شعارًا شبه شفاف لمنع إعادة الاستخدام غير المصرح به.  
- **المعالجة الدفعية:** أتمتة وضع العلامات المائية لمكتبات صور كبيرة على الخادم.  
- **معاينات إبداعية:** عرض مسودات مائية للعملاء مع الحفاظ على الملفات الأصلية دون تعديل.

## استكشاف الأخطاء وإصلاحها والنصائح
- **الشفافية غير مرئية؟** زد قيمة ألفا (مثلاً `100`) للحصول على علامة مائية أقوى.  
- **العلامة المائية تظهر غير مركزة؟** تحقق من أن نقطة الدوران تستخدم القسمة الدقيقة لعرض/ارتفاع الصورة.  
- **مخاوف الأداء:** أعد استخدام نفس كائن `Graphics` عند معالجة عدة صور داخل حلقة.

## الأسئلة المتكررة
### ما هو Aspose.PSD؟
Aspose.PSD هي مكتبة Java تُستخدم للعمل مع ملفات PSD ومعالجتها دون الحاجة إلى Adobe Photoshop.

### هل يمكنني استخدام خطوط أخرى للعلامة المائية؟
نعم، يمكنك اختيار أي خط مثبت على نظامك للعلامة المائية.

### هل هناك طريقة لتخصيص شفافية العلامة المائية؟
بالتأكيد! يمكنك تعديل قيمة ألفا في `SolidBrush` لتغيير مستوى الشفافية.

### هل يمكنني إضافة علامات مائية متعددة؟
نعم، يمكنك استدعاء طريقة `drawString` عدة مرات بمعلمات مختلفة لإضافة المزيد من العلامات المائية.

### أين يمكنني العثور على مزيد من المعلومات حول Aspose.PSD؟
يمكنك الاطلاع على الوثائق [here](https://reference.aspose.com/psd/java/).

---

**آخر تحديث:** 2026-03-04  
**تم الاختبار مع:** Aspose.PSD 24.12 for Java  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}