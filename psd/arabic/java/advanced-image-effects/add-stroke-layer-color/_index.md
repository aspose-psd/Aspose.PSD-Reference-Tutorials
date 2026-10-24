---
date: 2026-10-24
description: تعلم كيفية إنشاء طبقة حد في Java باستخدام Aspose.PSD. يوضح لك هذا الدليل
  خطوة بخطوة كيفية إضافة طبقة حد، تغيير لونها، تعديل الشفافية، وحفظ ملف PSD.
keywords:
- create stroke layer java
- change stroke color java
- modify stroke opacity
- apply stroke effect
- psd stroke tutorial
lastmod: 2026-10-24
linktitle: إضافة لون طبقة الحد
og_description: إنشاء طبقة حد في Java باستخدام Aspose.PSD. اتبع هذا الدرس المختصر
  لإضافة طبقة حد، تغيير لونها، تعديل الشفافية، وتصدير ملف PSD.
og_image_alt: Screenshot of a Java IDE showing Aspose.PSD code that creates and modifies
  a stroke layer in a PSD file
og_title: إنشاء طبقة حد في Java باستخدام Aspose.PSD – دليل سريع
schemas:
- author: Aspose
  dateModified: '2026-10-24'
  description: Learn how to create stroke layer Java with Aspose.PSD for Java. This
    step‑by‑step guide shows you how to add a stroke layer, change its color, adjust
    opacity, and save the PSD.
  headline: How to create stroke layer Java using Aspose.PSD
  type: TechArticle
- description: Learn how to create stroke layer Java with Aspose.PSD for Java. This
    step‑by‑step guide shows you how to add a stroke layer, change its color, adjust
    opacity, and save the PSD.
  name: How to create stroke layer Java using Aspose.PSD
  steps:
  - name: set up your project
    text: Create a new Java project, add the Aspose.PSD JAR to the build path, and
      verify the library loads without errors.
  - name: load the PSD file
    text: Enable loading of effect resources so the stroke information is available.
  - name: access the stroke effect layer
    text: '`StrokeEffect` is Aspose.PSD’s class that represents a vector outline applied
      to a layer. Retrieve the first stroke effect from the second layer (index 1).'
  - name: validate stroke properties
    text: '`ColorFillSettings` holds the color and opacity values for a stroke. Confirm
      the existing properties before making changes to avoid unexpected results.'
  - name: set color and opacity (how to change stroke color)
    text: Here we **change stroke color** to yellow and reduce opacity to 50 % (127
      / 255). `ColorFillSettings` also lets you specify blend mode and size.
  - name: save the modified PSD
    text: Write the updated image back to disk. The new file now contains the modified
      stroke.
  type: HowTo
