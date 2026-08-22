---
date: 2026-07-17
description: دروس معالجة الصور بجافا باستخدام Aspose.PSD تعلم كيفية تطبيق مرشحات Gaussian
  و Wiener خطوة بخطوة للحصول على نتائج بصرية مذهلة.
keywords:
- java image processing tutorial
- export png java
- gaussian filter java
- wiener filter java
lastmod: 2026-07-17
linktitle: تطبيق مرشحات Gaussian و Wiener
og_description: دروس معالجة الصور بجافا توضح تطبيق مرشحات Gaussian و Wiener باستخدام
  Aspose.PSD لجافا، بما في ذلك التصدير إلى PNG وصيغ أخرى.
og_image_alt: 'Developer guide: Apply Gaussian and Wiener filters to images in Java
  using Aspose.PSD'
og_title: دروس معالجة الصور بجافا – تطبيق مرشحات Gaussian و Wiener
schemas:
- author: Aspose
  dateModified: '2026-07-17'
  description: Java image processing tutorial using Aspose.PSD learn how to apply
    Gaussian and Wiener filters step‑by‑step for stunning visual results.
  headline: Java Image Processing Tutorial – Apply Gaussian & Wiener Filters
  type: TechArticle
- questions:
  - answer: It smooths an image by averaging neighboring pixels, reducing high‑frequency
      noise.
    question: What does the Gaussian filter do?
  - answer: It performs adaptive smoothing, preserving edges while diminishing noise.
    question: What is the Wiener filter?
  - answer: Aspose.PSD for Java provides built‑in support for both filters.
    question: Which library is used?
  - answer: A trial works for testing, but a commercial license is required for production.
    question: Do I need a license?
  - answer: Yes—Aspose.PSD supports PNG, JPEG, BMP, and many more.
    question: Can I output formats other than GIF?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- java image processing
- Aspose.PSD
- gaussian filter
- wiener filter
- export png java
title: دروس معالجة الصور بجافا – تطبيق مرشحات Gaussian و Wiener
url: /ar/java/image-processing/apply-gaussian-wiener-filters/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# دليل معالجة الصور في Java – تطبيق مرشحات Gaussian و Wiener باستخدام Aspose.PSD

## مقدمة

مرحبًا بكم في **دليل معالجة الصور في Java** الذي يوضح لك كيفية تطبيق مرشحات Gaussian و Wiener باستخدام Aspose.PSD للغة Java. سواءً كنت تقوم بتنظيف الصور المشوشة أو تحضير الرسومات للتسليم على الويب، فإن هذه المرشحات تمنحك نتائج ناعمة ومظهرًا احترافيًا. خلال الدقائق القليلة القادمة ستشاهد سير العمل الكامل — من تحميل ملف PSD إلى حفظ النتيجة المفلترة كملف GIF.

## إجابات سريعة
- **ماذا يفعل مرشح Gaussian؟** يقوم بتمليس الصورة عن طريق متوسط البكسلات المجاورة، مما يقلل الضوضاء ذات التردد العالي.  
- **ما هو مرشح Wiener؟** يقوم بتمليس تكيفي، يحافظ على الحواف مع تقليل الضوضاء.  
- **ما المكتبة المستخدمة؟** Aspose.PSD للغة Java توفر دعمًا مدمجًا لكلا المرشحين.  
- **هل أحتاج إلى ترخيص؟** النسخة التجريبية تعمل للاختبار، لكن الترخيص التجاري مطلوب للإنتاج.  
- **هل يمكنني إخراج صيغ غير GIF؟** نعم—Aspose.PSD تدعم PNG، JPEG، BMP، والعديد غيرها.

## ما هو دليل معالجة الصور في Java؟

دليل معالجة الصور في Java يوجه المطورين عبر الخطوات الأساسية لتحميل صورة، تطبيق التحولات مثل المرشحات أو تغيير الحجم، وأخيرًا حفظ النتيجة بالصيغ المطلوبة. من خلال توفير أمثلة شفرة واضحة وشروحات، يساعدك على دمج قدرات معالجة الصور مباشرةً في تطبيقات Java، مما يقلل الحاجة إلى أدوات خارجية.

## لماذا نستخدم مرشحات Gaussian و Wiener؟

حمّل صورتك، طبّق مرشح Gaussian‑Wiener المدمج، وستلاحظ انخفاضًا كبيرًا في الحبيبات بينما تبقى الحواف الرئيسية حادة — مثالي لتحضير الرسومات للويب أو للنسخ الأرشيفية. الجزء Gaussian يزيل الضوضاء ذات التردد العالي، والجزء Wiener يتكيف مع التباين المحلي، محافظًا على التفاصيل حيث يهم الأمر أكثر.

## المتطلبات المسبقة

قبل أن نبدأ، تأكد من وجود ما يلي:

