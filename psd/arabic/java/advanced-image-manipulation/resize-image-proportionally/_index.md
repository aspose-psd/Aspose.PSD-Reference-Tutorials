---
date: 2025-12-08
description: تعلم كيفية تحويل ملفات PSD إلى PNG وتغيير حجم الصور بشكل متناسب في Java
  باستخدام Aspose.PSD. يغطي هذا الدليل خطوة بخطوة تخزين الصور مؤقتًا، وتغيير الحجم،
  وحفظها كملف PNG.
linktitle: Convert PSD to PNG & Resize Proportionally
second_title: Aspose.PSD Java API
title: كيفية تحويل PSD إلى PNG وتغيير الحجم بشكل متناسب باستخدام Aspose.PSD للـ Java
url: /ar/java/advanced-image-manipulation/resize-image-proportionally/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# كيفية تحويل PSD إلى PNG وإعادة التحجيم بالتناسب باستخدام Aspose.PSD للـ Java

## المقدمة

إذا كنت بحاجة إلى **convert PSD to PNG** مع الحفاظ على نسبة العرض إلى الارتفاع الأصلية، فقد وصلت إلى المكان الصحيح. في هذا الدرس سنستعرض **Aspose.PSD tutorial** كامل يوضح لك **how to resize image** بصورة متناسبة في Java، وكيفية تخزين الصورة مؤقتًا لتحسين الأداء، وأخيرًا حفظ النتيجة كملف PNG. في النهاية ستتمكن من دمج هذا سير العمل في أي خط أنابيب لمعالجة الصور مبني على Java.

## إجابات سريعة
- **Can Aspose.PSD convert PSD to PNG?** نعم – ما عليك سوى تحميل ملف PSD وحفظه باستخدام `PngOptions`.
- **Does the library support proportional resizing?** بالتأكيد؛ استخدم `resizeWidthProportionally` و `resizeHeightProportionally`.
- **Do I need to cache the image first?** التخزين المؤقت (`image.cacheData()`) يحسن الأداء لملفات PSD الكبيرة.
- **What Java version is required?** Java 8 أو أحدث مدعومان بالكامل.
- **Is a license required for production?** نعم، الترخيص التجاري يزيل علامات التقييم المائية.

## ما هو “convert PSD to PNG” ولماذا هو مهم؟

تحويل مستند Photoshop (PSD) إلى ملف Portable Network Graphics (PNG) يتيح لك مشاركة التصاميم الطبقية بصيغة خفيفة وصديقة للويب. يحتفظ PNG بالشفافية والجودة غير الضائعة، مما يجعله مثاليًا لأصول واجهة المستخدم، المصغرات، أو أي سيناريو حيث تكون دقة الصورة مهمة.

## لماذا إعادة تحجيم الصورة بالتناسب في Java؟

إعادة تحجيم **how to resize image** دون تشويه نسبة العرض إلى الارتفاع تضمن أن تبدو الرسومات طبيعية على شاشات مختلفة. توفر API الخاصة بـ `Aspose.PSD` طرقًا مخصصة للتكبير/التصغير المتناسب، والتي تحسب تلقائيًا الارتفاع أو العرض المناسب، مما يوفر عليك الأخطاء الحسابية اليدوية.

## المتطلبات المسبقة

قبل الغوص في الكود، تأكد من وجود ما يلي:

