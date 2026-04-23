---
date: 2026-02-14
description: تعلم كيفية إضافة ظل داخلي إلى ملف PSD باستخدام Aspose.PSD للغة Java وتطبيق
  تأثير طبقة PSD برمجياً من خلال هذا الدليل خطوة بخطوة، بما يشمل النصائح وأفضل الممارسات.
linktitle: Add Inner Shadow PSD Layer Effect in Java
second_title: Aspose.PSD Java API
title: كيفية إضافة تأثير الظل الداخلي لطبقة PSD في جافا
url: /ar/java/advanced-psd-layer-features-effects/add-inner-shadow-layer-effect-psd/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# كيفية إضافة تأثير الظل الداخلي لطبقة PSD في جافا

## المقدمة
إذا كنت بحاجة إلى **إضافة ظل داخلي لملف PSD** برمجياً، فقد وصلت إلى المكان المناسب. في هذا الدليل، سنوضح لك **كيفية إضافة ظل داخلي** إلى أي مستند فوتوشوب باستخدام Aspose.PSD for Java. سواء كنت تبني أداة معالجة دفعات، أو خط أنابيب تصميم آلي، أو مجرد تجربة تأثيرات الصور، فإن الخطوات أدناه ستوفر لك حلاً جاهزاً للإنتاج يمكنك دمجه في تطبيقات جافا الخاصة بك.

## إجابات سريعة
- **ما المكتبة التي أحتاجها؟** Aspose.PSD for Java.  
- **كم يستغرق التنفيذ؟** حوالي 10‑15 دقيقة لإعداد أساسي.  
- **هل أحتاج إلى تثبيت فوتوشوب؟** لا، المكتبة تعمل مستقلة عن فوتوشوب.  
- **هل يمكنني تغيير لون الظل؟** نعم – طريقة `setColor` تقبل أي `Color`.  
- **هل يلزم ترخيص للإنتاج؟** يتطلب ترخيص تجاري؛ يتوفر نسخة تجريبية مجانية.

## ما هو “add inner shadow psd”؟
إضافة ظل داخلي إلى ملف PSD يعني إنشاء تأثير تظليل خفيف داخل الطبقة يعطي انطباع العمق داخل العنصر. يُستخدم هذا التأثير عادةً لجعل عناصر واجهة المستخدم، الأيقونات، أو النصوص تبرز دون إضافة توهج خارجي.

## لماذا نطبق تأثير طبقة PSD باستخدام جافا؟
استخدام جافا لتطبيق **تأثير طبقة PSD** يتيح لك أتمتة مهام التصميم المتكررة، دمج معالجة الصور في خدمات الخلفية، وإنشاء الأصول بشكل فوري دون الحاجة إلى عمل يدوي في فوتوشوب. توفر Aspose.PSD واجهة برمجة تطبيقات كائنية نظيفة تُبسط تعقيدات تنسيق ملفات PSD.

## المتطلبات المسبقة
قبل الغوص في الكود، تأكد من وجود ما يلي:

1. **مجموعة تطوير جافا (JDK 11 أو أعلى)** – حمّلها من [موقع Oracle](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).  
2. **Aspose.PSD for Java** – احصل على أحدث ملف JAR من [صفحة إصدارات Aspose](https://releases.aspose.com/psd/java/).  
3. **بيئة تطوير متكاملة (IDE)** – IntelliJ IDEA، Eclipse، أو NetBeans (أي منها).  
4. **معرفة أساسية بجافا** – يجب أن تكون مرتاحاً مع الفئات، الكائنات، ومعالجة الاستثناءات.  
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
تُتيح لك هذه الاستيرادات الوصول إلى الفئات الأساسية اللازمة لتحميل PSD، تعديل الطبقات، وتكوين تأثيرات الظل.

## كيفية إضافة ظل داخلي لملف PSD باستخدام جافا
فيما يلي دليل خطوة بخطوة. كل خطوة تتضمن شرحًا قصيرًا يليه الكود الدقيق الذي تحتاج إلى نسخه.

### الخطوة 1: تعريف مسارات المصدر والوجهة
```java
String sourceDir = "Your Source Directory";
String outputDir = "Your Document Directory";
String sourceFile = sourceDir + "sample.psd";
String destName = outputDir + "sample_out.psd";
```
استبدل مسارات العنصر النائب بالمواقع الفعلية على جهازك.

### الخطوة 2: تحميل ملف PSD مع موارد التأثير
```java
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);
PsdImage image = (PsdImage) Image.load(sourceFile, loadOptions);
```
`setLoadEffectsResource(true)` يضمن تحميل أي تأثيرات طبقة موجودة، مما يسمح لنا بتعديلها.

### الخطوة 3: الوصول إلى الطبقة المستهدفة
```java
try {
    Layer layer = image.getLayers()[image.getLayers().length - 1];
```
هنا نلتقط **الطبقة الأخيرة** في المستند، وهي غالبًا ما تكون التي تريد تعديلها. عدّل الفهرس إذا كنت تحتاج إلى طبقة مختلفة.

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
- **اللون** – مضبوط على الأخضر (يمكن تغييره إلى أي `Color` تفضله).  
- **الشفافية** – 50 % (`128` من `255`).  
- **المسافة، الحجم، الزاوية** – تتحكم في إزاحة الظل وانتشاره.  
- **الانتشار والضوضاء** – تضيف تنوعًا فنيًا.

### الخطوة 5: حفظ ملف PSD المعدل
```java
    image.save(destName, new PsdOptions(image));
```
الملف `sample_out.psd` الآن يحتوي على تأثير الظل الداخلي.

### الخطوة 6: تنظيف الموارد
```java
} finally {
    image.dispose();
}
```
تحرير كائن `image` يحرر الذاكرة ويمنع التسريبات، وهو أمر مهم خاصةً عند معالجة العديد من الملفات داخل حلقة.

## حالات الاستخدام الشائعة
- **خطوط أنابيب العلامة التجارية الآلية** – إضافة ظلال داخلية متسقة للشعارات قبل النشر.  
- **إنشاء أصول واجهة مستخدم ديناميكية** – توليد حالات أزرار بعمق في الوقت الفعلي لتطبيقات الويب أو الجوال.  
- **معالجة دفعات لمكتبات PSD القديمة** – تحديث التصاميم القديمة بظلال حديثة دون فتح فوتوشوب.

## المشكلات الشائعة والحلول
| المشكلة | لماذا يحدث | الحل |
|--------|------------|------|
| **`ArrayIndexOutOfBoundsException` على `getEffects()[0]`** | الطبقة المستهدفة لا تحتوي على أي تأثيرات مرفقة بعد. | أضف `IShadowEffect` جديد عبر `layer.getBlendingOptions().addEffect(new ShadowEffect())` قبل التحويل. |
| **لون الظل لا يتغير** | الطبقة لديها نوع تأثير مختلف يطغى على الظل. | تأكد من تعديل الفهرس الصحيح للتأثير أو امسح التأثيرات الحالية بـ `layer.getBlendingOptions().clearEffects()`. |
| **الملف لا يُحفظ** | دليل الوجهة غير موجود أو لا تملك صلاحيات كتابة. | أنشئ الدليل مسبقًا (`new File(outputDir).mkdirs();`) أو اختر مسارًا قابلًا للكتابة. |

## الأسئلة المتكررة

**س: ما هو Aspose.PSD؟**  
ج: Aspose.PSD هي مكتبة جافا للعمل مع ملفات PSD، تتيح للمطورين تعديل تأثيرات الطبقات، الأقنعة، وخصائص الصورة برمجيًا.

**س: هل أحتاج إلى فوتوشوب لاستخدام Aspose.PSD؟**  
ج: لا، لا تحتاج إلى فوتوشوب لاستخدام Aspose.PSD. المكتبة تعمل بشكل مستقل لمعالجة ملفات PSD.

**س: هل يمكنني تطبيق تأثيرات متعددة على نفس الطبقة؟**  
ج: بالتأكيد! يمكنك تطبيق تأثيرات متعددة عبر الوصول إلى كل نوع تأثير بنفس الطريقة التي وصلنا بها إلى تأثير الظل الداخلي.

**س: هل Aspose.PSD مجاني؟**  
ج: Aspose.PSD منتج تجاري؛ ومع ذلك، يمكنك الاستفادة من نسخة تجريبية مجانية متوفرة عبر Aspose.

**س: أين يمكنني العثور على مزيد من الوثائق؟**  
ج: يمكنك العثور على وثائق شاملة لـ Aspose.PSD [هنا](https://reference.aspose.com/psd/java/).

## الخاتمة
لقد رأيت الآن كيف **تضيف ظلًا داخليًا لملف PSD** و**تطبق تأثير طبقة PSD** باستخدام Aspose.PSD for Java. يتيح لك هذا النهج أتمتة تعديلات التصميم المتقدمة، دمجها في خدمات الخلفية، أو بناء معالجات دفعات لمكتبات صور كبيرة. لا تتردد في تجربة أنواع تأثير أخرى—ظلال خارجية، توهجات، حواف—لتوسيع مجموعة أدواتك.

---

**آخر تحديث:** 2026-02-14  
**تم الاختبار مع:** Aspose.PSD 24.12 for Java  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}