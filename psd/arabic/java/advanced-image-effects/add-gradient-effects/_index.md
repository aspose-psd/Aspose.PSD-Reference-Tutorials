---
date: 2026-10-18
description: تعلم كيفية إنشاء تأثيرات التدرج الشعاعي في صور Java باستخدام Aspose.PSD.
  اتبع هذا الدليل خطوة بخطوة للتكامل السلس.
keywords:
- create radial gradient java
- apply gradient overlay psd
- add radial gradient image
lastmod: 2026-10-18
linktitle: إضافة تأثيرات التدرج
og_description: تعلم إنشاء تأثيرات التدرج الشعاعي java باستخدام Aspose.PSD. يوضح هذا
  البرنامج التعليمي كيفية إضافة وتخصيص وحفظ طبقات التدرج في دقائق.
og_image_alt: Screenshot of Aspose.PSD Java code creating a radial gradient effect
og_title: إنشاء تدرج شعاعي java مع Aspose.PSD – دليل خطوة بخطوة
schemas:
- author: Aspose
  dateModified: '2026-10-18'
  description: Learn how to create radial gradient effects in Java images using Aspose.PSD.
    Follow this step‑by‑step guide for seamless integration.
  headline: How to create radial gradient effects in Aspose.PSD for Java
  type: TechArticle
