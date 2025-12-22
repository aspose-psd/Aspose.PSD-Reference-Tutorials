---
date: 2025-12-21
description: تعلم كيفية إجراء معالجة الصور في جافا عن طريق تعديل جاما الصورة باستخدام
  Aspose.PSD. دليل خطوة بخطوة لتحويل PSD إلى TIFF وتطبيق تصحيح الجاما.
linktitle: Adjust Gamma of an Image
second_title: Aspose.PSD Java API
title: معالجة الصور بجافا – تعديل غاما باستخدام Aspose.PSD
url: /ar/java/advanced-techniques/adjust-gamma/
weight: 23
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# معالجة الصور في Java – تعديل Gamma باستخدام Aspose.PSD

## مقدمة

إذا كنت تعمل على **معالجة الصور في Java**، فإن تعديل قيمة gamma للصورة يُعد تقنية أساسية لتحسين السطوع والتباين دون فقدان التفاصيل. في هذا الدرس سنستعرض كيفية استخدام **Aspose.PSD for Java** لتطبيق تصحيح gamma على ملف PSD ثم تصدير النتيجة كصورة TIFF. ستتعرف على لماذا هذه الطريقة سريعة، موثوقة، ومثالية لسلاسل معالجة الصور على الخادم.

## إجابات سريعة
- **ماذا يفعل تصحيح gamma؟** يعيد رسم قيم الإضاءة لجعل المناطق الداكنة أكثر إشراقًا أو المناطق الفاتحة أكثر قتامة مع الحفاظ على التفاصيل العامة.  
- **أي مكتبة تتولى المعالجة؟** Aspose.PSD for Java توفر طريقة `adjustGamma` مخصصة للصور النقطية.  
- **هل يمكنني تحويل PSD إلى TIFF في نفس العملية؟** نعم – بعد تعديل gamma يمكنك حفظ الصورة مباشرةً كـ TIFF باستخدام `TiffOptions`.  
- **هل أحتاج إلى ترخيص للتطوير؟** نسخة تجريبية مجانية تكفي للاختبار؛ يلزم الحصول على ترخيص تجاري للاستخدام في الإنتاج.  
- **ما نسخة Java المدعومة؟** Aspose.PSD تدعم Java 8 وما بعدها.

## ما هي معالجة الصور في Java؟

تشير معالجة الصور في Java إلى تعديل، تحليل، وتحويل البيانات البصرية باستخدام مكتبات Java. تشمل المهام تغيير الحجم، الترشيح، تصحيح الألوان، وتحويل الصيغ—ويمكن أتمتتها في تطبيقات سطح المكتب أو الويب.

## لماذا نستخدم Aspose.PSD لتصحيح gamma؟

توفر Aspose.PSD واجهة برمجة تطبيقات عالية المستوى تُبسط تعقيد صيغة PSD، مما يتيح لك التركيز على تعديل الصورة الفعلي. تتعامل مع التخزين المؤقت، ملفات تعريف الألوان، وتقدم استدعاء `adjustGamma` مباشر، مما يجعلها مثالية لتصحيح gamma للصور و**تحويل PSD إلى TIFF**.

## المتطلبات المسبقة

قبل الغوص في الدرس، تأكد من إعداد المتطلبات التالية:

