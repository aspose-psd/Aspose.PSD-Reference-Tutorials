---
date: 2026-09-03
description: تعلم كيفية إنشاء gradient stroke java وتخصيص تدرجات الخط في ملفات PSD
  باستخدام Aspose.PSD for Java. دليل خطوة بخطوة للمطورين.
keywords:
- create gradient stroke java
- add gradient stroke psd
- Aspose.PSD Java
- PSD gradient stroke
lastmod: 2026-09-03
linktitle: كيفية إنشاء طبقة Gradient Stroke في Java
og_description: إنشاء gradient stroke java باستخدام Aspose.PSD for Java في دقائق.
  يوضح هذا الدليل كيفية إضافة وتخصيص gradient strokes في ملفات PSD، مع أمثلة شفرة
  وأفضل الممارسات.
og_image_alt: Screenshot of a PSD file showing a gradient stroke applied via Aspose.PSD
  Java API
og_title: إنشاء gradient stroke java – دليل Aspose.PSD التعليمي
schemas:
- author: Aspose
  dateModified: '2026-09-03'
  description: Learn how to create gradient stroke java and customize stroke gradients
    in PSD files using Aspose.PSD for Java. Step‑by‑step guide for developers.
  headline: Create gradient stroke java – Aspose.PSD tutorial guide
  type: TechArticle
