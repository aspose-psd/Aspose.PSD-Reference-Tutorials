---
date: 2026-07-22
description: تعلم كيفية استخراج طبقات PSD وتحويل طبقات PSD إلى PNG باستخدام Aspose.PSD
  للغة Java. مثالي للمطورين الذين يحتاجون إلى معالجة رسومات قوية.
keywords:
- extract psd layers
- how to extract psd
- convert psd to png
lastmod: 2026-07-22
linktitle: استخراج طبقات PSD وإضافة دعم الطبقات لملفات PSD باستخدام Aspose.PSD Java
og_description: استخراج طبقات PSD وتحويلها إلى PNG باستخدام Aspose.PSD للغة Java.
  اتبع هذا الدليل خطوة بخطوة لأتمتة استخراج الطبقات وتحويل الصور.
og_image_alt: Developer guide showing Java code to extract PSD layers and save as
  PNG using Aspose.PSD
og_title: استخراج طبقات PSD – إضافة دعم الطبقات لملفات PSD باستخدام Aspose.PSD Java
schemas:
- author: Aspose
  dateModified: '2026-07-22'
  description: Learn how to extract PSD layers and convert PSD layers to PNG using
    Aspose.PSD for Java. Ideal for developers needing robust graphics manipulation.
  headline: Extract PSD Layers and Add Layer Support for PSD Files using Aspose.PSD
    Java
  type: TechArticle
