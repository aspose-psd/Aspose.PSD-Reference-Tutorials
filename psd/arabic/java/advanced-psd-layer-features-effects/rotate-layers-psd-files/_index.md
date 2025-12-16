---
date: 2025-12-15
description: تعلم كيفية تحويل ملفات PSD إلى PNG وتدوير طبقات PSD في Java باستخدام
  Aspose.PSD. دليل خطوة بخطوة مع عينات من الشيفرة.
linktitle: Convert PSD to PNG and Rotate Layers in PSD Files using Java
second_title: Aspose.PSD Java API
title: تحويل PSD إلى PNG وتدوير الطبقات في ملفات PSD باستخدام Java
url: /ar/java/advanced-psd-layer-features-effects/rotate-layers-psd-files/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# تحويل PSD إلى PNG وتدوير الطبقات في ملفات PSD باستخدام Java

## مقدمة
إذا كنت بحاجة إلى **convert PSD to PNG** مع تدوير الطبقات أيضًا، فهذا الدليل لك. سواءً كنت تبني أداة معالجة دفعات أو تدمج تعديل الصور في خدمة ويب، فإن القيام بذلك برمجياً يوفر الوقت ويزيل الاعتماد على Adobe Photoshop. في هذا البرنامج التعليمي سنوضح لك **how to rotate PSD** الطبقات ونصدّر النتيجة كملف PNG باستخدام مكتبة Aspose.PSD للـ Java. هيا نُشرّع أكمامنا ونُحسّن سير عمل التصميم الخاص بك!

## إجابات سريعة
- **ما المكتبة التي يمكنني استخدامها؟** Aspose.PSD for Java  
- **هل يمكنني تدوير وتحويل في خطوة واحدة؟** نعم – قم بتدوير الـ PSD ثم احفظه كـ PNG  
- **هل أحتاج إلى ترخيص؟** النسخة التجريبية المجانية تعمل للاختبار؛ يلزم ترخيص مدفوع للإنتاج  
- **ما نسخة Java المدعومة؟** Java 8 وما بعدها  
- **هل ناتج PNG شفاف؟** نعم، عندما تقوم بتعيين `PngColorType.TruecolorWithAlpha`

## ما هو “convert PSD to PNG”؟
تحويل مستند Photoshop (PSD) إلى صورة PNG يعني استخراج المحتوى البصري — بما في ذلك جميع الطبقات والأقنعة والشفافية — إلى تنسيق نقطي مدعوم على نطاق واسع. يحافظ PNG على قنوات ألفا، مما يجعله مثالياً للرسومات على الويب، والصور المصغرة، ومعالجة الصور الإضافية.

## لماذا نستخدم Aspose.PSD للـ Java لتحويل PSD إلى PNG وتدوير طبقات PSD؟
- **لا حاجة لـ Photoshop** – يعمل على أي خادم أو بيئة CI  
- **دعم كامل للطبقات** – الحفاظ على الشفافية وتأثيرات الطبقة دون تغيير  
- **واجهة برمجة تطبيقات بسيطة** – تدوير، انعكاس، وحفظ ببضع نداءات للطرق فقط  
- **متعدد المنصات** – يعمل على Windows وLinux وmacOS  