- description: Learn how to create radial gradient effects in Java images using Aspose.PSD.
    Follow this step‑by‑step guide for seamless integration.
  name: How to create radial gradient effects in Aspose.PSD for Java
  steps:
  - name: Load the PSD file and access the gradient overlay
    text: '`PsdLoadOptions` configures how a PSD file is loaded, allowing you to enable
      loading of effect resources. `Image.load` reads the file into an `Image` object.
      In this step, we load a PSD file and retrieve the first `GradientOverlayEffect`
      from the second layer (index 1). The `loadOptions.setLoadEffec'
  - name: Verify Initial Settings
    text: Before making changes, it’s a good practice to confirm the current blend
      mode, opacity, and visibility. This helps you understand the baseline state
      of the gradient overlay.
  - name: Modify Gradient Settings
    text: Here you can customize the gradient’s color, opacity, and blend mode. The
      example changes the color to green, reduces opacity to 193 (out of 255), and
      switches the blend mode to **Lighten**. Feel free to experiment with other `BlendMode`
      values such as `Multiply`, `Screen`, or `Overlay`.
  - name: Save the Edited Image
    text: After applying your modifications, persist the changes by saving the PSD
      to a new file. This step ensures the original file remains untouched.
  - name: Verify Changes
    text: The snippet above demonstrates how to open a PSD, pull the second layer’s
      first effect (assumed to be a gradient overlay), and prepare it for modification.
  - name: Verify the original settings (optional but recommended)
    text: Before you change anything, checking the existing blend mode, opacity, and
      visibility helps you understand the baseline. The `Assert` calls in the code
      confirm that the effect is currently set to **Normal** blend mode, fully opaque,
      and visible.
  - name: Adjust gradient properties to achieve a radial style
    text: 'You can change the gradient’s color, opacity, and blend mode. For a true
      radial effect, set the gradient style: *Pro tip:* Use `Color.getGreen()` or
      any `java.awt.Color` instance to define the start color, and `gradientOverlay.setColor2(Color.getBlue())`
      for the end color.'
  - name: Save the edited PSD
    text: Calling `im.save(exportPath);` writes the modified image to disk. The saved
      file retains the radial gradient overlay and can be opened in Photoshop, previewed
      in browsers, or converted to other formats.
  type: HowTo
- questions:
  - answer: Yes. Retrieve the layer’s `BlendingOptions`, iterate through the `Effects`
      collection, and add a new `GradientOverlayEffect` for each gradient you need.
    question: Can I apply multiple gradient effects to a single image?
  - answer: Aspose.PSD provides shadows, glows, bevels, and more. Each effect appears
      in the `Effects` array and can be configured independently.
    question: What other effects can I combine with gradient overlays?
  - answer: Verify that the PSD was loaded with `setLoadEffectsResource(true)`, check
      layer visibility, and confirm you are modifying the correct effect index.
    question: How can I troubleshoot if the effects are not rendering correctly?
  - answer: Yes, you can get a free trial [here](https://releases.aspose.com/).
    question: Is there a trial version available for Aspose.PSD for Java?
  - answer: Visit the [purchase page](https://purchase.aspose.com/buy) for licensing
      information.
    question: Where can I purchase a license for Aspose.PSD for Java?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- create radial gradient
- gradient overlay effect
- Aspose.PSD Java
title: كيفية إنشاء تأثيرات التدرج الشعاعي في Aspose.PSD للـ Java
url: /ar/java/advanced-image-effects/add-gradient-effects/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# كيفية إنشاء تأثيرات التدرج الشعاعي في Aspose.PSD للـ Java

## المقدمة

في هذا الدليل ستتعلم كيفية **إنشاء تأثيرات التدرج الشعاعي Java** باستخدام مكتبة Aspose.PSD. التدرجات الشعاعية مثالية لإضافة العمق أو التركيز أو توهج خفيف إلى طبقات PSD الخاصة بك دون فتح Photoshop. في نهاية الدرس ستكون قادرًا على تحميل ملف PSD، تطبيق تدرج فوقي، تعديل خصائصه، وحفظ النتيجة — كل ذلك من خلال كود Java.

## إجابات سريعة
- **What can I achieve?** أضف، حرر، واخلط تدرجات شعاعية فوقية على طبقات PSD.  
- **Which library is required?** Aspose.PSD for Java (أحدث إصدار).  
- **Do I need a license?** النسخة التجريبية المجانية تعمل للتطوير؛ يلزم الحصول على ترخيص تجاري للإنتاج.  
- **How long does implementation take?** تقريبًا 10‑15 دقيقة لإنشاء تدرج شعاعي أساسي.  
- **Is it compatible with Java 8+?** نعم، الـ API يدعم Java 8 والإصدارات الأحدث.

## المتطلبات المسبقة

قبل أن نبدأ الدرس، تأكد من توفر المتطلبات المسبقة التالية:

1. **Aspose.PSD for Java Library** – تأكد من أنك قمت بتحميل وتثبيت مكتبة Aspose.PSD for Java. يمكنك العثور على المكتبة ووثائقها في [Aspose.PSD Java documentation page](https://reference.aspose.com/psd/java/).  
2. **Java Development Environment** – قم بإعداد بيئة تطوير Java على جهازك (JDK 8 أو أعلى، IDE من اختيارك).  
3. **Latest Aspose.PSD release** – حمّل أحدث نسخة من [Aspose releases page](https://releases.aspose.com/).  
4. **Support resources** – إذا واجهت مشاكل، راجع [Aspose.PSD Support forum](https://forum.aspose.com/c/psd/34).  
5. **License purchase** – عندما تكون جاهزًا للإنتاج، احصل على ترخيص عبر [purchase page](https://purchase.aspose.com/buy).

الآن بعد أن تم إعداد كل شيء، دعنا نتابع دليل الخطوة بخطوة.

## ما هو تأثير التدرج الفوقي؟

تأثير التدرج الفوقي يرسم انتقالًا سلسًا بين لونين أو أكثر عبر منطقة مختارة من الطبقة. في Photoshop يمكن دمج هذا التأثير، تلوينه، وتحديد موقعه لإنشاء تصاميم بصرية متقنة. فئة `GradientOverlayEffect` هي تمثيل Aspose.PSD لهذا النمط الطبقي، وتُظهر خصائص مثل نقاط اللون، الشفافية، وضع الدمج، ونمط التدرج.

## كيفية إنشاء تأثير التدرج الشعاعي

حمّل ملف PSD، حدد الطبقة المستهدفة، عدّل خصائص `GradientOverlayEffect`، وأخيرًا احفظ الملف. سير العمل الكامل يكتمل في أربع أسطر مختصرة من كود Java بمجرد تحميل الصورة.

### الخطوة 1: تحميل ملف PSD والوصول إلى التدرج الفوقي

`PsdLoadOptions` يضبط طريقة تحميل ملف PSD، مما يتيح لك تمكين تحميل موارد التأثير. `Image.load` يقرأ الملف إلى كائن `Image`.

```javaString dataDir = "Your Document Directory";

// Gradient overlay effect. Example
String sourceFileName = dataDir + "GradientOverlay.psd";
String exportPath = dataDir + "GradientOverlayChanged.psd";

PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);

