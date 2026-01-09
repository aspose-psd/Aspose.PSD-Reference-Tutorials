---
date: 2026-01-09
description: تعلم كيفية تنفيذ تقسيم الصورة باستخدام طريقة أوتسو باستخدام Aspose.PSD
  للغة Java. يغطي هذا الدرس معالجة الصور بلغة Java، وكيفية تحويل الصورة إلى ثنائية،
  وتطبيق عتبة أوتسو.
linktitle: Binarization with Otsu Threshold
second_title: Aspose.PSD Java API
title: تقسيم الصورة بأوتسو – تحويل إلى ثنائي باستخدام عتبة أوتسو في Aspose.PSD للـ
  Java
url: /ar/java/image-processing/binarization-otsu-threshold/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# التحويل إلى ثنائي باستخدام عتبة أوتسو في Aspose.PSD للـ Java

## المقدمة

مرحبًا! في هذا الدليل خطوة بخطوة ستتعلم **image segmentation otsu** باستخدام مكتبة Aspose.PSD للـ Java. سواءً كنت تبني أداة تحرير صور، أو خط أنابيب تحليل مستندات آلي، أو أي مشروع **java image processing**، فإن إتقان طريقة تحويل الصور إلى ثنائية باستخدام عتبة أوتسو سيمنحك طريقة موثوقة لإنشاء **binary image conversion** نظيفة. دعنا نستعرض العملية بالكامل—من إعداد البيئة إلى حفظ ملف JPEG النهائي—حتى تتمكن من تطبيق أوتسو في تطبيقاتك الخاصة.

## إجابات سريعة
- **ماذا تفعل عتبة أوتسو؟** تقوم تلقائيًا بإيجاد قيمة القطع المثالية للمستوى الرمادي التي تفصل بين بكسلات المقدمة والخلفية.  
- **أي مكتبة تدعمها في Java؟** توفر Aspose.PSD للـ Java طريقة مدمجة `binarizeOtsu()`.  
- **هل أحتاج إلى ترخيص لتجربتها؟** تتوفر نسخة تجريبية مجانية؛ يلزم وجود ترخيص للاستخدام في الإنتاج.  
- **ما صيغ الإخراج التي يمكنني استخدامها؟** المثال يحفظ بصيغة JPEG، لكن أي صيغة يدعمها `RasterCachedImage.save()` تعمل.  
- **كم من الوقت تستغرق عملية التنفيذ؟** مع الـ API الجاهز، يمكنك الحصول على حل يعمل في أقل من 10 دقائق.

## ما هو Image Segmentation Otsu؟

**Image segmentation otsu** هي تقنية إحصائية تحدد قيمة عتبة مثالية لتحويل صورة رمادية إلى صورة ثنائية. تقوم الطريقة بتقييم التباين داخل الفئات (المقدمة والخلفية) وتختار العتبة التي تقلل هذا التباين، مما ينتج فصلًا واضحًا بين الكائنات والخلفية.

## لماذا نستخدم Aspose.PSD للـ Java؟

- **تخزين مؤقت عالي الأداء** – يعمل بكفاءة مع ملفات PSD الكبيرة.  
- **تحويل إلى ثنائي بسطر واحد** – `binarizeOtsu()` يتولى الجزء الثقيل.  
- **دعم صيغ متعدد** – تحميل PSD، المعالجة، والحفظ كـ JPEG، PNG، إلخ.  
- **ترخيص جاهز للمؤسسات** – مناسب للتطبيقات التجارية.

## المتطلبات المسبقة

قبل أن نغوص في الكود، تأكد من توفر ما يلي:

