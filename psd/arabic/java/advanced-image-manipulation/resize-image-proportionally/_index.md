---
date: 2026-06-23
description: تعلم كيفية تحويل PSD إلى PNG وإعادة تحجيم الصور بنسبية في Java باستخدام
  Aspose.PSD. يغطي هذا البرنامج التعليمي خطوة بخطوة تخزين الصور مؤقتًا، وإعادة التحجيم،
  وحفظها كملف PNG.
keywords:
- convert psd to png
- save psd as png
- how to cache image
- resize image without distortion
- proportional image scaling
linktitle: تحويل PSD إلى PNG وإعادة التحجيم بنسبية
schemas:
- author: Aspose
  dateModified: '2026-06-23'
  description: Learn how to convert PSD to PNG and resize images proportionally in
    Java using Aspose.PSD. This step‑by‑step tutorial covers image caching, resizing,
    and saving as PNG.
  headline: How to Convert PSD to PNG and Resize Proportionally with Aspose.PSD for
    Java
  type: TechArticle
- description: Learn how to convert PSD to PNG and resize images proportionally in
    Java using Aspose.PSD. This step‑by‑step tutorial covers image caching, resizing,
    and saving as PNG.
  name: How to Convert PSD to PNG and Resize Proportionally with Aspose.PSD for Java
  steps:
  - name: '**Java Development Kit (JDK)** – Java 8 or later installed.'
    text: '**Java Development Kit (JDK)** – Java 8 or later installed.'
  - name: '**Aspose.PSD for Java** – download the latest JAR from the official site [here](https://releases.aspose.com/psd/java/).'
    text: '**Aspose.PSD for Java** – download the latest JAR from the official site [here](https://releases.aspose.com/psd/java/).'
  - name: A sample PSD file (`sample.psd`) placed in a directory you can reference
      from your project.
    text: A sample PSD file (`sample.psd`) placed in a directory you can reference
      from your project.
  type: HowTo
