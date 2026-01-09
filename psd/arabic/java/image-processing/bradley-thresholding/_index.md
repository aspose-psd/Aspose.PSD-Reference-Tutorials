---
date: 2026-01-09
description: تعلم كيفية تحويل PSD إلى PNG باستخدام تقنية برادلي للحدود في Aspose.PSD
  للغة Java. يوضح هذا الدليل كيفية اختيار العتبة المثلى وتحويل صورة PSD إلى صورة ثنائية
  بكفاءة.
linktitle: Bradley Thresholding
second_title: Aspose.PSD Java API
title: تحويل PSD إلى PNG باستخدام عتبة برادلي (Aspose.PSD Java)
url: /ar/java/image-processing/bradley-thresholding/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# تحويل PSD إلى PNG باستخدام عتبة برادلي (Aspose.PSD Java)

مرحبًا بكم في هذا الدليل الشامل حول **convert PSD to PNG** باستخدام عتبة برادلي في Aspose.PSD للـ Java. خلال الدقائق القليلة القادمة، ستتعرفون على سبب كفاءة هذه التقنية لإنشاء ملفات PNG ذات تباين عالٍ ومُثنّية من مستندات Photoshop، وستحصلون على شرح عملي خطوة بخطوة.

## إجابات سريعة
- **هل يمكنني تحويل PSD إلى PNG باستخدام Aspose.PSD؟** نعم – قم بتحميل ملف PSD، تطبيق `binarizeBradley`، ثم حفظه كـ PNG.  
- **ماذا يعني “choose optimal threshold”؟** هو قيمة الحساسية (0‑1) التي تحدد كيفية تصنيف البكسلات الداكنة/الفاتحة.  
- **هل أحتاج إلى ترخيص للاستخدام في الإنتاج؟** يلزم ترخيص تجاري؛ النسخة التجريبية المجانية تكفي للتقييم.  
- **ما صيغ الصور المدعومة للحفظ؟** PNG، JPEG، BMP، والعديد غيرها عبر فئات `ImageOptions`.  
- **هل الكود متوافق مع Java 8 وما بعده؟** بالتأكيد – يدعم Aspose.PSD Java API Java 8+.

## ما هو عتبة برادلي؟
عتبة برادلي هي خوارزمية تمثيل ثنائي تكيفية تحسب المتوسط المحلي لكل بكسل وتقارن شدة البكسل مع ذلك المتوسط مضروبًا في عتبة يحددها المستخدم. النتيجة هي صورة أبيض‑أسود نظيفة تحتفظ بالتفاصيل المهمة.

## لماذا تحويل PSD إلى PNG باستخدام عتبة برادلي؟
- **الحفاظ على الحواف الحادة** – مثالي لتقنية OCR، كشف الباركود، أو أي سير عمل يحتاج إلى فصل واضح بين المقدمة والخلفية.  
- **تقليل حجم الملف** – PNG غير مضغوط لكنه غالبًا أصغر بعد التمثيل الثنائي.  
- **التوافق عبر المنصات** – PNG يعمل في جميع الأماكن، بينما PSD مخصص لـ Photoshop.  

## المتطلبات المسبقة
قبل أن نبدأ، تأكد من أن لديك:

