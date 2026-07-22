---
date: 2026-07-22
description: تعلم كيفية حفظ PSD كـ PNG، الحفاظ على شفافية PNG، وتدوير طبقات PSD في
  Java باستخدام Aspose.PSD. دليل خطوة بخطوة، شروحات بدون كتابة كود، ونصائح لحل المشكلات.
keywords:
- save psd as png
- export psd layers png
- convert photoshop file png
- psd to png transparency
lastmod: 2026-07-22
linktitle: حفظ PSD كـ PNG وتدوير الطبقات في Java باستخدام Aspose.PSD
og_description: احفظ PSD كـ PNG باستخدام Aspose.PSD لـ Java. حافظ على الشفافية، دوّر
  الطبقات، وصدر PNG في بضع أسطر من الكود فقط—مثالي لتدفقات العمل الآلية.
og_image_alt: 'Developer guide: save PSD as PNG and rotate layers using Aspose.PSD
  for Java'
og_title: حفظ PSD كـ PNG وتدوير الطبقات في Java باستخدام Aspose.PSD
schemas:
- author: Aspose
  dateModified: '2026-07-22'
  description: Learn how to save psd as png, preserve PNG transparency, and rotate
    PSD layers in Java with Aspose.PSD. Step‑by‑step guide, code‑free explanations,
    and troubleshooting tips.
  headline: save psd as png and rotate layers in Java using Aspose.PSD
  type: TechArticle
- description: Learn how to save psd as png, preserve PNG transparency, and rotate
    PSD layers in Java with Aspose.PSD. Step‑by‑step guide, code‑free explanations,
    and troubleshooting tips.
  name: save psd as png and rotate layers in Java using Aspose.PSD
  steps:
  - name: Set Up Your Java Project
    text: Create a new Java project in your IDE and add the Aspose.PSD JAR to the
      project’s build path.
  - name: Import Required Classes
    text: '`PsdImage` is the core class that represents a Photoshop document in memory.
      `PngOptions` controls PNG‑specific settings, and `RotateFlipType` defines rotation
      and flip operations. These imports give you access to image loading, rotation,
      and PNG‑specific options.'
  - name: Define File Paths
    text: Specify where your source PSD lives and where the output files should be
      written. Using absolute paths during testing avoids “file not found” errors.
      > **Pro tip:** Store paths in a configuration file for easier maintenance in
      larger projects.
  - name: Load the PSD File
    text: '`PsdImage` loads the entire Photoshop document, including all layers, masks,
      and effects, into a manipulable object. Now `im` represents the whole PSD, ready
      for transformations.'
  - name: Rotate the Image (How to rotate PSD)
    text: '`RotateFlipType` enumerates all supported rotations and flips. In this
      example we rotate 270° and flip both axes, which swaps width and height while
      mirroring the image. Feel free to experiment with other values such as `Rotate90FlipNone`
      or `Rotate180FlipX`.'
  - name: Save the Rotated Image as PNG (save PSD as PNG)
    text: Configure `PngOptions` to keep transparency (`PngColorType.TruecolorWithAlpha`)
      and then call `save`. The PNG retains layer transparency, ensuring it works
      seamlessly in web or mobile apps. The resulting PNG preserves alpha channels,
      making it suitable for compositing or further processing.
  - name: Save the Modified PSD (optional)
    text: If you also need a new PSD with the rotation applied, you can save the modified
      `PsdImage` back to disk. You now have both a PNG preview and an updated PSD
      file.
  type: HowTo