- questions:
  - answer: Aspose.PSD supports PSD, PNG, JPEG, BMP, GIF, and many more. See the full
      list in the [documentation](https://reference.aspose.com/psd/java/). For the
      full API reference, see the guide **here**.
    question: Is Aspose.PSD compatible with all image formats?
  - answer: Yes. Purchase a commercial license on the [Aspose store](https://purchase.aspose.com/buy).
    question: Can I use Aspose.PSD for commercial projects?
  - answer: Absolutely – request a temporary license [here](https://purchase.aspose.com/temporary-license/)
      for evaluation purposes.
    question: Are temporary licenses available for testing?
  - answer: The [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) is a great place
      to ask questions and share solutions.
    question: Where can I find community support?
  - answer: Detailed API docs are available [here](https://reference.aspose.com/psd/java/).
    question: How do I access the full API reference?
  type: FAQPage
second_title: Aspose.PSD Java API
title: كيفية تحويل PSD إلى PNG وإعادة التحجيم بنسبية باستخدام Aspose.PSD للـ Java
url: /ar/java/advanced-image-manipulation/resize-image-proportionally/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# كيفية تحويل PSD إلى PNG وإعادة التحجيم بنسبية باستخدام Aspose.PSD للـ Java

## المقدمة

إذا كنت بحاجة إلى **تحويل PSD إلى PNG** مع الحفاظ على نسبة العرض إلى الارتفاع الأصلية، فقد وصلت إلى المكان الصحيح. في هذا الدرس **Aspose.PSD Java** سنستعرض دليلًا كاملًا **لمعالجة الصور في Java** يوضح لك **كيفية إعادة تحجيم الصورة** بنسبية، وتخزين الصورة مؤقتًا لأداء مثالي، وأخيرًا حفظ النتيجة كملف PNG. في النهاية ستتمكن من دمج هذا سير العمل في أي خط أنابيب لمعالجة الصور مبني على Java.

## الإجابات السريعة
- **هل يمكن لـ Aspose.PSD تحويل PSD إلى PNG؟** نعم – ما عليك سوى تحميل ملف PSD وحفظه باستخدام `PngOptions`.
- **هل تدعم المكتبة إعادة التحجيم بنسبية؟** بالتأكيد؛ استخدم `resizeWidthProportionally` و `resizeHeightProportionally`.
- **هل أحتاج إلى تخزين الصورة مؤقتًا أولاً؟** التخزين المؤقت (`image.cacheData()`) يحسن الأداء لملفات PSD الكبيرة.
- **ما نسخة Java المطلوبة؟** Java 8 أو أحدث مدعومة بالكامل.
- **هل يلزم وجود ترخيص للإنتاج؟** نعم، الترخيص التجاري يزيل علامات التقييم.

## ما هو “convert PSD to PNG” ولماذا هو مهم؟

**convert PSD to PNG** يعني تحويل مستند Photoshop متعدد الطبقات إلى ملف PNG أحادي الطبقة غير مضغوط يحافظ على الشفافية والدقة البصرية. يتيح لك هذا التحويل مشاركة التصاميم دون الحاجة إلى Photoshop، وإنشاء أصول جاهزة للويب وصور مصغرة، وتخفيف عبء ملفات PSD الكبيرة عن متصفحات العملاء مع الحفاظ على الجودة المطلوبة للمكونات البصرية والعلامات التجارية.

## لماذا إعادة تحجيم الصورة بنسبية في Java؟

إعادة تحجيم الصورة **بدون تشويه** تحافظ على نسبة العرض إلى الارتفاع الأصلية، بحيث تحتفظ الرسومات بمظهرها المقصود على أي حجم شاشة. تقوم طرق التحجيم النسبية في Aspose.PSD بحساب البُعد المفقود تلقائيًا، مما يلغي الحاجة إلى حسابات يدوية ويقلل خطر الصور المشوهة أو المضغوطة.

## لماذا هذا مهم للمطورين

بالنسبة للمطورين، يقلل التحجيم النسبى وتحويل PSD إلى PNG من استهلاك الذاكرة ويحسن أوقات التحميل، مما يضمن أن التطبيقات تتعامل مع الرسومات الكبيرة بكفاءة. من خلال تحجيم الصور مبكرًا، تحافظ على تناسق عرض واجهة المستخدم عبر الأجهزة وتلغي الحاجة إلى Photoshop على خوادم البناء، مما يبسط النشر ويقلل التكاليف التشغيلية.

- **تقليل حجم ملف PSD** – عن طريق تقليل حجم ملفات PSD الكبيرة قبل التحويل، تقلل من استهلاك الذاكرة وتسرّع المعالجة اللاحقة.  
- **عرض واجهة مستخدم متسق** – تضمن إعادة التحجيم النسبية أن الأيقونات والرسومات تحافظ على توازنها البصري عبر الأجهزة.  
- **عدم الاعتماد على Photoshop** – يمكنك تنفيذ هذه العمليات على خادم أو خط أنابيب CI دون تثبيت Photoshop.

## المتطلبات المسبقة

قبل الغوص في الكود، تأكد من وجود ما يلي:

1. **مجموعة تطوير Java (JDK)** – يجب تثبيت Java 8 أو أحدث.  
2. **Aspose.PSD للـ Java** – قم بتحميل أحدث ملف JAR من الموقع الرسمي [هنا](https://releases.aspose.com/psd/java/).  
3. ملف PSD تجريبي (`sample.psd`) وضعه في دليل يمكنك الإشارة إليه من مشروعك.

## استيراد الحزم

الفئة `PsdImage` هي الكائن الأساسي في Aspose.PSD الذي يمثل ملف PSD في الذاكرة. استورد الحزم اللازمة للعمل مع التحميل، التخزين المؤقت، التحجيم، وتصدير PNG.

```java
import com.aspose.psd.Image;
import com.aspose.psd.imageoptions.PngOptions;
```

## الخطوة 1: تحميل صورة PSD

**الإجابة المباشرة:** حمّل الملف المصدر باستخدام `new PsdImage("sample.psd")`؛ ثم استدعِ `image.cacheData()` لتحميل بيانات الصورة مسبقًا، مما يمنع قراءات القرص المتكررة أثناء العمليات اللاحقة.

`cacheData()` يحمل ملف PSD بالكامل في الذاكرة، مما يتيح معالجة أسرع لاحقًا. طريقة `cacheData()` تقرأ المستند بالكامل في الذاكرة، مما يسرّع المعالجة اللاحقة للملفات الكبيرة. أولاً، حمّل ملف PSD المصدر. إذا كان الملف كبيرًا، فإن تخزين بيانات الصورة مؤقتًا يقلل من استهلاك الذاكرة عند تنفيذ العمليات اللاحقة.

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

Image image = Image.load(sourceFile);

if (!image.isCached()) {
    // Image caching java – improves performance for large files
    image.cacheData();
}
```

## الخطوة 2: إعادة تحجيم الصورة بنسبية (Java)

**الإجابة المباشرة:** استدعِ `image.resizeWidthProportionally(targetWidth)` (أو `resizeHeightProportionally`) لتقليص الصورة مع الحفاظ تلقائيًا على نسبة العرض إلى الارتفاع الأصلية.

`resizeWidthProportionally(int targetWidth)` يضبط عرض الصورة ويحسب تلقائيًا الارتفاع المطابق للحفاظ على النسبة الأصلية. الآن حدد الأبعاد الجديدة. في هذا المثال نقوم بتقليص الصورة إلى **نصف** حجمها الأصلي مع الحفاظ على النسبة. يمكنك تعديل العرض أو الارتفاع المستهدف حسب الحاجة.

طريقة `resizeWidthProportionally` تحسب الارتفاع المطابق بناءً على النسبة الأصلية، لذا يتم تحجيم الصورة **بدون تشويه**. استخدم أيًا من الطريقتين—Aspose.PSD يتولى حساب البُعد المكمل لك.

```java
int newWidth = image.getWidth() / 2;
image.resizeWidthProportionally(newWidth);

int newHeight = image.getHeight() / 2;
image.resizeHeightProportionally(newHeight);
```

> **نصيحة احترافية:** استخدم إما `resizeWidthProportionally` *أو* `resizeHeightProportionally`—المكتبة تحسب البُعد الآخر تلقائيًا للحفاظ على النسبة.

## الخطوة 3: حفظ الصورة المعاد تحجيمها كـ PNG

**الإجابة المباشرة:** أنشئ كائنًا من `PngOptions`، عينه إلى الصورة، واستدعِ `image.save("output.png", pngOptions)` لكتابة الملف المحوَّل بصيغة PNG.

`PngOptions` يحدد إعدادات تصدير PNG مثل مستوى الضغط وعمق اللون. أخيرًا، صدّر الصورة المعاد تحجيمها إلى صيغة PNG. تُكمل هذه الخطوة سير عمل **convert PSD to PNG**.

عند تشغيل الكود، ستجد ملف PNG بحجم نصف حجم ملف PSD الأصلي، مع نفس الجودة البصرية دون تشويه.

```java
String destName = dataDir + "SimpleResizeImageProportionally_out.png";
image.save(destName, new PngOptions());
```

عند تشغيل الكود، ستجد ملف PNG بحجم نصف حجم ملف PSD الأصلي، مع نفس الجودة البصرية دون تشويه.

## المشكلات الشائعة والحلول

| المشكلة | السبب | الحل |
|-------|-------|-----|
| **OutOfMemoryError** | عدم تخزين PSD مؤقتًا | استدعِ `image.cacheData()` قبل التحجيم |
| **Blank PNG output** | مسار ملف غير صحيح | تحقق من `dataDir` وأذونات الكتابة |
| **Aspect ratio looks off** | استخدام العرض والارتفاع يدويًا | استخدم طرق التحجيم النسبية التي توفرها Aspose.PSD |

## نصائح لتقليل حجم ملف PSD

- **قم بقص الطبقات غير الضرورية** قبل تحميل الملف.  
- **أعد التحجيم بنسبية** كما هو موضح أعلاه لتقليل الأبعاد مبكرًا.  
- **احفظ كـ PNG بعمق بت مناسب** لتجنب البيانات الزائدة.

## الأسئلة المتكررة

**س: هل Aspose.PSD متوافق مع جميع صيغ الصور؟**  
ج: يدعم Aspose.PSD صيغ PSD، PNG، JPEG، BMP، GIF، والعديد غيرها. راجع القائمة الكاملة في [الوثائق](https://reference.aspose.com/psd/java/). للحصول على مرجع API كامل، راجع الدليل **هنا**.

**س: هل يمكنني استخدام Aspose.PSD في المشاريع التجارية؟**  
ج: نعم. يمكنك شراء ترخيص تجاري من [متجر Aspose](https://purchase.aspose.com/buy).

**س: هل تتوفر تراخيص مؤقتة للاختبار؟**  
ج: بالتأكيد – اطلب ترخيصًا مؤقتًا [هنا](https://purchase.aspose.com/temporary-license/) لأغراض التقييم.

**س: أين يمكنني العثور على دعم المجتمع؟**  
ج: منتدى [Aspose.PSD](https://forum.aspose.com/c/psd/34) مكان رائع لطرح الأسئلة ومشاركة الحلول.

**س: كيف يمكنني الوصول إلى مرجع API الكامل؟**  
ج: الوثائق التفصيلية للـ API متاحة [هنا](https://reference.aspose.com/psd/java/).

## الخلاصة

أنت الآن تعرف كيف **تحول PSD إلى PNG**، **تعيد تحجيم الصورة بنسبية**، وتدير التخزين المؤقت بفعالية باستخدام Aspose.PSD للـ Java. دمج هذه الخطوات في تطبيقاتك يضمن معالجة صور سريعة وعالية الجودة دون الاعتماد على تثبيت Photoshop. هذا النهج **aspose psd java** هو جزء موثوق من أي **java image processing tutorial** ويساعدك على التحكم في حجم ملفات PSD مع الحفاظ على الدقة البصرية.

---

**Last Updated:** 2026-06-23  
**Tested With:** Aspose.PSD 24.12 for Java  
**Author:** Aspose

{{< blocks/products/products-backtop-button >}}

## الدروس ذات الصلة

- [إعادة تحجيم بسيطة باستخدام Aspose.PSD – مكتبة معالجة الصور للـ Java](/psd/java/basic-image-operations/simple-resizing/)
- [إعادة تحجيم صورة Java - باستخدام تعداد نوع التحجيم في Aspose.PSD للـ Java](/psd/java/advanced-image-manipulation/resizing-with-resize-type-enumeration/)
- [تحجيم صورة عالي الجودة باستخدام Resampler بيكوبك في Aspose.PSD للـ Java](/psd/java/advanced-image-manipulation/implement-bicubic-resampler/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}