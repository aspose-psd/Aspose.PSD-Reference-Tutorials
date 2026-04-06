---
date: 2026-01-07
description: تعلّم خطوة بخطوة تقنيات الفلترة لتطبيق مرشحات المتوسط وواينر باستخدام
  Aspose.PSD للغة Java، وحوّل ملفات PSD إلى GIF بكفاءة.
linktitle: Apply Median and Wiener Filters
second_title: Aspose.PSD Java API
title: 'تصفية خطوة بخطوة - تطبيق مرشحات المتوسط وواينر (جافا)'
url: /ar/java/image-processing/apply-median-wiener-filters/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# مرشح خطوة بخطوة: تطبيق مرشحات Median & Wiener (Java)

## مقدمة

إذا كنت تبحث عن سير عمل **step by step filter** لتنظيف الصور المشوشة في Java، فقد وجدت المكان المناسب. تجعل Aspose.PSD for Java من السهل تطبيق كل من مرشحات Median وWiener، وتتيح لك أيضًا **convert PSD to GIF** بعد المعالجة. في هذا الدرس سنستعرض كل ما تحتاجه — من إعداد المكتبة إلى حفظ النتيجة المفلترة — حتى تتمكن من دمج إزالة الضوضاء عالية الجودة في تطبيقاتك بثقة.

## إجابات سريعة
- **What does the Median filter do?** يقلل من ضوضاء الملح والفلفل مع الحفاظ على الحواف.  
- **When should I use the Wiener filter?** لتقليل الضوضاء التكيفية التي تأخذ في الاعتبار تباين الصورة المحلي.  
- **Do I need a license to run the code?** النسخة التجريبية المجانية تكفي للتطوير؛ تحتاج إلى ترخيص تجاري للإنتاج.  
- **Can I save the output as GIF?** نعم — تتيح لك Aspose.PSD **convert PSD to GIF** في خطوة واحدة.  
- **How long does the implementation take?** عادةً أقل من 10 دقائق للإعداد الأساسي.

## ما هو مرشح خطوة بخطوة؟

نهج *step by step filter* يقسم معالجة الصورة إلى مراحل واضحة وقابلة للإدارة — تحميل الصورة، تكوين خيارات الفلتر، تطبيق الفلتر، وأخيرًا حفظ النتيجة. يساعدك هذا التدفق المنهجي على تصحيح كل جزء، وإعادة استخدام الكود، وتكييف العملية مع صيغ صور مختلفة.

## لماذا تستخدم Aspose.PSD for Java؟

- **Broad format support** – يدعم صيغ PSD، PNG، JPEG، GIF، وغيرها.  
- **No external dependencies** – جافا نقي، سهل الإدماج في أي مشروع.  
- **Built‑in filter options** – مرشحات Median، Wiener، وغيرها من المرشحات المتقدمة جاهزة للاستخدام.  
- **One‑click conversion** – تصدير مباشرة إلى GIF أو PNG أو JPEG بعد المعالجة.

## المتطلبات المسبقة

قبل البدء، تأكد من أن لديك:

