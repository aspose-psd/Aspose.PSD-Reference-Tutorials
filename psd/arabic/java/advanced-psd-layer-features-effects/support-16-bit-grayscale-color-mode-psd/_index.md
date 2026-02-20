---
date: 2026-02-20
description: تعلم كيفية تحويل ملف PSD إلى PNG مع ضبط وضع لون PSD إلى تدرج رمادي 16‑بت
  باستخدام Aspose.PSD للغة Java. دليل خطوة بخطوة مع أمثلة على الشيفرة.
linktitle: Convert PSD to PNG – 16-bit Grayscale – Java
second_title: Aspose.PSD Java API
title: كيفية تحويل PSD إلى PNG مع وضع اللون الرمادي 16‑بت في جافا
url: /ar/java/advanced-psd-layer-features-effects/support-16-bit-grayscale-color-mode-psd/
weight: 11
---

Now produce final output with all translated content.{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# تحويل PSD إلى PNG مع وضع اللون الرمادي 16‑بت في Java

## Introduction
عند الغوص في عالم التصميم الجرافيكي ومعالجة الصور، معرفة **كيفية تحويل PSD إلى PNG** تشبه امتلاك سلاح سري. استخدام وضع الرمادي 16‑بت يضيف عمقًا مذهلاً وغنىً نغميًا، مما يجعل صورك بارزة. في هذا الدرس سنستعرض كيفية **تعيين وضع لون PSD** إلى الرمادي 16‑بت ثم **تصدير PSD كـ PNG** باستخدام Aspose.PSD for Java. هل أنت مستعد للارتقاء بسير عمل الصور؟ لنبدأ.

## Quick Answers
- **ماذا يتضمن “تحويل PSD إلى PNG”?** تحميل ملف PSD، مع إمكانية تغيير وضع اللون، ثم حفظه كملف PNG.  
- **ما هو الصنف في Aspose الذي يتعامل مع التحويل؟** `PsdImage` للتحميل و`PngOptions` للحفظ.  
- **هل أحتاج إلى ترخيص خاص؟** النسخة التجريبية تعمل للاختبار؛ يلزم ترخيص مدفوع للإنتاج.  
- **هل يمكنني الحفاظ على عمق 16‑بت في PNG؟** نعم، باستخدام `PngColorType.GrayscaleWithAlpha`.  
- **ما هي بيئات التطوير المتكاملة المدعومة؟** أي بيئة Java IDE – IntelliJ IDEA، Eclipse، VS Code، إلخ.

## Why Convert PSD to PNG with 16‑bit Grayscale?
* **الحفاظ على التفاصيل النغمية:** وضع الرمادي 16‑بت يخزن 65 536 درجة من الرمادي، وهو أكثر بكثير من 256 درجة في الصورة 8‑بت.  
* **توافق واسع:** PNG مدعوم على نطاق واسع عبر المتصفحات، تطبيقات الهواتف المحمولة، وأدوات سطح المكتب، مع الحفاظ على البيانات عالية الجودة.  
* **سير عمل بدون فقدان:** التحويل باستخدام Aspose.PSD يضمن عدم وجود تشوهات ضغط غير مرغوبة، وهو مثالي للأرشفة أو المعالجة اللاحقة.

## Prerequisites
قبل أن نبدأ، دعنا نتأكد من أن لديك كل ما يلزم للحصول على أفضل استفادة من هذا الدرس. إليك ما ستحتاجه:

1. **Java Development Kit (JDK)** – تأكد من تثبيت أحدث نسخة. يمكنك تنزيله من [Oracle's site](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).  
2. **Aspose.PSD for Java Library** – هذه هي المحرك الذي سيمكننا من معالجة ملفات PSD. احصل عليها من [Aspose download page](https://releases.aspose.com/psd/java/).  
3. **بيئة تطوير متكاملة (IDE)** – IntelliJ IDEA أو Eclipse أو Visual Studio Code ستعمل بشكل جيد.  
4. **معرفة أساسية بـ Java** – الإلمام بصياغة Java سيجعل الخطوات أسهل.  
5. **ملف PSD تجريبي** – إما أن تنشئه في Adobe Photoshop أو تنزل عينة مجانية من الإنترنت.

هل أنت مستعد؟ عظيم! لنستورد الحزم اللازمة ونبدأ بالبرمجة.

## Import Packages
لبدء العملية، أضف الاستيرادات المطلوبة من Aspose.PSD إلى ملف Java الخاص بك:

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

هذه الاستيرادات تمنحك الوصول إلى الوظائف التي ستستخدمها لمعالجة ملفات PSD، وتعيين وضع اللون، وتصدير النتيجة كـ PNG.

## Step 1: Define Your Directories
أولاً، قم بإعداد مجلدات المصدر والإخراج. هذا يخبر البرنامج من أين يقرأ ملف PSD الأصلي وإلى أين يكتب الملفات المحولة.

```java
String sourceDir = "Your Source Directory"; // Change to your source directory
String outputDir = "Your Document Directory"; // Change to your output directory
```

استبدل سلاسل النص الوهمية بالمسارات الفعلية على جهازك.

## Step 2: Create a Method to Handle Image Processing
سنغلف منطق التحويل داخل طريقة قابلة لإعادة الاستخدام. تستقبل جميع المعلمات التي قد ترغب في تعديلها، مثل وضع اللون، عمق البت، والضغط.

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

هذه الطريقة تتيح لك **تعيين وضع لون PSD** ثم **تصدير PSD كـ PNG** في تدفق واحد.

## Step 3: Define File Paths and Load the PSD
داخل الطريقة، أنشئ مسارات الملفات الكاملة وحمّل ملف PSD الرمادي 16‑بت الأصلي:

```java
String filePath = sourceDir + file + ".psd";
String postfix = Enum.getName(ColorModes.class, colorMode) + channelBitsCount + "_" +
                 channelsCount + "_" + Enum.getName(CompressionMethod.class, compression);
String exportPath = outputDir + file + postfix + ".psd";
String pngExportPath = outputDir + file + postfix + ".png";
// Load a predefined 16-bit grayscale PSD
PsdImage image = (PsdImage)Image.load(filePath);
```

`postfix` يساعدك على تتبع الإعدادات المستخدمة لكل ملف مُصدَّر.

## Step 4: Process the Layer or Full Image
الآن نرسم إما على طبقة محددة أو على الصورة بالكامل. في هذا المثال نضيف حدًا رماديًا خفيفًا لجعل النتيجة أكثر وضوحًا.

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

## Step 5: Save the Modified PSD File
بعد الرسم، نحفظ ملف PSD مع وضع اللون وعمق البت المحددين. هذا هو جوهر **تعيين وضع لون PSD** قبل التحويل.

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

## Step 6: Convert the PSD to PNG
أخيرًا، نحمل ملف PSD المحفوظ حديثًا ونصدّره كـ PNG. باستخدام `PngColorType.GrayscaleWithAlpha` نحافظ على عمق 16‑بت في ملف PNG.

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

الآن لقد نجحت في **تحويل PSD إلى PNG** مع الحفاظ على بيانات الرمادي 16‑بت عالية الجودة.

## Common Issues and Solutions
| المشكلة | سبب حدوثها | الحل |
|-------|----------------|-----|
| **استثناء “Unsupported color type”** | محاولة حفظ PSD بتكوين قناة غير مدعوم. | تأكد من أن `channelBitsCount` يطابق عمق البت الفعلي (16) وأن `channelsCount` صحيح للرمادي (1). |
| **الملف غير موجود** | مسار دليل المصدر غير صحيح. | تحقق مرة أخرى من سلسلة `sourceDir` وتأكد من وجود ملف PSD. |
| **PNG الناتج يظهر أسود** | تم حفظ PNG بدون معالجة قناة ألفا. | استخدم `PngColorType.GrayscaleWithAlpha` كما هو موضح أعلاه. |

## Frequently Asked Questions

**س: ما هو وضع اللون الرمادي 16‑بت؟**  
ج: يوفر 65 536 درجة من الرمادي، مما يقدم تفاصيل نغمية أكثر بكثير من الوضع القياسي 8‑بت (256 درجة).

**س: هل يمكنني استخدام Aspose.PSD للصور غير الرمادية؟**  
ج: بالتأكيد! Aspose.PSD يدعم RGB، CMYK، Lab، والعديد من أوضاع اللون الأخرى.

**س: هل هناك نسخة تجريبية من Aspose.PSD؟**  
ج: نعم، يمكنك تجربة نسخة تجريبية مجانية من Aspose.PSD. فقط انتقل إلى [Aspose download page](https://releases.aspose.com/).

**س: أين يمكنني العثور على مزيد من الأمثلة لاستخدام Aspose.PSD؟**  
ج: يمكنك الاطلاع على [documentation](https://reference.aspose.com/psd/java/) للحصول على أمثلة ودروس أكثر تفصيلاً.

**س: كيف يمكنني شراء ترخيص لـ Aspose.PSD؟**  
ج: يمكنك شراء ترخيص بزيارة [Aspose purchase page](https://purchase.aspose.com/buy).

---

**آخر تحديث:** 2026-02-20  
**تم الاختبار مع:** Aspose.PSD for Java 24.12 (latest at time of writing)  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}