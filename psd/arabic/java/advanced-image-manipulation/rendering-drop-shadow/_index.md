---
date: 2026-11-04
description: تعلم كيفية حفظ PSD كـ PNG، وتصدير PNG مع alpha، وإضافة طبقة Rendering
  Drop Shadow باستخدام Aspose.PSD for Java – دليل كامل خطوة بخطوة.
keywords:
- save psd as png
- convert psd to png
- export png with alpha
- batch psd to png
- java image manipulation
lastmod: 2026-11-04
linktitle: تطبيق Rendering Drop Shadow
og_description: حفظ psd كـ png باستخدام Aspose.PSD for Java، وتصدير PNG مع alpha transparency،
  وإضافة Rendering Drop Shadow—دليل خطوة بخطوة لمطوري Java.
og_image_alt: Developer guide showing how to convert PSD to PNG and apply drop shadow
  using Aspose.PSD Java
og_title: حفظ psd كـ png وتطبيق Rendering Drop Shadow في Aspose.PSD for Java
schemas:
- author: Aspose
  dateModified: '2026-11-04'
  description: Learn how to save PSD as PNG, export PNG with alpha, and add a drop
    shadow layer using Aspose.PSD for Java – a complete, step‑by‑step guide.
  headline: Save psd as png and apply rendering drop shadow in Aspose.PSD for Java
  type: TechArticle
- description: Learn how to save PSD as PNG, export PNG with alpha, and add a drop
    shadow layer using Aspose.PSD for Java – a complete, step‑by‑step guide.
  name: Save psd as png and apply rendering drop shadow in Aspose.PSD for Java
  steps:
  - name: define document directory
    text: Define the directory path where your PSD files are stored.
  - name: set psd and png file paths
    text: Specify the full file paths for the source PSD and the target PNG.
  - name: load psd file with effects
    text: '`PsdImage` loads the PSD and gives access to its layers and effects.'
  - name: access drop shadow effect
    text: '`DropShadowEffect` represents a drop‑shadow layer effect that can be read
      or modified.'
  - name: validate shadow effect properties
    text: '`shadowEffect` holds the properties of the drop‑shadow such as opacity,
      distance, and size. > **Pro tip:** Adjust `setSpread()` or `setNoise()` to create
      softer or more textured shadows.'
  - name: save as png – the “save psd as png” step
    text: '`PngOptions` configures PNG export settings, including color type and alpha
      channel handling. At this point you have successfully **converted psd to png**,
      **exported png with alpha**, and applied a rendering drop shadow in a single
      workflow.'
  type: HowTo