1. **بيئة تطوير Java** – JDK 8 أو أحدث مثبت.  
2. **مكتبة Aspose.PSD** – قم بتنزيل أحدث ملف JAR من [here](https://releases.aspose.com/psd/java/).  
3. **صورة PSD تجريبية** – أي ملف PSD ترغب في تحويله؛ يمكنك أيضًا استخدام العينة المتوفرة في أمثلة Aspose.

## استيراد الحزم
ابدأ باستيراد الفئات اللازمة إلى مشروع Java الخاص بك:

```java
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PngOptions;
```

## كيفية تحويل PSD إلى PNG باستخدام عتبة برادلي
فيما يلي سير العمل الكامل مقسم إلى خطوات مرقمة وواضحة. كل خطوة تتضمن شرحًا مختصرًا يليه الكود الدقيق الذي تحتاج إلى نسخه‑ولصقه.

### الخطوة 1: تحميل صورة PSD
أولاً، حدد ملف المصدر الخاص بك وقم بتحميله باستخدام Aspose.PSD.

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "binarized_out.png";

// Load an image
PsdImage image = (PsdImage)Image.load(sourceFile);
```

### الخطوة 2: اختيار العتبة المثلى
قيمة العتبة (النطاق 0 – 1) تتحكم في مدى شدة التمثيل الثنائي. نقطة الانطلاق النموذجية هي **0.15**، ولكن يمكنك تعديلها لتناسب صورتك.

```java
// Define threshold value
double threshold = 0.15;
```

### الخطوة 3: تمثيل صورة PSD ثنائيًا
الآن قم بتطبيق خوارزمية Bradley. هذه الخطوة **binarize PSD image** بناءً على العتبة التي اخترتها.

```java
// Call BinarizeBradley method and pass the threshold value as a parameter
image.binarizeBradley(threshold);
```

### الخطوة 4: حفظ الناتج كـ PNG
أخيرًا، احفظ الصورة المعالجة على القرص بصيغة PNG.

```java
// Save the output image
image.save(destName, new PngOptions());
```

كرر هذه الخطوات لأي عدد من ملفات PSD التي تحتاج إلى معالجتها، مع تعديل العتبة حسب الحاجة لتحقيق أفضل نتيجة بصرية.

## المشكلات الشائعة والنصائح
- **العتبة منخفضة/مرتفعة جدًا:** إذا كان الناتج يبدو صاخبًا جدًا أو باهتًا، قم بضبط قيمة `threshold` تدريجيًا (مثلاً، 0.10 – 0.20).  
- **استهلاك الذاكرة:** ملفات PSD الكبيرة قد تستهلك الكثير من الذاكرة. فكر في معالجتها واحدةً تلو الأخرى أو زيادة حجم الذاكرة المخصصة للـ JVM (`-Xmx`).  
- **معاينة قبل الحفظ:** استخدم `image.save("preview.bmp", new BmpOptions());` لتفحص النتيجة الثنائية قبل تصدير PNG النهائي.

## الأسئلة المتكررة

**س: ما الفرق بين `binarizeBradley` وطرق العتبة الأخرى؟**  
ج: `binarizeBradley` يحسب المتوسط المحلي لكل بكسل، مما يجعله أكثر صلابة للصور ذات الإضاءة غير المتساوية مقارنةً بالعتبة العامة.

**س: هل يمكنني تطبيق عتبة برادلي على ملفات JPEG أو BMP؟**  
ج: نعم. قم بتحميل أي صيغة مدعومة باستخدام `Image.load(...)`، ثم استدعِ `binarizeBradley` قبل الحفظ.

**س: هل هناك طريقة لمعاينة الصورة الثنائية قبل الحفظ؟**  
ج: بالتأكيد. استخدم أي من خيارات حفظ الصور في Aspose.PSD (مثل BMP) لكتابة ملف معاينة مؤقت.

**س: أين يمكنني العثور على مزيد من الدعم والموارد؟**  
ج: زر [منتدى Aspose.PSD](https://forum.aspose.com/c/psd/34) للحصول على مساعدة المجتمع واستكشف [الوثائق](https://reference.aspose.com/psd/java/) الكاملة للسيناريوهات المتقدمة.

## الخلاصة
لقد تعلمت الآن كيفية **convert PSD to PNG** بفعالية عن طريق **اختيار عتبة مثلى** و**تمثيل صورة PSD ثنائيًا** باستخدام عتبة برادلي. هذا النهج مثالي لسير العمل الذي يتطلب مخرجات PNG نظيفة وعالية التباين من ملفات Photoshop المعقدة.

---

**Last Updated:** 2026-01-09  
**Tested With:** Aspose.PSD Java 23.12 (latest at time of writing)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}