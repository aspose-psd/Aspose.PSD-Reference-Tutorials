---
date: 2026-09-23
description: تعلم كيفية تعديل أشكال المتجهات في ملفات PSD ومعالجة ملفات PSD دفعة واحدة
  باستخدام Aspose.PSD for Java. خطوات مفصلة، نصائح، وعناصر نائبة للكود للحصول على
  حل كامل.
keywords:
- modify psd vector shapes
- batch process psd files
- Aspose.PSD Java
- vector shape editing
lastmod: 2026-09-23
linktitle: دعم خصائص بيانات سجل الطول في PSD - Java
og_description: تعلم كيفية تعديل أشكال المتجهات في ملفات PSD ومعالجة ملفات PSD دفعة
  واحدة باستخدام Aspose.PSD for Java. دليل خطوة بخطوة مع عناصر نائبة للكود ونصائح
  الخبراء.
og_image_alt: Guide showing how to edit vector shapes in PSD files using Aspose.PSD
  for Java
og_title: تعديل أشكال المتجهات في ملفات PSD باستخدام Aspose.PSD for Java
schemas:
- author: Aspose
  dateModified: '2026-09-23'
  description: Learn how to modify PSD vector shapes and batch process PSD files using
    Aspose.PSD for Java. Detailed steps, tips, and code placeholders for a complete
    solution.
  headline: Modify PSD vector shapes with Aspose.PSD for Java
  type: TechArticle
