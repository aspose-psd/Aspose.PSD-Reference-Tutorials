---
date: 2026-02-27
description: تعلم كيفية تعديل جاما في معالجة الصور بجافا باستخدام Aspose.PSD، وتحويل
  PSD إلى TIFF، وإصلاح الصور الباهتة في دليل مختصر.
linktitle: Adjust Gamma of an Image
second_title: Aspose.PSD Java API
title: كيفية تعديل جاما في معالجة الصور بجافا باستخدام Aspose.PSD
url: /ar/java/advanced-techniques/adjust-gamma/
weight: 23
---

ا باستخدام Aspose.PSD". Keep same heading level.

Proceed.

I'll produce final content.{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# كيفية تعديل جاما في معالجة الصور بجافا باستخدام Aspose.PSD

## المقدمة

إذا كنت تعمل على **معالجة صور جافا**، فإن تعلم **كيفية تعديل جاما** يُعد تقنية أساسية لتحسين السطوع والتباين دون فقدان التفاصيل. في هذا الدرس سنستعرض كيفية استخدام **Aspose.PSD for Java** لتطبيق تصحيح الجاما على ملف PSD، **تحويل PSD إلى TIFF**، وتجنب **الصورة الباهتة**. ستتعرف على سبب كون هذا النهج سريعًا، موثوقًا، ومثاليًا لسلاسل معالجة الصور على الخادم.

## إجابات سريعة
- **ماذا يفعل تصحيح الجاما؟** يعيد رسم قيم الإضاءة لجعل المناطق الداكنة أكثر إشراقًا أو المناطق الفاتحة أكثر ظلامًا مع الحفاظ على التفاصيل العامة.  
- **أي مكتبة تتولى المعالجة؟** توفر Aspose.PSD for Java طريقة `adjustGamma` مخصصة للصور النقطية.  
- **هل يمكنني تحويل PSD إلى TIFF في نفس التدفق؟** نعم – بعد تعديل الجاما يمكنك حفظ الصورة مباشرةً بصيغة TIFF باستخدام `TiffOptions`.  
- **هل أحتاج إلى ترخيص للتطوير؟** نسخة تجريبية مجانية تكفي للاختبار؛ الترخيص التجاري مطلوب للاستخدام في الإنتاج.  
- **ما نسخة جافا المدعومة؟** تدعم Aspose.PSD جافا 8 وما بعدها.

## كيفية تعديل جاما في معالجة الصور بجافا
تعديل الجاما هو جزء أساسي من أي **درس معالجة صور جافا** يتعامل مع السطوع أو التباين. أدناه نقسم الخطوات، نشرح لماذا كل سطر مهم، ونظهر لك كيفية دمج العملية في قاعدة الشيفرة الحالية.

## ما هو تصحيح جاما في جافا؟
تصحيح الجاما يغيّر العلاقة غير الخطية بين قيم البكسل المشفرة والسطوع المعروض. من خلال تعديل منحنى الجاما يمكنك **إصلاح مشاكل الصورة الباهتة** أو تعزيز التفاصيل في الظلال دون زيادة إضاءة الإبرازات.

## لماذا نستخدم Aspose.PSD لتصحيح الجاما؟
تعمل Aspose.PSD كمكتبة **معالجة صور جافا** قوية تُبسط تعقيدات تنسيق PSD. فهي تتعامل مع ملفات تعريف الألوان، التخزين المؤقت، وتوفر استدعاء بسيط `adjustGamma`، مما يجعلها مثالية لتصحيح **جاما جافا** و**تحويل PSD إلى TIFF**.

## المتطلبات المسبقة

