---
date: 2026-06-03
description: احفظ ملف PSD كـ PNG على القرص بسهولة باستخدام Aspose.PSD for Java. مكتبة
  Java قوية لمعالجة ملفات PSD.
keywords:
- save psd as png
- convert psd to png
- export psd to png
- save image file java
linktitle: حفظ الصور على القرص
schemas:
- author: Aspose
  dateModified: '2026-06-03'
  description: Effortlessly save PSD as PNG to disk using Aspose.PSD for Java. A powerful
    Java library for PSD file manipulation.
  headline: Save PSD as PNG with Aspose.PSD for Java
  type: TechArticle
- description: Effortlessly save PSD as PNG to disk using Aspose.PSD for Java. A powerful
    Java library for PSD file manipulation.
  name: Save PSD as PNG with Aspose.PSD for Java
  steps:
  - name: Define Your Document Directory
    text: 'Set the path for your document directory, where your PSD file is located:'
  - name: Specify Source and Destination Paths
    text: 'Define the paths for your source PSD file and the destination file where
      the image will be saved:'
  - name: Load PSD Image
    text: 'Load the PSD image using Aspose.PSD:'
  - name: Save Image with Options
    text: '`PsdImage` is Aspose.PSD''s core class that represents a Photoshop document
      in memory. Cast the loaded image to a `PsdImage` and save it as a PNG file:
      Repeat these steps for each image you want to save, ensuring a seamless process
      with Aspose.PSD.'
  type: HowTo