GradientOverlayEffect gradientOverlay = (GradientOverlayEffect)im.getLayers()[1].getBlendingOptions().getEffects()[0];
```

في هذه الخطوة، نقوم بتحميل ملف PSD ونستخرج أول `GradientOverlayEffect` من الطبقة الثانية (الفهرس 1). استدعاء `loadOptions.setLoadEffectsResource(true)` يضمن توفر موارد التأثير للتحرير.

### الخطوة 2: التحقق من الإعدادات الأولية

```java
// Verify initial settings
Assert.areEqual(BlendMode.Normal, gradientOverlay.getBlendMode());
Assert.areEqual(255, gradientOverlay.getOpacity());
Assert.areEqual(true, gradientOverlay.isVisible());
// ... (additional verifications)
```

قبل إجراء أي تغييرات، من الممارسات الجيدة التأكد من وضع الدمج الحالي، الشفافية، والظهور. هذا يساعدك على فهم الحالة الأساسية للتدرج الفوقي.

### الخطوة 3: تعديل إعدادات التدرج

```java
// Modify gradient settings
settings.setColor(Color.getGreen());
gradientOverlay.setOpacity((byte)193);
gradientOverlay.setBlendMode(BlendMode.Lighten);
// ... (additional modifications)
```

هنا يمكنك تخصيص لون التدرج، الشفافية، ووضع الدمج. المثال يغيّر اللون إلى الأخضر، يقلل الشفافية إلى 193 (من 255)، ويبدل وضع الدمج إلى **Lighten**. لا تتردد في تجربة قيم `BlendMode` أخرى مثل `Multiply` أو `Screen` أو `Overlay`.

### الخطوة 4: حفظ الصورة المعدلة

```java
// Save the edited image
im.save(exportPath);
```

بعد تطبيق التعديلات، احفظ التغييرات عن طريق حفظ ملف PSD إلى ملف جديد. هذه الخطوة تضمن بقاء الملف الأصلي دون تعديل.

### الخطوة 5: التحقق من التغييرات

```java
// Verify changes after editing
PsdImage img = (PsdImage)Image.load(sourceFileName, loadOptions);

