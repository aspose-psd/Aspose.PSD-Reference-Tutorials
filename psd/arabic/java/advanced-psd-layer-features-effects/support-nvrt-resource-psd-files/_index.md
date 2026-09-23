---
date: 2026-09-23
description: تعلم كيفية تحميل ملفات PSD، قراءة الطبقات، واستخراج مورد Nvrt من طبقات
  تعديل الانعكاس باستخدام Aspose.PSD للغة Java، بالإضافة إلى معالجة دفعة من ملفات
  PSD.
keywords:
- how to load psd
- batch process psd files
- invert adjustment layer java
- nvrt resource extraction
- Aspose.PSD
lastmod: 2026-09-23
linktitle: دعم مورد Nvrt في ملفات PSD باستخدام Java
og_description: تعلم كيفية تحميل ملفات PSD، قراءة الطبقات، واستخراج مورد Nvrt من طبقات
  تعديل الانعكاس باستخدام Aspose.PSD للغة Java. كما يمكنك معرفة كيفية معالجة دفعة
  من ملفات PSD بكفاءة.
og_image_alt: 'Developer guide: Load PSD and extract Nvrt resource using Aspose.PSD
  for Java'
og_title: كيفية تحميل ملفات PSD واستخراج مورد Nvrt باستخدام Aspose.PSD
schemas:
- author: Aspose
  dateModified: '2026-09-23'
  description: Learn how to load PSD files, read layers, and extract the Nvrt resource
    from invert adjustment layers using Aspose.PSD for Java, plus batch process PSD
    files.
  headline: How to load PSD and extract Nvrt resource with Aspose.PSD
  type: TechArticle
