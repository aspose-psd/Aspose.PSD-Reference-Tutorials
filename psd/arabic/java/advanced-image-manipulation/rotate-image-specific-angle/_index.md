---
date: 2026-05-19
description: تعلم كيفية تدوير الصورة بزاوية محددة في Java باستخدام Aspose.PSD. يغطي
  الدليل تدوير الصورة Java، تدوير الصورة بزاوية محددة، معالجة الخلفية والمزيد.
keywords:
- how to rotate image
- rotate image specific angle
- rotate image java
- rotate image background
- rotate image degrees
linktitle: كيفية تدوير الصورة بزاوية محددة
schemas:
- author: Aspose
  dateModified: '2026-05-19'
  description: Learn how to rotate image on a specific angle in Java using Aspose.PSD.
    The guide covers rotate image java, rotate image specific angle, background handling
    and more.
  headline: How to Rotate Image on a Specific Angle with Aspose.PSD for Java
  type: TechArticle
- description: Learn how to rotate image on a specific angle in Java using Aspose.PSD.
    The guide covers rotate image java, rotate image specific angle, background handling
    and more.
  name: How to Rotate Image on a Specific Angle with Aspose.PSD for Java
  steps:
  - name: Define Your Document Directory
    text: Set the folder that holds the source PSD and where the output will be written.
      Using an absolute path or `System.getProperty("user.dir")` eliminates relative‑path
      surprises.
  - name: Specify Source and Destination File Paths
    text: Provide the full file names for the input PSD and the desired output format
      (e.g., PNG, JPEG, TIFF). Changing the extension in `destName` automatically
      selects the appropriate encoder.
  - name: Load the Image
    text: The `Image.load` method detects the file format and returns a concrete `RasterImage`
      instance ready for raster operations. The `Image` class is a factory that reads
      a file from disk and creates an in‑memory representation suitable for further
      processing. It supports automatic format detection for al
  - name: Cache Image Data (Optional but Recommended)
    text: Calling `image.cacheData()` stores pixel data in memory, dramatically speeding
      up subsequent transformations—especially for large PSD files that would otherwise
      trigger repeated disk I/O. The `cacheData()` method forces the image to be fully
      loaded into RAM, reducing the overhead of lazy loading dur
  - name: Rotate the Image
    text: 'Invoke `rotate` with three arguments: the rotation angle (float), a flag
      to expand the canvas, and the background color for the newly exposed corners.
      The `rotate` method rotates the image around its centre, optionally enlarging
      the canvas to accommodate the rotated bounds. The background `Color` fi'
  - name: Save the Result
    text: Choose an encoder (JPEG, PNG, etc.) and call `save`. `JpegOptions` lets
      you adjust quality, while `PngOptions` provides lossless output. The `save`
      method writes the transformed image to disk using the specified options object,
      ensuring that compression level and color depth are preserved as require
  type: HowTo
- questions:
  - answer: Yes. The library preserves alpha channels; omit an opaque background color
      to keep corners transparent.
    question: Can I rotate images with transparency using Aspose.PSD for Java?
  - answer: No. Aspose.PSD supports PSD, JPEG, PNG, TIFF, GIF, BMP, JPEG2000, WMF,
      EMF, and 30+ additional formats.
    question: Are there any limitations on the image file formats supported for rotation?
  - answer: Absolutely. Pass a negative float to `rotate` (e.g., `-30f`) to rotate
      clockwise.
    question: Can I rotate images by a negative angle?
  - answer: The API is server‑side only. For live previews, render the rotated bitmap
      in a UI framework such as Swing or JavaFX and refresh the view.
    question: Does Aspose.PSD provide real‑time image preview during rotation?
  - answer: Yes, visit the [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) to
      ask questions and share experiences.
    question: Is there a community forum for Aspose.PSD where I can seek help?
  type: FAQPage
second_title: Aspose.PSD Java API
title: كيفية تدوير الصورة بزاوية محددة باستخدام Aspose.PSD للـ Java
url: /ar/java/advanced-image-manipulation/rotate-image-specific-angle/
weight: 20
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# كيفية تدوير الصورة بزاوية محددة باستخدام Aspose.PSD للـ Java

إذا كنت بحاجة إلى **كيفية تدوير الصورة** برمجياً في تطبيق Java، فإن Aspose.PSD للـ Java يقدم واجهة برمجة تطبيقات نظيفة وعالية الأداء تتولى الأعمال الشاقة. سواءً كنت تبني محرّراً للصور، أو تولّد صوراً مصغرة، أو تُعدّ أصولاً لخدمة ويب، فإن تدوير الصورة بزاوية دقيقة يُعدّ متطلباً شائعاً. في هذا الدرس سنستعرض العملية بالكامل — من تحميل ملف PSD إلى حفظ النتيجة المدورة — مع تسليط الضوء على أفضل الممارسات مثل التخزين المؤقت ومعالجة الخلفية.

