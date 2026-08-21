---
date: 2026-06-18
description: تعلم كيفية تغيير لون Shadow في Java وتخصيص تأثيرات Shadow باستخدام Aspose.PSD
  for Java. اتبع هذا الدليل خطوة بخطوة لتأثير Shadow.
keywords:
- change shadow color java
- Aspose.PSD shadow effect
- Java PSD manipulation
linktitle: دعم تأثير Shadow
schemas:
- author: Aspose
  dateModified: '2026-06-18'
  description: Learn how to change shadow color java and customize shadow effects
    using Asprose.PSD for Java. Follow this step‑by‑step shadow effect tutorial.
  headline: Change Shadow Color Java with Aspose.PSD for Java
  type: TechArticle
- description: Learn how to change shadow color java and customize shadow effects
    using Asprose.PSD for Java. Follow this step‑by‑step shadow effect tutorial.
  name: Change Shadow Color Java with Aspose.PSD for Java
  steps:
  - name: Load the PSD Image
    text: 'First, load the source PSD while enabling the loading of effect resources:'
  - name: Retrieve the Existing Drop Shadow Effect
    text: 'Locate the shadow effect on the desired layer (in this example, the second
      layer):'
  - name: Verify the Default Settings (Optional)
    text: 'Running these assertions helps you understand the original values before
      you modify them:'
  - name: '**Change Shadow Color** and Customize Other Properties'
    text: Now we actually **change shadow color** to green, adjust opacity, distance,
      size, and other attributes. This demonstrates the **customize shadow effect**
      capabilities of Aspose.PSD. The `setOpacity(byte)` method sets the shadow's
      opacity level (0‑255).
  - name: Save the Modified Image
    text: 'Finally, write the updated PSD back to disk using the `save` method of
      `PsdImage`:'
  type: HowTo