- questions:
  - answer: Yes, Aspose.PSD can be combined with libraries such as Apache Commons
      Imaging or Java2D for extended functionality.
    question: Can I use Aspose.PSD with other Java graphic libraries?
  - answer: Absolutely. The library supports the newest Photoshop specifications and
      over 150 PSD features.
    question: Is Aspose.PSD compatible with the latest PSD file format?
  - answer: Wrap your code in try‑catch blocks and consult the [support forum](https://forum.aspose.com/c/psd/34)
      for detailed troubleshooting examples.
    question: How do I handle exceptions while using Aspose.PSD?
  - answer: Certainly! Grab a [free trial](https://releases.aspose.com/) to explore
      all features.
    question: Can I try Aspose.PSD before purchasing?
  - answer: Obtain a [temporary license](https://purchase.aspose.com/temporary-license/)
      to evaluate the library in your development environment.
    question: Where can I get a temporary license for Aspose.PSD?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- create stroke layer
- Aspose.PSD
- Java image processing
title: كيفية إنشاء طبقة الحد في Java باستخدام Aspose.PSD
url: /ar/java/advanced-image-effects/add-stroke-layer-color/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# كيفية إنشاء طبقة حد Java باستخدام Aspose.PSD

## مقدمة

إذا كنت بحاجة إلى **create stroke layer Java** في مستند Photoshop برمجيًا، فإن Aspose.PSD for Java يوفّر لك نهجًا نظيفًا يعتمد على الكود أولًا. في هذا البرنامج التعليمي ستتعلم كيفية إضافة طبقة حد جديدة، تغيير لونها، تعديل الشفافية، وحفظ النتيجة — كل ذلك دون تشغيل Photoshop. في النهاية ستعرف أيضًا كيفية تعديل حد طبقة موجودة، مما يمنحك تحكمًا إبداعيًا كاملًا مباشرةً من تطبيق Java الخاص بك.

## إجابات سريعة
- **ما المكتبة المطلوبة؟** Aspose.PSD for Java (latest version).  
- **هل يمكنني تغيير لون الحد؟** Yes – use `ColorFillSettings` to set any `Color`.  
- **هل أحتاج إلى ترخيص؟** A temporary license works for evaluation; a full license is required for production.  
- **ما إصدار Java المدعوم؟** Java 8 or higher.  
- **كم من الوقت تستغرق العملية؟** Typically under 10 minutes for a basic stroke change.

## ما هي طبقة الحد في ملف PSD؟

طبقة الحد هي تأثير متجهي يرسم حدودًا حول محتويات الطبقة. يمكن تخصيصها باللون والسُمك والشفافية ووضع الدمج. تعديل هذا التأثير برمجيًا يتيح العلامة التجارية الآلية، المعالجة الدفعية، أو إنشاء رسومات ديناميكية.

## لماذا تستخدم Aspose.PSD لتغيير لون الحد؟

Aspose.PSD يدعم **150+** من ميزات PSD — بما في ذلك الأقنعة المتجهية، الكائنات الذكية، وتأثيرات الطبقة — مع معالجة ملفات مئات الصفحات دون تحميل المستند بالكامل إلى الذاكرة. تعمل المكتبة على أي نظام تشغيل يحتوي على JVM، وتقدّم أداءً أقل من الثانية للأصول النموذجية، ولا تتطلب تثبيت Photoshop.

## كيفية إنشاء طبقة حد Java؟

حمّل ملف PSD، أضف تأثير حد، اضبط مظهره، واحفظ الملف — كل ذلك في بضع أسطر بسيطة. الإجابة أدناه توضح لك ما يجب فعله قبل أن نغوص في الشرح خطوة بخطوة.

**الإجابة المباشرة (40‑70 كلمة):**  
`PsdImage` represents a PSD document and provides methods to load and save files. Start by loading your PSD with `PsdImage.load("input.psd", loadOptions)`. Create a new `StrokeEffect`, set its `ColorFillSettings` to the desired `Color`, adjust opacity and size, then attach the effect to the target layer’s `BlendingOptions`. Finally, call `psd.save("output.psd", SaveFormat.PSD)`. This sequence creates a stroke layer in Java with Aspose.PSD.

### المتطلبات المسبقة

- **مكتبة Aspose.PSD** – تحميل من [official documentation](https://reference.aspose.com/psd/java/).  
- **Java Development Kit (JDK)** – version 8 or newer.  
- **IDE** – Eclipse, IntelliJ IDEA, or any Java‑compatible editor.

### استيراد الحزم

أولاً، استورد الفئات التي ستحتاجها. هذا يمنح مشروعك الوصول إلى واجهات برمجة تطبيقات معالجة PSD وتأثير الحد.

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;


import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.BlendMode;
import com.aspose.psd.fileformats.psd.layers.fillsettings.ColorFillSettings;
import com.aspose.psd.fileformats.psd.layers.fillsettings.FillType;
import com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
```

### الخطوة 1: إعداد مشروعك

أنشئ مشروع Java جديد، أضف ملف Aspose.PSD JAR إلى مسار البناء، وتأكد من تحميل المكتبة دون أخطاء.

### الخطوة 2: تحميل ملف PSD

فعّل تحميل موارد التأثير حتى تتوفر معلومات الحد.

```java
String dataDir = "Your Document Directory";

String sourceFileName = dataDir + "Stroke.psd";
String exportPath = dataDir + "StrokeGradientChanged.psd";

PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);
```

### الخطوة 3: الوصول إلى طبقة تأثير الحد

`StrokeEffect` هي فئة Aspose.PSD التي تمثل حدودًا متجهية تُطبق على طبقة. استرجع أول تأثير حد من الطبقة الثانية (الفهرس 1).

```java
StrokeEffect colorStroke = (StrokeEffect)im.getLayers()[1].getBlendingOptions().getEffects()[0];
```

### الخطوة 4: التحقق من خصائص الحد

`ColorFillSettings` يحتوي على قيم اللون والشفافية للحد. تأكد من الخصائص الحالية قبل إجراء التغييرات لتجنب النتائج غير المتوقعة.

```java
Assert.areEqual(BlendMode.Normal, colorStroke.getBlendMode());
Assert.areEqual(255, colorStroke.getOpacity());
Assert.areEqual(true, colorStroke.isVisible());
```

### الخطوة 5: ضبط اللون والشفافية (كيفية تغيير لون الحد)

هنا ن**change stroke color** إلى الأصفر ونقلل الشفافية إلى 50 % (127 / 255). `ColorFillSettings` يتيح لك أيضًا تحديد وضع الدمج والحجم.

```java
ColorFillSettings fillSettings = (ColorFillSettings)colorStroke.getFillSettings();
fillSettings.setColor(Color.getYellow());

colorStroke.setOpacity((byte)127);
```

### الخطوة 6: حفظ ملف PSD المعدل

اكتب الصورة المحدثة مرة أخرى إلى القرص. الملف الجديد الآن يحتوي على الحد المعدل.

```java
im.save(exportPath);
```

## كيفية تغيير لون الحد Java؟

`Color` تمثل قيمة لون ARGB. حمّل ملف PSD الخاص بك، حدد الطبقة المستهدفة، حدّث `ColorFillSettings` بلون جديد `Color`، واحفظ الملف. هذه العملية تحتاج إلى بضع أسطر من الكود فقط وتكتمل في أقل من ثانية للأصول النموذجية، مما يجعلها سريعة وفعّالة.

**الإجابة المباشرة (40‑70 كلمة):**  
استخدم `layer.getEffects().getStrokeEffect()` للحصول على الحد الموجود، استدعِ `stroke.getColorFillSettings().setColor(Color.getRed())` (أو أي `Color` تحتاجه)، يمكنك تعديل `setOpacity((byte)200)` للحصول على شفافية 78 %، ثم احفظ ملف PSD باستخدام `psd.save("output.psd", SaveFormat.PSD)`. يتم تطبيق التغيير فورًا دون إعادة تصيير المستند بالكامل.

## كيفية تعديل شفافية الحد؟

إذا كنت بحاجة فقط إلى تعديل الشفافية مع الحفاظ على اللون الأصلي، غيّر قيمة `setOpacity` (0‑255) في `ColorFillSettings`. على سبيل المثال، `colorStroke.setOpacity((byte)200);` سيجعل الحد شفافًا تقريبًا بنسبة 78 %. تعديل الشفافية يتيح لك إنشاء حدود خفيفة أو حدود صلبة تمامًا، حسب متطلبات التصميم.

**الإجابة المباشرة (40‑70 كلمة):**  
استخرج `StrokeEffect` من الطبقة المطلوبة، ثم استدعِ `stroke.getColorFillSettings().setOpacity((byte)desiredValue)`، حيث يتراوح `desiredValue` بين 0 (شفاف) و255 (معتم تمامًا). احفظ ملف PSD وسيظهر التغيير في الشفافية فورًا. هذا النهج يعمل مع أي حد موجود، بغض النظر عن لونه الأصلي.

## كيفية تطبيق تأثير الحد؟

لإضافة تأثير حد جديد إلى طبقة لا تحتوي على أحد مسبقًا، أنشئ كائن `StrokeEffect`، اضبط `ColorFillSettings` الخاص به، وأرفقه بـ `BlendingOptions` للطبقة. تُستخدم نفس طُرُق `setColor` و `setOpacity` لتحديد المظهر العام.

**الإجابة المباشرة (40‑70 كلمة):**  
أنشئ `StrokeEffect newStroke = new StrokeEffect(); newStroke.getColorFillSettings().setColor(Color.getBlue()); newStroke.getColorFillSettings().setOpacity((byte)255); layer.getBlendingOptions().setEffect(newStroke);`. بعد إرفاق التأثير، احفظ ملف PSD. يضيف هذا طبقة حد جديدة وقابلة للتخصيص بالكامل إلى أي طبقة موجودة في المستند.

## حالات الاستخدام الشائعة لتغيير لون الحد
- **أتمتة العلامة التجارية:** تطبيق لون الشركة على الشعارات عبر مئات ملفات PSD في تشغيل دفعي واحد.  
- **إنشاء واجهة مستخدم ديناميكية:** تغيير ألوان الحد في الوقت الفعلي بناءً على السمات المختارة من قبل المستخدم في أداة تصميم ويب.  
- **التحضير المسبق:** التأكد من أن جميع ألوان الحد تتوافق مع مواصفات الطباعة قبل إرسال الملفات إلى المطبعة.

## المشكلات الشائعة والنصائح

- **فحوصات null** – تحقق دائمًا من أن `getEffects()` تُعيد مصفوفة غير فارغة قبل التحويل.  
- **فهرس الطبقة** – طبقات PSD تبدأ من الصفر؛ تأكد من استهداف الطبقة الصحيحة.  
- **تنسيق اللون** – `Color.getYellow()` مجرد مثال؛ يمكنك إنشاء ألوان مخصصة باستخدام `new Color(r, g, b)`.  
- **نطاق الشفافية** – الشفافية هي بايت (0–255)؛ القيم فوق 255 سيتم تقليصها.  
- **تحميل الموارد** – نسيان `loadOptions.setLoadEffectsResource(true)` سيؤدي إلى مصفوفة تأثيرات `null`.

## الأسئلة المتكررة

**س: هل يمكنني استخدام Aspose.PSD مع مكتبات رسومات Java أخرى؟**  
ج: نعم، يمكن دمج Aspose.PSD مع مكتبات مثل Apache Commons Imaging أو Java2D للحصول على وظائف موسعة.

**س: هل Aspose.PSD متوافق مع أحدث تنسيق ملفات PSD؟**  
ج: بالتأكيد. تدعم المكتبة أحدث مواصفات Photoshop وأكثر من 150 ميزة في PSD.

**س: كيف أتعامل مع الاستثناءات أثناء استخدام Aspose.PSD؟**  
ج: ضع الكود داخل كتل try‑catch واستشر [support forum](https://forum.aspose.com/c/psd/34) للحصول على أمثلة تفصيلية لحل المشكلات.

**س: هل يمكنني تجربة Aspose.PSD قبل الشراء؟**  
ج: بالطبع! احصل على [free trial](https://releases.aspose.com/) لاستكشاف جميع الميزات.

**س: أين يمكنني الحصول على ترخيص مؤقت لـ Aspose.PSD؟**  
ج: احصل على [temporary license](https://purchase.aspose.com/temporary-license/) لتقييم المكتبة في بيئة التطوير الخاصة بك.

---

**آخر تحديث:** 2026-10-24  
**تم الاختبار مع:** Aspose.PSD 24.11 for Java  
**المؤلف:** Aspose

## دروس ذات صلة

- [كيفية تغيير لون الحد Java باستخدام Aspose.PSD](/psd/java/advanced-image-effects/add-stroke-layer-color/)
- [كيفية إضافة ظل في PSD باستخدام Java – تأثيرات الطبقة المتقدمة](/psd/java/advanced-psd-layer-features-effects/)
- [تراكب نمط PSD: إضافة تأثيرات مع Aspose.PSD for Java](/psd/java/advanced-image-effects/add-pattern-effects/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}