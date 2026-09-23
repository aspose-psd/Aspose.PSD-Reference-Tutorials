---
date: 2026-09-23
description: تعلم كيفية تصدير PSD إلى PNG مع الأقنعة باستخدام Aspose.PSD for Java،
  مع الحفاظ على شفافية الطبقات ودعم المعالجة الدفعية.
keywords:
- how to export psd to png
- layer mask support
- aspose.psd java
- java image conversion
- png export
lastmod: 2026-09-23
linktitle: كيفية تصدير PSD إلى PNG مع الأقنعة باستخدام Aspose.PSD for Java
og_description: تعلم كيفية تصدير PSD إلى PNG مع الأقنعة باستخدام Aspose.PSD for Java،
  مع الحفاظ على شفافية الطبقات ودعم المعالجة الدفعية. يوضح لك هذا الدليل خطوة بخطوة
  الشيفرة الدقيقة والخيارات.
og_image_alt: 'Developer guide: Export PSD to PNG with layer masks using Aspose.PSD
  for Java'
og_title: كيفية تصدير PSD إلى PNG مع الأقنعة باستخدام Aspose.PSD for Java
schemas:
- author: Aspose
  dateModified: '2026-09-23'
  description: Learn how to export PSD to PNG with masks via Aspose.PSD for Java,
    preserving layer transparency and supporting batch processing.
  headline: How to export PSD to PNG with masks via Aspose.PSD for Java
  type: TechArticle
- description: Learn how to export PSD to PNG with masks via Aspose.PSD for Java,
    preserving layer transparency and supporting batch processing.
  name: How to export PSD to PNG with masks via Aspose.PSD for Java
  steps:
  - name: set up your project directory
    text: Define the folder that contains the source PSD and will hold the output
      PNG. This variable is used throughout the tutorial to build absolute file paths.
      Replace `Your Document Directory` with the absolute path on your machine.
  - name: specify the source PSD file
    text: Point to the PSD you want to convert. In this example we use a file that
      contains a complex mask, demonstrating full alpha‑channel preservation.
  - name: define the export path for the PNG
    text: Tell the program where to write the resulting PNG file. The path can be
      the same folder as the source or a dedicated output location.
  - name: load the PSD file
    text: The `Image.load` method reads the file into a `PsdImage` object, which gives
      you programmatic access to layers, masks, and image data.
  - name: set up PNG export options
    text: Configure the PNG exporter to keep the alpha channel, which is crucial for
      layer mask transparency. The `PngExportOptions` class also lets you control
      compression level and color type.
  - name: save the PNG file
    text: Perform the conversion by calling the `save` method with the configured
      options. The resulting file will contain the original PSD’s masked regions as
      transparent pixels. If everything is set up correctly, you’ll find `MaskComplex.png`
      in your output folder, displaying the original PSD’s masked regio
  type: HowTo