- **بيئة تطوير Java** – JDK 8 أو أعلى مثبتة.  
- **مكتبة Aspose.PSD للـ Java** – حمّلها من الموقع الرسمي [هنا](https://releases.aspose.com/psd/java/).  
- **ملف PSD تجريبي** – PSD تريد تحويله إلى ثنائي (مثلاً `sample.psd`).  

## استيراد الحزم

ابدأ باستيراد الفئات اللازمة:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterCachedImage;

import com.aspose.psd.imageoptions.JpegOptions;
```

## الخطوة 1: إعداد دليل المستندات

عرّف المجلد الذي يحتوي على ملف PSD المصدر ومكان كتابة الناتج:

```java
String dataDir = "Your Document Directory";
```

## الخطوة 2: تحميل ملف PSD

حمّل الـ PSD في كائن `Image` لتتمكن من العمل معه:

```java
String sourceFile = dataDir + "sample.psd";
Image image = Image.load(sourceFile);
```

## الخطوة 3: تخزين الصورة مؤقتًا

إذا لم تكن الصورة مخزنة مؤقتًا بالفعل، قم بتخزينها لتحسين سرعة المعالجة:

```java
RasterCachedImage rasterCachedImage = (RasterCachedImage)image;

if (!rasterCachedImage.isCached()) {
    rasterCachedImage.cacheData();
}
```

## الخطوة 4: تحويل الصورة إلى ثنائي باستخدام عتبة أوتسو

طبق خوارزمية أوتسو—هذا هو جوهر **how to apply otsu** لتحويل **binary image conversion**:

```java
rasterCachedImage.binarizeOtsu();
```

## الخطوة 5: حفظ الصورة الناتجة

أخيرًا، اكتب الصورة المحوّلة إلى ثنائي على القرص باستخدام `JpegOptions` (يمكنك أيضًا استخدام PNG أو BMP):

```java
String destName = dataDir + "BinarizationWithOtsuThreshold_out.jpg";
rasterCachedImage.save(destName, new JpegOptions());
```

## المشكلات الشائعة والحلول

| المشكلة | السبب | الحل |
|-------|--------|-----|
| **`ClassCastException`** | محاولة تحويل صورة غير raster | تأكد من أن الـ PSD يحتوي على طبقات raster أو استخدم `image.convertToRasterImage()` قبل التحويل. |
| **نفاد الذاكرة** | ملفات PSD الكبيرة تستهلك الكثير من RAM | استدعِ `rasterCachedImage.cacheData()` مبكرًا وفكّر في زيادة حجم heap للـ JVM (`-Xmx`). |
| **ألوان الإخراج غير صحيحة** | لم يتم تخزين الصورة مؤقتًا بشكل صحيح | تحقق من أن `isCached()` أعاد `true` قبل استدعاء `binarizeOtsu()`. |

## الأسئلة المتكررة

### س1: ما هو التحويل إلى ثنائي باستخدام عتبة أوتسو؟

ج1: التحويل إلى ثنائي باستخدام عتبة أوتسو هو طريقة تُستخدم لتقسيم الصورة إلى مقدمة وخلفية بناءً على عتبة مثالية.

### س2: هل يمكنني استخدام Aspose.PSD للـ Java مجانًا؟

ج2: Aspose.PSD للـ Java مكتبة تجارية، لكن يمكنك استكشاف ميزاتها عبر نسخة تجريبية مجانية. احصل عليها [هنا](https://releases.aspose.com/).

### س3: أين يمكنني العثور على توثيق Aspose.PSD للـ Java؟

ج3: التوثيق متوفر [هنا](https://reference.aspose.com/psd/java/).

### س4: كيف أحصل على دعم Aspose.PSD للـ Java؟

ج4: زر منتدى Aspose.PSD [هنا](https://forum.aspose.com/c/psd/34) للحصول على دعم المجتمع.

### س5: هل هناك ترخيص مؤقت متاح لـ Aspose.PSD للـ Java؟

ج5: نعم، يمكنك الحصول على ترخيص مؤقت [هنا](https://purchase.aspose.com/temporary-license/).

**أسئلة وإجابات إضافية**

**س: كيف يتناسب هذا الأسلوب مع سير عمل أكبر لمعالجة الصور في Java؟**  
ج: بعد التحويل إلى ثنائي، يمكنك تمرير الصورة الثنائية إلى وحدات اكتشاف الحواف، أو إعداد ما قبل OCR، أو تحليل الأشكال.

**س: هل يمكنني تعديل معلمات خوارزمية أوتسو؟**  
ج: طريقة `binarizeOtsu()` تستخدم تنفيذ أوتسو القياسي؛ إذا أردت عتبة مخصصة، استخدم `binarize(int threshold)` بدلاً منها.

## الخاتمة

لقد رأيت الآن كيفية تنفيذ **image segmentation otsu** باستخدام Aspose.PSD للـ Java. باتباع هذه الخطوات—إعداد البيئة، تحميل وتخزين الـ PSD مؤقتًا، تطبيق `binarizeOtsu()`، وحفظ النتيجة—يمكنك دمج تحويل الصور إلى ثنائي قوي في أي مشروع **java image processing**. جرّب ملفات مصدر مختلفة، اجمع الناتج مع OCR، أو أنشئ معالج دفعي يتعامل مع عدة ملفات PSD تلقائيًا.

---

**آخر تحديث:** 2026-01-09  
**تم الاختبار مع:** Aspose.PSD للـ Java 24.11 (أحدث نسخة وقت الكتابة)  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}