- questions:
  - answer: Aspose.PSD for Java is a library that enables developers to create, edit,
      convert, and render PSD files directly from Java code.
    question: What is Aspose.PSD for Java?
  - answer: Yes, a commercial license is required for production use. You can explore
      purchasing options [purchase Aspose.PSD](https://purchase.aspose.com/buy).
    question: Can I use Aspose.PSD in commercial products?
  - answer: 'The complete documentation is available here: [Aspose.PSD Documentation](https://reference.aspose.com/psd/java/).'
    question: Where can I find the documentation for Aspose.PSD?
  - answer: Absolutely! You can get a free trial of Aspose.PSD for Java [download
      free trial](https://releases.aspose.com/).
    question: Is there a free trial available?
  - answer: 'You can ask questions and get support on the Aspose forum: [Aspose Support](https://forum.aspose.com/c/psd/34).'
    question: How can I get support for Aspose.PSD?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- load PSD
- Aspose.PSD
- Java image processing
- invert adjustment layer
- Nvrt resource
title: كيفية تحميل ملفات PSD واستخراج مورد Nvrt باستخدام Aspose.PSD
url: /ar/java/advanced-psd-layer-features-effects/support-nvrt-resource-psd-files/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# كيفية تحميل ملف PSD واستخراج مورد Nvrt من طبقات تعديل الانعكاس باستخدام Java

## إجابات سريعة
- **ما المكتبة التي تتعامل مع ملفات PSD في Java؟** Aspose.PSD for Java  
- **هل يمكنني قراءة طبقات PSD؟** نعم، توفر API وصولًا كاملاً إلى هياكل الطبقات  
- **هل يلزم وجود ترخيص للإنتاج؟** نعم، يلزم الحصول على ترخيص تجاري  
- **ما إصدار JDK المدعوم؟** Java 8 وما فوق  
- **من أين يمكنني تنزيل المكتبة؟** من صفحة التحميل الرسمية لـ Aspose  

## ما هي طبقة تعديل الانعكاس؟
طبقة تعديل الانعكاس تعكس قيم الألوان لكل بكسل تحتها، مما يخلق تأثيرًا سلبيًا فوتوغرافيًا. باستخدام Aspose.PSD، يمكنك اكتشاف هذه الطبقة وقراءتها ومعالجتها دون تحويل الصورة إلى نقطية، وهو مثالي لسلاسل المعالجة الدفعية التي تحتاج إلى تصحيح لون ثابت عبر ملفات متعددة.

## لماذا نستخدم طبقة تعديل الانعكاس مع Aspose.PSD؟
يدعم Aspose.PSD **أكثر من 30 تنسيقًا للإدخال والإخراج** ويمكنه معالجة ملفات تصل إلى **2 GB** دون تحميل المستند بالكامل في الذاكرة، مما يمنحك تحكمًا دقيقًا وفعّالًا في استهلاك الذاكرة عند عكس الألوان. كما أن المكتبة تكشف عن بيانات التعديل، مما يتيح لك أتمتة إزالة أو تعديل تأثير الانعكاس عبر مكتبات تصميم كبيرة.

## كيفية تحميل ملف Photoshop ومعالجة ملفات PSD دفعيًا
حمّل ملف PSD مرة واحدة، افحص طبقاته، وكرر نفس المنطق داخل حلقة **لمعالجة ملفات PSD دفعيًا** بكفاءة. من خلال إنشاء كائن `PsdImage` جديد لكل ملف وتفريغه فورًا، تحافظ على انخفاض استهلاك الذاكرة وتضمن معدل معالجة عالي للعمليات الضخمة.

## المتطلبات المسبقة
قبل البدء في الترميز، تأكد من توفر ما يلي:

- **مجموعة تطوير Java (JDK)** مثبتة (يوصى بـ Java 8+)  
- **بيئة تطوير متكاملة (IDE)** مثل IntelliJ IDEA أو Eclipse أو VS Code  
- **مكتبة Aspose.PSD for Java** – قم بتنزيلها من الموقع الرسمي: [Download Aspose.PSD for Java](https://releases.aspose.com/psd/java/)  
- **معرفة أساسية بـ Java** (الفئات، الكائنات، معالجة الاستثناءات)  

## استيراد الحزم
فئة `PsdImage` هي الكائن الأعلى مستوى في Aspose.PSD الذي يمثل مستند Photoshop واحد في الذاكرة، وتكشف عن الطبقات والموارد للتلاعب.

```java
import com.aspose.psd.Image;
import com.aspose.psd.examples.Utils.Assert;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
import com.aspose.psd.fileformats.psd.layers.LayerResource;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.InvertAdjustmentLayer;
import com.aspose.psd.fileformats.psd.layers.layerresources.NvrtResource;
```

## لماذا قراءة طبقات PSD؟
تمنحك قراءة طبقات PSD نظرة عميقة على بنية المستند، مما يسمح لك بعزل الأصول الفردية، وفهم أي تعديلات تم تطبيقها، وإعادة استخدام المكونات في مشاريع أو تنسيقات أخرى. هذه الرؤية ضرورية للأتمتة، واستخراج الأصول، والحفاظ على اتساق التصميم عبر ملفات متعددة.

- استخراج الأصول الفردية (مثل الأيقونات، الأقنعة) لإعادة الاستخدام  
- تحديد الطبقات التي تحتوي على طبقة تعديل الانعكاس لفهم تعديلات الصورة  
- أتمتة المعالجة الدفعية لملفات التصميم  

## الخطوة 1: تحديد دليل المصدر الخاص بك
حدد المجلد الذي يحتوي على ملفات PSD التي تريد العمل معها.

```java
String sourceDir = "Your Source Directory";
String inPsdFilePath = sourceDir + "InvertAdjustmentLayer.psd";
```

استبدل `"Your Source Directory"` بالمسار الفعلي على جهازك.

## الخطوة 2: تحميل ملف PSD
`Image.load()` يحمل ملفًا إلى كائن `PsdImage`، محللاً بنية PSD بحيث يمكنك فحص الطبقات والموارد وبيانات التعديل.

```java
PsdImage psdImage = (PsdImage)Image.load(inPsdFilePath);
```

تفتح الطريقة الملف وتجهّزه للفحص.

## الخطوة 3: تهيئة متغير مورد Nvrt
فئة `NvrtResource` تمثل بيانات تعديل الانعكاس المخزنة داخل ملف Photoshop.

```java
NvrtResource nvrtResource = null;
```

## الخطوة 4: البحث عن طبقة تعديل الانعكاس
`InvertAdjustmentLayer` هو نوع الطبقة المحدد الذي يطبق تأثير اللون السلبي. من خلال التكرار عبر مجموعة الطبقات يمكنك تحديد هذه الطبقة ثم استرجاع `NvrtResource` المرتبط بها.

```java
try {
    for (Layer layer : psdImage.getLayers()) {
        if (layer instanceof InvertAdjustmentLayer) {
            for (LayerResource layerResource : layer.getResources()) {
                if (layerResource instanceof NvrtResource) {
                    // The NvrtResource is found
                    nvrtResource = (NvrtResource)layerResource;
                    break;
                }
            }
        }
    }
} finally {
    psdImage.dispose();
}
```

يضمن كتلة `finally` التخلص من صورة PSD، مما يحافظ على نظافة استهلاك الذاكرة.

## الخطوة 5: التحقق من مورد Nvrt
تأكد من أن المورد تم تحديده بنجاح عن طريق فحص المتغير الذي ملأته في الخطوة السابقة.

```java
Assert.isNotNull(nvrtResource);
```

إذا نجحت العبارة الشرطية، فقد قرأت طبقات PSD بنجاح واستخراجت مورد Nvrt.

## الأخطاء الشائعة والنصائح
- **تحقق من القيم الفارغة:** تأكد دائمًا من أن `psdImage` وكائنات الطبقة ليست null قبل الوصول إليها.  
- **التخلص من الموارد:** نسيان `psdImage.dispose()` قد يؤدي إلى تسرب الذاكرة في التطبيقات طويلة التشغيل.  
- **مشكلات مسار الملف:** استخدم مسارات مطلقة أو تأكد من ضبط دليل العمل بشكل صحيح لتجنب `FileNotFoundException`.  
- **ملاحظة المعالجة الدفعية:** عند التكرار على العديد من الملفات، أعد إنشاء `PsdImage` داخل الحلقة وتخلص منه فور الانتهاء من معالجة كل ملف.

## الخلاصة
أنت الآن تعرف **كيفية تحميل ملفات PSD**، قراءة طبقاتها، واستخراج مورد طبقة تعديل الانعكاس **Nvrt** باستخدام Java وAspose.PSD. هذه الأساسيات تتيح لك بناء أدوات أتمتة رسومية قوية، **معالجة ملفات PSD دفعيًا**، أو دمج بيانات Photoshop في سير عمل أوسع.

## الأسئلة المتكررة

**س: ما هو Aspose.PSD for Java؟**  
ج: Aspose.PSD for Java هي مكتبة تمكّن المطورين من إنشاء وتحرير وتحويل وعرض ملفات PSD مباشرةً من خلال كود Java.

**س: هل يمكنني استخدام Aspose.PSD في المنتجات التجارية؟**  
ج: نعم، يلزم الحصول على ترخيص تجاري للاستخدام في الإنتاج. يمكنك استكشاف خيارات الشراء [purchase Aspose.PSD](https://purchase.aspose.com/buy).

**س: أين يمكنني العثور على وثائق Aspose.PSD؟**  
ج: الوثائق الكاملة متاحة هنا: [Aspose.PSD Documentation](https://reference.aspose.com/psd/java/).

**س: هل هناك نسخة تجريبية مجانية متاحة؟**  
ج: بالتأكيد! يمكنك الحصول على نسخة تجريبية مجانية من Aspose.PSD for Java [download free trial](https://releases.aspose.com/).

**س: كيف يمكنني الحصول على الدعم لـ Aspose.PSD؟**  
ج: يمكنك طرح الأسئلة والحصول على الدعم في منتدى Aspose: [Aspose Support](https://forum.aspose.com/c/psd/34).

**آخر تحديث:** 2026-09-23  
**تم الاختبار مع:** Aspose.PSD for Java 24.11 (أحدث نسخة عند كتابة هذا المقال)  
**المؤلف:** Aspose

## دروس ذات صلة

- [مكتبة معالجة الصور Java: طبقة الانعكاس باستخدام Aspose.PSD](/psd/java/advanced-image-manipulation/invert-adjustment-layer/)
- [إضافة طبقة تعديل المستوى إلى ملفات PSD باستخدام Aspose.PSD for Java](/psd/java/modifying-converting-psd-images/add-level-adjustment-layer-psd/)
- [قراءة طبقات PSD مع Aspose.PSD for Java – استخدام محمل بيانات خام مخصص](/psd/java/advanced-psd-layer-features-effects/use-custom-raw-data-loader-psd-files/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}