- بيئة تطوير Java (JDK 8 أو أحدث).  
- مكتبة Aspose.PSD للغة Java. يمكنك تنزيلها **[هنا](https://releases.aspose.com/psd/java/)**.  
- إلمام أساسي بصياغة Java ومفاهيم البرمجة الكائنية.

## استيراد الحزم

جمل الاستيراد تجلب فئات Aspose.PSD إلى النطاق حتى تتمكن من العمل مع الصور النقطية، خيارات المرشحات، وصيغ الإخراج.

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.imagefilters.filteroptions.GaussWienerFilterOptions;
import com.aspose.psd.imageoptions.GifOptions;
```

هذه الاستيرادات تمنحك القدرة على تحميل الصور، معالجة النقطية، ضبط خيارات المرشح، وحفظ الصيغ.

## الخطوة 1: تحميل الصورة

فئة `RasterImage` تمثل صورة نقطية يمكن معالجتها بكسلًا بكسلًا.

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

Image image = Image.load(sourceFile);
RasterImage rasterImage = (RasterImage)image;
```

نحمّل ملف PSD من الدليل المحدد ونحوّله إلى `RasterImage` حتى نتمكن من التعامل مع بيانات البكسل.

## الخطوة 2: التحقق من RasterImage

فحص أمان يضمن أن الملف المحمّل هو صورة نقطية؛ وإلا فإن الروتين يخرج بأمان.

```java
if (rasterImage == null) {
    return;
}
```

## الخطوة 3: تكوين خيارات المرشح

فئة `GaussWienerFilterOptions` تتيح لك ضبط معلمات كل من Gaussian و Wiener في كائن واحد.

```java
GaussWienerFilterOptions options = new GaussWienerFilterOptions(12, 3);
options.setGrayscale(true);
```

- الوسيط الأول (`12`) يحدد حجم نصف القطر لنواة Gaussian.  
- الوسيط الثاني (`3`) يحدد قيمة التمليس المستخدمة من قبل خوارزمية Wiener.  
- `setGrayscale(true)` يطلب من المرشح العمل بالأبيض والأسود، وهو ما ينتج غالبًا نتائج أنظف لتقليل الضوضاء.

## الخطوة 4: تطبيق المرشح وحفظه

طريقة `filter` تطبق تركيبة Gaussian‑Wiener المكوّنة على كامل حدود الصورة. أخيرًا، نحفظ الصورة المعالجة كملف GIF باستخدام `GifOptions`. يمكنك استبدال `GifOptions` بـ `PngOptions` أو `JpegOptions` وغيرها لتصدير **PNG Java** أو صيغ أخرى.

```java
rasterImage.filter(image.getBounds(), options);
String destName = dataDir + "gauss_wiener_out.gif";
image.save(destName, new GifOptions());
```

## المشكلات الشائعة والنصائح

- **RasterImage فارغ:** تأكد من أن الملف المصدر هو PSD أو صيغة أخرى متوافقة مع الصور النقطية.  
- **الأداء:** قد تستغرق الصور الكبيرة وقتًا أطول؛ فكر في تقليل نصف القطر أو معالجة نسخة مصغرة أولًا.  
- **اللون مقابل الأبيض والأسود:** إذا كنت بحاجة للحفاظ على اللون، اضبط `options.setGrayscale(false)`.

## الأسئلة المتكررة

**س1: هل يمكنني تطبيق هذه المرشحات على صور بصيغ غير PSD؟**  
ج1: نعم، Aspose.PSD للغة Java يدعم صيغ صور متعددة غير PSD، مثل PNG، JPEG، BMP، و GIF.

**س2: هل هناك أي قيود في نسخة التجربة من Aspose.PSD للغة Java؟**  
ج2: نسخة التجربة تقيد حجم الإخراج وتضيف علامة مائية. للحصول على كامل الإمكانات، احصل على ترخيص صالح.

**س3: كيف يمكنني الحصول على دعم لـ Aspose.PSD للغة Java؟**  
ج3: زر **[منتدى Aspose.PSD](https://forum.aspose.com/c/psd/34)** للحصول على مساعدة المجتمع والردود الرسمية.

**س4: هل هناك ترخيص مؤقت متاح لأغراض الاختبار؟**  
ج4: نعم، يمكنك الحصول على ترخيص مؤقت **[هنا](https://purchase.aspose.com/temporary-license/)**.

**س5: أين يمكنني العثور على وثائق مفصلة لـ Aspose.PSD للغة Java؟**  
ج5: راجع **[الوثائق](https://reference.aspose.com/psd/java/)** للحصول على مراجع API متعمقة وأمثلة إضافية.

## الخاتمة

لقد أكملت الآن دليل **معالجة الصور في Java** الكامل الذي يوضح كيفية **تطبيق مرشح Gaussian** و Wiener باستخدام Aspose.PSD للغة Java. جرّب قيم نصف القطر والتمليس المختلفة، غيّر وضع الأبيض والأسود، وجرب صيغ إخراج أخرى مثل PNG لترى كيف تؤثر المرشحات على صورك. برمجة سعيدة!

---

**آخر تحديث:** 2026-07-17  
**تم الاختبار مع:** Aspose.PSD للغة Java 23.12 (أحدث نسخة وقت الكتابة)  
**المؤلف:** Aspose

## دروس ذات صلة

- [Step by Step Filter - Apply Motion Wiener Filters using Aspose.PSD for Java](/psd/java/image-processing/apply-motion-wiener-filters/)
- [Step by Step Filter - Apply Median & Wiener Filters (Java)](/psd/java/image-processing/apply-median-wiener-filters/)
- [How to Filter PNG Files in Aspose.PSD for Java](/psd/java/optimizing-png-files/apply-filters-png-files/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}