- questions:
  - answer: Yes, Aspose.PSD for Java supports various formats, including JPEG, BMP,
      TIFF, and more.
    question: Can I use Aspose.PSD for Java with other image formats?
  - answer: Yes, you can explore a free trial of Aspose.PSD for Java by visiting [this
      link](https://releases.aspose.com/).
    question: Is there a free trial available for Aspose.PSD for Java?
  - answer: Refer to the [documentation](https://reference.aspose.com/psd/java/) for
      detailed information on Aspose.PSD for Java.
    question: Where can I find comprehensive documentation for Aspose.PSD for Java?
  - answer: Visit the [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) for community
      support and discussions.
    question: How can I get support for Aspose.PSD for Java?
  - answer: Yes, you can obtain a temporary license [here](https://purchase.aspose.com/temporary-license/).
    question: Are temporary licenses available for Aspose.PSD for Java?
  type: FAQPage
second_title: Aspose.PSD Java API
title: حفظ ملف PSD كـ PNG باستخدام Aspose.PSD for Java
url: /ar/java/advanced-techniques/save-images-to-disk/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# حفظ PSD كـ PNG باستخدام Aspose.PSD للـ Java

## مقدمة

**Save PSD as PNG** هو مطلب شائع عند العمل مع ملفات Photoshop في تطبيقات Java. باستخدام Aspose.PSD للـ Java يمكنك تحويل أي طبقة PSD أو المستند بالكامل إلى صورة PNG ببضع أسطر من الشيفرة فقط. يشرح هذا الدليل الخطوات الدقيقة، ويوضح لماذا المكتبة مثالية لهذا الغرض، ويظهر كيفية معالجة صور متعددة بكفاءة.

## إجابات سريعة
- **ما المكتبة التي تتعامل مع تحويل PSD إلى PNG؟** Aspose.PSD for Java.
- **كم عدد أسطر الشيفرة المطلوبة؟** عادةً سطران بعد تحميل الملف.
- **هل يمكنني معالجة ملفات PSD الكبيرة؟** نعم – الـ API يبث البيانات ويدعم الملفات التي تزيد عن 2 GB.
- **هل أحتاج إلى ترخيص للتطوير؟** النسخة التجريبية المجانية تعمل للاختبار؛ الترخيص مطلوب للإنتاج.
- **ما إصدارات Java المدعومة؟** Java 8 حتى Java 21 (LTS والأحدث).

## ما هو “حفظ PSD كـ PNG”؟

حفظ PSD كـ PNG يعني تصدير بيانات الصورة النقطية من مستند Photoshop إلى تنسيق PNG القابل للنقل مع الحفاظ على الشفافية، ودقة الألوان، وأي ملفات تعريف ألوان مدمجة. يمكن استخدام PNG الناتج عبر تطبيقات الويب، والهواتف المحمولة، وسطح المكتب، حيث يوفر ضغطًا غير فقدانٍ وتوافقًا واسعًا مع عارضات ومحررات الصور.

## لماذا تستخدم Aspose.PSD للـ Java لتحويل PSD إلى PNG؟

Aspose.PSD يدعم **أكثر من 30 تنسيقًا للإدخال والإخراج** ويمكنه **معالجة ملفات تصل إلى 2 GB** دون تحميل المستند بالكامل في الذاكرة، مما يحقق تحويلًا أسرع حتى **3×** مقارنةً بالمعالجة اليدوية للبكسلات. كما أن المكتبة تحتفظ بتأثيرات الطبقات، والأقنعة، وملفات تعريف الألوان تلقائيًا، مما يلغي الحاجة إلى المعالجة اللاحقة.

## المتطلبات المسبقة

قبل الغوص في الدليل، تأكد من توفر المتطلبات التالية:
- مكتبة Aspose.PSD للـ Java: قم بتنزيل وتثبيت المكتبة من [صفحة الإصدار](https://releases.aspose.com/psd/java/).
- بيئة تطوير Java: تأكد من أن لديك بيئة تطوير Java تعمل على جهازك.

## استيراد الحزم

الاستيرادات التالية تجلب الفئات الأساسية من Aspose.PSD اللازمة لتحميل ملفات PSD وتكوين خيارات تصدير PNG.  
```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PngOptions;
```

دعونا نفصل عملية حفظ الصور إلى خطوات متعددة لفهم واضح وشامل.

## كيفية حفظ PSD كـ PNG باستخدام Aspose.PSD للـ Java؟

الفئة `PsdImage` تمثل مستند Photoshop في الذاكرة، بينما `ImageSaveOptions` مع `SaveFormat` يحددان تنسيق الإخراج المطلوب وإعدادات الضغط. من خلال تحميل PSD واستدعاء طريقة الحفظ مع خيارات PNG، يمكنك تحويل الملف في نداء واحد فعال.

حمّل ملف PSD باستخدام `new PsdImage("source.psd")` واستدعِ `psd.save("output.png", ImageSaveOptions.createSaveOptions(SaveFormat.Png))`. هذا النداء ذو السطر الواحد يتعامل مع تسطيح الطبقات، والحفاظ على ملف تعريف اللون، وضغط PNG تلقائيًا. للعمليات الدفعية، ضع النداء داخل حلقة تكرار على ملفات المصدر الخاصة بك.

### الخطوة 1: تحديد دليل المستند الخاص بك

حدد المسار لدليل المستندات الخاص بك، حيث يقع ملف PSD الخاص بك:
```java
String dataDir = "Your Document Directory";
```

### الخطوة 2: تحديد مسارات المصدر والوجهة

حدد المسارات لملف PSD المصدر وملف الوجهة الذي سيتم حفظ الصورة فيه:
```java
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "result.png";
```

### الخطوة 3: تحميل صورة PSD

حمّل صورة PSD باستخدام Aspose.PSD:
```java
Image image = Image.load(sourceFile);
```

### الخطوة 4: حفظ الصورة مع الخيارات

`PsdImage` هي الفئة الأساسية في Aspose.PSD التي تمثل مستند Photoshop في الذاكرة. قم بتحويل الصورة المحملة إلى `PsdImage` واحفظها كملف PNG:
```java
PsdImage psdImage = (PsdImage)image;
psdImage.save(destName, new PngOptions());
```

كرر هذه الخطوات لكل صورة تريد حفظها، لضمان عملية سلسة مع Aspose.PSD.

## المشكلات الشائعة والحلول

- **OutOfMemoryError على الملفات الكبيرة** – فعّل البث باستخدام `PsdImage.load(inputStream, true)` لتجنب تحميل الملف بالكامل إلى الذاكرة.
- **غياب الشفافية** – تأكد من استخدام `PngOptions` مع `ColorType = PngColorType.Rgba` للحفاظ على قناة ألفا.
- **ألوان غير صحيحة** – تحقق من أن ملف تعريف اللون في PSD المصدر مدمج؛ Aspose.PSD يطبقه تلقائيًا أثناء التصدير.

## الأسئلة المتكررة

**س: هل يمكنني استخدام Aspose.PSD للـ Java مع صيغ صور أخرى؟**  
ج: نعم، Aspose.PSD للـ Java يدعم صيغًا متعددة، بما في ذلك JPEG، BMP، TIFF، وغيرها.

**س: هل هناك نسخة تجريبية مجانية متاحة لـ Aspose.PSD للـ Java؟**  
ج: نعم، يمكنك تجربة نسخة تجريبية مجانية من Aspose.PSD للـ Java بزيارة [هذا الرابط](https://releases.aspose.com/).

**س: أين يمكنني العثور على وثائق شاملة لـ Aspose.PSD للـ Java؟**  
ج: راجع [الوثائق](https://reference.aspose.com/psd/java/) للحصول على معلومات مفصلة حول Aspose.PSD للـ Java.

**س: كيف يمكنني الحصول على دعم لـ Aspose.PSD للـ Java؟**  
ج: زر [منتدى Aspose.PSD](https://forum.aspose.com/c/psd/34) للحصول على دعم المجتمع والنقاشات.

**س: هل تتوفر تراخيص مؤقتة لـ Aspose.PSD للـ Java؟**  
ج: نعم، يمكنك الحصول على ترخيص مؤقت [هنا](https://purchase.aspose.com/temporary-license/).

**س: هل تدعم المكتبة تصدير طبقة واحدة كـ PNG؟**  
ج: بالتأكيد – استخرج كائن `Layer` المطلوب واستدعِ `layer.save("layer.png", ImageSaveOptions.createSaveOptions(SaveFormat.Png))`.

**س: هل يمكنني التحكم في مستوى ضغط PNG؟**  
ج: نعم، اضبط `PngOptions.setCompressionLevel(int level)` حيث يتراوح `level` بين 0 (بدون ضغط) إلى 9 (أقصى ضغط).

## الخلاصة

حفظ PSD كـ PNG باستخدام Aspose.PSD للـ Java هو عملية بسيطة لكنها قوية. باتباع الخطوات أعلاه، يمكنك دمج تصدير صور عالي الأداء في تطبيقات Java الخاصة بك، ومعالجة الملفات الكبيرة بكفاءة، والحفاظ على كامل الدقة البصرية.

---

**آخر تحديث:** 2026-06-03  
**تم الاختبار مع:** Aspose.PSD 24.10 for Java  
**المؤلف:** Aspose

## دروس ذات صلة

- [تحويل PSD إلى صيغ صور نقطية مع Aspose.PSD للـ Java](/psd/java/advanced-techniques/convert-psd-to-raster-formats/)
- [حفظ الصور إلى تدفق مع Aspose.PSD للـ Java](/psd/java/advanced-techniques/save-images-to-stream/)
- [حفظ PSD كـ PNG وتطبيق ظل إسقاط Rendering في Aspose.PSD للـ Java](/psd/java/advanced-image-manipulation/rendering-drop-shadow/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}