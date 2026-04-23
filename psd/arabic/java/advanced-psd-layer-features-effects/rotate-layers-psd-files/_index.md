---
date: 2026-02-17
description: تعلم كيفية تحويل PSD إلى PNG، والحفاظ على شفافية PNG، وتدوير طبقات PSD
  في Java باستخدام Aspose.PSD. دليل خطوة بخطوة مع أمثلة على الشيفرة.
linktitle: Convert PSD to PNG and Rotate Layers in PSD Files using Java
second_title: Aspose.PSD Java API
title: تحويل PSD إلى PNG وتدوير الطبقات في ملفات PSD باستخدام Java
url: /ar/java/advanced-psd-layer-features-effects/rotate-layers-psd-files/
weight: 21
---

.{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# تحويل PSD إلى PNG وتدوير الطبقات في ملفات PSD باستخدام Java

## مقدمة
إذا كنت بحاجة إلى **تحويل PSD إلى PNG** مع تدوير الطبقات أيضًا، فهذا الدليل لك. سواء كنت تبني أداة معالجة دفعات، أو خدمة ويب تحتاج إلى تعديل الصور في الوقت الفعلي، أو ببساطة تقوم بأتمتة سير عمل التصميم، فإن القيام بذلك برمجياً يوفر الوقت ويزيل الاعتماد على Adobe Photoshop. في هذا البرنامج التعليمي سنستعرض **كيفية تدوير PSD** للطبقات وتصدير النتيجة كملف PNG باستخدام مكتبة Aspose.PSD للغة Java. هيا نبدأ!

## إجابات سريعة
- **ما المكتبة التي يمكنني استخدامها؟** Aspose.PSD for Java  
- **هل يمكنني تدوير وتحويل في خطوة واحدة؟** نعم – قم بتدوير PSD ثم احفظه كـ PNG  
- **هل أحتاج إلى ترخيص؟** النسخة التجريبية المجانية تعمل للاختبار؛ الترخيص المدفوع مطلوب للإنتاج  
- **ما نسخة Java المدعومة؟** Java 8 وما بعدها  
- **هل مخرجات PNG شفافة؟** نعم، عندما تقوم بتعيين `PngColorType.TruecolorWithAlpha`

## ما هو “تحويل PSD إلى PNG”؟
تحويل مستند Photoshop (PSD) إلى صورة PNG يعني استخراج المحتوى البصري — بما في ذلك جميع الطبقات والأقنعة والشفافية — إلى تنسيق نقطي مدعوم على نطاق واسع. يحافظ PNG على قنوات ألفا، مما يجعله مثالياً للرسومات على الويب، والصور المصغرة، ومعالجة الصور الإضافية.

## لماذا نستخدم Aspose.PSD للغة Java لتحويل PSD إلى PNG وتدوير طبقات PSD؟
- **لا حاجة إلى Photoshop** – يعمل على أي خادم أو بيئة CI  
- **دعم كامل للطبقات** – الحفاظ على الشفافية وتأثيرات الطبقة دون تغيير  
- **واجهة برمجة تطبيقات بسيطة** – تدوير، انعكاس، وحفظ ببضع نداءات للطرق فقط  
- **متعدد المنصات** – يعمل على Windows وLinux وmacOS  
- **تحويل الصور في Java** أصبح سهلاً مع مكتبة واحدة  

## المتطلبات المسبقة
قبل الغوص في الكود، تأكد من أن لديك ما يلي:

- **مجموعة تطوير Java (JDK)** – قم بالتنزيل من [موقع Oracle](https://www.oracle.com/java/technologies/javase-downloads.html).  
- **بيئة تطوير متكاملة (IDE)** – IntelliJ IDEA أو Eclipse أو NetBeans كلها مناسبة.  
- **مكتبة Aspose.PSD للغة Java** – احصل على أحدث ملف JAR من [صفحة الإصدار](https://releases.aspose.com/psd/java/).  
- **معرفة أساسية بـ Java** – الإلمام بالصفوف (classes)، الكائنات (objects)، ومعالجة الاستثناءات.  

## دليل خطوة بخطوة

### الخطوة 1: إعداد مشروع Java الخاص بك
أنشئ مشروع Java جديد في بيئة التطوير الخاصة بك وأضف ملف Aspose.PSD JAR إلى مسار بناء المشروع.

### الخطوة 2: استيراد الفئات المطلوبة
أضف الاستيرادات التالية في أعلى ملف المصدر Java الخاص بك:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RotateFlipType;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PngOptions;
```

هذه الفئات تمنحك الوصول إلى تحميل الصور، التدوير، وخيارات PNG الخاصة.

### الخطوة 3: تعريف مسارات الملفات
حدد موقع ملف PSD المصدر ومكان كتابة ملفات الإخراج.

```java
String dataDir = "Your Document Directory"; // Change this to your actual document directory.
String sourceFile = dataDir + "1.psd"; // Source PSD file
String pngPath = dataDir + "RotateFlipTest2617.png"; // Output PNG file path
String psdPath = dataDir + "RotateFlipTest2617.psd"; // Output PSD file path
```

> **نصيحة احترافية:** استخدم مسارًا مطلقًا أثناء الاختبار لتجنب أخطاء “الملف غير موجود”.

### الخطوة 4: تحميل ملف PSD
حمّل ملف PSD إلى كائن يمكن التلاعب به.

```java
PsdImage im = (PsdImage) Image.load(sourceFile);
```

الآن `im` يمثل مستند Photoshop بالكامل، بما في ذلك جميع الطبقات.

### الخطوة 5: تدوير الصورة (كيفية تدوير PSD)
اختر نوع التدوير من `RotateFlipType`. في هذا المثال نقوم بتدوير 270° وعكس كلا المحورين.

```java
int flipType = RotateFlipType.Rotate270FlipXY; // Choose the rotation type
im.rotateFlip(flipType); // Rotate the image
```

لا تتردد في تجربة قيم أخرى مثل `Rotate90FlipNone` أو `Rotate180FlipX`. هذا هو جزء **كيفية تدوير PSD** من البرنامج التعليمي.

### الخطوة 6: حفظ الصورة المدورة كـ PNG (تحويل PSD إلى PNG)
قم بتكوين خيارات PNG للحفاظ على الشفافية، ثم احفظ.

```java
PngOptions options = new PngOptions();
options.setColorType(PngColorType.TruecolorWithAlpha); // Preserve transparency
im.save(pngPath, options); // Save the rotated image
```

يحافظ PNG الناتج على شفافية الطبقة، مما يضمن **preserve PNG transparency** للاستخدام لاحقًا.

### الخطوة 7: حفظ ملف PSD المعدل (اختياري)
إذا كنت بحاجة أيضًا إلى ملف PSD جديد مع تطبيق التدوير، احفظه مرة أخرى.

```java
im.save(psdPath);
```

الآن لديك كل من معاينة PNG وملف PSD محدث.

## المشكلات الشائعة والحلول
- **الملف غير موجود:** تحقق من أن `dataDir` ينتهي بفاصل مسار (`/` أو `\`).  
- **OutOfMemoryError** عند ملفات PSD الكبيرة: زد حجم ذاكرة JVM (`-Xmx2g`).  
- **فقدان الشفافية:** تأكد من تعيين `PngColorType.TruecolorWithAlpha`؛ وإلا سيتم حفظ PNG بدون قناة ألفا.  
- **قلب صورة PSD لا يعمل كما هو متوقع:** تحقق مرة أخرى من الثابت `RotateFlipType` الذي اخترته؛ بعض الثوابت تجمع بين التدوير والقلب في خطوة واحدة.  

## الأسئلة المتكررة

**س: هل يمكنني تدوير طبقة محددة في ملف PSD؟**  
ج: نعم، يمكنك استخدام `Layer.rotateFlip()` على الطبقات الفردية بعد التجول عبر `im.getLayers()`.

**س: هل هناك أي قيود أداء مع Aspose.PSD للغة Java؟**  
ج: المكتبة تتعامل مع معظم الملفات بكفاءة، لكن ملفات PSD الضخمة جدًا (>500 MB) قد تحتاج إلى ذاكرة إضافية.

**س: هل Aspose.PSD مجانية للاستخدام؟**  
ج: تقدم Aspose نسخة تجريبية مجانية، لكن الترخيص المدفوع مطلوب للإنتاج. تحقق من [الرخصة المؤقتة](https://purchase.aspose.com/temporary-license/) للاختبار.

**س: أين يمكنني العثور على وثائق مفصلة؟**  
ج: يمكنك العثور على وثائق شاملة في [توثيق Aspose.PSD](https://reference.aspose.com/psd/java/).

**س: ماذا أفعل إذا واجهت مشكلات أثناء استخدام Aspose.PSD؟**  
ج: اطلب المساعدة عبر [منتدى دعم Aspose](https://forum.aspose.com/c/psd/34).

**س: هل يحافظ تحويل PSD إلى PNG على تأثيرات الطبقة؟**  
ج: نعم، عند الحفظ باستخدام `PngColorType.TruecolorWithAlpha`، يتم تحويل معظم التأثيرات البصرية إلى PNG.

**س: هل يمكنني معالجة عدة ملفات PSD دفعة واحدة؟**  
ج: بالتأكيد. ضع الكود داخل حلقة تتجول في دليل يحتوي على ملفات PSD.

**س: هل يمكن ضبط مستوى ضغط PNG؟**  
ج: توفر فئة `PngOptions` طريقة `setCompressionLevel(int)` لضبط الضغط بدقة.

**س: هل يجب إغلاق كائن الصورة؟**  
ج: `PsdImage` تُنفّذ `Closeable`؛ استدعِ `im.close()` داخل كتلة `finally` أو استخدم try‑with‑resources.

**س: هل سيحتفظ PNG المدور بنفس أبعاد الأصل؟**  
ج: التدوير بزاوية 90° أو 270° يبدل العرض والارتفاع. سيعكس PNG الاتجاه الجديد.

## الخلاصة
باستخدام Aspose.PSD للغة Java، يمكنك **تحويل PSD إلى PNG**، **الحفاظ على شفافية PNG**، و**تدوير طبقات PSD** ببضع أسطر من الكود فقط. هذه الطريقة تلغي الحاجة إلى Photoshop، وتسرّع سير العمل الآلي، وتمنحك تحكمًا كاملاً في مخرجات الصورة. جرّبها في مشاريعك الخاصة وشاهد مقدار الوقت الذي ستوفره!

**آخر تحديث:** 2026-02-17  
**تم الاختبار باستخدام:** Aspose.PSD for Java 24.11  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}