1. **Java Development Kit (JDK)** – تثبيت Java 8 أو أحدث.
2. **Aspose.PSD for Java** – تحميل أحدث ملف JAR من الموقع الرسمي [here](https://releases.aspose.com/psd/java/).
3. ملف PSD تجريبي (`sample.psd`) موجود في دليل يمكنك الإشارة إليه من مشروعك.

## استيراد الحزم

أضف الاستيرادات اللازمة إلى فئة Java الخاصة بك. هذه الفئات تمنحك الوصول إلى تحميل الصور، التخزين المؤقت، إعادة التحجيم، وخيارات إخراج PNG.

```java
import com.aspose.psd.Image;
import com.aspose.psd.imageoptions.PngOptions;
```

## الخطوة 1: تحميل صورة PSD

أولاً، قم بتحميل ملف PSD المصدر. إذا كان الملف كبيرًا، فإن تخزين بيانات الصورة مؤقتًا يقلل من استهلاك الذاكرة عند تنفيذ العمليات اللاحقة.

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

Image image = Image.load(sourceFile);

if (!image.isCached()) {
    // Image caching java – improves performance for large files
    image.cacheData();
}
```

## الخطوة 2: إعادة تحجيم الصورة بالتناسب (Java)

الآن حدد الأبعاد الجديدة. في هذا المثال نقوم بتصغير الصورة إلى **نصف** حجمها الأصلي مع الحفاظ على نسبة العرض إلى الارتفاع. يمكنك تعديل العرض أو الارتفاع المستهدف حسب الحاجة.

```java
int newWidth = image.getWidth() / 2;
image.resizeWidthProportionally(newWidth);

int newHeight = image.getHeight() / 2;
image.resizeHeightProportionally(newHeight);
```

> **Pro tip:** استخدم إما `resizeWidthProportionally` *or* `resizeHeightProportionally`—المكتبة تحسب تلقائيًا البعد الآخر للحفاظ على تناسق الصورة.

## الخطوة 3: حفظ الصورة المعاد تحجيمها كـ PNG

أخيرًا، صدّر الصورة المعاد تحجيمها إلى صيغة PNG. هذه الخطوة تكمل سير عمل **convert PSD to PNG**.

```java
String destName = dataDir + "SimpleResizeImageProportionally_out.png";
image.save(destName, new PngOptions());
```

عند تشغيل الكود، ستجد ملف PNG بحجم نصف حجم PSD الأصلي، مع الحفاظ على الجودة البصرية دون أي تشويه.

## المشكلات الشائعة والحلول

| المشكلة | السبب | الحل |
|-------|-------|-----|
| **OutOfMemoryError** | PSD كبير غير مخزن مؤقتًا | استدعِ `image.cacheData()` قبل إعادة التحجيم |
| **Blank PNG output** | مسار ملف غير صحيح | تحقق من `dataDir` وصلاحيات الكتابة |
| **Aspect ratio looks off** | استخدام العرض والارتفاع يدويًا معًا | استخدم الطرق المتناسبة المتوفرة في Aspose.PSD |

## الأسئلة المتكررة

**س: هل Aspose.PSD متوافق مع جميع صيغ الصور؟**  
ج: يدعم Aspose.PSD الصيغ PSD, PNG, JPEG, BMP, GIF، والعديد غيرها. راجع القائمة الكاملة في [documentation](https://reference.aspose.com/psd/java/).

**س: هل يمكنني استخدام Aspose.PSD في المشاريع التجارية؟**  
ج: نعم. يمكنك شراء ترخيص تجاري من [Aspose store](https://purchase.aspose.com/buy).

**س: هل تتوفر تراخيص مؤقتة للاختبار؟**  
ج: بالتأكيد – اطلب ترخيصًا مؤقتًا [here](https://purchase.aspose.com/temporary-license/) لأغراض التقييم.

**س: أين يمكنني العثور على دعم المجتمع؟**  
ج: منتدى [Aspose.PSD](https://forum.aspose.com/c/psd/34) مكان رائع لطرح الأسئلة ومشاركة الحلول.

**س: كيف يمكنني الوصول إلى مرجع API الكامل؟**  
ج: الوثائق التفصيلية للـ API متاحة [here](https://reference.aspose.com/psd/java/).

## الخاتمة

أنت الآن تعرف كيفية **convert PSD to PNG**، وإعادة تحجيم الصورة بالتناسب، ومعالجة التخزين المؤقت بفعالية باستخدام Aspose.PSD للـ Java. دمج هذه الخطوات في تطبيقاتك سيضمن معالجة صور سريعة وعالية الجودة دون الاعتماد على تثبيتات Photoshop الأصلية.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**آخر تحديث:** 2025-12-08  
**تم الاختبار مع:** Aspose.PSD 24.12 for Java  
**المؤلف:** Aspose