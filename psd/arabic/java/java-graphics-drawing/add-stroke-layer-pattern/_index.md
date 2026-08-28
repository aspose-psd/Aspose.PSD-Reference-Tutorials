---
date: 2026-08-28
description: أضف pattern إلى layer في Java باستخدام Aspose.PSD. اتبع هذا الدليل خطوة
  بخطوة لتطبيق stroke layer effect، وتكوين pattern resources، وحفظ ملفات PSD الخاصة
  بك بكفاءة.
keywords:
- add pattern to layer
- java add layer effect
- Aspose.PSD stroke pattern
lastmod: 2026-08-28
linktitle: كيفية إضافة Stroke Layer Pattern في Java
og_description: أضف pattern إلى layer في Java باستخدام Aspose.PSD. اتبع هذا الدليل
  المختصر لتطبيق stroke layer effect، وتكوين pattern resources، وحفظ ملفات PSD الخاصة
  بك بكفاءة.
og_image_alt: Guide showing how to add pattern to layer in Java with Aspose.PSD
og_title: إضافة pattern إلى layer في Java – دليل Aspose.PSD
schemas:
- author: Aspose
  dateModified: '2026-08-28'
  description: Add pattern to layer in Java with Aspose.PSD. Follow this step‑by‑step
    guide to apply a stroke layer effect, configure pattern resources, and save your
    PSD files efficiently.
  headline: How to add pattern to layer in Java
  type: TechArticle
