---
date: 2026-09-28
description: تعلم كيفية تصدير PSD كـ PNG مع ضبط وضع اللون الرمادي 16‑بت باستخدام Aspose.PSD
  for Java. دليل خطوة بخطوة مع أمثلة على الشيفرة.
keywords:
- export psd as png
- how to convert psd to png
- 16-bit grayscale java
lastmod: 2026-09-28
linktitle: تصدير PSD كـ PNG – اللون الرمادي 16‑بت – Java
og_description: تصدير PSD كـ PNG مع اللون الرمادي 16‑بت باستخدام Aspose.PSD for Java.
  اتبع هذا الدرس خطوة بخطوة للحفاظ على 65,536 درجة من الرمادي.
og_image_alt: Guide showing how to export PSD as PNG with 16-bit grayscale using Aspose.PSD
  Java
og_title: تصدير PSD كـ PNG مع اللون الرمادي 16‑بت في Java – دليل Aspose.PSD
schemas:
- author: Aspose
  dateModified: '2026-09-28'
  description: Learn how to export PSD as PNG while setting PSD color mode to 16-bit
    grayscale using Aspose.PSD for Java. Step‑by‑step guide with code examples.
  headline: How to export PSD as PNG with 16‑bit grayscale color mode in Java
  type: TechArticle