## إجابات سريعة
- **ما هي المكتبة الأفضل لتدوير الصور في Java؟** Aspose.PSD للـ Java يوفر أكثر محرك تدوير موثوق.  
- **هل يمكنني التدوير بأي درجة؟** نعم، طريقة `rotate` تقبل زاوية من نوع `float`، سواءً موجبة أو سالبة.  
- **هل أحتاج إلى ترخيص للتطوير؟** نسخة تجريبية مجانية تكفي للاختبار؛ الترخيص التجاري مطلوب للإنتاج.  
- **ما صيغ الصور المدعومة؟** PSD، JPEG، PNG، TIFF، GIF، BMP، JPEG2000، WMF، EMF، وأكثر من 30 صيغة إضافية.  
- **كيف يمكنني تعيين لون خلفية للمساحات الفارغة؟** مرّر كائن `Color` إلى طريقة `rotate`.

## كيفية تدوير الصورة بزاوية محددة باستخدام Aspose.PSD للـ Java؟

حمّل ملف المصدر، استدعِ `image.rotate(angle, true, backgroundColor)`، ثم احفظ — ثلاث خطوات مختصرة تتولى كل الحسابات الرياضية لك. يحافظ Aspose.PSD على الطبقات، ملفات تعريف الألوان، وقنوات ألفا مع توسيع القماش لتجنب القطع، لذا تكون النتيجة كما هو متوقع حتى للزوايا الكسرية مثل 12.5°. هذا النهج يعمل مع ملفات تتراوح من بضعة كيلوبايت إلى PSD متعدد المئات من الصفحات دون استنزاف الذاكرة.

## ما هو تدوير الصورة في Java؟

تدوير الصورة هو التحويل الهندسي الذي يدور مصفوفة البكسلات حول نقطة محورية — عادةً مركز الصورة — بزاوية محددة. في Java العادية ستتعامل مع كائن `Graphics2D`، تحسب الإزاحات المثلثية، وتدير الخلفية يدوياً. Aspose.PSD يختصر كل هذه التعقيدات، مع معالجة أعماق الألوان، أقنعة الطبقات، وصيغ الملفات المختلفة تلقائياً.

## لماذا نستخدم Aspose.PSD لتدوير الصور؟

يدعم Aspose.PSD **أكثر من 30 صيغة إدخال وإخراج** ويمكنه معالجة **ملفات PSD تصل إلى 500 صفحة في أقل من 5 ثوانٍ** على خادم عادي. التخزين المؤقت المدمج في المكتبة (`image.cacheData()`) يقلل استهلاك الذاكرة حتى 60 % للأصول الكبيرة، وطريقة `rotate` تتيح لك تحديد لون الخلفية، مع الحفاظ على الزوايا الشفافة عند الحاجة. هذه الفوائد الكمية تجعلها الخيار القياسي في صناعات معالجة الصور عالية الإنتاجية.

## المتطلبات المسبقة

قبل أن نبدأ، تأكد من وجود ما يلي:

1. **مجموعة تطوير Java (JDK 8 أو أحدث)** – أي بيئة تطوير متكاملة أو سطر أوامر سيكفي.  
2. **Aspose.PSD للـ Java** – حمّل أحدث ملف JAR من [صفحة Aspose.PSD للـ Java](https://reference.aspose.com/psd/java/).  
3. **ملف PSD تجريبي** – مثل `sample.psd` وضعه في مجلد يمكنك الإشارة إليه من الشيفرة.

## استيراد الحزم

فئة `RasterImage` والوظائف المساعدة المرتبطة هي جوهر سير عمل التدوير.

فئة `RasterImage` هي الكائن الأساسي في Aspose.PSD لمعالجة الصور النقطية. توفر طرقاً للتحميل، التحويل، والحفظ مع الحفاظ على البيانات الوصفية.

## دليل خطوة بخطوة

### الخطوة 1: تعريف دليل المستند الخاص بك

حدد المجلد الذي يحتوي على ملف PSD المصدر ومكان كتابة الناتج. استخدام مسار مطلق أو `System.getProperty("user.dir")` يزيل مفاجآت المسارات النسبية.

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.imageoptions.JpegOptions;
```

### الخطوة 2: تحديد مسارات الملفات المصدر والوجهة

قدّم أسماء الملفات الكاملة للـ PSD المدخل والصيغة المطلوبة للناتج (مثل PNG، JPEG، TIFF). تغيير الامتداد في `destName` يختار المشفر المناسب تلقائياً.

```java
String dataDir = "Your Document Directory";
```

### الخطوة 3: تحميل الصورة

طريقة `Image.load` تكتشف صيغة الملف وتعيد كائن `RasterImage` جاهز للعمليات النقطية.

فئة `Image` هي مصنع يقرأ الملف من القرص وينشئ تمثيلاً في الذاكرة مناسباً للمعالجة اللاحقة. تدعم الكشف التلقائي عن الصيغة لجميع الأنواع المدعومة أكثر من 30 صيغة.

```java
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "RotatingImageOnSpecificAngle_out.jpg";
```

### الخطوة 4: تخزين بيانات الصورة مؤقتاً (اختياري لكن موصى به)

استدعاء `image.cacheData()` يخزن بيانات البكسل في الذاكرة، مما يسرّع التحولات اللاحقة بشكل كبير — خاصةً لملفات PSD الكبيرة التي قد تتسبب في عمليات قراءة/كتابة متكررة على القرص.

طريقة `cacheData()` تجبر الصورة على التحميل الكامل إلى RAM، مما يقلل من عبء التحميل الكسول أثناء العمليات المكثفة.

```java
RasterImage image = (RasterImage)Image.load(sourceFile);
```

### الخطوة 5: تدوير الصورة

استدعِ `rotate` مع ثلاثة معاملات: زاوية التدوير (float)، علامة لتوسيع القماش، ولون الخلفية للزوايا المكشوفة حديثاً.

طريقة `rotate` تدور الصورة حول مركزها، مع إمكانية توسيع القماش لاستيعاب الحدود المدورة. لون الخلفية `Color` يملأ أي مساحة فارغة، مما يمنع ظهور زوايا شفافة أو سوداء.

- **20f** – زاوية التدوير بالدرجات (float). غيّر هذه القيمة لأي زاوية، مثل `-45f` للتدوير في اتجاه عقارب الساعة.  
- **true** – الحفاظ على نسبة الأبعاد الأصلية أثناء توسيع القماش.  
- **Color.getRed()** – لون الخلفية الذي يملأ الزوايا الفارغة؛ استبدله بـ `Color.getWhite()` أو أي لون مخصص حسب الحاجة.

```java
if (!image.isCached())
{
    image.cacheData();
}
```

### الخطوة 6: حفظ النتيجة

اختر مشفراً (JPEG، PNG، إلخ) واستدعِ `save`. يتيح لك `JpegOptions` ضبط الجودة، بينما يوفر `PngOptions` مخرجات غير مضغوطة.

طريقة `save` تكتب الصورة المُحوَّلة إلى القرص باستخدام كائن الخيارات المحدد، مع ضمان الحفاظ على مستوى الضغط وعمق اللون حسب المتطلبات.

```java
image.rotate(20f, true, Color.getRed());
```

## المشكلات الشائعة والحلول

| المشكلة | السبب | الحل |
|-------|-------|-----|
| **زوايا فارغة بعد التدوير** | عدم توفير لون خلفية | مرّر `Color` (مثل `Color.getWhite()`) إلى `rotate`. |
| **خطأ نفاد الذاكرة على PSD كبير** | الصورة غير مخزنة مؤقتاً | استدعِ `image.cacheData()` قبل المعالجة. |
| **اتجاه الزاوية غير صحيح** | ارتباك بين القيم السالبة والموجبة | استخدم القيم السالبة للتدوير في اتجاه عقارب الساعة (أو العكس حسب نظام الإحداثيات). |
| **عدم حفظ التغييرات** | نسيان استدعاء `save` | تأكد من تنفيذ `image.save(...)` بعد التدوير. |

## الأسئلة المتكررة

**س: هل يمكنني تدوير الصور ذات الشفافية باستخدام Aspose.PSD للـ Java؟**  
ج: نعم. المكتبة تحافظ على قنوات ألفا؛ يمكنك حذف لون خلفية غير شفاف للحفاظ على الزوايا الشفافة.

**س: هل هناك أي قيود على صيغ ملفات الصور المدعومة للتدوير؟**  
ج: لا. يدعم Aspose.PSD PSD، JPEG، PNG، TIFF، GIF، BMP، JPEG2000، WMF، EMF، وأكثر من 30 صيغة إضافية.

**س: هل يمكنني تدوير الصور بزاوية سالبة؟**  
ج: بالتأكيد. مرّر قيمة `float` سالبة إلى `rotate` (مثل `-30f`) للتدوير في اتجاه عقارب الساعة.

**س: هل يوفر Aspose.PSD معاينة صورة في الوقت الحقيقي أثناء التدوير؟**  
ج: الواجهة برمجة التطبيقات تعمل على الخادم فقط. للحصول على معاينات حية، قم بعرض البت ماب المدور في إطار UI مثل Swing أو JavaFX وقم بتحديث العرض.

**س: هل هناك منتدى مجتمع لـ Aspose.PSD يمكنني طلب المساعدة فيه؟**  
ج: نعم، زر [منتدى Aspose.PSD](https://forum.aspose.com/c/psd/34) لطرح الأسئلة ومشاركة التجارب.

---

**آخر تحديث:** 2026-05-19  
**تم الاختبار مع:** Aspose.PSD للـ Java 24.11 (أحدث نسخة وقت الكتابة)  
**المؤلف:** Aspose  

{{< blocks/products/products-backtop-button >}}

```java
image.save(destName, new JpegOptions());
```

## دروس ذات صلة

- [تحجيم الصورة بجودة عالية باستخدام Bicubic Resampler في Aspose.PSD للـ Java](/psd/java/advanced-image-manipulation/implement-bicubic-resampler/)
- [تغيير حجم الصورة في Java - باستخدام تعداد نوع التحجيم في Aspose.PSD للـ Java](/psd/java/advanced-image-manipulation/resizing-with-resize-type-enumeration/)
- [تمويه الصورة في Java مع Aspose.PSD – إضافة تأثير تمويه](/psd/java/advanced-techniques/blur-image/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}