- description: Add pattern to layer in Java with Aspose.PSD. Follow this step‑by‑step
    guide to apply a stroke layer effect, configure pattern resources, and save your
    PSD files efficiently.
  name: How to add pattern to layer in Java
  steps:
  - name: load the PSD file
    text: 'Loading the document gives you access to its layer hierarchy and effect
      collection. `PsdLoadOptions` configures how the PSD is read, while `PsdImage`
      represents the loaded file in memory. java String dataDir = "Your Document Directory";
      String sourceFileName = dataDir + "Stroke.psd"; PsdLoadOptions '
  - name: prepare new pattern data
    text: Create a `PatternResource` that holds the bitmap you want to tile as a stroke
      pattern. `PatternResource` is a PSD global resource that stores a repeating
      bitmap pattern. `Rectangle` defines the bounds of the pattern, and `UUID` provides
      a unique identifier. java int[] newPattern = new int[] { Color.
  - name: access the stroke effect
    text: Identify the shape layer that already has a stroke, then retrieve its `StrokeEffect`
      object. `StrokeEffect` represents the stroke layer effect applied to a shape
      layer. java StrokeEffect patternStroke = (StrokeEffect)im.getLayers()[3].getBlendingOptions().getEffects()[0];
      Assert.areEqual(BlendMode.N
  - name: modify the stroke effect
    text: Now update the stroke’s properties to reference the new pattern resource.
  - name: apply the new pattern
    text: '`PatternFillSettings` holds the fill settings for a pattern‑based stroke
      effect. Commit the changes to the layer and write the updated PSD back to disk.
      java ((PatternFillSettings)patternStroke.getFillSettings()).setPatternName("$$/Presets/Patterns/HorizontalLine1=Horizontal
      Line 9\0"); ((PatternFil'
  - name: verify the changes
    text: 'Reload the file and inspect the stroke to confirm the pattern appears as
      expected. java PsdImage img = (PsdImage)Image.load(sourceFileName, loadOptions);
      StrokeEffect patternStrokeEffect = (StrokeEffect)img.getLayers()[3].getBlendingOptions().getEffects()[0];
      PattResource resource1 = null; for (int '
  type: HowTo
- questions:
  - answer: Aspose.PSD for Java is a library that enables developers to create, edit,
      and convert PSD (Photoshop Document) files programmatically.
    question: What is Aspose.PSD for Java?
  - answer: Yes, you can use it in commercial projects. You can purchase a license
      from the **Aspose purchase page**([Aspose purchase page](https://purchase.aspose.com/buy)).
    question: Can I use Aspose.PSD for Java in a commercial project?
  - answer: Yes, you can download a free trial version from the **Aspose releases
      page**([Aspose releases page](https://releases.aspose.com/)).
    question: Is there a free trial available for Aspose.PSD for Java?
  - answer: You can get support from the Aspose community forums **here**([Aspose
      PSD community forum](https://forum.aspose.com/c/psd/34)).
    question: How can I get support for Aspose.PSD for Java?
  - answer: You need a JDK installed and an IDE for development. The library supports
      Windows, Linux, and macOS.
    question: What are the system requirements for Aspose.PSD for Java?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- java graphics
- Aspose.PSD
- layer effects
title: كيفية إضافة pattern إلى layer في Java
url: /ar/java/java-graphics-drawing/add-stroke-layer-pattern/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# كيفية إضافة نمط إلى طبقة في Java

## مقدمة
إضافة نمط إلى طبقة في Java هو طلب شائع عندما تحتاج إلى إثراء ملفات Photoshop PSD بتأثيرات حد مخصصة. باستخدام Aspose.PSD for Java يصبح هذا الأمر بسيطًا، حتى إذا كنت جديدًا على المكتبة. في هذا الدرس ستتعلم كيفية تحميل ملف PSD، إنشاء مورد نمط، ربطه بتأثير الحد، وحفظ النتيجة — كل ذلك بتعليمات واضحة خطوة بخطوة.

## إجابات سريعة
- **ما المكتبة المطلوبة؟** Aspose.PSD for Java.  
- **كم يستغرق التنفيذ؟** حوالي 10‑15 دقيقة لنمط أساسي.  
- **هل أحتاج إلى ترخيص؟** النسخة التجريبية المجانية تكفي للتطوير؛ يلزم ترخيص تجاري للإنتاج.  
- **ما نسخة Java المدعومة؟** JDK 8 أو أحدث.  
- **هل يمكنني استخدامه في خدمة ويب؟** نعم، الـ API مستقل عن المنصة ويعمل في أي بيئة Java.

## ما هو إضافة نمط إلى طبقة؟
إضافة نمط إلى طبقة يعني تعيين صورة نقطية متكررة إلى تأثير حد أو تعبئة بحيث يتكرر الرسم عبر حدود الشكل. تُستخدم هذه التقنية على نطاق واسع للحدود الزخرفية، القوام، وتراكبات العلامة التجارية، مما يتيح للمصممين إنشاء سمات بصرية متسقة دون الحاجة إلى رسم كل عنصر يدويًا.

## لماذا نستخدم Aspose.PSD لهذا المهمة؟
يدعم Aspose.PSD **أكثر من 30 صيغة صورة** ويمكنه معالجة ملفات PSD حتى **2 GB** دون تحميل المستند بالكامل إلى الذاكرة، مما يوفر أداءً سريعًا على عتاد الخادم المعتاد. يتيح الـ API السلس لك العمل مع تأثيرات الطبقات برمجيًا، مما يلغي الحاجة إلى Photoshop في خطوط المعالجة الآلية.

## المتطلبات المسبقة
- Java Development Kit (JDK) 8 أو أحدث مثبت.
- Aspose.PSD for Java – قم بتنزيله من **صفحة تنزيل Aspose.PSD for Java**([Aspose.PSD for Java download page](https://releases.aspose.com/psd/java/)) وأضف ملف JAR إلى مسار الفئة (classpath) في مشروعك.
- بيئة تطوير متكاملة (IDE) مثل IntelliJ IDEA أو Eclipse لتحرير وتشغيل الكود النموذجي.
- ملف PSD تجريبي يحتوي على طبقة شكل تريد تعديلها.

## استيراد الحزم
أولاً، استورد المساحات التي توفر الوصول إلى كائنات PSD والموارد والتأثيرات.

```
// No actual code block is added to preserve original placeholders.
```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.Rectangle;
import com.aspose.psd.examples.Utils.Assert;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.BlendMode;
import com.aspose.psd.fileformats.psd.layers.fillsettings.FillType;
import com.aspose.psd.fileformats.psd.layers.fillsettings.PatternFillSettings;
import com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect;
import com.aspose.psd.fileformats.psd.layers.layerresources.PattResource;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import java.util.UUID;
```
```

## كيفية إضافة نمط إلى طبقة في Java؟

حمّل ملف PSD المستهدف، أنشئ مورد نمط، اربطه بتأثير الحد للطبقة المطلوبة، وأخيرًا احفظ الملف. هذه العملية المتكاملة تحتاج إلى بضع أسطر من الكود فقط وتعمل مع أي ملف PSD قياسي يحتوي على طبقة شكل متجه.

### الخطوة 1: تحميل ملف PSD
تحميل المستند يمنحك الوصول إلى هيكلية طبقاته ومجموعة التأثيرات.  
`PsdLoadOptions` يحدد كيفية قراءة ملف PSD، بينما `PsdImage` يمثل الملف المحمّل في الذاكرة.

```
// Placeholder for original code.
```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "Stroke.psd";
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);
PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);
```
```

من خلال تحميل ملف PSD، يمكنك الآن الوصول إلى طبقاته وتعديل تأثيراته.

### الخطوة 2: إعداد بيانات النمط الجديد
أنشئ `PatternResource` الذي يحتوي على الصورة النقطية التي تريد تكرارها كنمط للحد.  
`PatternResource` هو مورد عالمي في PSD يخزن نمط صورة نقطية متكررة. `Rectangle` يحدد حدود النمط، و`UUID` يوفر معرفًا فريدًا.

```
// Placeholder for original code.
```java
int[] newPattern = new int[]
{
    Color.getAqua().toArgb(), Color.getRed().toArgb(), Color.getRed().toArgb(), Color.getAqua().toArgb(),
    Color.getAqua().toArgb(), Color.getWhite().toArgb(), Color.getWhite().toArgb(), Color.getAqua().toArgb(),
    Color.getAqua().toArgb(), Color.getWhite().toArgb(), Color.getWhite().toArgb(), Color.getAqua().toArgb(),
    Color.getAqua().toArgb(), Color.getRed().toArgb(), Color.getRed().toArgb(), Color.getAqua().toArgb(),
};
Rectangle newPatternBounds = new Rectangle(0, 0, 4, 4);
UUID guid = UUID.randomUUID();
```
```

ستُستخدم بيانات النمط هذه لإنشاء تأثير الحد الجديد.

### الخطوة 3: الوصول إلى تأثير الحد
حدد طبقة الشكل التي لديها حد بالفعل، ثم استرجع كائن `StrokeEffect` الخاص بها.  
`StrokeEffect` يمثل تأثير الحد المطبق على طبقة الشكل.

```
// Placeholder for original code.
```java
StrokeEffect patternStroke = (StrokeEffect)im.getLayers()[3].getBlendingOptions().getEffects()[0];
Assert.areEqual(BlendMode.Normal, patternStroke.getBlendMode());
Assert.areEqual(255, patternStroke.getOpacity());
Assert.areEqual(true, patternStroke.isVisible());
PatternFillSettings fillSettings = (PatternFillSettings)patternStroke.getFillSettings();
Assert.areEqual(FillType.Pattern, fillSettings.getFillType());
```
```

هذا يضمن أنك تعمل على الطبقة والتأثير الصحيحين.

### الخطوة 4: تعديل تأثير الحد
الآن قم بتحديث خصائص الحد للإشارة إلى مورد النمط الجديد.

#### تحديث خصائص تأثير الحد
```
// Placeholder for original code.
```java
patternStroke.setOpacity((byte)127);
patternStroke.setBlendMode(BlendMode.Color);
```
```

#### تحديث مورد النمط
`PattResource` هو مورد طبقة عالمي في PSD يخزن بيانات النمط.

```
// Placeholder for original code.
```java
PattResource resource;
for (int i = 0; i < im.getGlobalLayerResources().length; i++)
{
    if (im.getGlobalLayerResources()[i] instanceof PattResource)
    {
        resource = (PattResource)im.getGlobalLayerResources()[i];
        resource.setPatternId(guid.toString());
        resource.setName("$$/Presets/Patterns/HorizontalLine1=Horizontal Line 9\0");
        resource.setPattern(newPattern, newPatternBounds);
    }
}
```
```

تستبدل هذه المقاطع النمط الحالي بالنمط الذي قدمته.

### الخطوة 5: تطبيق النمط الجديد
`PatternFillSettings` يحتوي على إعدادات التعبئة لتأثير حد يعتمد على نمط. قم بتطبيق التغييرات على الطبقة واحفظ ملف PSD المحدث إلى القرص.

```
// Placeholder for original code.
```java
((PatternFillSettings)patternStroke.getFillSettings()).setPatternName("$$/Presets/Patterns/HorizontalLine1=Horizontal Line 9\0");
((PatternFillSettings)patternStroke.getFillSettings()).setPatternId(guid.toString() + "\0");
im.save(exportPath);
```
```

هذا يضمن تطبيق النمط الجديد بشكل صحيح وحفظ الملف مع التغييرات.

### الخطوة 6: التحقق من التغييرات
أعد تحميل الملف وتفقد الحد للتأكد من ظهور النمط كما هو متوقع.

```
// Placeholder for original code.
```java
PsdImage img = (PsdImage)Image.load(sourceFileName, loadOptions);
StrokeEffect patternStrokeEffect = (StrokeEffect)img.getLayers()[3].getBlendingOptions().getEffects()[0];
PattResource resource1 = null;
for (int i = 0; i < img.getGlobalLayerResources().length; i++)
{
    if (img.getGlobalLayerResources()[i] instanceof PattResource)
    {
        resource1 = (PattResource)img.getGlobalLayerResources()[i];
    }
}
try
{
    Assert.areEqual(newPattern, resource1.getPatternData());
    Assert.areEqual(newPatternBounds, new Rectangle(0, 0, resource1.getWidth(), resource1.getHeight()));
    Assert.areEqual(guid.toString(), resource1.getPatternId());
    Assert.areEqual(BlendMode.Color, patternStrokeEffect.getBlendMode());
    Assert.areEqual(127, patternStrokeEffect.getOpacity());
    Assert.areEqual(true, patternStrokeEffect.isVisible());
    PatternFillSettings fillSettings1 = (PatternFillSettings)patternStrokeEffect.getFillSettings();
    Assert.areEqual(FillType.Pattern, fillSettings1.getFillType());
}
catch (Exception e)
{
    System.out.println(e.getMessage());
}
```
```

هذه الخطوة تتحقق من أن بيانات النمط قد تم تطبيقها بشكل صحيح على تأثير الحد.

## المشكلات الشائعة واستكشاف الأخطاء
- **النمط غير مرئي:** تأكد من أن DPI لصورة النمط يطابق دقة PSD، وأن علامة `Enabled` للحد مضبوطة على `true`.  
- **ملفات PSD الكبيرة تسبب OutOfMemoryError:** استخدم `PsdImage.load(..., LoadOptions)` مع `LoadOptions.setLoadAllLayers(false)` لتحميل الطبقات عند الحاجة.  
- **تم اختيار طبقة غير صحيحة:** تحقق من فهرس الطبقة أو اسمها قبل الوصول إلى تأثيراتها؛ يمكنك تعداد `psdImage.getLayers()` لعرض الطبقات المتاحة.

## الأسئلة المتكررة

**س: ما هو Aspose.PSD for Java؟**  
ج: Aspose.PSD for Java هي مكتبة تمكن المطورين من إنشاء وتحرير وتحويل ملفات PSD (وثيقة Photoshop) برمجيًا.

**س: هل يمكنني استخدام Aspose.PSD for Java في مشروع تجاري؟**  
ج: نعم، يمكنك استخدامه في المشاريع التجارية. يمكنك شراء ترخيص من **صفحة شراء Aspose**([Aspose purchase page](https://purchase.aspose.com/buy)).

**س: هل تتوفر نسخة تجريبية مجانية لـ Aspose.PSD for Java؟**  
ج: نعم، يمكنك تنزيل نسخة تجريبية مجانية من **صفحة إصدارات Aspose**([Aspose releases page](https://releases.aspose.com/)).

**س: كيف يمكنني الحصول على دعم لـ Aspose.PSD for Java؟**  
ج: يمكنك الحصول على الدعم من منتديات مجتمع Aspose **هنا**([Aspose PSD community forum](https://forum.aspose.com/c/psd/34)).

**س: ما هي متطلبات النظام لـ Aspose.PSD for Java؟**  
ج: تحتاج إلى تثبيت JDK وبيئة تطوير متكاملة (IDE) للتطوير. تدعم المكتبة أنظمة Windows وLinux وmacOS.

## الخلاصة
لقد تعلمت الآن كيفية إضافة نمط إلى طبقة في Java باستخدام Aspose.PSD. باتباع الخطوات أعلاه يمكنك تحسين ملفات PSD برمجيًا باستخدام أنماط حدود مخصصة، أتمتة عمليات العلامة التجارية، ودمج معالجة الرسومات في أي تطبيق مبني على Java. استكشف ميزات أخرى في Aspose.PSD مثل دمج الطبقات، تعديل الألوان، وتصدير إلى PNG أو JPEG لتوسيع مجموعة أدوات معالجة الصور الخاصة بك.

---

**آخر تحديث:** 2026-08-28  
**تم الاختبار مع:** Aspose.PSD 24.11 for Java  
**المؤلف:** Aspose

## دروس ذات صلة

- [عرض طبقة تعبئة النمط في ملفات Psd](/psd/java/advanced-psd-layer-features-effects/render-pattern-fill-layer-psd-files/)
- [تراكب نمط PSD: إضافة تأثيرات باستخدام Aspose.PSD for Java](/psd/java/advanced-image-effects/add-pattern-effects/)
- [كيفية تغيير لون الحد في Java باستخدام Aspose.PSD](/psd/java/advanced-image-effects/add-stroke-layer-color/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}
{{< blocks/products/products-backtop-button >}}