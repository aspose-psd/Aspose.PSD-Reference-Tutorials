---
date: 2026-09-03
description: تعلم كيفية تحويل PSD إلى BMP في Java باستخدام Aspose.PSD، واكتشف ميزات
  الرسم الأساسية مثل تطبيق gradients وإنشاء rectangles.
keywords:
- convert PSD to BMP
- how to draw PSD
- apply gradient PSD
- create rectangle PSD
lastmod: 2026-09-03
linktitle: كيفية تحويل PSD إلى BMP والرسم باستخدام Java
og_description: تحويل PSD إلى BMP في Java باستخدام Aspose.PSD. يوضح هذا الدليل خطوة
  بخطوة كيفية تحميل ملفات PSD، تعديل البكسلات، تطبيق gradients، إنشاء rectangles،
  وحفظها كـ BMP بكفاءة.
og_image_alt: 'Tutorial: converting PSD to BMP and drawing shapes in Java using Aspose.PSD'
og_title: تحويل PSD إلى BMP في Java – دليل الرسم الأساسي
schemas:
- author: Aspose
  dateModified: '2026-09-03'
  description: Learn how to convert PSD to BMP in Java using Aspose.PSD, and discover
    core drawing features like applying gradients and creating rectangles.
  headline: How to convert PSD to BMP and draw with Java
  type: TechArticle
