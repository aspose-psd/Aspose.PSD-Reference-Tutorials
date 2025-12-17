---
date: 2025-12-17
description: تعلم كيفية تحويل ملفات PSD إلى PNG مع ضبط وضع اللون في PSD إلى تدرج رمادي
  16‑بت باستخدام Aspose.PSD للغة Java. دليل خطوة بخطوة مع أمثلة على الشيفرة.
linktitle: Convert PSD to PNG – 16-bit Grayscale – Java
second_title: Aspose.PSD Java API
title: كيفية تحويل PSD إلى PNG مع وضع اللون الرمادي 16‑بت في جافا
url: /ar/java/advanced-psd-layer-features-effects/support-16-bit-grayscale-color-mode-psd/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# تحويل PSD إلى PNG بوضع اللون الرمادي 16‑بت في جافا

## المقدمة
عند الغوص في عالم التصميم الجرافيكي ومعالجة الصور، فإن فهم كيفية **تحويل PSD إلى PNG** يشبه امتلاك سلاح سري. على وجه الخصوص، يمنحك وضع اللون الرمادي 16‑بت عمقًا وتفاصيل مذهلة تجعل صورك تبرز حقًا. في هذا الدرس سنستعرض كيفية **تعيين وضع لون PSD** إلى 16‑بت رمادي ثم **تصدير PSD كـ PNG** باستخدام Aspose.PSD for Java. هل أنت مستعد للارتقاء بسير عملك في معالجة الصور؟ لنبدأ.

## إجابات سريعة
- **ماذا يتضمن “تحويل PSD إلى PNG”؟** تحميل ملف PSD، تعديل وضع اللون إذا لزم الأمر، ثم حفظه كملف PNG.  
- **أي فئة في Aspose تتولى التحويل؟** `PsdImage` للتحميل و`PngOptions` للحفظ.  
- **هل أحتاج إلى ترخيص خاص؟** النسخة التجريبية تكفي للاختبار؛ الترخيص المدفوع مطلوب للإنتاج.  
- **هل يمكن الحفاظ على عمق 16‑بت في PNG؟** نعم، باستخدام `PngColorType.GrayscaleWithAlpha`.  
- **ما هي بيئات التطوير المتكاملة المدعومة؟** أي بيئة جافا – IntelliJ IDEA، Eclipse، VS Code، إلخ.

## المتطلبات المسبقة
قبل أن نبدأ، دعنا نتأكد من أن لديك كل ما يلزم للحصول على أفضل تجربة مع هذا الدرس. إليك ما ستحتاجه:

1. **مجموعة تطوير جافا (JDK)** – تأكد من تثبيت أحدث نسخة. يمكنك تنزيلها من [موقع Oracle](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).  
2. **مكتبة Aspose.PSD for Java** – هذه هي المحرك الذي سيمكننا من تعديل ملفات PSD. احصل عليها من [صفحة تحميل Aspose](https://releases.aspose.com/psd/java/).  
3. **بيئة تطوير متكاملة (IDE)** – IntelliJ IDEA، Eclipse، أو Visual Studio Code ستعمل جميعًا بشكل جيد.  
4. **معرفة أساسية بجافا** – الإلمام بصياغة جافا سيسهل عليك تنفيذ الخطوات.  
5. **ملف PSD تجريبي** – إما أن تنشئه في Adobe Photoshop أو تنزل عينة مجانية من الإنترنت.

هل أنت جاهز؟ عظيم! لنستورد الحزم الضرورية ونبدأ بالبرمجة.

## استيراد الحزم
لبدء العمل، أضف الاستيرادات المطلوبة من Aspose.PSD إلى ملف جافا الخاص بك:

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

هذه الاستيرادات تمنحك الوصول إلى الوظائف التي ستستخدمها لمعالجة ملفات PSD، تعيين وضع اللون، وتصدير النتيجة كـ PNG.

## الخطوة 1: تعريف الأدلة
أولًا، قم بإعداد مجلدي المصدر والإخراج. هذا يخبر البرنامج من أين يقرأ ملف PSD الأصلي وإلى أين يكتب الملفات المحوّلة.

```java
String sourceDir = "Your Source Directory"; // Change to your source directory
String outputDir = "Your Document Directory"; // Change to your output directory
```

استبدل سلاسل النص الوهمية بالمسارات الفعلية على جهازك.

## الخطوة 2: إنشاء طريقة لمعالجة الصورة
سنُغلف منطق التحويل داخل طريقة قابلة لإعادة الاستخدام. تستقبل جميع المعاملات التي قد ترغب في تعديلها، مثل وضع اللون، عمق البت، والضغط.

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

## الخطوة 3: تعريف مسارات الملفات وتحميل PSD
داخل الطريقة، بنِ مسارات الملفات الكاملة وحمّل ملف PSD الرمادي 16‑بت الأصلي:

```java
String filePath = sourceDir + file + ".psd";
String postfix = Enum.getName(ColorModes.class, colorMode) + channelBitsCount + "_" +
                 channelsCount + "_" + Enum.getName(CompressionMethod.class, compression);
String exportPath = outputDir + file + postfix + ".psd";
String pngExportPath = outputDir + file + postfix + ".png";
// Load a predefined 16-bit grayscale PSD
PsdImage image = (PsdImage)Image.load(filePath);
```

المتغير `postfix` يساعدك على تتبع الإعدادات المستخدمة لكل ملف تم تصديره.

## الخطوة 4: معالجة الطبقة أو الصورة بالكامل
الآن إما نرسم على طبقة محددة أو على الصورة بأكملها. في هذا المثال نضيف إطارًا رماديًا خفيفًا لجعل النتيجة أكثر وضوحًا.

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

## الخطوة 5: حفظ ملف PSD المعدل
بعد الرسم، نحفظ ملف PSD مع وضع اللون وعمق البت المحددين بالضبط. هذا هو جوهر **تعيين وضع لون PSD** قبل التحويل.

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

## الخطوة 6: تحويل PSD إلى PNG
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

الآن قد نجحت في **تحويل PSD إلى PNG** مع الحفاظ على بيانات اللون الرمادي عالية الجودة 16‑بت.

## المشكلات الشائعة والحلول
| المشكلة | السبب | الحل |
|---------|-------|------|
| **استثناء “Unsupported color type”** | محاولة حفظ PSD بتكوين قناة غير مدعوم. | تأكد من أن `channelBitsCount` يطابق عمق البت الفعلي (16) وأن `channelsCount` صحيح للرمادي (1). |
| **الملف غير موجود** | مسار دليل المصدر غير صحيح. | راجع سلسلة `sourceDir` وتأكد من وجود ملف PSD. |
| **PNG الناتج يظهر أسود** | حفظ PNG دون معالجة قناة ألفا. | استخدم `PngColorType.GrayscaleWithAlpha` كما هو موضح أعلاه. |

## الأسئلة المتكررة

**س: ما هو وضع اللون الرمادي 16‑بت؟**  
ج: يوفر 65 536 درجة من الرمادي، مما يمنح تفاصيل نغمية أكبر بكثير من الوضع القياسي 8‑بت (256 درجة).

**س: هل يمكنني استخدام Aspose.PSD للصور غير الرمادية؟**  
ج: بالتأكيد! يدعم Aspose.PSD وضع RGB، CMYK، Lab، والعديد من أوضاع اللون الأخرى.

**س: هل هناك نسخة تجريبية من Aspose.PSD؟**  
ج: نعم، يمكنك تجربة نسخة تجريبية مجانية من Aspose.PSD. فقط توجه إلى [صفحة تحميل Aspose](https://releases.aspose.com/).

**س: أين يمكنني العثور على المزيد من الأمثلة لاستخدام Aspose.PSD؟**  
ج: يمكنك الاطلاع على [الوثائق](https://reference.aspose.com/psd/java/) للحصول على أمثلة وشروحات أكثر تفصيلاً.

**س: كيف أشتري ترخيصًا لـ Aspose.PSD؟**  
ج: يمكنك شراء ترخيص عبر زيارة [صفحة الشراء الخاصة بـ Aspose](https://purchase.aspose.com/buy).

---

**آخر تحديث:** 2025-12-17  
**تم الاختبار مع:** Aspose.PSD for Java 24.12 (أحدث نسخة وقت كتابة الدليل)  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}