- questions:
  - answer: Yes, you can call `layer.rotateFlip(RotateFlipType.Rotate90FlipNone)`
      after iterating through `im.getLayers()`.
    question: Can I rotate a specific layer in a PSD file?
  - answer: The library handles most files efficiently, but extremely large PSDs (>500
      MB) may require additional memory or streaming options.
    question: Is there any performance limitation with Aspose.PSD for Java?
  - answer: Aspose offers a free trial, but a paid license is needed for production.
      See the [temporary license](https://purchase.aspose.com/temporary-license/)
      for testing.
    question: Is Aspose.PSD free to use?
  - answer: Comprehensive docs are available at [Aspose.PSD Documentation](https://reference.aspose.com/psd/java/).
    question: Where can I find detailed documentation?
  - answer: Get help via the [Aspose Support Forum](https://forum.aspose.com/c/psd/34).
    question: What if I encounter issues while using Aspose.PSD?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- convert PSD
- Aspose.PSD
- Java image processing
- rotate PSD layers
title: حفظ PSD كـ PNG وتدوير الطبقات في Java باستخدام Aspose.PSD
url: /ar/java/advanced-psd-layer-features-effects/rotate-layers-psd-files/
weight: 21
---

## الدروس ذات الصلة

- [حفظ PSD كـ PNG وتطبيق ظل الإظهار في Aspose.PSD للـ Java](/psd/java/advanced-image-manipulation/rendering-drop-shadow/)
- [كيفية ضغط ملفات PNG باستخدام Aspose.PSD للـ Java](/psd/java/optimizing-png-files/compress-png-files/)
- [كيفية تدوير الصورة في Java باستخدام Aspose.PSD](/psd/java/advanced-image-manipulation/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< blocks/products/pf/main-wrap-class >}}

# حفظ psd كـ png وتدوير الطبقات في Java باستخدام Aspose.PSD

## مقدمة
إذا كنت بحاجة إلى **حفظ PSD كـ PNG** مع تدوير الطبقات أيضًا، فهذا الدليل لك. سواء كنت تبني أداة معالجة دفعات، أو خدمة ويب تحتاج إلى تعديل الصور في الوقت الفعلي، أو ببساطة تقوم بأتمتة سير عمل التصميم، فإن القيام بذلك برمجياً يوفر الوقت ويزيل الاعتماد على Adobe Photoshop. في هذا البرنامج التعليمي سنستعرض **كيفية تدوير طبقات PSD** وتصدير النتيجة كـ PNG باستخدام مكتبة Aspose.PSD للـ Java. هيا ن roll up our sleeves ونجعل سير عمل التصميم يعمل بسلاسة!

## إجابات سريعة
- **ما المكتبة التي يمكنني استخدامها؟** Aspose.PSD for Java  
- **هل يمكنني تدوير وحفظ PSD كـ PNG في خطوة واحدة؟** نعم – قم بتدوير PSD ثم احفظه كـ PNG  
- **هل أحتاج إلى ترخيص؟** النسخة التجريبية المجانية تعمل للاختبار؛ الترخيص المدفوع مطلوب للإنتاج  
- **ما نسخة Java المدعومة؟** Java 8 وما بعدها  
- **هل ناتج PNG شفاف؟** نعم، عندما تقوم بتعيين `PngColorType.TruecolorWithAlpha`

## ما هو “convert PSD to PNG”؟
تحويل مستند Photoshop (PSD) إلى صورة PNG يستخرج المحتوى المرئي — بما في ذلك الطبقات والأقنعة وقنوات ألفا — إلى تنسيق نقطي مدعوم على نطاق واسع يحافظ على الشفافية. يجعل ذلك PNG مثالياً للرسومات على الويب، والصور المصغرة، ومعالجة الصور اللاحقة. يمكن استخدام PNG الناتج مباشرةً في صفحات الويب، وتطبيقات الهواتف المحمولة، أو معالجته لاحقاً بواسطة مكتبات صور أخرى.

## لماذا تستخدم Aspose.PSD للـ Java لحفظ PSD كـ PNG وتدوير طبقات PSD؟
تمكنك Aspose.PSD من **حفظ PSD كـ PNG** وتدوير الطبقات دون الحاجة لتثبيت Photoshop. تدعم **أكثر من 50 تنسيق إدخال وإخراج**، وتتعامل مع ملفات PSD متعددة المئات من الصفحات باستخدام أقل من 200 ميغابايت من الذاكرة، وتعمل على Windows وLinux وmacOS. يتطلب الـ API فقط بضع استدعاءات للطرق، مما يقدم نتائج عالية الدقة مع معالجة مدمجة لتأثيرات الطبقات، والأقنعة، وقنوات ألفا.

## المتطلبات المسبقة
قبل أن نغوص في الشيفرة، تأكد من أن لديك ما يلي:

- **Java Development Kit (JDK)** – قم بتنزيله من [موقع Oracle](https://www.oracle.com/java/technologies/javase-downloads.html).  
- **Integrated Development Environment (IDE)** – IntelliJ IDEA أو Eclipse أو NetBeans جميعها مناسبة.  
- **Aspose.PSD for Java library** – احصل على أحدث ملف JAR من [صفحة الإصدار](https://releases.aspose.com/psd/java/).  
- **Basic Java knowledge** – الإلمام بالصفوف (classes)، الكائنات (objects)، ومعالجة الاستثناءات.

## دليل خطوة بخطوة

### الخطوة 1: إعداد مشروع Java الخاص بك
أنشئ مشروع Java جديد في بيئة التطوير المتكاملة الخاصة بك وأضف ملف Aspose.PSD JAR إلى مسار بناء المشروع.

### الخطوة 2: استيراد الفئات المطلوبة
`PsdImage` هي الفئة الأساسية التي تمثل مستند Photoshop في الذاكرة. `PngOptions` تتحكم في إعدادات PNG الخاصة، و `RotateFlipType` تحدد عمليات التدوير والقلب.

```java
import com.aspose.psd.Image;
import com.aspose.psd.RotateFlipType;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PngOptions;
```

هذه الاستيرادات تمنحك إمكانية تحميل الصورة، وتدويرها، وإعدادات PNG الخاصة.

### الخطوة 3: تعريف مسارات الملفات
حدد موقع ملف PSD المصدر ومكان كتابة ملفات الإخراج. استخدام المسارات المطلقة أثناء الاختبار يتجنب أخطاء “الملف غير موجود”.

```java
String dataDir = "Your Document Directory"; // Change this to your actual document directory.
String sourceFile = dataDir + "1.psd"; // Source PSD file
String pngPath = dataDir + "RotateFlipTest2617.png"; // Output PNG file path
String psdPath = dataDir + "RotateFlipTest2617.psd"; // Output PSD file path
```

> **نصيحة احترافية:** احفظ المسارات في ملف إعدادات لتسهيل الصيانة في المشاريع الكبيرة.

### الخطوة 4: تحميل ملف PSD
`PsdImage` يقوم بتحميل مستند Photoshop بالكامل، بما في ذلك جميع الطبقات، الأقنعة، والتأثيرات، إلى كائن يمكن التلاعب به.

```java
PsdImage im = (PsdImage) Image.load(sourceFile);
```

الآن `im` يمثل كامل ملف PSD، جاهز للتحويلات.

### الخطوة 5: تدوير الصورة (كيفية تدوير PSD)
`RotateFlipType` يعدد جميع عمليات التدوير والقلب المدعومة. في هذا المثال نقوم بتدوير 270° وقلب كلا المحورين، مما يبدل العرض والارتفاع مع عكس الصورة.

```java
int flipType = RotateFlipType.Rotate270FlipXY; // Choose the rotation type
im.rotateFlip(flipType); // Rotate the image
```

لا تتردد في تجربة قيم أخرى مثل `Rotate90FlipNone` أو `Rotate180FlipX`.

### الخطوة 6: حفظ الصورة المدورة كـ PNG (حفظ PSD كـ PNG)
قم بإعداد `PngOptions` للحفاظ على الشفافية (`PngColorType.TruecolorWithAlpha`) ثم استدعِ `save`. يحتفظ PNG بشفافية الطبقة، مما يضمن عمله بسلاسة في تطبيقات الويب أو الهواتف المحمولة.

```java
PngOptions options = new PngOptions();
options.setColorType(PngColorType.TruecolorWithAlpha); // Preserve transparency
im.save(pngPath, options); // Save the rotated image
```

يحافظ PNG الناتج على قنوات ألفا، مما يجعله مناسبًا للدمج أو المعالجة الإضافية.

### الخطوة 7: حفظ ملف PSD المعدل (اختياري)
إذا كنت بحاجة أيضًا إلى ملف PSD جديد مع تطبيق التدوير، يمكنك حفظ `PsdImage` المعدل مرة أخرى إلى القرص.

```java
im.save(psdPath);
```

الآن لديك كل من معاينة PNG وملف PSD محدث.

## المشكلات الشائعة والحلول
- **File not found:** تحقق من أن `dataDir` ينتهي بفاصل مسار (`/` أو `\`).  
- **OutOfMemoryError on large PSDs:** زد حجم كومة JVM (`-Xmx2g`).  
- **Transparency lost:** تأكد من ضبط `PngColorType.TruecolorWithAlpha`؛ وإلا سيتم حفظ PNG بدون ألفا.  
- **Flip PSD image not behaving as expected:** تحقق مرة أخرى من الثابت `RotateFlipType` الذي اخترته؛ بعض الثوابت تجمع بين التدوير والقلب في خطوة واحدة.

## الأسئلة المتكررة

**Q: هل يمكنني تدوير طبقة محددة في ملف PSD؟**  
A: نعم، يمكنك استدعاء `layer.rotateFlip(RotateFlipType.Rotate90FlipNone)` بعد التكرار عبر `im.getLayers()`.

**Q: هل هناك أي قيود أداء مع Aspose.PSD للـ Java؟**  
A: المكتبة تتعامل مع معظم الملفات بكفاءة، لكن ملفات PSD الضخمة جدًا (>500 ميغابايت) قد تتطلب ذاكرة إضافية أو خيارات البث.

**Q: هل Aspose.PSD مجانية للاستخدام؟**  
A: توفر Aspose نسخة تجريبية مجانية، لكن الترخيص المدفوع مطلوب للإنتاج. راجع [temporary license](https://purchase.aspose.com/temporary-license/) للاختبار.

**Q: أين يمكنني العثور على الوثائق التفصيلية؟**  
A: الوثائق الشاملة متاحة على [Aspose.PSD Documentation](https://reference.aspose.com/psd/java/).

**Q: ماذا أفعل إذا واجهت مشاكل أثناء استخدام Aspose.PSD؟**  
A: احصل على المساعدة عبر [Aspose Support Forum](https://forum.aspose.com/c/psd/34).

**Q: هل يحافظ تحويل PSD إلى PNG على تأثيرات الطبقة؟**  
A: نعم، عند الحفظ باستخدام `PngColorType.TruecolorWithAlpha`، يتم تحويل معظم التأثيرات البصرية إلى PNG.

**Q: هل يمكنني معالجة دفعة من ملفات PSD متعددة؟**  
A: بالطبع. ضع الشيفرة داخل حلقة تتكرر على مجلد يحتوي على ملفات PSD.

**Q: هل يمكن ضبط مستوى ضغط PNG؟**  
A: `PngOptions` توفر طريقة `setCompressionLevel(int)` لضبط حجم الإخراج بدقة.

**Q: هل أحتاج إلى إغلاق كائن الصورة؟**  
A: `PsdImage` تنفذ `Closeable`؛ استخدم try‑with‑resources أو استدعِ `im.close()` داخل كتلة `finally`.

**Q: هل سيكون للـ PNG المدور نفس أبعاد الأصل؟**  
A: التدوير بزاوية 90° أو 270° يبدل العرض والارتفاع، لذا يعكس PNG الاتجاه الجديد تلقائيًا.

## الخلاصة
من خلال الاستفادة من Aspose.PSD للـ Java، يمكنك **حفظ PSD كـ PNG**، **الحفاظ على شفافية PNG**، و**تدوير طبقات PSD** ببضع أسطر من الشيفرة فقط. يلغي هذا النهج الحاجة إلى Photoshop، ويسرّع سير العمل الآلي، ويمنحك التحكم الكامل في مخرجات الصورة. جرّبه في مشاريعك الخاصة وشاهد مقدار الوقت الذي ستوفره!

---

**آخر تحديث:** 2026-07-22  
**تم الاختبار مع:** Aspose.PSD for Java 24.11  
**المؤلف:** Aspose  

{{< blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/products-backtop-button >}}