## المتطلبات المسبقة
- **Java Development Kit (JDK)** – حمّل من [موقع Oracle](https://www.oracle.com/java/technologies/javase-downloads.html).  
- **بيئة تطوير متكاملة (IDE)** – IntelliJ IDEA أو Eclipse أو NetBeans كلها مناسبة.  
- **مكتبة Aspose.PSD للـ Java** – احصل على أحدث JAR من [صفحة الإصدار](https://releases.aspose.com/psd/java/).  
- **معرفة أساسية بـ Java** – الإلمام بالصفوف (classes)، الكائنات (objects)، ومعالجة الاستثناءات.  

## دليل خطوة بخطوة

### الخطوة 1: إعداد مشروع Java الخاص بك
أنشئ مشروع Java جديد في بيئة التطوير الخاصة بك وأضف ملف JAR الخاص بـ Aspose.PSD إلى مسار بناء المشروع.

### الخطوة 2: استيراد الفئات المطلوبة
Add the following imports at the top of your Java source file:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RotateFlipType;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PngOptions;
```

### الخطوة 3: تحديد مسارات الملفات
Specify where your source PSD lives and where the output files should be written.

```java
String dataDir = "Your Document Directory"; // Change this to your actual document directory.
String sourceFile = dataDir + "1.psd"; // Source PSD file
String pngPath = dataDir + "RotateFlipTest2617.png"; // Output PNG file path
String psdPath = dataDir + "RotateFlipTest2617.psd"; // Output PSD file path
```

> **نصيحة احترافية:** استخدم مسارًا مطلقًا أثناء الاختبار لتجنب أخطاء “file not found”.

### الخطوة 4: تحميل ملف PSD
Load the PSD into a manipulable object.

```java
PsdImage im = (PsdImage) Image.load(sourceFile);
```

الآن `im` يمثل مستند Photoshop بالكامل، بما في ذلك جميع الطبقات.

### الخطوة 5: تدوير الصورة (كيفية تدوير PSD)
Choose a rotation type from `RotateFlipType`. In this example we rotate 270° and flip both axes.

```java
int flipType = RotateFlipType.Rotate270FlipXY; // Choose the rotation type
im.rotateFlip(flipType); // Rotate the image
```

لا تتردد في تجربة قيم أخرى مثل `Rotate90FlipNone` أو `Rotate180FlipX`.

### الخطوة 6: حفظ الصورة المدورة كـ PNG (convert PSD to PNG)
Configure PNG options to keep transparency, then save.

```java
PngOptions options = new PngOptions();
options.setColorType(PngColorType.TruecolorWithAlpha); // Preserve transparency
im.save(pngPath, options); // Save the rotated image
```

يحافظ PNG الناتج على شفافية الطبقة، مما يجعله جاهزًا للاستخدام على الويب.

### الخطوة 7: حفظ ملف PSD المعدل (اختياري)
If you also need a new PSD with the rotation applied, save it back.

```java
im.save(psdPath);
```

الآن لديك كل من معاينة PNG وملف PSD محدث.

## مشكلات شائعة وحلولها
- **الملف غير موجود:** تحقق من أن `dataDir` ينتهي بفاصل مسار (`/` أو `\`).  
- **OutOfMemoryError** عند ملفات PSD الكبيرة: زد حجم الذاكرة المخصصة للـ JVM (`-Xmx2g`).  
- **فقدان الشفافية:** تأكد من تعيين `PngColorType.TruecolorWithAlpha`؛ وإلا سيُحفظ PNG بدون قناة ألفا.

## الأسئلة المتكررة
### هل يمكنني تدوير طبقة محددة في ملف PSD؟
نعم، يمكنك استخدام `Layer.rotateFlip()` على الطبقات الفردية بعد iterating عبر `im.getLayers()`.

### هل هناك أي قيود أداء مع Aspose.PSD للـ Java؟
المكتبة تتعامل مع معظم الملفات بكفاءة، لكن ملفات PSD الضخمة جدًا (>500 MB) قد تحتاج إلى ذاكرة إضافية.

### هل Aspose.PSD مجاني للاستخدام؟
تقدم Aspose نسخة تجريبية مجانية، لكن يلزم ترخيص مدفوع للإنتاج. تحقق من [temporary license](https://purchase.aspose.com/temporary-license/) للاختبار.

### أين يمكنني العثور على وثائق مفصلة؟
يمكنك العثور على وثائق شاملة في [Aspose.PSD Documentation](https://reference.aspose.com/psd/java/).

### ماذا أفعل إذا واجهت مشكلات أثناء استخدام Aspose.PSD؟
اطلب المساعدة عبر [Aspose Support Forum](https://forum.aspose.com/c/psd/34).

## أسئلة متكررة إضافية

**س: هل يحافظ تحويل PSD إلى PNG على تأثيرات الطبقة؟**  
ج: نعم، عند الحفظ باستخدام `PngColorType.TruecolorWithAlpha`، يتم تحويل معظم التأثيرات البصرية إلى PNG.

**س: هل يمكنني معالجة عدة ملفات PSD دفعةً واحدة؟**  
ج: بالتأكيد. ضع الكود داخل حلقة تتنقل عبر مجلد يحتوي على ملفات PSD.

**س: هل يمكن ضبط مستوى ضغط PNG؟**  
ج: توفر فئة `PngOptions` طريقة `setCompressionLevel(int)` لضبط الضغط بدقة.

**س: هل يجب إغلاق كائن الصورة؟**  
ج: `PsdImage` تنفّذ `Closeable`؛ استدعِ `im.close()` داخل كتلة `finally` أو استخدم try‑with‑resources.

**س: هل سيحتفظ PNG المدور بنفس أبعاد الأصل؟**  
ج: تدوير 90° أو 270° يبدّل العرض والارتفاع. سيعكس PNG الاتجاه الجديد.

## الخلاصة
باستخدام Aspose.PSD للـ Java، يمكنك **convert PSD to PNG** و**rotate PSD** الطبقات ببضع أسطر من الشيفرة فقط. يزيل هذا النهج الحاجة إلى Photoshop، يسرّع سير العمل الآلي، ويمنحك تحكمًا كاملاً في مخرجات الصورة. جرّبه في مشاريعك الخاصة وشاهد مقدار الوقت الذي ستوفره!

---

**آخر تحديث:** 2025-12-15  
**تم الاختبار مع:** Aspose.PSD for Java 24.11  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}