- questions:
  - answer: Yes, the library fully supports layered PSD files, including transparency,
      blending modes, and layer effects.
    question: Can Aspose.PSD for Java handle layers and transparency in PSD files?
  - answer: Absolutely. You can automate batch jobs by iterating over a folder, loading
      each PSD, applying the same drawing logic, and saving as BMP or any other supported
      format.
    question: Is Aspose.PSD for Java suitable for batch processing of PSD files?
  - answer: Besides PSD, the API handles BMP, PNG, JPEG, TIFF, GIF, and over 20 additional
      raster formats for both input and output.
    question: Does Aspose.PSD for Java support multiple image formats other than PSD?
  - answer: Visit the [Aspose.PSD temporary license](https://purchase.aspose.com/temporary-license/)
      page for obtaining a temporary license.
    question: How can I obtain a temporary license for Aspose.PSD for Java?
  - answer: Explore the [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) for
      community support, tips, and additional resources.
    question: Where can I find more help and resources for Aspose.PSD for Java?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- convert PSD
- Aspose.PSD
- Java image processing
title: كيفية تحويل PSD إلى BMP والرسم باستخدام Java
url: /ar/java/java-graphics-drawing/core-drawing-features/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# كيفية تحويل PSD إلى BMP والرسم باستخدام Java

## مقدمة
Aspose.PSD for Java هي مكتبة جافا تتيح إنشاء وتحرير وتحويل ملفات Adobe Photoshop PSD برمجيًا. في هذا البرنامج التعليمي ستتعلم كيفية **تحويل PSD إلى BMP** واستكشاف ميزات الرسم الأساسية التي تتيح لك **رسم طبقات PSD، وتطبيق التدرجات، وإنشاء المستطيلات** مباشرةً من كود Java. إتقان هذه القدرات يتيح لك أتمتة خطوط معالجة الصور المعقدة دون الحاجة إلى تثبيت Photoshop.

## إجابات سريعة
- **هل يمكنني تحويل PSD إلى BMP بسطر واحد من الكود؟** نعم – قم بتحميل PSD باستخدام `PsdImage` واستدعِ `save("output.bmp", SaveFormat.Bmp)`.  
- **ما هو إصدار Aspose.PSD المطلوب؟** أحدث إصدار 24.x يدعم جميع واجهات برمجة التطبيقات للرسم الأساسية.  
- **هل أحتاج إلى ترخيص للتطوير؟** ترخيص مؤقت مجاني يعمل للاختبار؛ الترخيص الكامل مطلوب للإنتاج.  
- **ما إصدارات Java المدعومة؟** Java 8 حتى Java 21 متوافقة بالكامل.  
- **هل يمكنني معالجة دفعة من ملفات PSD؟** بالتأكيد – كرر عبر دليل وأعد استخدام نفس منطق التحويل.

## كيفية تحويل PSD إلى BMP في Java؟
حمّل ملف PSD المصدر، واختياريًا عدّل بكسلاته أو طبقات الرسم، ثم احفظه كملف BMP. يحدث التحويل في الذاكرة، لذا تتجنب الملفات الوسيطة ويمكنك معالجة آلاف الصور بكفاءة. تقوم Aspose.PSD ببث البيانات، مما يعني أن حتى الملفات التي تحتوي على مئات الصفحات تُعالج دون استنزاف مساحة الذاكرة.

### ما هي ميزات الرسم الأساسية في Aspose.PSD for Java؟
توفر المكتبة مجموعة كاملة من البدائل الرسومية التي تتيح لك **رسم أشكال PSD**، **تطبيق تعبئة بالتدرج**، و**إنشاء طبقات مستطيلة** برمجيًا. تعمل هذه الواجهات على نفس محرك البكسل الذي يستخدمه Photoshop، مما يضمن دقة بصرية عبر الصيغ.

## المتطلبات المسبقة
قبل البدء، تأكد من جاهزية ما يلي:

### بيئة تطوير Java
قم بتثبيت مجموعة تطوير جافا (JDK) من [موقع Oracle](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html). تم اختبار البرنامج التعليمي باستخدام JDK 11، لكن أي JDK 8+ سيعمل.

### تثبيت Aspose.PSD for Java
1. **قم بتنزيل Aspose.PSD for Java** – انتقل إلى [صفحة التنزيل](https://releases.aspose.com/psd/java/) وحمّل أحدث أرشيف ZIP.  
2. **أضف ملفات JAR إلى مشروعك** – انسخ `aspose-psd.jar` واعتماداته إلى مسار الفئة (classpath)، أو أشر إليها عبر Maven/Gradle كما هو موضح في وثائق المنتج.

الآن لديك كل ما تحتاجه للبدء في كتابة الكود.

## استيراد الحزم
للعمل مع Aspose.PSD يجب استيراد المساحات الاسمية الأساسية. هذه الاستيرادات تمنحك الوصول إلى تحميل الصور، ومعالجة البكسلات، وأدوات الرسم.  
```java
import com.aspose.psd.Rectangle;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.BmpOptions;
```

## الخطوة 1: تحميل صورة PSD
الخطوة الأولى هي إنشاء مثال `PsdImage` يمثل ملف المصدر في الذاكرة. هذا الكائن يمنحك إمكانية القراءة/الكتابة للطبقات والقنوات والبكسلات الفردية.  
```java
String dataDir = "Your Document Directory";
String loadpath = dataDir + "sample.psd";
// Load the PSD image
PsdImage image = new PsdImage(loadpath);
```

## الخطوة 2: تعديل البكسلات
بعد تحميل PSD يمكنك تغيير بيانات البكسل، رسم أشكال جديدة، أو تطبيق تعبئة بالتدرج. واجهة برمجة الرسم تعكس أدوات Photoshop نفسها، مما يتيح لك **رسم مستطيلات PSD** أو **تطبيق تأثيرات تدرج PSD** ببضع استدعاءات للطرق فقط.  
```java
// Load pixels of a specific region (e.g., a 100x10 rectangle starting from top-left corner)
int[] pixels = image.loadArgb32Pixels(new Rectangle(0, 0, 100, 10));
// Modify the pixels (e.g., apply a gradient effect)
for (int i = 0; i < pixels.length; i++) {
    pixels[i] = i;  // Apply your desired manipulation logic here
}
```

## الخطوة 3: حفظ الصورة المعدلة
بعد الانتهاء من التعديل، استدعِ طريقة `save` وحدد `SaveFormat.Bmp`. تقوم المكتبة بكتابة ملف BMP يحافظ على التغييرات البصرية التي أجريتها، مكملةً سير عمل **تحويل PSD إلى BMP**.  
```java
String outpath = dataDir + "CoreDrawingFeatures.bmp";
// Save modified pixels back to the image
image.saveArgb32Pixels(new Rectangle(0, 0, 100, 10), pixels);
// Save the image to BMP format
image.save(outpath, new BmpOptions());
```

## المشكلات الشائعة واستكشاف الأخطاء
- **أخطاء نفاد الذاكرة** – تقوم Aspose.PSD ببث البيانات؛ ومع ذلك، قد تحتاج ملفات PSD الضخمة جدًا (>2 GB) إلى مساحة heap إضافية للـ JVM (`-Xmx4g`).  
- **عدم تطابق ملفات تعريف الألوان** – إذا كان BMP الناتج يبدو باهتًا، تأكد من حفظ ملف تعريف ICC الخاص بـ PSD المصدر عن طريق استدعاء `psdImage.getColorProfile()` قبل الحفظ.  
- **غياب الطبقات بعد التحويل** – تحقق من عدم تجاهل الطبقات المخفية عن طريق فحص `layer.isVisible()` قبل الحفظ.

## الأسئلة المتكررة

**س: هل يمكن لـ Aspose.PSD for Java التعامل مع الطبقات والشفافية في ملفات PSD؟**  
ج: نعم، تدعم المكتبة بالكامل ملفات PSD ذات الطبقات، بما في ذلك الشفافية، وأنماط المزج، وتأثيرات الطبقة.

**س: هل Aspose.PSD for Java مناسب لمعالجة دفعات من ملفات PSD؟**  
ج: بالتأكيد. يمكنك أتمتة وظائف الدفعات عبر التكرار على مجلد، تحميل كل PSD، تطبيق نفس منطق الرسم، وحفظه كـ BMP أو أي صيغة مدعومة أخرى.

**س: هل يدعم Aspose.PSD for Java صيغ صور متعددة غير PSD؟**  
ج: بالإضافة إلى PSD، تتعامل الواجهة مع BMP، PNG، JPEG، TIFF، GIF، وأكثر من 20 صيغة نقطية إضافية للإدخال والإخراج.

**س: كيف يمكنني الحصول على ترخيص مؤقت لـ Aspose.PSD for Java؟**  
ج: زر صفحة [ترخيص Aspose.PSD المؤقت](https://purchase.aspose.com/temporary-license/) للحصول على ترخيص مؤقت.

**س: أين يمكنني العثور على مزيد من المساعدة والموارد لـ Aspose.PSD for Java؟**  
ج: استكشف [منتدى Aspose.PSD](https://forum.aspose.com/c/psd/34) للحصول على دعم المجتمع، والنصائح، والموارد الإضافية.

---

**آخر تحديث:** 2026-09-03  
**تم الاختبار مع:** Aspose.PSD 24.12 for Java  
**المؤلف:** Aspose

## دروس ذات صلة

- [كيفية إنشاء تأثيرات تدرج شعاعي في Aspose.PSD for Java](/psd/java/advanced-image-effects/add-gradient-effects/)
- [رسم وحفظ مستطيل في PSD باستخدام Aspose.PSD for Java](/psd/java/basic-image-operations/simple-drawing/)
- [كيفية تحويل PSD إلى صيغ صور نقطية باستخدام Aspose.PSD for Java](/psd/java/advanced-techniques/convert-psd-to-raster-formats/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}
{{< blocks/products/products-backtop-button >}}