1. **بيئة تطوير Java** – تأكد من تثبيت بيئة تطوير Java على نظامك.  
2. **مكتبة Aspose.PSD** – قم بتحميل وتكامل مكتبة Aspose.PSD في مشروع Java الخاص بك. يمكنك العثور على الموارد اللازمة في [الوثائق](https://reference.aspose.com/psd/java/).  
3. **صورة نموذجية** – حضّر ملف PSD تجريبي ستستخدمه لتطبيق تعديل gamma.

## استيراد الحزم

لبدء العملية، استورد الحزم المطلوبة في مشروع Java الخاص بك. هذا يهيئ البيئة لاستخدام وظائف Aspose.PSD بسلاسة.

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

## الخطوة 1: تحميل الصورة

ابدأ بتحميل ملف PSD النموذجي إلى كائن من فئة `RasterImage`. هذا هو الأساس لتعديلات gamma اللاحقة.

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// Load an existing image into an instance of RasterImage class
Image image = Image.load(sourceFile);

// Cast object of Image to RasterImage
RasterImage rasterImage = (RasterImage)image;

// Check if RasterImage is cached for better performance
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

## الخطوة 2: تعديل Gamma

الآن، عدّل قيمة gamma للصورة المحمّلة باستخدام طريقة `adjustGamma`. اضبط قيم gamma وفقًا لمتطلباتك.

```java
// Adjust the gamma
rasterImage.adjustGamma(2.2f, 2.2f, 2.2f);
```

## الخطوة 3: إنشاء TiffOptions

أنشئ كائنًا من `TiffOptions` للصورة الناتجة. عيّن الخصائص المختلفة، مثل عدد البتات لكل عينة وخيارات الفوتومتريك، لتخصيص الإخراج وفقًا لمواصفاتك.

```java
// Create an instance of TiffOptions for the resultant image
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
int[] ushort = { 8, 8, 8 };
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);
```

## الخطوة 4: حفظ الصورة الناتجة

احفظ الصورة المعدلة بصيغة TIFF باستخدام `TiffOptions` التي تم تعريفها مسبقًا.

```java
// Save the resultant image to TIFF format
String destName = dataDir + "AdjustGamma_out.tiff";
rasterImage.save(destName, tiffOptions);
```

## المشكلات الشائعة والحلول

| المشكلة | السبب | الحل |
|-------|--------|------|
| **الصورة تبدو باهتة** | قيمة gamma مرتفعة جدًا (مثلاً > 2.5) | خفّض عامل gamma إلى قيمة بين 1.8 و2.2. |
| **`rasterImage.isCached()` يعيد false** | الصورة لم تُحمَّل بعد إلى الذاكرة | استدعِ `rasterImage.cacheData()` قبل تعديل gamma. |
| **حجم ملف TIFF كبير** | تم ضبط البتات لكل عينة إلى 16‑bit | استخدم عينة 8‑bit (`{8,8,8}`) كما هو موضح في المثال. |

## الأسئلة المتكررة

**س: هل يمكنني تطبيق قيم gamma مختلفة لكل قناة لون؟**  
ج: نعم – طريقة `adjustGamma` تقبل قيم float منفصلة للقنوات الحمراء، الخضراء، والزرقاء.

**س: هل يمكن ربط عدة تعديلات صورة قبل الحفظ؟**  
ج: بالتأكيد. يمكنك تنفيذ تغيير الحجم، القص، أو تصحيح الألوان بالتتابع على نفس كائن `RasterImage`.

**س: هل تدعم Aspose.PSD ملفات PSD متعددة الصفحات؟**  
ج: نعم، يمكن الوصول إلى كل طبقة ومعالجتها على حدة.

**س: ما الصيغ التي يمكنني التصدير إليها غير TIFF؟**  
ج: تدعم Aspose.PSD صيغ PNG، JPEG، BMP، والعديد من الصيغ الأخرى عبر فئات الخيارات الخاصة بها.

## الخلاصة

تهانينا! لقد نجحت في تنفيذ **معالجة الصور في Java** عن طريق تعديل gamma لملف PSD وتصديره كصورة TIFF باستخدام Aspose.PSD for Java. تمنحك هذه السلسلة من الخطوات تحكمًا دقيقًا في سطوع وتباين الصورة، مما يجعلها مثالية لسلاسل الرسوم الآلية، خدمات الويب، أو الأدوات المكتبية.

---

**آخر تحديث:** 2025-12-21  
**تم الاختبار مع:** Aspose.PSD 24.11 for Java  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