- questions:
  - answer: Absolutely! Aspose.PSD for Java is a powerful library designed for professional
      graphic design tasks.
    question: Is Aspose.PSD for Java suitable for professional graphic design projects?
  - answer: Yes, Aspose.PSD for Java is a commercial product. You can purchase it
      [here](https://purchase.aspose.com/buy).
    question: Can I use Aspose.PSD for Java in commercial applications?
  - answer: Yes, you can explore a free trial version [here](https://releases.aspose.com/).
    question: Is there a free trial available?
  - answer: Refer to the comprehensive documentation [here](https://reference.aspose.com/psd/java/).
    question: Where can I find detailed documentation?
  - answer: Join the community forum [here](https://forum.aspose.com/c/psd/34) for
      any support queries.
    question: How can I get support for Aspose.PSD for Java?
  type: FAQPage
second_title: Aspose.PSD Java API
title: تغيير لون Shadow في Java باستخدام Aspose.PSD for Java
url: /ar/java/basic-image-operations/support-shadow-effect/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# تغيير لون الظل في Java باستخدام Aspose.PSD for Java

## المقدمة

إضافة العمق إلى رسوماتك غالبًا ما يعني **تغيير لون الظل** ليتناسب مع مزاج التصميم. باستخدام Aspose.PSD for Java يمكنك بسهولة إضافة أو تعديل تأثيرات الظل المتساقط، التحكم في الشفافية، وضبط معلمات أخرى بدقة — كل ذلك من خلال كود Java. في هذا **دليل تأثير الظل** سنستعرض تحميل ملف PSD، قراءة الظل الموجود، تخصيص لونه، شفافيته، مسافته، وأخيرًا حفظ الملف المحدث. يوضح هذا الدليل بالضبط كيفية **تغيير لون الظل java** بطريقة قابلة لإعادة الإنتاج.

## الإجابات السريعة
- **ماذا يعني “تغيير لون الظل”؟** يقوم بتحديث خاصية اللون لتأثير DropShadowEffect المطبق على طبقة PSD.  
- **أي مكتبة تدعم ذلك؟** Aspose.PSD for Java توفر دعمًا كاملاً لتأثيرات الظل.  
- **هل أحتاج إلى ترخيص؟** النسخة التجريبية تعمل للتطوير؛ الترخيص التجاري مطلوب للإنتاج.  
- **هل يمكنني ضبط شفافية الظل؟** نعم – استخدم `setOpacity(byte)` لتحديد الشفافية (0‑255).  
- **هل الكود متوافق مع Java 8+؟** بالتأكيد، الـ API تستهدف Java 8 وما بعدها.

## ما هو “تغيير لون الظل” في ملفات PSD؟

تغيير لون الظل ي modifies اللون البصري للظل المتساقط الذي يظهر خلف الطبقة. يتيح هذا التعديل للمصممين محاكاة ظروف إضاءة مختلفة، مواءمة الظلال مع لوحات ألوان العلامة التجارية، وإضافة لمسة فنية إلى التكوينات. من خلال تعديل اللون، يمكنك جعل الظلال تبدو أكثر دفئًا أو برودة، أو مطابقة لون معين تمامًا، مما يعزز التأثير البصري العام.

## لماذا تستخدم Aspose.PSD for Java لتخصيص تأثيرات الظل؟

Aspose.PSD for Java يحافظ على **أكثر من 100 تنسيق صورة** ويمكنه معالجة ملفات PSD حتى **2 GB** دون تحميل المستند بالكامل في الذاكرة، مما يوفر أداءً من مستوى المؤسسات. تمنحك المكتبة تحكمًا كاملاً في كل خاصية للظل — اللون، الشفافية، المسافة، الزاوية، الانتشار، والضوضاء — دون الحاجة إلى تثبيت Photoshop. تعمل على JVMs في Windows، Linux، و macOS، مما يجعلها الخيار الأكثر موثوقية لأنابيب الرسومات المؤتمتة.

## المتطلبات المسبقة

- معرفة أساسية ببرمجة Java.  
- Aspose.PSD for Java مثبت. يمكنك تنزيله [هنا](https://releases.aspose.com/psd/java/).  

## استيراد الحزم

قبل البدء، استورد الفئات المطلوبة حتى تتمكن من العمل مع الصور وتأثيرات الظل:

فئة `Color` تمثل قيمة اللون المستخدمة في جميع أنحاء الـ API.  
فئة `Image` هي النوع الأساسي لجميع كائنات الصورة.  
فئة `PsdImage` توفر وظائف خاصة بملفات PSD.  
فئة `PsdLoadOptions` تسمح لك بتحديد خيارات تحميل ملفات PSD، مثل تمكين موارد التأثير.  
فئة `DropShadowEffect` تمثل مرشح الظل المتساقط المطبق على طبقة PSD وتمنحك الوصول إلى جميع خصائصه القابلة للتعديل.

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;


import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.layereffects.DropShadowEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
```

## دليل خطوة بخطوة

### الخطوة 1: تحميل صورة PSD

أولاً، حمّل ملف PSD المصدر مع تمكين تحميل موارد التأثير:

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "Shadow.psd";
String psdPathAfterChange = dataDir + "ShadowChanged.psd";

PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);
```

### الخطوة 2: استرجاع تأثير الظل المتساقط الموجود

حدد تأثير الظل على الطبقة المطلوبة (في هذا المثال، الطبقة الثانية):

```java
DropShadowEffect shadowEffect = (DropShadowEffect)(im.getLayers()[1].getBlendingOptions().getEffects()[0]);
```

### الخطوة 3: التحقق من الإعدادات الافتراضية (اختياري)

تشغيل هذه التأكيدات يساعدك على فهم القيم الأصلية قبل تعديلها:

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

### الخطوة 4: **تغيير لون الظل** وتخصيص الخصائص الأخرى

الآن نقوم فعليًا **بتغيير لون الظل** إلى الأخضر، وضبط الشفافية، والمسافة، والحجم، وغيرها من السمات. هذا يوضح قدرات **تخصيص تأثير الظل** في Aspose.PSD. طريقة `setOpacity(byte)` تحدد مستوى شفافية الظل (0‑255).  

```java
shadowEffect.setColor(Color.getGreen());          // change shadow color
shadowEffect.setOpacity((byte)128);               // set shadow opacity (50% transparent)
shadowEffect.setDistance(11);                     // move shadow farther from the object
shadowEffect.setUseGlobalLight(false);            // use local lighting
shadowEffect.setSize(9);                          // adjust blur radius
shadowEffect.setAngle(45);                        // rotate light source
shadowEffect.setSpread(3);                        // increase spread
shadowEffect.setNoise(50);                        // add texture noise
```

### الخطوة 5: حفظ الصورة المعدلة

أخيرًا، اكتب ملف PSD المحدث إلى القرص باستخدام طريقة `save` الخاصة بـ `PsdImage`:

```java
im.save(psdPathAfterChange);
```

## المشكلات الشائعة والنصائح

- **NullPointerException عند استرجاع التأثيرات** – تأكد من استدعاء `setLoadEffectsResource(true)`؛ وإلا لن يتم تحميل التأثيرات.  
- **اللون لا يتغير** – تحقق من أنك تعدل الفهرس الصحيح للطبقة (`im.getLayers()[1]` في هذا المثال).  
- **الشفافية تبدو غير متغيرة** – تذكر أن الشفافية هي بايت (0‑255). يلزم التحويل إلى `(byte)`.  

## الخلاصة

باتباع هذه الخطوات يمكنك **تغيير لون الظل**، **ضبط شفافية الظل**، وتخصيص جميع معلمات تأثير الظل في أي ملف PSD باستخدام Aspose.PSD for Java. هذا يمكّنك من إنشاء رسومات أغنى برمجيًا دون الحاجة إلى عمل يدوي في Photoshop، وهو مثالي لأنابيب التصميم المؤتمتة ومعالجة الدفعات.

## الأسئلة المتكررة

**س: هل Aspose.PSD for Java مناسب لمشاريع التصميم الجرافيكي الاحترافية؟**  
ج: بالتأكيد! Aspose.PSD for Java مكتبة قوية مصممة لمهام التصميم الجرافيكي الاحترافية.

**س: هل يمكنني استخدام Aspose.PSD for Java في التطبيقات التجارية؟**  
ج: نعم، Aspose.PSD for Java منتج تجاري. يمكنك شرائه [هنا](https://purchase.aspose.com/buy).

**س: هل هناك نسخة تجريبية مجانية متاحة؟**  
ج: نعم، يمكنك تجربة نسخة تجريبية مجانية [هنا](https://releases.aspose.com/).

**س: أين يمكنني العثور على الوثائق التفصيلية؟**  
ج: راجع الوثائق الشاملة [هنا](https://reference.aspose.com/psd/java/).

**س: كيف يمكنني الحصول على دعم لـ Aspose.PSD for Java؟**  
ج: انضم إلى منتدى المجتمع [هنا](https://forum.aspose.com/c/psd/34) لأي استفسارات دعم.

---

**آخر تحديث:** 2026-06-18  
**تم الاختبار مع:** Aspose.PSD for Java 24.10  
**المؤلف:** Aspose  

{{< blocks/products/products-backtop-button >}}

## الدروس ذات الصلة

- [معالجة صور Java - إضافة تأثيرات في وقت التشغيل باستخدام Aspose.PSD for Java](/psd/java/advanced-techniques/add-effects-runtime/)
- [حفظ PSD كـ PNG وتطبيق ظل إسقاط Rendering في Aspose.PSD for Java](/psd/java/advanced-image-manipulation/rendering-drop-shadow/)
- [تمويه صورة Java باستخدام Aspose.PSD – إضافة تأثير تمويه](/psd/java/advanced-techniques/blur-image/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}