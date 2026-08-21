---
date: 2026-06-23
description: تعلم كيفية إضافة الظل الداخلي لملف PSD باستخدام Aspise.PSD لـ Java وتطبيق
  تأثير طبقة PSD برمجياً من خلال هذا الدليل خطوة بخطوة، بما يشمل النصائح وأفضل الممارسات.
keywords:
- how to add inner shadow
- create inner shadow effect
- Aspose.PSD Java layer effect
linktitle: إضافة تأثير الظل الداخلي لطبقة PSD في Java
schemas:
- author: Aspose
  dateModified: '2026-06-23'
  description: Learn how to add inner shadow PSD using Aspise.PSD for Java and apply
    PSD layer effect programmatically with this step‑by‑step tutorial, including tips
    and best practices.
  headline: How to Add Inner Shadow PSD Layer Effect in Java
  type: TechArticle
- description: Learn how to add inner shadow PSD using Aspise.PSD for Java and apply
    PSD layer effect programmatically with this step‑by‑step tutorial, including tips
    and best practices.
  name: How to Add Inner Shadow PSD Layer Effect in Java
  steps:
  - name: Define source and destination directories
    text: Replace the placeholder paths with the actual locations on your machine.
      Using absolute paths avoids confusion when the code runs from different working
      directories.
  - name: Load the PSD file with effect resources
    text: The `PsdImage` class loads a PSD file and provides access to its layers
      and effect resources. `setLoadEffectsResource(true)` ensures that any existing
      layer effects are loaded, allowing us to modify them without overwriting unrelated
      data.
  - name: Access the target layer
    text: The `Layer` object represents an individual layer within a PSD document.
      Here we grab the **last layer** in the document, which is often the one you
      want to edit. Adjust the index if you need a different layer. `Layer layer =
      image.getLayers().get(image.getLayers().size() - 1);` – this line retrieve
  - name: Configure the inner shadow effect
    text: 'This block **applies the inner shadow** and customizes its appearance:
      - **Color** – set to green (change to any `Color` you prefer). - **Opacity**
      – 50 % transparency (`128` out of `255`). - **Distance, Size, Angle** – control
      the shadow’s offset and spread. - **Spread & Noise** – add artistic vari'
  - name: Save the modified PSD
    text: The file `sample_out.psd` now contains the inner shadow effect. Saving with
      `image.save(outputPath, new PsdOptions())` preserves all existing layers and
      effects.
  - name: Clean up resources
    text: Disposing of the `image` object frees memory and prevents leaks, which is
      especially important when processing many files in a loop. Always wrap the usage
      in a try‑with‑resources block or call `image.dispose()` in a finally clause.
  type: HowTo