- description: Learn how to extract PSD layers and convert PSD layers to PNG using
    Aspose.PSD for Java. Ideal for developers needing robust graphics manipulation.
  name: Extract PSD Layers and Add Layer Support for PSD Files using Aspose.PSD Java
  steps:
  - name: '**Java Development Environment** – JDK installed. You can download it from
      the [Oracle website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).'
    text: '**Java Development Environment** – JDK installed. You can download it from
      the [Oracle website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).'
  - name: '**Aspose.PSD for Java** – Grab the latest library from the official download
      page [here](https://releases.aspose.com/psd/java/).'
    text: '**Aspose.PSD for Java** – Grab the latest library from the official download
      page [here](https://releases.aspose.com/psd/java/).'
  - name: '**Basic Java knowledge** – Familiarity with compiling and running Java
      programs.'
    text: '**Basic Java knowledge** – Familiarity with compiling and running Java
      programs.'
  - name: '**IDE** – IntelliJ IDEA, Eclipse, or any editor you prefer.'
    text: '**IDE** – IntelliJ IDEA, Eclipse, or any editor you prefer.'
  - name: '**A PSD file** – Use any PSD you have, or download a sample PSD for testing.'
    text: '**A PSD file** – Use any PSD you have, or download a sample PSD for testing.'
  type: HowTo
- questions:
  - answer: Aspose.PSD for Java is a library that allows you to manipulate PSD files
      without having Photoshop installed.
    question: What is Aspose.PSD for Java?
  - answer: Yes! While primarily for PSD files, Aspose offers libraries for a wide
      range of formats, including AI, PDF, and SVG.
    question: Can I use Aspose.PSD for other file formats?
  - answer: Absolutely! You can download a free trial version [here](https://releases.aspose.com/).
    question: Is a trial version available?
  - answer: Access the Aspose forum for PSD‑related questions [here](https://forum.aspose.com/c/psd/34).
    question: Where can I get support if I run into problems?
  - answer: Iterate over `image.getLayers()`, create a new `Bitmap` for each layer,
      and save it with its own `PngOptions`. This yields individual PNG files per
      layer.
    question: Can I convert each layer to a separate PNG?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- extract psd
- Aspose.PSD
- Java image processing
title: استخراج طبقات PSD وإضافة دعم الطبقات لملفات PSD باستخدام Aspose.PSD Java
url: /ar/java/advanced-psd-layer-features-effects/add-layer-support-psd-files/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# استخراج طبقات PSD وإضافة دعم الطبقات لملفات PSD باستخدام Aspose.PSD Java

## مقدمة
العمل مع ملفات وثيقة فوتوشوب (PSD) هو واقع يومي للمصممين الجرافيكيين والمطورين على حد سواء، و**extract psd layers** غالبًا ما تكون الخطوة الأولى لإعادة استخدام الأصول أو أتمتة خطوط معالجة الصور. في هذا الدرس ستتعلم كيفية سحب الطبقات الفردية من ملف PSD، تمكين دعم الطبقات الكامل، و**convert PSD layers to PNG** باستخدام Aspose.PSD for Java. سنغطي كل شيء من إعداد البيئة إلى نصائح الممارسات الأفضل، بحيث يمكنك دمج هذا سير العمل في أي تطبيق Java خلال دقائق.

## إجابات سريعة
- **ما معنى “extract PSD layers”؟** يعني تحميل ملف PSD والوصول إلى كل طبقة فردية للتعديل أو التصدير.  
- **أي مكتبة تتعامل مع ذلك في Java؟** توفر Aspose.PSD for Java معالجة PSD كاملة دون الحاجة إلى Photoshop.  
- **هل يمكنني تحويل طبقات PSD إلى PNG في خطوة واحدة؟** نعم — عن طريق تحميل الملف مع الخيارات المناسبة وحفظه بخيارات PNG التي تحافظ على الشفافية.  
- **هل أحتاج إلى ترخيص للاستخدام في الإنتاج؟** يلزم ترخيص تجاري للإنتاج؛ يتوفر إصدار تجريبي مجاني للتقييم.  
- **ما نسخة Java المطلوبة؟** JDK 8 أو أعلى (يستخدم الدرس JDK 11 كمثال).

## كيفية استخراج طبقات PSD باستخدام Aspose.PSD for Java؟
حمّل ملف PSD، فعّل تأثيرات الطبقة، واحفظ النتيجة كملف PNG في بضع أسطر من كود Java فقط. هذا النهج المباشر يلغي الحاجة إلى Photoshop على الخادم ويعمل على أي منصة تدعم Java 8+. تبدأ بإنشاء كائن `PsdLoadOptions` مع `setLoadEffectsResource(true)` و `setUseDiskForLoadEffectsResource(true)`، ثم تحميل الملف باستخدام `PsdImage.load(path, options)`. بعد التحميل، يمكنك إما دمج الطبقات باستخدام `image.save(outputPath, new PngOptions())` أو التكرار عبر `image.getLayers()` لتصدير كل طبقة على حدة، مع ضمان احتفاظ جميع التأثيرات مع الحفاظ على استهلاك الذاكرة منخفضًا.

## لماذا استخراج طبقات PSD وتحويلها إلى PNG؟
استخراج الطبقات يتيح لك **إعادة استخدام الأصول**، **أتمتة إنشاء الصور المصغرة**، و**الحفاظ على الشفافية** للرسومات الجاهزة للويب. تدعم Aspose.PSD **أكثر من 50 تنسيقًا للإدخال والإخراج** ويمكنها معالجة ملفات PSD متعددة المئات من الصفحات دون تحميل الملف بالكامل في الذاكرة، بفضل معالجة الموارد القائمة على القرص.

## المتطلبات المسبقة
قبل أن نغوص في التفاصيل، تأكد من توفر ما يلي:

1. **بيئة تطوير Java** – تم تثبيت JDK. يمكنك تنزيله من [Oracle website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).  
2. **Aspose.PSD for Java** – احصل على أحدث مكتبة من صفحة التحميل الرسمية [here](https://releases.aspose.com/psd/java/).  
3. **معرفة أساسية بـ Java** – الإلمام بعملية تجميع وتشغيل برامج Java.  
4. **IDE** – IntelliJ IDEA أو Eclipse أو أي محرر تفضله.  
5. **ملف PSD** – استخدم أي ملف PSD لديك، أو قم بتنزيل ملف PSD تجريبي للاختبار.

بمجرد أن تكون هذه العناصر جاهزة، فأنت مستعد لبدء استخراج طبقات PSD.

## استيراد الحزم
الفئات `PsdImage` و `PsdLoadOptions` و `PngOptions` هي جوهر سير العمل.  

`PsdImage` هو الكائن الأعلى مستوى في Aspose.PSD الذي يمثل ملف PSD واحد في الذاكرة.  

`PsdLoadOptions` يتيح لك التحكم في كيفية تحميل الموارد مثل تأثيرات الطبقة.  

`PngOptions` يحدد تنسيق الإخراج ومعالجة الشفافية لملف PNG.

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import com.aspose.psd.imageoptions.PngOptions;
```

## الخطوة 1: تعريف الأدلة الخاصة بك
قم بإعداد المسارات لملف PSD المصدر وملف PNG الناتج. عدّل المتغير `dataDir` ليشير إلى المجلد الذي توجد فيه ملفاتك.

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "layers.psd";
String output = dataDir + "layers.png";
```

- `dataDir` – استبدل `"Your Document Directory"` بمسار المجلد الفعلي الخاص بك.  
- `sourceFileName` – المسار الكامل لملف PSD الذي تريد معالجته.  
- `output` – مسار الوجهة لملف PNG الذي سيحتوي على الطبقات المستخرجة.

## الخطوة 2: إعداد خيارات التحميل
تضمن إعداد `PsdLoadOptions` تحميل جميع تأثيرات الطبقة والموارد بشكل صحيح، وهو أمر أساسي عندما تقوم **extract PSD layers**.

```java
PsdLoadOptions imageLoadOptions = new PsdLoadOptions();
imageLoadOptions.setLoadEffectsResource(true);
imageLoadOptions.setUseDiskForLoadEffectsResource(true);
```

- `setLoadEffectsResource(true)` – يحمل التأثيرات الإضافية (مثل الظلال) المرفقة بالطبقات.  
- `setUseDiskForLoadEffectsResource(true)` – ينقل الموارد الثقيلة إلى القرص، مما يقلل من ضغط الذاكرة.

## الخطوة 3: تحميل ملف PSD
الآن نقوم بتحميل ملف PSD إلى كائن `PsdImage` باستخدام الخيارات المحددة أعلاه.

```java
PsdImage image = (PsdImage) Image.load(sourceFileName, imageLoadOptions);
```

في هذه المرحلة، يحتوي `image` على جميع الطبقات والأقنعة والتأثيرات، جاهزًا للاستخراج.

## الخطوة 4: إعداد خيارات الحفظ
قم بتكوين كيفية حفظ ملف PNG. استخدام `TruecolorWithAlpha` يحافظ على الشفافية من الطبقات الأصلية.

```java
PngOptions saveOptions = new PngOptions();
saveOptions.setColorType(PngColorType.TruecolorWithAlpha);
```

## الخطوة 5: حفظ الصورة (تحويل طبقات PSD إلى PNG)
صدّر ملف PSD المحمّل (مع جميع طبقاته) إلى ملف PNG واحد. هذه الخطوة تقوم فعليًا **convert psd layers png** في عملية واحدة.

```java
image.save(output, saveOptions);
```

إذا كنت بحاجة إلى كل طبقة كملف PNG منفصل، يمكنك التكرار عبر `image.getLayers()` — لكن للعديد من الحالات يكون PNG المدمج كافيًا.

## الخطوة 6: إنهاء العملية
أضف رسالة صديقة إلى وحدة التحكم لتعرف أن العملية نجحت.

```java
System.out.println("PSD Layers have been successfully converted to PNG!");
```

## المشكلات الشائعة والنصائح
- **Out‑of‑Memory Errors:** إذا كنت تعالج ملفات PSD كبيرة جدًا، حافظ على تمكين `setUseDiskForLoadEffectsResource(true)` لنقل البيانات المؤقتة إلى القرص.  
- **Missing Effects:** تأكد من ضبط `setLoadEffectsResource(true)`؛ وإلا قد يتم تجاهل بعض تأثيرات الطبقة.  
- **Path Problems:** استخدم `Paths.get(...)` من `java.nio.file` لمعالجة المسارات بشكل مستقل عن النظام الأساسي.

## الأسئلة المتكررة

**س: ما هو Aspose.PSD for Java؟**  
ج: Aspose.PSD for Java هي مكتبة تسمح لك بالتعامل مع ملفات PSD دون الحاجة إلى تثبيت Photoshop.

**س: هل يمكنني استخدام Aspose.PSD لتنسيقات ملفات أخرى؟**  
ج: نعم! بينما تُركز أساسًا على ملفات PSD، تقدم Aspose مكتبات لمجموعة واسعة من التنسيقات، بما في ذلك AI و PDF و SVG.

**س: هل تتوفر نسخة تجريبية؟**  
ج: بالتأكيد! يمكنك تنزيل نسخة تجريبية مجانية [here](https://releases.aspose.com/).

**س: أين يمكنني الحصول على الدعم إذا واجهت مشاكل؟**  
ج: يمكنك الوصول إلى منتدى Aspose لأسئلة متعلقة بـ PSD [here](https://forum.aspose.com/c/psd/34).

**س: هل يمكنني تحويل كل طبقة إلى PNG منفصل؟**  
ج: قم بالتكرار عبر `image.getLayers()`، أنشئ كائن `Bitmap` جديد لكل طبقة، واحفظه باستخدام `PngOptions` الخاص به. سيؤدي ذلك إلى إنشاء ملفات PNG فردية لكل طبقة.

## الخلاصة
لقد تعلمت الآن كيفية **extract PSD layers**، تمكين دعم الطبقات الكامل، و**convert PSD layers to PNG** باستخدام Aspose.PSD for Java. سواء كنت تبني خط أنابيب أصول آلي أو تضيف قدرات رسومية لتطبيق سطح مكتب، يمنحك هذا النهج تحكمًا دقيقًا في ملفات Photoshop دون الحاجة إلى Photoshop نفسه. استكشف المزيد بتطبيق الفلاتر، دمج الطبقات برمجيًا، أو تصدير كل طبقة على حدة لتتناسب مع سير عملك.

---

**Last Updated:** 2026-07-22  
**Tested With:** Aspose.PSD for Java 24.11 (latest at time of writing)  
**Author:** Aspose

## دروس ذات صلة

- [تصدير PSD إلى PNG وإضافة طبقة عادية جديدة باستخدام Aspose.PSD for Java](/psd/java/advanced-image-effects/add-new-regular-layer/)
- [تصدير PSD إلى PNG مع دعم قناع الطبقة في Java](/psd/java/advanced-psd-layer-features-effects/support-layer-mask-psd-files/)
- [تحويل PSD إلى صورة في Java – تطبيق طبقات الضبط باستخدام Aspose.PSD](/psd/java/advanced-psd-layer-features-effects/apply-adjustment-layers-psd-files/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< blocks/products/products-backtop-button >}}
{{< /blocks/products/pf/main-wrap-class >}}