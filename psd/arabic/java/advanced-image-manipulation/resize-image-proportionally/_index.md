---
date: 2026-02-09
description: تعلم كيفية تحويل ملفات PSD إلى PNG وتغيير حجم الصور بنسب متناسبة في Java
  باستخدام Aspose.PSD. يغطي هذا الدليل خطوة بخطوة تخزين الصور مؤقتًا، وتغيير الحجم،
  وحفظها كملفات PNG.
linktitle: Convert PSD to PNG & Resize Proportionally
second_title: Aspose.PSD Java API
title: كيفية تحويل PSD إلى PNG وتغيير الحجم بشكل متناسب باستخدام Aspose.PSD للغة Java
url: /ar/java/advanced-image-manipulation/resize-image-proportionally/
weight: 17
---

.{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# كيفية تحويل PSD إلى PNG وإعادة التحجيم بشكل متناسب باستخدام Aspose.PSD للـ Java

## مقدمة

إذا كنت بحاجة إلى **تحويل PSD إلى PNG** مع الحفاظ على نسبة الأبعاد الأصلية، فقد وجدت المكان المناسب. في هذا الدرس **Aspose.PSD Java** سنستعرض دليلًا كاملًا **java image processing tutorial** يوضح لك **كيفية إعادة تحجيم الصورة** بشكل متناسب، وتخزين الصورة مؤقتًا لأداء مثالي، وأخيرًا حفظ النتيجة كملف PNG. في النهاية ستتمكن من دمج هذا سير العمل في أي خط أنابيب معالجة صور مبني على Java.

## الإجابات السريعة
- **هل يمكن لـ Aspose.PSD تحويل PSD إلى PNG؟** نعم – ما عليك سوى تحميل ملف PSD وحفظه باستخدام `PngOptions`.
- **هل تدعم المكتبة إعادة التحجيم بشكل متناسب؟** بالتأكيد؛ استخدم `resizeWidthProportionally` و `resizeHeightProportionally`.
- **هل يجب عليّ تخزين الصورة مؤقتًا أولاً؟** التخزين المؤقت (`image.cacheData()`) يحسن الأداء لملفات PSD الكبيرة.
- **ما نسخة Java المطلوبة؟** Java 8 أو أحدث مدعومة بالكامل.
- **هل يلزم وجود ترخيص للإنتاج؟** نعم، الترخيص التجاري يزيل علامات التقييم.

## ما هو “تحويل PSD إلى PNG” ولماذا هو مهم؟

تحويل مستند Photoshop (PSD) إلى ملف Portable Network Graphics (PNG) يتيح لك مشاركة التصاميم الطبقية بصيغة خفيفة ومناسبة للويب. يحتفظ PNG بالشفافية والجودة غير الفاقدة، مما يجعله مثاليًا لأصول واجهة المستخدم، المصغرات، أو أي سيناريو تتطلب دقة الصورة.

## لماذا نعيد تحجيم الصورة بشكل متناسب في Java؟

إعادة تحجيم **كيفية إعادة تحجيم الصورة** دون تشويه نسبة الأبعاد تضمن أن الرسومات تبدو طبيعية على شاشات مختلفة. توفر واجهة برمجة تطبيقات `Aspose.PSD` طرقًا مخصصة لـ **إعادة تحجيم الصورة بشكل متناسب**، والتي تحسب تلقائيًا الارتفاع أو العرض المطابق، مما يحفظك من أخطاء الحساب اليدوي.

## لماذا هذا مهم للمطورين

- **تقليل حجم ملف PSD** – عن طريق تصغير ملفات PSD الكبيرة قبل التحويل، تقلل من استهلاك الذاكرة وتسرّع المعالجة اللاحقة.  
- **عرض واجهة مستخدم متسق** – إعادة التحجيم المتناسبة تضمن أن الأيقونات والرسومات تحافظ على توازنها البصري عبر الأجهزة.  
- **عدم الاعتماد على Photoshop** – يمكنك تنفيذ هذه العمليات على خادم أو خط أنابيب CI دون الحاجة لتثبيت Photoshop.

## المتطلبات المسبقة

قبل الغوص في الكود، تأكد من أن لديك:

1. **مجموعة تطوير Java (JDK)** – يجب تثبيت Java 8 أو أحدث.  
2. **Aspose.PSD للـ Java** – قم بتنزيل أحدث ملف JAR من الموقع الرسمي [هنا](https://releases.aspose.com/psd/java/).  
3. ملف PSD تجريبي (`sample.psd`) موجود في دليل يمكنك الإشارة إليه من مشروعك.

## استيراد الحزم

أضف الاستيرادات اللازمة إلى فئة Java الخاصة بك. هذه الفئات تمنحك إمكانية تحميل الصور، التخزين المؤقت، إعادة التحجيم، وخيارات إخراج PNG.

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

## الخطوة 2: إعادة تحجيم الصورة بشكل متناسب (Java)

الآن حدد الأبعاد الجديدة. في هذا المثال نقوم بتصغير الصورة إلى **نصف** حجمها الأصلي مع الحفاظ على نسبة الأبعاد. يمكنك تعديل العرض أو الارتفاع المستهدف حسب الحاجة.

```java
int newWidth = image.getWidth() / 2;
image.resizeWidthProportionally(newWidth);

int newHeight = image.getHeight() / 2;
image.resizeHeightProportionally(newHeight);
```

> **نصيحة احترافية:** استخدم إما `resizeWidthProportionally` *أو* `resizeHeightProportionally`—المكتبة تحسب تلقائيًا البُعد الآخر للحفاظ على تناسق الصورة.

## الخطوة 3: حفظ الصورة المعاد تحجيمها كـ PNG

أخيرًا، قم بتصدير الصورة المعاد تحجيمها إلى صيغة PNG. هذه الخطوة تكمل سير عمل **تحويل PSD إلى PNG**.

```java
String destName = dataDir + "SimpleResizeImageProportionally_out.png";
image.save(destName, new PngOptions());
```

عند تشغيل الكود، ستجد ملف PNG بحجم نصف حجم PSD الأصلي، مع نفس الجودة البصرية دون أي تشويه.

## المشكلات الشائعة والحلول

| المشكلة | السبب | الحل |
|-------|-------|-----|
| **OutOfMemoryError** | PSD كبير غير مخزن مؤقتًا | استدعِ `image.cacheData()` قبل إعادة التحجيم |
| **Blank PNG output** | مسار ملف غير صحيح | تحقق من `dataDir` وصلاحيات الكتابة |
| **Aspect ratio looks off** | استخدام العرض والارتفاع يدويًا معًا | استخدم الطرق المتناسبة المقدمة من Aspose.PSD |

## نصائح لتقليل حجم ملف PSD

- **قص الطبقات غير الضرورية** قبل تحميل الملف.  
- **إعادة التحجيم بشكل متناسب** كما هو موضح أعلاه لتقليل الأبعاد مبكرًا.  
- **احفظ كـ PNG بعمق لون مناسب** لتجنب البيانات الزائدة.

## الأسئلة المتكررة

**س: هل Aspose.PSD متوافق مع جميع صيغ الصور؟**  
ج: يدعم Aspose.PSD صيغ PSD، PNG، JPEG، BMP، GIF، والعديد غيرها. راجع القائمة الكاملة في [الوثائق](https://reference.aspose.com/psd/java/).

**س: هل يمكنني استخدام Aspose.PSD للمشاريع التجارية؟**  
ج: نعم. يمكنك شراء ترخيص تجاري من [متجر Aspose](https://purchase.aspose.com/buy).

**س: هل تتوفر تراخيص مؤقتة للاختبار؟**  
ج: بالتأكيد – اطلب ترخيصًا مؤقتًا [هنا](https://purchase.aspose.com/temporary-license/) لأغراض التقييم.

**س: أين يمكنني العثور على دعم المجتمع؟**  
ج: منتدى [Aspose.PSD](https://forum.aspose.com/c/psd/34) مكان رائع لطرح الأسئلة ومشاركة الحلول.

**س: كيف يمكنني الوصول إلى مرجع API الكامل؟**  
ج: الوثائق التفصيلية للـ API متاحة [هنا](https://reference.aspose.com/psd/java/).

## الخلاصة

أنت الآن تعرف كيف **تحويل PSD إلى PNG**، **إعادة تحجيم الصورة بشكل متناسب**، وكيفية التعامل مع التخزين المؤقت بفعالية باستخدام Aspose.PSD للـ Java. دمج هذه الخطوات في تطبيقاتك يتيح لك تقديم معالجة صور سريعة وعالية الجودة دون الاعتماد على تثبيت Photoshop الأصلي. هذا النهج **aspose psd java** هو جزء موثوق من أي **java image processing tutorial** ويساعدك على الحفاظ على حجم ملفات PSD تحت السيطرة مع الحفاظ على الدقة البصرية.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Last Updated:** 2026-02-09  
**Tested With:** Aspose.PSD 24.12 for Java  
**Author:** Aspose