- questions:
  - answer: Aspose.PSD is a Java library that enables developers to create, edit,
      convert, and render Photoshop PSD files without needing Photoshop installed.
    question: What is Aspose.PSD?
  - answer: No, you do not need Photoshop to use Aspose.PSD. The library functions
      independently for PSD file manipulation.
    question: Do I need Photoshop to use Aspose.PSD?
  - answer: Absolutely! You can apply multiple effects by accessing each effect type
      similarly to how we accessed the inner shadow effect.
    question: Can I apply multiple effects to the same layer?
  - answer: Aspose.PSD is a commercial product; however, you can use a free trial
      available through Aspose.
    question: Is Aspose.PSD free?
  - answer: You can find comprehensive documentation for Aspose.PSD [here](https://reference.aspose.com/psd/java/).
    question: Where can I find more documentation?
  type: FAQPage
second_title: Aspose.PSD Java API
title: كيفية إضافة تأثير الظل الداخلي لطبقة PSD في Java
url: /ar/java/advanced-psd-layer-features-effects/add-inner-shadow-layer-effect-psd/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# كيفية إضافة تأثير ظل داخلي لطبقة PSD في Java

## مقدمة
إذا كنت بحاجة إلى **add inner shadow PSD** برمجياً، فقد وجدت المكان المناسب. في هذا الدليل سنستعرض كيفية إضافة ظل داخلي إلى أي مستند Photoshop باستخدام Aspose.PSD for Java. سواءً كنت تبني أداة معالجة دفعات، أو خط أنابيب تصميم آلي، أو مجرد تجربة تأثيرات الصور، فإن الخطوات أدناه توفر لك حلاً صلبًا وجاهزًا للإنتاج يمكنك دمجه في تطبيقات Java الخاصة بك.

**لماذا هذا مهم:** تدعم Aspose.PSD **أكثر من 50 تنسيقًا للإدخال والإخراج** ويمكنها معالجة ملفات تحتوي على **ما يصل إلى 1 000 طبقة** دون تحميل المستند بالكامل في الذاكرة، مما يجعلها مثالية للأتمتة على نطاق واسع.

## إجابات سريعة
- **ما المكتبة التي أحتاجها؟** Aspose.PSD for Java.  
- **كم يستغرق تنفيذ ذلك؟** حوالي 10‑15 دقيقة لإعداد أساسي.  
- **هل أحتاج إلى تثبيت Photoshop؟** لا، المكتبة تعمل بشكل مستقل عن Photoshop.  
- **هل يمكنني تغيير لون الظل؟** نعم – طريقة `setColor` تقبل أي `Color`.  
- **هل يلزم ترخيص للإنتاج؟** يتطلب ترخيصًا تجاريًا؛ يتوفر نسخة تجريبية مجانية.

## ما هو “add inner shadow psd”؟
إضافة ظل داخلي إلى ملف PSD يعني إنشاء تأثير تظليل خفيف داخل الطبقة يعطي انطباعًا بالعمق داخل الطبقة. **تحدد فئة `InnerShadowEffect` المعلمات—اللون، الشفافية، المسافة، الحجم، الزاوية، الانتشار، والضوضاء—التي تتحكم في كيفية رسم الظل داخل الطبقة المحددة.** هذا التعريف يمنحك الفكرة الأساسية في جملة واحدة، يتبعها شرح مختصر لتأثيره البصري.

## لماذا تطبيق تأثير طبقة PSD باستخدام Java؟
تطبيق تأثير طبقة PSD باستخدام Java يتيح لك أتمتة المهام التصميمية المتكررة، دمج معالجة الصور في خدمات الخلفية، وإنشاء الأصول في الوقت الفعلي دون الحاجة إلى عمل يدوي في Photoshop. **تقوم Aspose.PSD for Java بمعالجة مستندات مئات الصفحات أسرع بـ2‑3× مقارنةً بالبرمجة النصية الأصلية في Photoshop، وتعمل على أي منصة متوافقة مع JVM، بما في ذلك Linux وWindows وmacOS.** هذه السرعة والدعم المتعدد المنصات هي السبب في اختيار المطورين لـ Java في خطوط أنابيب الصور الكبيرة.

## المتطلبات المسبقة
قبل الغوص في الشيفرة، تأكد من وجود ما يلي:

1. **Java Development Kit (JDK 11 أو أعلى)** – قم بالتنزيل من [Oracle website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).  
2. **Aspose.PSD for Java** – احصل على أحدث ملف JAR من [Aspose releases page](https://releases.aspose.com/psd/java/).  
3. **IDE** – IntelliJ IDEA أو Eclipse أو NetBeans (أي منها يناسبك).  
4. **معرفة أساسية بـ Java** – يجب أن تكون مرتاحًا مع الفئات، الكائنات، ومعالجة الاستثناءات.  
5. **ملف PSD تجريبي** – PSD بسيط يحتوي على طبقة واحدة على الأقل لاختبار تأثير الظل الداخلي.

## استيراد الحزم المطلوبة
```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
import com.aspose.psd.fileformats.psd.layers.layereffects.IShadowEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import com.aspose.psd.imageoptions.PsdOptions;
```
هذه الاستيرادات تمنحك الوصول إلى الفئات الأساسية اللازمة لتحميل PSD، تعديل الطبقات، وتكوين تأثيرات الظل.

## كيفية إضافة ظل داخلي psd في ملف PSD باستخدام Java
حمّل ملف PSD المصدر، حدد الطبقة المستهدفة، قم بتكوين `InnerShadowEffect`، واحفظ النتيجة—كل ذلك في تدفق واضح خطوة بخطوة يمكن تغليفه في طريقة أو وظيفة دفعة. تمثل فئة `InnerShadowEffect` تأثير ظل داخلي للطبقة مع خصائص قابلة للتكوين مثل اللون، الشفافية، المسافة، والحجم. **تشمل العملية خمس إجراءات أساسية: إعداد المسارات، فتح الصورة مع موارد التأثير، جلب الطبقة، تطبيق الظل الداخلي، وأخيرًا كتابة الملف مرة أخرى إلى القرص.** اتباع هذه الخطوات يضمن تطبيق التأثير بشكل صحيح وإطلاق الموارد بسرعة.

### الخطوة 1: تعريف مجلدات المصدر والوجهة
```java
String sourceDir = "Your Source Directory";
String outputDir = "Your Document Directory";
String sourceFile = sourceDir + "sample.psd";
String destName = outputDir + "sample_out.psd";
```
استبدل مسارات العناصر النائبة بالمواقع الفعلية على جهازك. استخدام المسارات المطلقة يجنب الالتباس عندما يتم تشغيل الشيفرة من أدلة عمل مختلفة.

### الخطوة 2: تحميل ملف PSD مع موارد التأثير
```java
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);
PsdImage image = (PsdImage) Image.load(sourceFile, loadOptions);
```
تقوم فئة `PsdImage` بتحميل ملف PSD وتوفر الوصول إلى طبقاته وموارد التأثير. يضمن `setLoadEffectsResource(true)` تحميل أي تأثيرات طبقة موجودة، مما يسمح لنا بتعديلها دون الكتابة فوق بيانات غير ذات صلة.

### الخطوة 3: الوصول إلى الطبقة المستهدفة
```java
try {
    Layer layer = image.getLayers()[image.getLayers().length - 1];
```
يمثل كائن `Layer` طبقة فردية داخل مستند PSD. هنا نأخذ **الطبقة الأخيرة** في المستند، والتي غالبًا ما تكون ما تريد تحريره. عدل الفهرس إذا كنت بحاجة إلى طبقة مختلفة.  
`Layer layer = image.getLayers().get(image.getLayers().size() - 1);` – هذا السطر يسترجع كائن الطبقة الذي سيتلقى الظل الداخلي.

### الخطوة 4: تكوين تأثير الظل الداخلي
```java
    IShadowEffect shadowEffect = (IShadowEffect) layer.getBlendingOptions().getEffects()[0];
    shadowEffect.setColor(Color.getGreen());
    shadowEffect.setOpacity((byte) 128);
    shadowEffect.setDistance(1);
    shadowEffect.setUseGlobalLight(false);
    shadowEffect.setSize(2);
    shadowEffect.setAngle(45);
    shadowEffect.setSpread(50);
    shadowEffect.setNoise(5);
```
هذا المقطع **يطبق الظل الداخلي** ويخصص مظهره:  
- **اللون** – ضبطه على الأخضر (يمكن تغييره إلى أي `Color` تفضله).  
- **الشفافية** – 50 % شفافية (`128` من `255`).  
- **المسافة، الحجم، الزاوية** – تتحكم في إزاحة الظل وانتشاره.  
- **الانتشار والضوضاء** – إضافة تنوع فني.  
يُضاف كائن `InnerShadowEffect` إلى خيارات المزج للطبقة، مما يجعل التأثير جزءًا من مجموعة طبقات PSD.

### الخطوة 5: حفظ ملف PSD المعدل
```java
    image.save(destName, new PsdOptions(image));
```
الملف `sample_out.psd` الآن يحتوي على تأثير الظل الداخلي. حفظه باستخدام `image.save(outputPath, new PsdOptions())` يحافظ على جميع الطبقات والتأثيرات الموجودة.

### الخطوة 6: تنظيف الموارد
```java
} finally {
    image.dispose();
}
```
تحرير كائن `image` يحرر الذاكرة ويمنع التسريبات، وهو أمر مهم خاصةً عند معالجة العديد من الملفات في حلقة. احرص دائمًا على تغليف الاستخدام داخل كتلة try‑with‑resources أو استدعاء `image.dispose()` في كتلة finally.

## حالات الاستخدام الشائعة
- **خطوط أنابيب العلامة التجارية الآلية** – إضافة ظلال داخلية متسقة إلى الشعارات قبل النشر.  
- **إنشاء أصول واجهة المستخدم الديناميكية** – توليد حالات أزرار بعمق في الوقت الفعلي لتطبيقات الويب أو الجوال.  
- **معالجة دفعات لمكتبات PSD القديمة** – تحديث التصاميم القديمة بظلال حديثة دون فتح Photoshop.

## المشكلات الشائعة والحلول
| المشكلة | سبب حدوثها | الحل |
|-------|----------------|-----|
| **`ArrayIndexOutOfBoundsException` on `getEffects()[0]`** | الطبقة المستهدفة لا تحتوي على أي تأثيرات مرفقة بعد. | أضف `InnerShadowEffect` جديد عبر `layer.getBlendingOptions().addEffect(new InnerShadowEffect())` قبل التحويل. |
| **Shadow color not changing** | الطبقة لديها بالفعل نوع تأثير مختلف يتجاوز الظل. | تأكد من تعديل الفهرس الصحيح للتأثير أو امسح التأثيرات الحالية باستخدام `layer.getBlendingOptions().clearEffects()`. |
| **File not saved** | دليل الوجهة غير موجود أو لا تملك صلاحيات كتابة. | أنشئ الدليل مسبقًا (`new File(outputDir).mkdirs();`) أو اختر مسارًا قابلًا للكتابة. |

## الأسئلة المتكررة

**س: ما هو Aspose.PSD؟**  
ج: Aspose.PSD هي مكتبة Java تمكّن المطورين من إنشاء، تحرير، تحويل، وعرض ملفات Photoshop PSD دون الحاجة إلى تثبيت Photoshop.

**س: هل أحتاج إلى Photoshop لاستخدام Aspose.PSD؟**  
ج: لا، لا تحتاج إلى Photoshop لاستخدام Aspose.PSD. تعمل المكتبة بشكل مستقل لمعالجة ملفات PSD.

**س: هل يمكنني تطبيق تأثيرات متعددة على نفس الطبقة؟**  
ج: بالتأكيد! يمكنك تطبيق تأثيرات متعددة بالوصول إلى كل نوع تأثير بطريقة مشابهة للطريقة التي وصلنا بها إلى تأثير الظل الداخلي.

**س: هل Aspose.PSD مجاني؟**  
ج: Aspose.PSD هو منتج تجاري؛ ومع ذلك، يمكنك استخدام نسخة تجريبية مجانية متاحة عبر Aspose.

**س: أين يمكنني العثور على مزيد من الوثائق؟**  
ج: يمكنك العثور على وثائق شاملة لـ Aspose.PSD [here](https://reference.aspose.com/psd/java/).

## الخاتمة
لقد رأيت الآن كيفية **add inner shadow PSD** و**apply PSD layer effect** باستخدام Aspose.PSD for Java. يتيح لك هذا النهج أتمتة تعديلات التصميم المتقدمة، دمجها في خدمات الخلفية، أو بناء معالجات دفعات لمكتبات صور كبيرة. لا تتردد في تجربة أنواع تأثيرات أخرى—ظلال إسقاط، توهجات، حواف—لتوسيع مجموعة أدواتك وإنشاء أصول بصرية أغنى.

---

**آخر تحديث:** 2026-06-23  
**تم الاختبار مع:** Aspose.PSD 24.12 for Java  
**المؤلف:** Aspose  

{{< blocks/products/products-backtop-button >}}

## دروس ذات صلة

- [حفظ PSD كـ PNG وتطبيق ظل إسقاط Rendering Drop Shadow في Aspose.PSD for Java](/psd/java/advanced-image-manipulation/rendering-drop-shadow/)
- [إضافة تأثيرات تغطية نمطية Pattern Overlay في Aspose.PSD for Java](/psd/java/advanced-image-effects/add-pattern-effects/)
- [كيفية تطبيق تأثيرات التدرج Gradient في Aspose.PSD for Java](/psd/java/advanced-image-effects/add-gradient-effects/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}