1. **Aspose.PSD for Java Library** – قم بتنزيل وتثبيت المكتبة من [here](https://releases.aspose.com/psd/java/).  
2. **Java Development Environment** – JDK 8+ وبيئة تطوير (IDE) أو أداة بناء (Maven/Gradle) مُعدة على جهازك.

## استيراد الحزم

ابدأ باستيراد الفئات الضرورية التي تمنحك الوصول إلى معالجة الصور وخيارات الفلتر.

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.imagefilters.filteroptions.MedianFilterOptions;
import com.aspose.psd.imageoptions.GifOptions;
```

## مرشح خطوة بخطوة: كيفية تطبيق مرشح Median

### الخطوة 1: تحميل الصورة

أولاً، وجه الـ API إلى ملف PSD الذي تريد تنظيفه.

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// Load the source image
Image image = Image.load(sourceFile);
```

### الخطوة 2: تحويل Image إلى RasterImage

يعمل الفلتر على بيانات الراستر، لذا نقوم بتحويل الـ `Image` العامة إلى `RasterImage`.

```java
// Cast the image into RasterImage
RasterImage rasterImage = (RasterImage)image;
if (rasterImage == null) {
    return;
}
```

### الخطوة 3: إنشاء كائن MedianFilterOptions

قم بتكوين حجم نواة الـ median. حجم **4** يعمل جيدًا للضوضاء المتوسطة.

```java
// Create an instance of MedianFilterOptions class and set the filter size
MedianFilterOptions options = new MedianFilterOptions(4);
```

### الخطوة 4: تطبيق مرشح Median

الآن قم بتطبيق الفلتر على كامل حدود الصورة.

```java
// Apply MedianFilterOptions filter to RasterImage object
rasterImage.filter(image.getBounds(), options);
```

### الخطوة 5: حفظ الصورة الناتجة (Convert PSD to GIF)

بعد الفلترة، سنحفظ الناتج كملف GIF — لتوضيح قدرة **convert PSD to GIF**.

```java
String destName = dataDir + "median_test_denoise_out.gif";
// Save the resultant image as a GIF
image.save(destName, new GifOptions());
```

باتباع هذه الخطوات، قمت بتطبيق مرشح Median بنجاح وتصدير الصورة المنقاة كملف GIF.

## تطبيق مرشح Wiener (امتداد اختياري)

إذا كان مشروعك يتطلب تقليل الضوضاء التكيفية، يمكنك استبدال مرشح Median بمرشح Wiener. هيكل الكود هو نفسه؛ كل ما عليك هو استيراد `WienerFilterOptions` وإنشاء كائن به باستخدام نصف القطر المطلوب.

> **Pro tip:** جرب أحجام نوى مختلفة لكلا المرشحين للعثور على التوازن المثالي بين إزالة الضوضاء والحفاظ على التفاصيل.

## المشكلات الشائعة & استكشاف الأخطاء

| العَرَض | السبب المحتمل | الحل |
|---------|---------------|-----|
| `ClassCastException` عند التحويل إلى `RasterImage` | ملف الإدخال ليس PSD متوافقًا مع الراستر | تحقق من أن PSD يحتوي على طبقات راستر أو حوّل الطبقات إلى راستر أولاً |
| ملف GIF الناتج فارغ | مسار الوجهة غير صحيح أو المجلد يفتقر إلى صلاحية الكتابة | تأكد من أن `dataDir` يشير إلى دليل موجود قابل للكتابة |
| يبدو أن الفلتر لا يؤثر | حجم النواة صغير جدًا بالنسبة لمستوى الضوضاء | زد حجم النواة (مثال: `new MedianFilterOptions(6)`) |

## الأسئلة المتكررة

**س1: هل يمكنني تطبيق هذه المرشحات على صور بأي صيغة؟**  
ج1: نعم، يدعم Aspose.PSD مجموعة واسعة من صيغ الصور، مما يجعله مرنًا لمختلف المشاريع.

**س2: هل هناك نسخة تجريبية مجانية متاحة لـ Aspose.PSD for Java؟**  
ج2: نعم، يمكنك الحصول على نسخة تجريبية مجانية [here](https://releases.aspose.com/).

**س3: كيف أحصل على الدعم لـ Aspose.PSD for Java؟**  
ج3: زر [منتدى Aspose.PSD](https://forum.aspose.com/c/psd/34) للحصول على دعم المجتمع.

**س4: أين يمكنني العثور على الوثائق الخاصة بـ Aspose.PSD for Java؟**  
ج4: راجع الوثائق [here](https://reference.aspose.com/psd/java/).

**س5: كيف يمكنني شراء Aspose.PSD for Java؟**  
ج5: يمكنك شراء المنتج [here](https://purchase.aspose.com/buy).

## الخلاصة

في هذا الدليل، عرضنا عملية **step by step filter** لتطبيق مرشحات Median (وباختياري Wiener) باستخدام Aspose.PSD for Java، وأظهرنا كيفية **convert PSD to GIF** بعد إزالة الضوضاء. باستخدام هذه اللبنات الأساسية يمكنك دمج خطوط معالجة صور قوية في أي تطبيق Java — سواء كنت تنظف الصور، أو تُعد الأصول للويب، أو تُ automatisation تحويلات دفعة.

---

**آخر تحديث:** 2026-01-07  
**تم الاختبار مع:** Aspose.PSD for Java 24.12 (latest at time of writing)  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}