GradientOverlayEffect gradientOverlayEffect = (GradientOverlayEffect)img.getLayers()[1].getBlendingOptions().getEffects()[0];
// ... (additional verifications)
```

المقتطف أعلاه يوضح كيفية فتح ملف PSD، استخراج أول تأثير من الطبقة الثانية (المفترض أنه تدرج فوقي)، وتحضيرها للتعديل.

### الخطوة 2: التحقق من الإعدادات الأصلية (اختياري لكن موصى به)

قبل أن تقوم بأي تغيير، يساعد فحص وضع الدمج الحالي، الشفافية، والظهور على فهم الحالة الأساسية. استدعاءات `Assert` في الكود تؤكد أن التأثير مضبوط حاليًا على وضع الدمج **Normal**، شفاف بالكامل، ومظهر.

### الخطوة 3: تعديل خصائص التدرج لتحقيق نمط شعاعي

يمكنك تغيير لون التدرج، الشفافية، ووضع الدمج. للحصول على تأثير شعاعي حقيقي، اضبط نمط التدرج:

```java
gradientOverlay.setGradientStyle(GradientStyle.Radial);
gradientOverlay.setAngle(0f); // angle is ignored for radial, but required by API
gradientOverlay.setScale(100f); // 100 % fills the layer
```

*نصيحة احترافية:* استخدم `Color.getGreen()` أو أي كائن `java.awt.Color` لتحديد لون البداية، واستخدم `gradientOverlay.setColor2(Color.getBlue())` للون النهاية.

### الخطوة 4: حفظ ملف PSD المعدل

استدعاء `im.save(exportPath);` يكتب الصورة المعدلة إلى القرص. الملف المحفوظ يحتفظ بالتدرج الشعاعي الفوقي ويمكن فتحه في Photoshop، معاينته في المتصفحات، أو تحويله إلى صيغ أخرى.

## لماذا إنشاء تدرجات شعاعية فوقية؟

التدرجات الشعاعية تضيف العمق والتركيز إلى التصاميم، مما يجعل العناصر تبدو ثلاثية الأبعاد أو مسلطة الضوء. إنها مثالية لـ:

- **ملء الخلفيات** التي تجذب الانتباه إلى العنصر المركزي.  
- **تسليط الضوء على الأزرار أو الأيقونات** حيث يلزم توهج خفيف.  
- **تأثيرات صور إبداعية** مثل الفينيت أو انفجارات الضوء.

Aspose.PSD يعالج **أكثر من 50 تنسيق إدخال وإخراج** ويمكنه التعامل مع ملفات PSD متعددة المئات من الصفحات دون تحميل المستند بالكامل إلى الذاكرة، مما يتيح لك أتمتة إنشاء التدرجات عبر مكتبات أصول كبيرة.

## المشكلات الشائعة والنصائح

- **Effect not visible:** تأكد من أن `gradientOverlay.isVisible()` تُعيد `true`. بعض ملفات PSD تخفي التأثيرات افتراضيًا.  
- **Incorrect layer index:** الطبقات تبدأ من الصفر؛ تحقق مرة أخرى أنك تستهدف الطبقة الصحيحة (`im.getLayers()[1]` تشير إلى الطبقة الثانية).  
- **Opacity casting:** طريقة `setOpacity` تتوقع `byte`. تمرير `int` سيسبب خطأ تجميع؛ قم بالتحويل الصريح كما هو موضح.  
- **Resource loading:** إذا صادفت `null` عند الوصول إلى التأثيرات، تأكد من ضبط `loadOptions.setLoadEffectsResource(true)` قبل تحميل الصورة.

## الأسئلة المتكررة

**س: هل يمكنني تطبيق تأثيرات تدرج متعددة على صورة واحدة؟**  
ج: نعم. استخرج `BlendingOptions` للطبقة، وتكرار عبر مجموعة `Effects`، وأضف `GradientOverlayEffect` جديد لكل تدرج تحتاجه.

**س: ما هي التأثيرات الأخرى التي يمكنني دمجها مع التدرجات الفوقية؟**  
ج: Aspose.PSD يوفر الظلال، التوهجات، الحواف، وأكثر. كل تأثير يظهر في مصفوفة `Effects` ويمكن تكوينه بشكل مستقل.

**س: كيف يمكنني استكشاف الأخطاء إذا لم يتم عرض التأثيرات بشكل صحيح؟**  
ج: تأكد من أن ملف PSD تم تحميله باستخدام `setLoadEffectsResource(true)`، تحقق من ظهور الطبقة، وتأكد من تعديل فهرس التأثير الصحيح.

**س: هل هناك نسخة تجريبية متاحة لـ Aspose.PSD for Java؟**  
ج: نعم، يمكنك الحصول على نسخة تجريبية مجانية [هنا](https://releases.aspose.com/).

**س: أين يمكنني شراء ترخيص لـ Aspose.PSD for Java؟**  
ج: زر [صفحة الشراء](https://purchase.aspose.com/buy) للحصول على معلومات الترخيص.

## أسئلة شائعة إضافية

**س: هل يمكنني تغيير اتجاه التدرج برمجيًا؟**  
ج: نعم. استخدم طريقة `GradientOverlayEffect.setAngle(float angle)` لتعيين زاوية التدرج بالدرجات. بالنسبة للتدرجات الشعاعية تُهمل الزاوية، لكن يجب استدعاء الطريقة.

**س: هل يدعم Aspose.PSD التدرجات الشعاعية؟**  
ج: بالتأكيد. اضبط نمط التدرج إلى `GradientStyle.Radial` عبر خصائص `GradientOverlayEffect`.

**س: هل يتم حفظ التدرجات الفوقية عند تحويل PSD إلى صيغ أخرى (مثل PNG)؟**  
ج: عند تحويل PSD إلى صورة نقطية (مثل حفظ كـ PNG)، يتم الاحتفاظ بالنتيجة البصرية للتدرج الفوقي، لكن يصبح التأثير جزءًا من بيانات البكسل.

**س: كيف يمكنني إزالة تدرج فوقي من طبقة؟**  
ج: استخرج `BlendingOptions` للطبقة، حدد `GradientOverlayEffect` في مجموعة `Effects`، وأزله باستخدام `remove(effect)`.

**س: هل يمكن تحريك تغييرات التدرج؟**  
ج: رغم أن Aspose.PSD لا يتعامل مباشرة مع الرسوم المتحركة، يمكنك إنشاء سلسلة من ملفات PSD بمعلمات تدرج مختلفة ثم تجميعها في فيديو أو GIF باستخدام مكتبة أخرى.

## الخاتمة

تهانينا! لقد تعلمت **كيفية إنشاء تأثيرات التدرج الشعاعي Java** لصورك باستخدام Aspose.PSD for Java. باتباع الخطوات أعلاه، يمكنك برمجيًا إضافة، تعديل، وحفظ التدرجات الفوقية، مما يمنحك سيطرة إبداعية كاملة على موارد PSD. جرّب ألوانًا مختلفة، وضعيات دمج، وقيم شفافية لتحقيق التأثير البصري الذي تحتاجه.

---

**آخر تحديث:** 2026-10-18  
**تم الاختبار مع:** Aspose.PSD for Java 24.12 (أحدث نسخة وقت الكتابة)  
**المؤلف:** Aspose  








```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;


import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.BlendMode;
import com.aspose.psd.fileformats.psd.layers.IGradientColorPoint;
import com.aspose.psd.fileformats.psd.layers.fillsettings.*;
import com.aspose.psd.fileformats.psd.layers.layereffects.GradientOverlayEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
```

## دروس ذات صلة

- [إنشاء تعبئة تدرج في PSD باستخدام Java و Aspose.PSD – إضافة طبقة تعبئة تدرج](/psd/java/psd-image-modification-conversion/add-gradient-fill-layer-psd-files/)
- [نمط فوقي PSD: إضافة تأثيرات باستخدام Aspose.PSD for Java](/psd/java/advanced-image-effects/add-pattern-effects/)
- [تطبيق تراكب لون وتعيين الشفافية في Java مع Aspose.PSD](/psd/java/image-editing/color-overlay-effect/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}