- questions:
  - answer: Yes. Loop through `im.getLayers()` and add or modify a `DropShadowEffect`
      for each target layer, which also lets you perform a batch psd to png conversion.
    question: Can I apply drop shadows to multiple layers simultaneously?
  - answer: '`Spread` determines how abruptly the shadow transitions from full opacity
      to transparent. A higher value creates a harder edge.'
    question: What does the ‘Spread’ parameter control?
  - answer: Aspose.PSD supports PSD files from Photoshop 3.0 up to the latest release,
      handling most layer types and effects.
    question: Is Aspose.PSD compatible with all Photoshop versions?
  - answer: Download the free trial from the [Aspose.PSD download page](https://releases.aspose.com/psd/java/)
      and run the sample without a license key.
    question: How can I test the code before purchasing a license?
  - answer: Post your question on the [Aspose.PSD forum](https://forum.aspose.com/c/psd/34)
      where the community and Aspose engineers can assist.
    question: Where can I get help if I run into problems?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- save psd as png
- aspose psd java
- java image manipulation
- png transparency
- rendering drop shadow
title: حفظ psd كـ png وتطبيق Rendering Drop Shadow في Aspose.PSD for Java
url: /ar/java/advanced-image-manipulation/rendering-drop-shadow/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# حفظ PSD كـ PNG وتطبيق ظل إسقاط عند العرض في Aspose.PSD للـ Java

## مقدمة

إذا كنت تعمل مع ملفات Photoshop في Java، فإن **حفظ PSD كـ PNG** هو أحد أكثر المهام شيوعًا التي ستواجهها. في العديد من المشاريع ستحتاج إلى **حفظ PSD كـ PNG** لتسليم الأصول إلى الويب أو تطبيقات الهواتف المحمولة، مع الحفاظ على الشفافية والتأثيرات البصرية. باستخدام Aspose.PSD يمكنك ليس فقط **تحويل PSD إلى PNG** بل أيضًا تحسين الصورة عن طريق **إضافة طبقة ظل إسقاط**. في هذا البرنامج التعليمي سنستعرض العملية بالكامل — تحميل ملف PSD، تطبيق ظل إسقاط عند العرض، وأخيرًا **حفظ PSD كملف PNG** — حتى تتمكن من دمج سير العمل في مشاريعك بثقة.

## إجابات سريعة

- **ما المكتبة التي تتعامل مع تحويل PSD إلى PNG؟** Aspose.PSD for Java.  
- **كم من الوقت تستغرق تنفيذ ظل الإسقاط؟** حوالي 10‑15 دقيقة للمثال الأساسي.  
- **هل أحتاج إلى ترخيص لتشغيل الكود؟** الإصدار التجريبي المجاني يعمل للتقييم؛ الترخيص مطلوب للإنتاج.  
- **هل يمكنني تطبيق الظل على طبقات متعددة؟** نعم — فقط قم بالتكرار عبر الطبقات المطلوبة، مما يتيح لك أيضًا إجراء تحويل دفعة من PSD إلى PNG.  
- **ما نسخة Java المطلوبة؟** Java 8 أو أعلى.

## ما هو “حفظ PSD كـ PNG” ولماذا هو مهم؟

**حفظ PSD كـ PNG ينتج صورة غير مضغوطة مدعومة على نطاق واسع وتحتفظ بالشفافية.** هذا التنسيق أساسي عندما تحتاج إلى عرض أصول Photoshop على الويب، في تطبيقات الهواتف المحمولة، أو كجزء من خط أنابيب معالجة صور أكبر. إضافة ظل إسقاط في الوقت نفسه يتيح لك إنتاج تأثير بصري مصقول دون فتح Photoshop.

## لماذا تستخدم Aspose.PSD لهذا سير العمل؟

العرض في وقت التحميل لتأثيرات الطبقات مدمج، لذا لا تحتاج إلى Photoshop. يدعم Aspose.PSD أكثر من 50 تنسيقًا للإدخال والإخراج (PSD، PNG، JPEG، TIFF، BMP) ويمكنه معالجة مستندات كبيرة دون تحميل الملف بالكامل إلى الذاكرة. يحافظ على التأثيرات مثل ظلال الإسقاط والوهج تمامًا كما تظهر، ويصدر PNG تلقائيًا مع شفافية ألفا.

## المتطلبات المسبقة

- **بيئة تطوير Java** – JDK 8 أو أحدث مثبت.  
- **Aspose.PSD للـ Java** – قم بتنزيل أحدث JAR من [صفحة تحميل Aspose.PSD](https://releases.aspose.com/psd/java/).  
- **ملف PSD** – يجب أن يحتوي الملف على طبقة واحدة على الأقل تريد تحسينها بظل إسقاط (مثال: *Shadow.psd*).  

## استيراد الحزم

مساحة الأسماء `com.aspose.psd` توفر الفئات الأساسية لتحميل الصور، ومعالجة الطبقات، وتصدير ملفات PNG. `PsdImage` هي الفئة الرئيسية المستخدمة لتحميل ومعالجة ملفات PSD.  

```java
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.layereffects.DropShadowEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import com.aspose.psd.Color;

import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.imageoptions.PngOptions;
```

## دليل خطوة بخطوة

### الخطوة 1: تعريف دليل المستند
حدد مسار الدليل حيث يتم تخزين ملفات PSD الخاصة بك.  

```java
String dataDir = "Your Document Directory";
```

### الخطوة 2: تعيين مسارات ملفات PSD و PNG
حدد المسارات الكاملة للملف المصدر PSD والملف الهدف PNG.  

```java
String sourceFileName = dataDir + "Shadow.psd";
String pngExportPath = dataDir + "Shadowchanged1.png";
```

### الخطوة 3: تحميل ملف PSD مع التأثيرات
`PsdImage` يقوم بتحميل ملف PSD ويوفر الوصول إلى طبقاته وتأثيراته.  

```java
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage) Image.load(sourceFileName, loadOptions);
```

### الخطوة 4: الوصول إلى تأثير ظل الإسقاط
`DropShadowEffect` يمثل تأثير طبقة ظل إسقاط يمكن قراءته أو تعديله.  

```java
DropShadowEffect shadowEffect = (DropShadowEffect) (im.getLayers()[1].getBlendingOptions().getEffects()[0]);
```

### الخطوة 5: التحقق من خصائص تأثير الظل
`shadowEffect` يحتوي على خصائص ظل الإسقاط مثل الشفافية، والمسافة، والحجم.  

```java
Assert.areEqual(Color.getBlack(), shadowEffect.getColor());
Assert.areEqual(255, shadowEffect.getOpacity());
Assert.areEqual(3, shadowEffect.getDistance());
Assert.areEqual(7, shadowEffect.getSize());
Assert.areEqual(true, shadowEffect.getUseGlobalLight());
Assert.areEqual(90, shadowEffect.getAngle());
Assert.areEqual(0, shadowEffect.getSpread());
Assert.areEqual(0, shadowEffect.getNoise());
```

> **نصيحة احترافية:** اضبط `setSpread()` أو `setNoise()` لإنشاء ظلال أكثر نعومة أو ذات نسيج.

### الخطوة 6: حفظ كـ PNG – خطوة “حفظ PSD كـ PNG”
`PngOptions` يضبط إعدادات تصدير PNG، بما في ذلك نوع اللون ومعالجة قناة ألفا.  

```java
PngOptions saveOptions = new PngOptions();
saveOptions.setColorType(PngColorType.TruecolorWithAlpha);
im.save(pngExportPath, saveOptions);
```

في هذه المرحلة، لقد نجحت في **تحويل PSD إلى PNG**، **تصدير PNG مع ألفا**، وتطبيق ظل إسقاط عند العرض في سير عمل واحد.

## تصدير PNG مع شفافية ألفا

عندما تحتاج إلى أن يحتفظ إخراج PNG بخلفية شفافة — خاصةً لتراكبات واجهة المستخدم أو رسومات الويب — تأكد من استخدام `PngColorType.TruecolorWithAlpha` كما هو موضح في خطوة الحفظ أعلاه. هذا يضمن أن ظل الإسقاط يجلس على قماش شفاف بدلاً من خلفية صلبة، مما يساعدك على **الحفاظ على شفافية PNG**.

## إضافة طبقة ظل إسقاط باستخدام Java

إذا كان ملف PSD الخاص بك يحتوي على طبقات متعددة تحتاج إلى ظلال، ما عليك سوى تكرار **الخطوة 4** و **الخطوة 5** داخل حلقة تتكرر عبر `im.getLayers()`. يمكن لكل تكرار إنشاء أو تعديل مثيل `DropShadowEffect`، مما يمنحك تحكمًا دقيقًا في الشفافية، والمسافة، والحجم، والزاوية لكل طبقة. يتيح لك هذا النهج أيضًا إجراء تحويل **دفعة من PSD إلى PNG** حيث يحصل كل ملف على نفس معالجة الظل.

## حالات الاستخدام الشائعة لحفظ PSD كـ PNG

* **خطوط أنابيب أصول الويب** – تحويل ملفات PSD المقدمة من المصمم إلى PNG جاهزة للويب مع ظلال مدمجة.  
* **موارد تطبيقات الهواتف المحمولة** – إنشاء أيقونات PNG شفافة في الوقت الفعلي، تجنّب التصدير اليدوي.  
* **المعالجة الدفعية** – أتمتة تحويل مئات ملفات PSD في مهمة على الخادم، مع ضمان احتفاظ كل PNG بقناة ألفا وتأثيراته البصرية.  

## المشكلات الشائعة والحلول

| المشكلة | السبب المحتمل | الحل |
|-------|--------------|-----|
| **الظل غير مرئي** | `Opacity` مضبوط على 0 أو الطبقة مخفية | تحقق من أن `shadowEffect.getOpacity()` > 0 ورؤية الطبقة. |
| **PNG يبدو مسطحًا (بدون شفافية)** | `PngColorType` المستخدم غير صحيح | استخدم `PngColorType.TruecolorWithAlpha` كما هو موضح. |
| **استثناء عند التحميل** | لم يتم تحميل التأثيرات | تأكد من استدعاء `loadOptions.setLoadEffectsResource(true)`. |
| **فهرس طبقة غير صحيح** | بنية PSD مختلفة | افحص `im.getLayers()` واختر الفهرس الصحيح. |

## الأسئلة المتكررة

**س: هل يمكنني تطبيق ظلال إسقاط على طبقات متعددة في آن واحد؟**  
ج: نعم. قم بالتكرار عبر `im.getLayers()` وأضف أو عدل `DropShadowEffect` لكل طبقة مستهدفة، مما يتيح لك أيضًا إجراء تحويل دفعة من PSD إلى PNG.

**س: ما الذي يتحكم فيه معامل ‘Spread’?**  
ج: `Spread` يحدد مدى سرعة انتقال الظل من الشفافية الكاملة إلى الشفافية. القيمة الأعلى تنتج حافة أكثر صلابة.

**س: هل Aspose.PSD متوافق مع جميع إصدارات Photoshop؟**  
ج: يدعم Aspose.PSD ملفات PSD من Photoshop 3.0 وحتى أحدث إصدار، ويتعامل مع معظم أنواع الطبقات والتأثيرات.

**س: كيف يمكنني اختبار الكود قبل شراء الترخيص؟**  
ج: قم بتنزيل النسخة التجريبية المجانية من [صفحة تحميل Aspose.PSD](https://releases.aspose.com/psd/java/) وشغّل العينة دون مفتاح ترخيص.

**س: أين يمكنني الحصول على المساعدة إذا واجهت مشاكل؟**  
ج: انشر سؤالك على [منتدى Aspose.PSD](https://forum.aspose.com/c/psd/34) حيث يمكن للمجتمع ومهندسي Aspose مساعدتك.

## الخلاصة

أنت الآن تعرف كيف **تحفظ PSD كـ PNG**، **تصدّر PNG مع ألفا**، **تحوّل PSD إلى PNG**، و **تضيف طبقة ظل إسقاط** باستخدام Aspose.PSD للـ Java. يتيح لك هذا الجمع أتمتة إعداد الصور عالية الجودة للويب أو الهواتف المحمولة أو تطبيقات سطح المكتب — دون الحاجة إلى فتح Photoshop أبداً.

---

**آخر تحديث:** 2026-11-04  
**تم الاختبار مع:** Aspose.PSD 24.11 للـ Java  
**المؤلف:** Aspose

## دروس ذات صلة

- [تحويل PSD إلى PNG مع تراكب اللون – Aspose.PSD للـ Java](/psd/java/advanced-image-manipulation/rendering-color-effect/)
- [كيفية إضافة ظل في PSD باستخدام Java – تأثيرات الطبقة المتقدمة](/psd/java/advanced-psd-layer-features-effects/)
- [كيفية تحويل PSD إلى صيغ صور نقطية باستخدام Aspose.PSD للـ Java](/psd/java/advanced-techniques/convert-psd-to-raster-forms/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}