1. **بيئة تطوير جافا** – تثبيت جافا 8 أو أحدث.  
2. **مكتبة Aspose.PSD** – قم بتحميل الـ JAR وأضفه إلى مشروعك. راجع [التوثيق الرسمي](https://reference.aspose.com/psd/java/).  
3. **صورة تجريبية** – ملف PSD تريد معالجته (مثال: `sample.psd`).  

## استيراد الحزم

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

## الخطوة 1: تحميل الصورة

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

**نصيحة احترافية:** التخزين المؤقت لبيانات النقطية مرة واحدة يقلل من استهلاك الذاكرة عند تطبيق تعديلات متعددة متتالية.

## الخطوة 2: تعديل جاما

```java
// Adjust the gamma
rasterImage.adjustGamma(2.2f, 2.2f, 2.2f);
```

يمكنك تمرير قيم مختلفة للقنوات الحمراء، الخضراء، والزرقاء إذا كنت بحاجة إلى تعديل خاص لكل قناة.

## الخطوة 3: إنشاء TiffOptions

```java
// Create an instance of TiffOptions for the resultant image
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
int[] ushort = { 8, 8, 8 };
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);
```

تحديد عينة 8‑بت (`{8,8,8}`) يحافظ على حجم ملف TIFF معقولًا مع الحفاظ على دقة الألوان.

## الخطوة 4: حفظ الصورة الناتجة

```java
// Save the resultant image to TIFF format
String destName = dataDir + "AdjustGamma_out.tiff";
rasterImage.save(destName, tiffOptions);
```

بعد الحفظ، يمكنك تمرير ملف TIFF إلى الأنظمة اللاحقة مثل خدمات الطباعة أو واجهات برمجة التطبيقات على الويب.

## حالات الاستخدام الشائعة

- **خطوط أنابيب الرسومات الآلية** – تعديل جاما في الوقت الفعلي قبل إنشاء الصور المصغرة.  
- **أدوات التحويل الجماعي** – تحويل أرشيفات PSD الكبيرة إلى TIFF مع توحيد السطوع.  
- **الخدمات السحابية** – توفير نقطة نهاية تستقبل PSD، تطبق تصحيح جاما، وتعيد TIFF للعميل.

## المشكلات الشائعة والحلول

| المشكلة | السبب | الحل |
|-------|--------|------|
| **الصورة تظهر باهتة** | قيمة الجاما مرتفعة جدًا (مثلاً > 2.5) | خفّض عامل الجاما إلى قيمة بين 1.8 و2.2. |
| **`rasterImage.isCached()` يُعيد false** | الصورة لم تُحمَّل بعد إلى الذاكرة | استدعِ `rasterImage.cacheData()` قبل تعديل الجاما. |
| **حجم ملف TIFF كبير** | تم ضبط البتات لكل عينة إلى 16‑بت | استخدم عينة 8‑بت (`{8,8,8}`) كما هو موضح في المثال. |

## الأسئلة المتكررة

**س: هل يمكنني تطبيق قيم جاما مختلفة لكل قناة لون؟**  
ج: نعم – طريقة `adjustGamma` تقبل قيم float منفصلة للقنوات الحمراء، الخضراء، والزرقاء.

**س: هل يمكن ربط تعديلات صور متعددة قبل الحفظ؟**  
ج: بالتأكيد. يمكنك تنفيذ تغيير الحجم، القص، أو تصحيحات الألوان بالتسلسل على نفس كائن `RasterImage`.

**س: هل تدعم Aspose.PSD ملفات PSD متعددة الصفحات؟**  
ج: نعم، يمكن الوصول إلى كل طبقة ومعالجتها على حدة.

**س: ما الصيغ التي يمكنني التصدير إليها غير TIFF؟**  
ج: تدعم Aspose.PSD PNG، JPEG، BMP، والعديد من الصيغ الأخرى عبر فئات الخيارات الخاصة بها.

**س: كيف أتجنب الصورة الباهتة بعد تصحيح الجاما؟**  
ج: ابدأ بقيمة جاما معتدلة (حوالي 2.0) واعرض النتيجة؛ قلّل القيمة إذا بدت الصورة ساطعة جدًا.

## الخاتمة

تهانينا! لقد تعلمت بنجاح **كيفية تعديل جاما** في **سياق معالجة صور جافا**، وحولت ملف PSD إلى TIFF، وتجنبت المشكلات الشائعة مثل **الصورة الباهتة**. يمنحك هذا النمط تحكمًا دقيقًا في السطوع والتباين، مما يجعله مثاليًا لخطوط أنابيب الرسومات الآلية، الخدمات السحابية، أو الأدوات المكتبية.

---

**آخر تحديث:** 2026-02-27  
**تم الاختبار مع:** Aspose.PSD 24.11 for Java  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}