- description: Learn how to export PSD as PNG while setting PSD color mode to 16-bit
    grayscale using Aspose.PSD for Java. Step‑by‑step guide with code examples.
  name: How to export PSD as PNG with 16‑bit grayscale color mode in Java
  steps:
  - name: '**Java Development Kit (JDK)** – Install the latest JDK from [Oracle''s
      site](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).'
    text: '**Java Development Kit (JDK)** – Install the latest JDK from [Oracle''s
      site](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).'
  - name: '**Aspose.PSD for Java library** – Download the JAR from the [Aspose download
      page](https://releases.aspose.com/psd/java/).'
    text: '**Aspose.PSD for Java library** – Download the JAR from the [Aspose download
      page](https://releases.aspose.com/psd/java/).'
  - name: '**An IDE** – IntelliJ IDEA, Eclipse, or Visual Studio Code works perfectly.'
    text: '**An IDE** – IntelliJ IDEA, Eclipse, or Visual Studio Code works perfectly.'
  - name: '**Basic Java knowledge** – You should be comfortable creating classes,
      handling exceptions, and working with file paths.'
    text: '**Basic Java knowledge** – You should be comfortable creating classes,
      handling exceptions, and working with file paths.'
  - name: '**A sample PSD file** – Create one in Adobe Photoshop or grab a free sample
      online.'
    text: '**A sample PSD file** – Create one in Adobe Photoshop or grab a free sample
      online.'
  type: HowTo
- questions:
  - answer: It provides 65 536 shades of gray, delivering far more tonal detail than
      the standard 8‑bit (256 shades).
    question: What is 16‑bit grayscale color mode?
  - answer: Absolutely! Aspose.PSD supports RGB, CMYK, Lab, Indexed, and many other
      color modes.
    question: Can I use Aspose.PSD for non‑grayscale images?
  - answer: Yes, you can try a free trial version of Aspose.PSD. Just head to the
      [Aspose download page](https://releases.aspose.com/).
    question: Is there a trial version of Aspose.PSD?
  - answer: Check the official [documentation](https://reference.aspose.com/psd/java/)
      for in‑depth tutorials, API references, and sample projects.
    question: Where can I find more Aspose.PSD examples?
  - answer: You can buy a license by visiting the [Aspose purchase page](https://purchase.aspose.com/buy).
    question: How do I purchase a license for Aspose.PSD?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- convert psd
- Aspose.PSD
- Java image processing
title: كيفية تصدير PSD كـ PNG مع وضع اللون الرمادي 16‑بت في Java
url: /ar/java/advanced-psd-layer-features-effects/support-16-bit-grayscale-color-mode-psd/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# تصدير PSD كـ PNG مع وضع اللون الرمادي 16‑بت في Java

## المقدمة
يمنحك تصدير PSD كـ PNG مع الحفاظ على وضع اللون الرمادي 16‑بت عمق صورة احترافية وتوافقًا عالميًا لملف PNG. في هذا الدليل ستتعلم كيفية **تعيين وضع لون PSD إلى 16‑بت رمادي** ثم **تصدير PSD كـ PNG** باستخدام Aspose.PSD for Java. يغطي البرنامج التعليمي كل شيء من المتطلبات المسبقة إلى استكشاف الأخطاء وإصلاحها، بحيث يمكنك دمج سير العمل في أي خط أنابيب صور مبني على Java.

## إجابات سريعة
- **ما الذي يتضمنه “تصدير PSD كـ PNG”؟** تحميل ملف PSD، تعديل وضع لونه إذا لزم الأمر، ثم حفظه كملف PNG.  
- **أي فئة في Aspose تتعامل مع التحويل؟** `PsdImage` تقوم بتحميل PSD و`PngOptions` تحدد إعدادات إخراج PNG.  
- **هل أحتاج إلى ترخيص للإنتاج؟** نعم – النسخة التجريبية تعمل للاختبار، لكن الترخيص المدفوع مطلوب للاستخدام التجاري.  
- **هل يمكن الاحتفاظ بعمق 16‑بت في PNG؟** بالتأكيد، عبر استخدام `PngColorType.GrayscaleWithAlpha`.  
- **ما هي بيئات التطوير المتكاملة المدعومة؟** أي بيئة Java IDE – IntelliJ IDEA، Eclipse، VS Code، أو NetBeans.

## ما هو تصدير PSD كـ PNG؟
تصدير PSD كـ PNG هو عملية تحويل مستند Adobe Photoshop (PSD) إلى ملف Portable Network Graphics (PNG) مع الحفاظ على بيانات البكسل وعمق اللون. يُستخدم هذا التحويل عادةً لمشاركة أصول رمادية عالية الجودة على الويب دون فقدان التفاصيل النغمية.

## لماذا تصدير PSD كـ PNG مع وضع اللون الرمادي 16‑بت؟
يحافظ التصدير إلى PNG مع الحفاظ على وضع اللون الرمادي 16‑بت على 65 536 درجة من الرمادي، مما يوفر غنىً نغميًا أكبر بكثير من الصور 8‑بت. يضمن الدعم العالمي لملفات PNG إمكانية عرضها في المتصفحات، التطبيقات المحمولة، ومحررات سطح المكتب دون فقدان، بينما يضمن الضغط غير الفاقد في Aspose.PSD عدم إدخال أي تشوهات.

## المتطلبات المسبقة
قبل أن نبدأ، تأكد من أن لديك العناصر التالية جاهزة:

1. **Java Development Kit (JDK)** – قم بتثبيت أحدث JDK من [Oracle's site](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).  
2. **Aspose.PSD for Java library** – حمّل ملف JAR من صفحة [Aspose download page](https://releases.aspose.com/psd/java/).  
3. **An IDE** – IntelliJ IDEA، Eclipse، أو Visual Studio Code تعمل بشكل مثالي.  
4. **Basic Java knowledge** – يجب أن تكون مرتاحًا لإنشاء الفئات، معالجة الاستثناءات، والعمل مع مسارات الملفات.  
5. **A sample PSD file** – أنشئ واحدًا في Adobe Photoshop أو احصل على عينة مجانية عبر الإنترنت.

## كيفية تصدير PSD كـ PNG خطوة بخطوة

## كيف تقوم بتعيين وضع اللون الرمادي 16‑بت لملف PSD؟
`PsdImage` هي فئة Aspose.PSD التي تقوم بتحميل وتمثيل ملف PSD في الذاكرة.  
`ColorMode` هو تعداد يحدد وضع لون صورة PSD.  

حمّل الـ PSD باستخدام `PsdImage`، غير وضع لونه باستخدام خاصية `ColorMode`، ثم احفظ الملف المعدل. يتم تنفيذ هذه العملية بالكامل في الذاكرة، مما يلغي الحاجة إلى ملفات وسيطة ويضمن أن التحويل سريع وفعال.

```java
import com.aspose.psd.*;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.ColorModes;
import com.aspose.psd.fileformats.psd.CompressionMethod;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.imageoptions.PsdOptions;
import com.aspose.psd.system.Enum;
```

هذه الاستيرادات تمنحك الوصول إلى الوظائف التي ستستخدمها لمعالجة ملفات PSD، ضبط وضع اللون، وتصدير النتيجة كـ PNG.

## كيف تحدد مجلدات المصدر والإخراج؟
`File` هي فئة java.io تمثل مسار ملف أو دليل على نظام الملفات.  

تحتاج إلى إخبار البرنامج من أين يقرأ ملف PSD الأصلي وإلى أين يكتب ملف PNG المحول. يمكن استخدام مسارات مطلقة أو نسبية، لكن احرص على أن تكون متسقة عبر البيئات لتجنب أخطاء حل المسار.

```java
String sourceDir = "Your Source Directory"; // Change to your source directory
String outputDir = "Your Document Directory"; // Change to your output directory
```

استبدل سلاسل العناصر النائبة بالمسارات الفعلية على جهازك.

## كيف تغلف منطق التحويل في طريقة قابلة لإعادة الاستخدام؟
`convertPsdToPng` هي طريقة مخصصة تغلف جميع الخطوات المطلوبة لتحويل ملف PSD إلى PNG مع إعدادات اختيارية.  

إنشاء طريقة مخصصة يتيح لك إعادة استخدام نفس خطوات التحويل لملفات متعددة أو إعدادات مختلفة. مرّر معلمات مثل مسار المصدر، مجلد الوجهة، ومستوى الضغط الاختياري، مما يجعل سير العمل مرنًا وقابلًا للصيانة.

```java
class LocalScopeExtension {
    void saveToPsdThenLoadAndSaveToPng(
        String file,
        short colorMode,
        short channelBitsCount,
        short channelsCount,
        short compression,
        int layerNumber) {
```

هذه الطريقة تسمح لك **بتعيين وضع لون PSD** ثم **تصدير PSD كـ PNG** في تدفق واحد.

## كيف تقوم بتحميل PSD وتطبيق وضع اللون الرمادي 16‑بت؟
`PsdImage` هي فئة Aspose.PSD التي تقوم بتحميل ملف PSD إلى الذاكرة.  
`ColorMode.GRAYSCALE_16` هو قيمة تعداد تُعيّن الصورة إلى اللون الرمادي 16‑بت.  
`channelBitsCount` هي خاصية تحدد عدد البتات لكل قناة.  

داخل طريقة التحويل، ابنِ مسارات الملفات الكاملة، أنشئ كائن `PsdImage`، وغير خاصية `ColorMode` إلى `ColorMode.GRAYSCALE_16`. يجب ضبط خاصية `channelBitsCount` إلى 16 للحفاظ على العمق العالي للبت، مما يضمن بقاء الصورة تحتفظ بجميع المعلومات النغمية.

```java
String filePath = sourceDir + file + ".psd";
String postfix = Enum.getName(ColorModes.class, colorMode) + channelBitsCount + "_" +
                 channelsCount + "_" + Enum.getName(CompressionMethod.class, compression);
String exportPath = outputDir + file + postfix + ".psd";
String pngExportPath = outputDir + file + postfix + ".png";
// Load a predefined 16-bit grayscale PSD
PsdImage image = (PsdImage)Image.load(filePath);
```

يساعدك المتغير `postfix` على تتبع الإعدادات المستخدمة لكل ملف مُصدَّر.

## كيف ترسم حدًا خفيفًا على الصورة (خطوة اختيارية)؟
`Graphics` هي فئة توفر إمكانيات الرسم على لوحة `PsdImage`.  

يمكنك اختياريًا رسم مستطيل رمادي حول الصورة لجعل الإخراج أكثر وضوحًا أثناء الاختبار. تُظهر هذه الخطوة كيفية العمل مع الطبقات وكائنات الرسومات، ويتم حساب المستطيل ديناميكيًا بحيث يبقى مركزيًا بغض النظر عن حجم الصورة.

```java
try {
    RasterCachedImage raster = layerNumber >= 0 ? image.getLayers()[layerNumber] : image;
    // Draw a gray inner border around the perimeter of the layer
    Graphics graphics = new Graphics(raster);
    int width = raster.getWidth();
    int height = raster.getHeight();
    Rectangle rect = new Rectangle(
        width / 3,
        height / 3,
        width - (2 * (width / 3)) - 1,
        height - (2 * (height / 3)) - 1);
    graphics.drawRectangle(new Pen(Color.getDarkGray(), 1), rect);
```

يتم حساب المستطيل ديناميكيًا بحيث يبقى مركزيًا بغض النظر عن حجم الصورة.

## كيف تحفظ ملف PSD المعدل مع وضع اللون الجديد؟
`PsdOptions` هي فئة تتحكم في كيفية حفظ ملف PSD، بما في ذلك إعدادات وضع اللون وعمق البت.  

بعد الرسم (أو تخطي هذه الخطوة)، استدعِ `save` على كائن `PsdImage`، مع تمرير كائن `PsdOptions` الذي يحافظ على تكوين اللون الرمادي 16‑بت. يضمن ذلك أن ملف PSD المحفوظ يحتفظ بوضع اللون المطلوب دون أي فقدان للبيانات.

```java
    // Save a copy of PSD with specific characteristics
    PsdOptions psdOptions = new PsdOptions();
    psdOptions.setColorMode(colorMode);
    psdOptions.setChannelBitsCount(channelBitsCount);
    psdOptions.setChannelsCount(channelsCount);
    psdOptions.setCompressionMethod(compression);
    image.save(exportPath, psdOptions);
}
```

## كيف تحول PSD إلى PNG مع الحفاظ على عمق 16‑بت؟
`PngOptions` هي فئة تحدد إعدادات إخراج PNG مثل نوع اللون ومستوى الضغط.  
`PngColorType.GrayscaleWithAlpha` هو قيمة تعداد تخزن بيانات اللون الرمادي 16‑بت مع قناة ألفا.  

حمّل الـ PSD المحفوظ حديثًا، اضبط `PngOptions` باستخدام `PngColorType.GrayscaleWithAlpha`، ثم استدعِ `save`. سيحتفظ هذا ببيانات اللون الرمادي 16‑بت داخل ملف PNG، مما يوفر صورة غير مضغوطة وعالية الجودة مناسبة للمعالجة أو التوزيع الإضافي.

```java
finally {
    image.dispose();
}
// Load the saved PSD
PsdImage image1 = (PsdImage)Image.load(exportPath);
try {
    // Convert the saved PSD to a grayscale PNG image
    PngOptions pngOptions = new PngOptions();
    pngOptions.setColorType(PngColorType.GrayscaleWithAlpha);
    image1.save(pngExportPath, pngOptions); // here should be no exception
}
finally {
    image1.dispose();
}
```

الآن لقد نجحت في **تصدير PSD كـ PNG** مع الحفاظ على بيانات اللون الرمادي 16‑بت عالية الجودة.

## المشكلات الشائعة والحلول
| المشكلة | سبب حدوثه | الحل |
|-------|----------------|-----|
| **“Unsupported color type” exception** | محاولة حفظ PSD بتكوين قناة غير مدعوم. | تأكد من أن `channelBitsCount` يطابق عمق البت الفعلي (16) وأن `channelsCount` صحيح للون الرمادي (1). |
| **File not found** | مسار دليل المصدر غير صحيح. | تحقق مرة أخرى من سلسلة `sourceDir` وتأكد من وجود ملف PSD في ذلك الموقع. |
| **Output PNG appears black** | تم حفظ PNG دون معالجة قناة ألفا بشكل صحيح. | استخدم `PngColorType.GrayscaleWithAlpha` كما هو موضح أعلاه. |
| **Memory overflow on large PSDs** | تحميل الملف بالكامل في الذاكرة. | فعّل وضع البث عبر `PsdImage.load(inputStream, new LoadOptions())` لمعالجة الملفات الكبيرة بكفاءة. |

## الأسئلة المتكررة

**س: ما هو وضع اللون الرمادي 16‑بت؟**  
ج: يوفر 65 536 درجة من الرمادي، مما يقدم تفاصيل نغمية أكبر بكثير من الوضع القياسي 8‑بت (256 درجة).

**س: هل يمكنني استخدام Aspose.PSD للصور غير الرمادية؟**  
ج: بالتأكيد! يدعم Aspose.PSD وضع RGB، CMYK، Lab، Indexed، والعديد من أوضاع اللون الأخرى.

**س: هل هناك نسخة تجريبية من Aspose.PSD؟**  
ج: نعم، يمكنك تجربة نسخة تجريبية مجانية من Aspose.PSD. فقط توجه إلى صفحة [Aspose download page](https://releases.aspose.com/).

**س: أين يمكنني العثور على المزيد من أمثلة Aspose.PSD؟**  
ج: راجع الوثائق الرسمية على [documentation](https://reference.aspose.com/psd/java/) للحصول على دروس متعمقة، مراجع API، ومشروعات نموذجية.

**س: كيف أشتري ترخيصًا لـ Aspose.PSD؟**  
ج: يمكنك شراء ترخيص بزيارة صفحة [Aspose purchase page](https://purchase.aspose.com/buy).

---

**آخر تحديث:** 2026-09-28  
**تم الاختبار باستخدام:** Aspose.PSD for Java 24.12 (latest at time of writing)  
**المؤلف:** Aspose

## دروس ذات صلة

- [Convert PSD to PNG with Specified Bit Depth Using Aspose.PSD for Java](/psd/java/optimizing-png-files/specify-png-bit-depth/)
- [Export PSD to PNG with Layer Effects using Aspose.PSD for Java](/psd/java/psd-image-modification-conversion/apply-layer-effects-psd-files/)
- [Save PSD as JPEG and Support RGB Color with Aspose.PSD Java](/psd/java/advanced-psd-layer-features-effects/support-rgb-color-psd-files/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}