- description: Learn how to create gradient stroke java and customize stroke gradients
    in PSD files using Aspose.PSD for Java. Step‑by‑step guide for developers.
  name: Create gradient stroke java – Aspose.PSD tutorial guide
  steps:
  - name: '**Java Development Kit (JDK)** – Install the latest JDK from [Oracle''s
      website](https://www.oracle.com/java/technologies/javase-downloads.html).'
    text: '**Java Development Kit (JDK)** – Install the latest JDK from [Oracle''s
      website](https://www.oracle.com/java/technologies/javase-downloads.html).'
  - name: '**Aspose.PSD for Java** – Download the library from the [Aspose.PSD download
      page](https://releases.aspose.com/psd/java/).'
    text: '**Aspose.PSD for Java** – Download the library from the [Aspose.PSD download
      page](https://releases.aspose.com/psd/java/).'
  - name: '**IDE** – IntelliJ IDEA, Eclipse, or NetBeans.'
    text: '**IDE** – IntelliJ IDEA, Eclipse, or NetBeans.'
  - name: '**License** – Obtain a [temporary license](https://purchase.aspose.com/temporary-license/)
      if you don’t have a full commercial license.'
    text: '**License** – Obtain a [temporary license](https://purchase.aspose.com/temporary-license/)
      if you don’t have a full commercial license.'
  type: HowTo
- questions:
  - answer: Aspose.PSD for Java is a pure‑Java library that lets developers create,
      edit, convert, and render Photoshop PSD files without requiring Adobe Photoshop.
    question: What is Aspose.PSD for Java?
  - answer: Yes, a valid license is required for production use. You can obtain a
      [temporary license](https://purchase.aspose.com/temporary-license/) for evaluation.
    question: Do I need a license to use Aspose.PSD for Java?
  - answer: Absolutely. Aspose.PSD provides APIs to build a new PSD document, add
      layers, apply effects, and save the file entirely programmatically.
    question: Can I create PSD files from scratch with this library?
  - answer: Yes, you can apply shadows, glows, bevels, and many other layer effects
      using the same effect‑based API.
    question: Is it possible to apply other effects besides gradient strokes?
  - answer: The official documentation is available in the [Aspose.PSD Java API reference](https://reference.aspose.com/psd/java/).
    question: Where can I find the full reference documentation?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- gradient stroke
- Aspose.PSD
- Java graphics
title: إنشاء gradient stroke java – دليل Aspose.PSD التعليمي
url: /ar/java/java-graphics-drawing/add-stroke-layer-gradient/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# كيفية إنشاء حد تدرج لوني Java باستخدام Aspose.PSD

## مقدمة
إذا كنت بحاجة إلى **create gradient stroke java** دون فتح Photoshop، فقد وصلت إلى المكان الصحيح. في هذا الدرس ستتعلم كيفية استخدام Aspose.PSD for Java—مكتبة Java صافية تمنحك تحكمًا برمجيًا كاملاً في ملفات PSD. سنستعرض تحميل ملف PSD، الوصول إلى تأثير حد الطبقة، تكوين تعبئة تدرجية، وأخيرًا حفظ النتيجة. بنهاية الدرس ستكون قادرًا على إضافة حدود تدرجية احترافية إلى الأشكال أو النصوص ببضع أسطر من الشيفرة.

## إجابات سريعة
- **ما هو الهدف الأساسي؟** إنشاء طبقة حد تدرجية في ملف PSD باستخدام Java.  
- **أي مكتبة توفر الـ API؟** Aspose.PSD for Java (supports Java 8 +).  
- **هل أحتاج إلى ترخيص للإنتاج؟** نعم – يلزم ترخيص صالح أو مؤقت.  
- **كم من الوقت تستغرق تنفيذ أساسي؟** تقريبًا 10‑15 دقيقة لحد بسيط.  
- **هل يمكنني تخصيص نوع التدرج؟** بالتأكيد – التدرجات الخطية، الدائرية، وتلك القائمة على الزاوية كلها مدعومة.

## ما هي طبقة حد تدرجية؟
طبقة حد تدرجية هي مخطط حدودي متجه ينتقل لونه بسلاسة بين لونين أو أكثر. يمكن تطبيقها على الأشكال، النص، أو أي قناع متجه داخل ملف PSD، مما يمنح المصممين تأثيرًا بصريًا ديناميكيًا دون تحويل العمل إلى نقطية.

## لماذا تستخدم Aspose.PSD for Java؟
Aspose.PSD for Java يوفر **full PSD support** لأكثر من 100 ميزة—بما في ذلك الطبقات، الأقنعة، طبقات الضبط، وتأثيرات الطبقة—ويمكنه معالجة ملفات تصل إلى 2 GB دون تحميل المستند بالكامل في الذاكرة. تعمل المكتبة على أي نظام تشغيل يدعم Java، ولا تعتمد على أي مكوّنات أصلية، ويتم تحديثها شهريًا لتظل متوافقة مع أحدث مواصفات ملفات Photoshop.

## المتطلبات المسبقة
1. **Java Development Kit (JDK)** – قم بتثبيت أحدث JDK من [Oracle's website](https://www.oracle.com/java/technologies/javase-downloads.html).  
2. **Aspose.PSD for Java** – حمّل المكتبة من [Aspose.PSD download page](https://releases.aspose.com/psd/java/).  
3. **IDE** – IntelliJ IDEA، Eclipse، أو NetBeans.  
4. **License** – احصل على [temporary license](https://purchase.aspose.com/temporary-license/) إذا لم يكن لديك ترخيص تجاري كامل.

## استيراد الحزم
عبارات `import` تجلب الفئات الضرورية إلى النطاق.  

```text
```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.examples.Utils.Assert;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.BlendMode;
import com.aspose.psd.fileformats.psd.layers.IGradientColorPoint;
import com.aspose.psd.fileformats.psd.layers.fillsettings.FillType;
import com.aspose.psd.fileformats.psd.layers.fillsettings.GradientColorPoint;
import com.aspose.psd.fileformats.psd.layers.fillsettings.GradientFillSettings;
import com.aspose.psd.fileformats.psd.layers.fillsettings.GradientTransparencyPoint;
import com.aspose.psd.fileformats.psd.layers.fillsettings.GradientType;
import com.aspose.psd.fileformats.psd.layers.fillsettings.IGradientTransparencyPoint;
import com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
```
```

الآن لنقسم العملية إلى خطوات واضحة.

## الخطوة 1: تحميل ملف PSD
تحميل الملف المصدر هو الخطوة الأولى؛ يجب تمكين موارد التأثير حتى تكون معلومات الحد متاحة للتعديل. **PsdLoadOptions** يضبط طريقة تحميل ملف PSD، مما يسمح لك بتمكين أو تعطيل موارد محددة.  

```text
```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "Stroke.psd";
String exportPath = dataDir + "StrokeGradientChanged.psd";
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);
PsdImage im = (PsdImage) Image.load(sourceFileName, loadOptions);
```
```

## الخطوة 2: الوصول إلى تأثير الحد
**StrokeEffect** يمثل نمط الحدود المطبق على طبقة، بما في ذلك العرض، اللون، وتعبئة التدرج.  

```text
```java
StrokeEffect gradientStroke = (StrokeEffect) im.getLayers()[2].getBlendingOptions().getEffects()[0];
```
```

## الخطوة 3: التحقق من خصائص تأثير الحد
قبل تعديل أي شيء، من الجيد قراءة الخصائص الحالية. يساعدك ذلك على فهم التكوين الحالي وتجنب الكتابة فوق الإعدادات المهمة عن غير قصد. **GradientFillSettings** يحتوي على إعدادات تعبئة التدرج لتأثير الحد.  

```text
```java
Assert.areEqual(BlendMode.Normal, gradientStroke.getBlendMode());
Assert.areEqual(255, gradientStroke.getOpacity());
Assert.areEqual(true, gradientStroke.isVisible());
GradientFillSettings fillSettings = (GradientFillSettings) gradientStroke.getFillSettings();
Assert.areEqual(Color.getBlack(), fillSettings.getColor());
Assert.areEqual(FillType.Gradient, fillSettings.getFillType());
Assert.areEqual(true, fillSettings.getAlignWithLayer());
Assert.areEqual(GradientType.Linear, fillSettings.getGradientType());
Assert.isTrue(Math.abs(90 - fillSettings.getAngle()) < 0.001, "Angle is incorrect");
Assert.areEqual(false, fillSettings.getDither());
Assert.isTrue(Math.abs(0 - fillSettings.getHorizontalOffset()) < 0.001, "Horizontal offset is incorrect");
Assert.isTrue(Math.abs(0 - fillSettings.getVerticalOffset()) < 0.001, "Vertical offset is incorrect");
Assert.areEqual(false, fillSettings.getReverse());
```
```

## الخطوة 4: تعديل إعدادات تعبئة التدرج
`GradientFill` يحدد كيفية انتقال الألوان عبر الحد. يمكنك تغيير نوعه (خطّي، دائري)، الزاوية، ونمط المزج، ثم تعيين نقاط لون وشفافية جديدة.  

```text
```java
fillSettings.setColor(Color.getGreen());
gradientStroke.setOpacity((byte) 127);
gradientStroke.setBlendMode(BlendMode.Color);
fillSettings.setAlignWithLayer(false);
fillSettings.setGradientType(GradientType.Radial);
fillSettings.setAngle(45);
fillSettings.setDither(true);
fillSettings.setHorizontalOffset(15);
fillSettings.setVerticalOffset(11);
fillSettings.setReverse(true);
```
```

## الخطوة 5: إضافة وتعديل نقاط اللون والشفافية
يُبنى التدرج من سلسلة من نقاط إيقاف اللون وإيقاف الشفافية. **GradientColorPoint** يعرّف نقطة إيقاف اللون في التدرج، محددًا لونه وموقعه. **GradientTransparencyPoint** يعرّف نقطة إيقاف الشفافية في التدرج، محددًا شفافيته وموقعه. إضافة أو تعديل هذه النقاط يتيح لك تشكيل التدفق البصري للحد.  

```text
```java
// Add new color point
GradientColorPoint colorPoint = fillSettings.addColorPoint();
colorPoint.setColor(Color.getGreen());
colorPoint.setLocation(4096);
colorPoint.setMedianPointLocation(75);
// Change location of previous point
fillSettings.getColorPoints()[1].setLocation(1899);
// Add new transparency point
GradientTransparencyPoint transparencyPoint = fillSettings.addTransparencyPoint();
transparencyPoint.setOpacity(25);
transparencyPoint.setMedianPointLocation(25);
transparencyPoint.setLocation(4096);
// Change location of previous transparency point
fillSettings.getTransparencyPoints()[1].setLocation(2411);
```
```

## الخطوة 6: حفظ ملف PSD المعدل
بعد جميع التعديلات، اكتب المستند المحدث مرة أخرى إلى القرص. Aspose.PSD يحافظ تلقائيًا على جميع الطبقات والموارد الأخرى.  

```text
```java
im.save(exportPath);
```
```

## الخطوة 7: التحقق من التعديلات
أعد تحميل الملف المحفوظ وتأكد من أن خصائص تدرج الحد تتطابق مع القيم التي ضبطتها. هذه الخطوة ضرورية لسلاسل الأنابيب الآلية. **Assert** يوفر تأكيدات اختبار بسيطة للتحقق من الشروط أثناء وقت التشغيل.  

```text
```java
PsdImage img = (PsdImage) Image.load(exportPath, loadOptions);
StrokeEffect gradientStrokeEffect = (StrokeEffect) img.getLayers()[2].getBlendingOptions().getEffects()[0];
Assert.areEqual(BlendMode.Color, gradientStrokeEffect.getBlendMode());
Assert.areEqual(127, gradientStrokeEffect.getOpacity());
Assert.areEqual(true, gradientStrokeEffect.isVisible());
GradientFillSettings fillSetting = (GradientFillSettings) gradientStrokeEffect.getFillSettings();
Assert.areEqual(Color.getGreen(), fillSetting.getColor());
Assert.areEqual(FillType.Gradient, fillSetting.getFillType());
// Check color points
Assert.areEqual(3, fillSetting.getColorPoints().length);
IGradientColorPoint point = fillSetting.getColorPoints()[0];
Assert.areEqual(50, point.getMedianPointLocation());
Assert.areEqual(Color.getBlack(), point.getColor());
Assert.areEqual(0, point.getLocation());
point = fillSettings.getColorPoints()[1];
Assert.areEqual(50, point.getMedianPointLocation());
Assert.areEqual(Color.getWhite(), point.getColor());
Assert.areEqual(1899, point.getLocation());
point = fillSettings.getColorPoints()[2];
Assert.areEqual(75, point.getMedianPointLocation());
Assert.areEqual(Color.getGreen(), point.getColor());
Assert.areEqual(4096, point.getLocation());
// Check transparency points
Assert.areEqual(3, fillSettings.getTransparencyPoints().length);
IGradientTransparencyPoint transparencyPoint1 = fillSettings.getTransparencyPoints()[0];
Assert.areEqual(50, transparencyPoint1.getMedianPointLocation());
Assert.areEqual(100, transparencyPoint1.getOpacity());
Assert.areEqual(0, transparencyPoint1.getLocation());
transparencyPoint1 = fillSettings.getTransparencyPoints()[1];
Assert.areEqual(50, transparencyPoint1.getMedianPointLocation());
Assert.areEqual(100, transparencyPoint1.getOpacity());
Assert.areEqual(2411, transparencyPoint1.getLocation());
transparencyPoint1 = fillSettings.getTransparencyPoints()[2];
Assert.areEqual(25, transparencyPoint1.getMedianPointLocation());
Assert.areEqual(25, transparencyPoint1.getOpacity());
Assert.areEqual(4096, transparencyPoint1.getLocation());
```
```

## المشكلات الشائعة ونصائح استكشاف الأخطاء
- **Missing license error** – إذا رأيت استثناء ترخيص، تحقق مرة أخرى من أن ملف الترخيص المؤقت تم تحميله بشكل صحيح قبل أي استدعاء API.  
- **Gradient not visible** – تأكد من أن علم `strokeEnabled` للطبقة المستهدفة مضبوط على `true`؛ وإلا سيتجاهل التأثير أثناء العرض.  
- **Performance on large files** – للملفات التي تزيد عن 500 MB، فكر في استخدام `PsdImage.load(..., LoadOptions)` مع `loadResources = false` وتمكين الموارد التي تحتاجها فقط.

## الأسئلة المتكررة

**س: ما هو Aspose.PSD for Java؟**  
ج: Aspose.PSD for Java هي مكتبة Java صافية تتيح للمطورين إنشاء، تعديل، تحويل، وعرض ملفات Photoshop PSD دون الحاجة إلى Adobe Photoshop.

**س: هل أحتاج إلى ترخيص لاستخدام Aspose.PSD for Java؟**  
ج: نعم، يلزم وجود ترخيص صالح للاستخدام في الإنتاج. يمكنك الحصول على [temporary license](https://purchase.aspose.com/temporary-license/) للتقييم.

**س: هل يمكنني إنشاء ملفات PSD من الصفر باستخدام هذه المكتبة؟**  
ج: بالتأكيد. Aspose.PSD يوفر واجهات برمجة تطبيقات لبناء مستند PSD جديد، إضافة طبقات، تطبيق تأثيرات، وحفظ الملف برمجيًا بالكامل.

**س: هل يمكن تطبيق تأثيرات أخرى غير حدود التدرج؟**  
ج: نعم، يمكنك تطبيق الظلال، التوهجات، الحواف، والعديد من تأثيرات الطبقة الأخرى باستخدام نفس واجهة برمجة التطبيقات القائمة على التأثيرات.

**س: أين يمكنني العثور على الوثائق المرجعية الكاملة؟**  
ج: الوثائق الرسمية متاحة في [Aspose.PSD Java API reference](https://reference.aspose.com/psd/java/).

## الخاتمة
أصبح لديك الآن حل كامل من البداية إلى النهاية حول كيفية **create gradient stroke java** في ملفات PSD باستخدام Aspose.PSD. من خلال تحميل PSD، الوصول إلى تأثير الحد، تكوين تعبئة تدرجية، وحفظ الملف، يمكنك أتمتة سير عمل رسومي متقدم كان سيتطلب عملًا يدويًا في Photoshop. جرّب أنواع تدرج مختلفة، أنماط المزج، ونقاط الشفافية لتحقيق المظهر الدقيق الذي تحتاجه لتطبيقك.

---

**آخر تحديث:** 2026-09-03  
**تم الاختبار مع:** Aspose.PSD for Java 24.11  
**المؤلف:** Aspose

## دروس ذات صلة

- [إنشاء تعبئة تدرجية PSD باستخدام Java و Aspose.PSD – إضافة طبقة تعبئة تدرجية](/psd/java/psd-image-modification-conversion/add-gradient-fill-layer-psd-files/)
- [كيفية إنشاء تأثيرات تدرج دائرية في Aspose.PSD for Java](/psd/java/advanced-image-effects/add-gradient-effects/)
- [كيفية تغيير لون الحد Java باستخدام Aspose.PSD](/psd/java/advanced-image-effects/add-stroke-layer-color/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}