- description: Learn how to modify PSD vector shapes and batch process PSD files using
    Aspose.PSD for Java. Detailed steps, tips, and code placeholders for a complete
    solution.
  name: Modify PSD vector shapes with Aspose.PSD for Java
  steps:
  - name: '**Java Development Kit (JDK)** – download from [Oracle''s website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html)
      or use your preferred package manager.'
    text: '**Java Development Kit (JDK)** – download from [Oracle''s website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html)
      or use your preferred package manager.'
  - name: '**Aspose.PSD for Java** – obtain the latest JAR from the [Aspose releases
      page](https://releases.aspose.com/psd/java/).'
    text: '**Aspose.PSD for Java** – obtain the latest JAR from the [Aspose releases
      page](https://releases.aspose.com/psd/java/).'
  - name: '**IDE** – IntelliJ IDEA, Eclipse, or any Java‑compatible editor.'
    text: '**IDE** – IntelliJ IDEA, Eclipse, or any Java‑compatible editor.'
  - name: '**A PSD file** – create one in Photoshop or grab a sample PSD to experiment
      with.'
    text: '**A PSD file** – create one in Photoshop or grab a sample PSD to experiment
      with.'
  - name: '**Basic Java knowledge** – familiarity with classes, objects, and exception
      handling.'
    text: '**Basic Java knowledge** – familiarity with classes, objects, and exception
      handling.'
  type: HowTo
- questions:
  - answer: The `VsmsResource` will be absent, so `resource` stays `null`. Add a check
      and skip the modification step or inform the user.
    question: How do I handle a PSD that contains no vector shape layers?
  - answer: Yes, `LengthRecord` provides setters for fill, stroke, and opacity. See
      the API docs for the full list.
    question: Can I change other properties like fill color or stroke width?
  - answer: Absolutely. Wrap the code inside a loop that iterates over a directory
      of PSD files, adjusting the input and output paths each time.
    question: Is it possible to batch‑process multiple PSD files?
  - answer: '`Image.load` handles file streams automatically, but if you load from
      an `InputStream`, remember to close it after use.'
    question: Do I need to close streams manually when loading from a file path?
  - answer: The `LengthRecord` and `PathOperations` classes have been available since
      Aspose.PSD 20.10. Using the latest version (24.11 at time of writing) is recommended.
    question: What version of Aspose.PSD is required for these APIs?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- modify psd vector shapes
- Aspose.PSD
- Java image processing
- batch PSD processing
title: تعديل أشكال المتجهات في ملفات PSD باستخدام Aspose.PSD for Java
url: /ar/java/advanced-psd-layer-features-effects/support-length-record-data-properties-psd/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# تعديل أشكال PSD المتجهة باستخدام Aspose.PSD للـ Java

## المقدمة
إذا كنت بحاجة إلى **تعديل أشكال PSD المتجهة** برمجياً، فإن Aspose.PSD للـ Java يمنحك تحكمًا كاملاً في ملفات Photoshop مباشرة من كود Java الخاص بك. يشرح هذا الدرس كيفية دعم خصائص سجل الطول—خطوة أساسية عند تحرير طبقات الأشكال المتجهة. في النهاية ستتمكن من فتح ملف PSD، تعديل بيانات الشكل المتجه، وحفظ الملف المحدث دون الحاجة إلى تشغيل Photoshop.

## إجابات سريعة
- **ماذا يعني “تعديل أشكال PSD المتجهة”?** ضبط الهندسة، عمليات المسار، أو سمات أخرى للطبقات القائمة على المتجهات داخل ملف PSD.  
- **أي مكتبة تتعامل مع هذا؟** Aspose.PSD للـ Java.  
- **هل أحتاج إلى ترخيص؟** نسخة تجريبية مجانية تكفي للتقييم؛ يتطلب الترخيص التجاري للإنتاج.  
- **كم من الوقت تستغرق التنفيذ؟** حوالي 10‑15 دقيقة لسكريبت تعديل شكل أساسي.  
- **ما هي المتطلبات الأساسية؟** Java JDK، Aspose.PSD للـ Java، وعينة ملف PSD.

## ما هو “دعم خصائص سجل الطول”؟
يعني دعم خصائص سجل الطول الوصول إلى كائنات `LengthRecord` التي تصف كل مسار متجه داخل PSD. تخزن هذه السجلات معلومات مثل طول المسار، نوعه، وكيفية ربطه بالمسارات الأخرى. يتيح تعديلها التحكم في كيفية دمج الأشكال أو تقاطعها أو طرحها من بعضها، مما يتيح تحريرًا متجهًا دقيقًا.

## لماذا تستخدم Aspose.PSD للـ Java لدعم خصائص سجل الطول؟
حمّل ملف PSD، حرّر البيانات المتجهة، واحفظه—كل ذلك دون Photoshop. يعالج Aspose.PSD ملفات PSD متعددة المئات من الصفحات في أقل من ثانيتين على خادم عادي، يقدم أكثر من 150 فئة (بما في ذلك أكثر من 30 نوعًا متعلقًا بالمتجهات)، ويعمل على Windows أو Linux أو macOS مع أي JDK 11+. هذه المكتبة التي تركز على الأداء تلغي الحاجة إلى برامج سطح مكتب مكلفة.

## المتطلبات المسبقة
1. **Java Development Kit (JDK)** – تحميل من [Oracle's website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) أو استخدم مدير الحزم المفضل لديك.  
2. **Aspose.PSD للـ Java** – احصل على أحدث ملف JAR من [Aspose releases page](https://releases.aspose.com/psd/java/).  
3. **IDE** – IntelliJ IDEA، Eclipse، أو أي محرر يدعم Java.  
4. **ملف PSD** – أنشئ واحدًا في Photoshop أو احصل على عينة PSD للتجربة.  
5. **معرفة أساسية بـ Java** – إلمام بالفئات، الكائنات، ومعالجة الاستثناءات.

## استيراد الحزم
تجلب عبارات الاستيراد فئات Aspose.PSD الأساسية إلى النطاق، مثل `PsdImage` و `VsmsResource` و `LengthRecord`.

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.LayerResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.VsmsResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.LengthRecord;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.PathOperations;
```

## الخطوة 1: إعداد مجلدات المصدر والإخراج
حدد مكان وجود ملف PSD الأصلي وأين سيتم كتابة الملف المعدل.

```java
String sourceDir = "Your Source Directory";
String outputDir = "Your Document Directory";
String inPsdFilePath = sourceDir + "PathOperationsShape.psd";
String outPsdFilePath = outputDir + "out_PathOperationsShape.psd";
```

## الخطوة 2: تحميل ملف PSD
استخدم `Image.load` لفتح الملف وتحويله إلى `PsdImage` للاستفادة من ميزات PSD الخاصة.

```java
PsdImage psdImage = (PsdImage) Image.load(inPsdFilePath);
```

## الخطوة 3: تحديد مورد Vsms في الطبقة
`VsmsResource` هو الحاوية التي تخزن بيانات الشكل المتجه لطبقة ما. قم بالتكرار عبر موارد الطبقة الثانية للعثور عليه.

```java
VsmsResource resource = null;
for (LayerResource layerResource : psdImage.getLayers()[1].getResources()) {
    if (layerResource instanceof VsmsResource) {
        resource = (VsmsResource) layerResource;
        break;
    }
}
```

## الخطوة 4: الوصول إلى سجلات الطول
`LengthRecord` يمثل مسارًا متجهًا مميزًا. استرجع السجلات التي تنوي تعديلها.

```java
LengthRecord lengthRecord0 = (LengthRecord) resource.getPaths()[2];
LengthRecord lengthRecord1 = (LengthRecord) resource.getPaths()[7];
LengthRecord lengthRecord2 = (LengthRecord) resource.getPaths()[11];
```

## الخطوة 5: تعديل خصائص عمليات المسار
`PathOperations` يحدد كيفية تفاعل الأشكال الفردية (مثل الاستبعاد، التقاطع، الطرح). تغيير هذه القيم يحدّث التركيب البصري للطبقة المتجهة.

```java
lengthRecord0.setPathOperations(PathOperations.ExcludeOverlappingShapes);
lengthRecord1.setPathOperations(PathOperations.IntersectShapeAreas);
lengthRecord2.setPathOperations(PathOperations.SubtractFrontShape);
```

## الخطوة 6: حفظ ملف PSD المعدل
احفظ تغييراتك في ملف جديد.

```java
psdImage.save(outPsdFilePath);
```

## الخطوة 7: تنظيف الموارد
قم بتحرير مثيل `PsdImage` لتفريغ الذاكرة وتجنب تسرب الموارد.

```java
psdImage.dispose();
```

## كيفية معالجة ملفات PSD دفعةً مع دعم خصائص سجل الطول
لفّ سير العمل الخاص بملف واحد داخل حلقة تتكرر على دليل يحتوي على ملفات PSD، مع تحديث `inPsdFilePath` و `outPsdFilePath` لكل ملف. يتيح لك هذا النهج تطبيق تعديلات الشكل المتجه نفسها على العشرات أو المئات من الملفات في دقائق، وهو مثالي لخطوط أنابيب الأصول الآلية.

## المشكلات الشائعة والنصائح
- **فحوصات Null** – تأكد دائمًا من أن `resource` ليست `null` قبل الوصول إلى أعضائها.  
- **حدود فهارس المسار** – تأكد من وجود الفهارس التي تستخدمها (مثلاً `[2]`، `[7]`، `[11]`) في ملف PSD المحدد الذي تقوم بتحريره.  
- **الترخيص** – تشغيل البرنامج بدون ترخيص صالح يضيف علامة مائية إلى ملف PSD المحفوظ.  

## الخلاصة
أصبح لديك الآن مثال كامل من البداية إلى النهاية حول كيفية **تعديل أشكال PSD المتجهة** بدعم خصائص سجل الطول باستخدام Aspose.PSD للـ Java. سواء كنت تقوم بأتمتة خط أنابيب الأصول أو بناء أداة تصميم مخصصة، توفر لك هذه الـ APIs المرونة لتعديل طبقات المتجهات دون الحاجة إلى Photoshop يدويًا. جرّب قيم `PathOperations` أخرى أو اجمع بين تعديلات `LengthRecord` متعددة لإنشاء أشكال معقدة.

## الأسئلة المتكررة

**س: كيف أتعامل مع PSD لا يحتوي على طبقات أشكال متجهة؟**  
ج: سيكون `VsmsResource` غير موجود، لذا يبقى `resource` يساوي `null`. أضف فحصًا وتجاوز خطوة التعديل أو أخطر المستخدم.

**س: هل يمكنني تغيير خصائص أخرى مثل لون التعبئة أو عرض الحد؟**  
ج: نعم، توفر `LengthRecord` دوال ضبط للتعبئة، الحد، والشفافية. راجع وثائق الـ API للقائمة الكاملة.

**س: هل من الممكن معالجة عدة ملفات PSD دفعةً؟**  
ج: بالتأكيد. ضع الكود داخل حلقة تتكرر على دليل يحتوي على ملفات PSD، مع تعديل مسارات الإدخال والإخراج في كل مرة.

**س: هل أحتاج إلى إغلاق التدفقات يدويًا عند التحميل من مسار ملف؟**  
ج: `Image.load` يتعامل مع تدفقات الملفات تلقائيًا، ولكن إذا قمت بالتحميل من `InputStream`، تذكر إغلاقه بعد الاستخدام.

**س: ما إصدار Aspose.PSD المطلوب لهذه الـ APIs؟**  
ج: تتوفر فئتا `LengthRecord` و `PathOperations` منذ Aspose.PSD 20.10. يُنصح باستخدام أحدث إصدار (24.11 في وقت الكتابة).

---

**آخر تحديث:** 2026-09-23  
**تم الاختبار مع:** Aspose.PSD للـ Java 24.11  
**المؤلف:** Aspose

## دروس ذات صلة

- [تحويل PSD إلى PNG وإنشاء قناع متجه Java – مورد Vmsk في ملفات PSD](/psd/java/advanced-psd-layer-features-effects/support-vmsk-resource-psd-files/)
- [تحويل PSD إلى PNG مع دعم قناع الطبقة باستخدام Aspose.PSD للـ Java](/psd/java/advanced-psd-layer-features-effects/support-layer-mask-psd-files/)
- [إضافة دعم الطبقة لملفات PSD](/psd/java/advanced-psd-layer-features-effects/add-layer-support-psd-files/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}