- questions:
  - answer: A layer mask controls the transparency of a layer, allowing you to hide
      or reveal parts of the image without permanently erasing pixels.
    question: What is a layer mask in PSD files?
  - answer: While Aspose.PSD requires code, graphic designers can use Photoshop or
      other GUI tools for manual conversion.
    question: Can I work with PSD files without programming knowledge?
  - answer: A free trial is available from the download page; a paid license is required
      for commercial projects.
    question: Is Aspose.PSD free to use?
  - answer: The conversion still works; the resulting PNG will simply lack masked
      transparency effects.
    question: What happens if my PSD file contains no masks?
  - answer: Visit the [support forum](https://forum.aspose.com/c/psd/34) for help
      from Aspose experts and the community.
    question: Where can I get support if I have issues?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- convert PSD
- Aspose.PSD
- Java image conversion
- layer masks
- PNG export
title: كيفية تصدير PSD إلى PNG مع الأقنعة باستخدام Aspose.PSD for Java
url: /ar/java/advanced-psd-layer-features-effects/support-layer-mask-psd-files/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# تصدير PSD إلى PNG مع دعم قناع الطبقة في Java

## مقدمة
إذا كنت تبحث عن **how to export PSD to PNG** مع الحفاظ على أقنعة الطبقة المعقدة، فقد وجدت المكان المناسب. عندما تحتاج إلى **export PSD to PNG** والحفاظ على هذه الأقنعة سليمة، يمكن لمكتبة Java موثوقة أن توفر لك ساعات من العمل اليدوي. في هذا البرنامج التعليمي سنستعرض العملية بالكامل باستخدام **Aspose.PSD Java API**، مع تغطية كل شيء من تحميل ملف PSD إلى حفظه كصورة PNG مع دعم كامل لقناة ألفا. سواء كنت تبني أداة معالجة دفعات، أو خط أنابيب أصول مؤتمت، أو تحتاج فقط إلى سكريبت تحويل سريع، ستجد خطوات واضحة ومحادثة تجعل المهمة بسيطة.

## إجابات سريعة
- **What does “export PSD to PNG” mean?** تحويل ملف Photoshop PSD إلى صورة PNG نقطية مع الحفاظ على الدقة البصرية والشفافية.  
- **Which library handles layer masks?** توفر Aspose.PSD for Java دعمًا مدمجًا للأقنعة وقنوات ألفا.  
- **Do I need a license?** نسخة تجريبية مجانية تعمل للاختبار؛ يلزم الحصول على ترخيص تجاري للاستخدام في الإنتاج.  
- **Can I run this on any OS?** نعم – API Java مستقل عن النظام ويعمل على Windows و macOS و Linux.  
- **How long does the conversion take?** عادةً أقل من ثانية للملفات ذات الحجم القياسي؛ ملفات PSD الكبيرة متعددة الميجابكسل تنتهي خلال بضع ثوانٍ.

## كيفية تصدير PSD إلى PNG مع دعم قناع الطبقة
يعد تصدير PSD إلى PNG أمرًا أساسيًا عندما تريد مشاركة أعمال Photoshop على الويب، أو تضمينها في التطبيقات، أو إنشاء صور مصغرة. يحافظ PNG على الشفافية، مما يجعله مثاليًا للأصول التي تتضمن أقنعة طبقة. من خلال أتمتة التحويل باستخدام Java، تلغي خطوات التصدير اليدوية وتضمن نتائج متسقة عبر دفعات كبيرة.

## لماذا تستخدم Aspose.PSD Java لهذه المهمة؟
- **Full mask handling** – يقرأ API أقنعة PSD ويكتبها إلى قناة ألفا في PNG تلقائيًا.  
- **Java‑only workflow** – لا أدوات خارجية؛ كل شيء يعمل داخل عملية Java الخاصة بك.  
- **Batch‑ready** – دمج الكود مع حلقة لتنفيذ تحويلات **batch PSD to PNG** في دقائق.  
- **Cross‑platform** – يعمل على Windows و macOS و Linux دون تبعيات أصلية.  
- **Quantified capability** – يدعم Aspose.PSD **أكثر من 50 تنسيقًا للإدخال والإخراج** ويمكنه معالجة ملفات PSD حتى **2 GB** دون تحميل المستند بالكامل إلى الذاكرة.

## المتطلبات المسبقة
قبل أن نغوص في الكود، تأكد من وجود ما يلي:

- **Java Development Kit (JDK)** – تحقق باستخدام `java -version`. قم بتنزيله من [Oracle's website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) إذا لزم الأمر.  
- **Aspose.PSD library** – احصل على أحدث JAR من [download page](https://releases.aspose.com/psd/java/) أو أضفه عبر Maven/Gradle.  
- **IDE** – IntelliJ IDEA أو Eclipse أو أي محرر تفضله لتطوير Java.

### 1. بيئة تطوير Java
يضمن JDK حديث (11 أو أحدث) التوافق مع Aspose.PSD API.

### 2. مكتبة Aspose.PSD
تتعامل المكتبة مع **java image conversion**، وتحليل الأقنعة، وخيارات تصدير PNG.

### 3. IDE (بيئة تطوير متكاملة)
استخدام IDE يبسط عملية تصحيح الأخطاء وإعداد المشروع.

## استيراد الحزم
جمل الاستيراد تجلب فئات Aspose.PSD المطلوبة لتحميل ملفات PSD وتكوين خيارات تصدير PNG إلى مشروع Java الخاص بك.

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PngOptions;
```

## دليل خطوة بخطوة

### الخطوة 1: إعداد دليل المشروع
حدد المجلد الذي يحتوي على PSD المصدر وسيحفظ PNG الناتج. يتم استخدام هذا المتغير طوال البرنامج التعليمي لإنشاء مسارات ملفات مطلقة.

```java
String dataDir = "Your Document Directory";
```

استبدل `Your Document Directory` بالمسار المطلق على جهازك.

### الخطوة 2: تحديد ملف PSD المصدر
أشر إلى ملف PSD الذي تريد تحويله. في هذا المثال نستخدم ملفًا يحتوي على قناع معقد، يُظهر حفظ كامل لقناة ألفا.

```java
String sourceFileName = dataDir + "MaskComplex.psd";
```

### الخطوة 3: تحديد مسار تصدير PNG
أخبر البرنامج أين يكتب ملف PNG الناتج. يمكن أن يكون المسار نفس مجلد المصدر أو موقع إخراج مخصص.

```java
String exportPath = dataDir + "MaskComplex.png";
```

### الخطوة 4: تحميل ملف PSD
طريقة `Image.load` تقرأ الملف إلى كائن `PsdImage`، مما يمنحك وصولًا برمجيًا إلى الطبقات والأقنعة وبيانات الصورة.

```java
PsdImage im = (PsdImage) Image.load(sourceFileName);
```

### الخطوة 5: إعداد خيارات تصدير PNG
قم بتكوين مُصدّر PNG للحفاظ على قناة ألفا، وهو أمر حاسم لشفافية قناع الطبقة. تسمح لك فئة `PngExportOptions` أيضًا بالتحكم في مستوى الضغط ونوع اللون.

```java
PngOptions saveOptions = new PngOptions();
saveOptions.setColorType(PngColorType.TruecolorWithAlpha);
```

### الخطوة 6: حفظ ملف PNG
قم بإجراء التحويل عن طريق استدعاء طريقة `save` مع الخيارات المكوّنة. سيحتوي الملف الناتج على المناطق المقنّعة من PSD الأصلي كبكسلات شفافة.

```java
im.save(exportPath, saveOptions);
```

إذا تم إعداد كل شيء بشكل صحيح، ستجد `MaskComplex.png` في مجلد الإخراج، يعرض المناطق المقنّعة من PSD الأصلي بشكل مثالي.

## المشكلات الشائعة والحلول
- **File‑not‑found errors** – تحقق مرة أخرى من `dataDir` وتأكد من أن اسم ملف PSD يطابق تمامًا، بما في ذلك حساسية الأحرف.  
- **Missing transparency** – تحقق من تطبيق `saveOptions.setColorType(PngColorType.TruecolorWithAlpha)`؛ وإلا سيتم حفظ PNG بدون قناة ألفا.  
- **Out‑of‑memory for large files** – زد حجم ذاكرة JVM (`-Xmx2g`) عند معالجة ملفات PSD الكبيرة جدًا.  
- **Batch conversion tip** – ضع الخطوات السابقة داخل حلقة `for` تتكرر على قائمة بأسماء ملفات PSD لتحقيق معالجة **batch PSD to PNG**.

## الأسئلة المتكررة

**س: ما هو قناع الطبقة في ملفات PSD؟**  
ج: قناع الطبقة يتحكم في شفافية الطبقة، مما يسمح لك بإخفاء أو إظهار أجزاء من الصورة دون محو البكسلات بشكل دائم.

**س: هل يمكنني العمل مع ملفات PSD دون معرفة برمجية؟**  
ج: بينما يتطلب Aspose.PSD كتابة كود، يمكن لمصممي الجرافيك استخدام Photoshop أو أدوات واجهة مستخدم أخرى للتحويل اليدوي.

**س: هل Aspose.PSD مجاني للاستخدام؟**  
ج: تتوفر نسخة تجريبية مجانية من صفحة التحميل؛ يلزم الحصول على ترخيص مدفوع للمشاريع التجارية.

**س: ماذا يحدث إذا كان ملف PSD الخاص بي لا يحتوي على أقنعة؟**  
ج: لا يزال التحويل يعمل؛ سيحتوي PNG الناتج ببساطة على عدم وجود تأثيرات شفافية مقنّعة.

**س: أين يمكنني الحصول على الدعم إذا واجهت مشاكل؟**  
ج: زر [support forum](https://forum.aspose.com/c/psd/34) للحصول على مساعدة من خبراء Aspose والمجتمع.

## الخلاصة
لقد تعلمت الآن **how to export PSD to PNG** مع الحفاظ على أقنعة الطبقة باستخدام Aspose.PSD Java API. يبسّط هذا النهج **java image conversion**، يدعم المعالجة الدفعية، ويضمن أن تحتفظ أصولك البصرية بالشفافية المقصودة. لا تتردد في تجربة خيارات PNG المختلفة أو دمج هذا سير العمل في خطوط أنابيب أتمتة أكبر.

---

**Last Updated:** 2026-09-23  
**Tested With:** Aspose.PSD for Java 24.12  
**Author:** Aspose

## دروس ذات صلة

- [تصدير PSD إلى PNG مع تأثيرات الطبقة باستخدام Aspose.PSD for Java](/psd/java/psd-image-modification-conversion/apply-layer-effects-psd-files/)
- [تحويل PSD إلى PNG وإنشاء قناع متجهي Java – مورد Vmsk في ملفات PSD](/psd/java/advanced-psd-layer-features-effects/support-vmsk-resource-psd-files/)
- [كيفية ضغط ملفات PNG باستخدام Aspose.PSD for Java](/psd/java/optimizing-png-files/compress-png-files/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}