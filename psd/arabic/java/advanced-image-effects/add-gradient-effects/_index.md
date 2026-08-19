---
date: 2026-04-08
description: تعلم كيفية إنشاء تأثيرات التدرج الشعاعي في صور Java باستخدام Aspose.PSD.
  اتبع هذا الدليل خطوة بخطوة للتكامل السلس.
keywords:
- create radial gradient
- gradient overlay effect
- Aspose.PSD Java
linktitle: إضافة تأثيرات التدرج
second_title: Aspose.PSD Java API
title: كيفية إنشاء تأثيرات التدرج الشعاعي في Aspose.PSD للـ Java
url: /ar/java/advanced-image-effects/add-gradient-effects/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# كيفية إنشاء تأثيرات تدرج دائري في Aspose.PSD للـ Java

## مقدمة

مرحبًا بك في البرنامج التعليمي حول **كيفية إنشاء تدرج دائري** في Aspose.PSD للـ Java! إذا كنت تتطلع إلى تحسين صورك بتراكبات تدرج مذهلة، فأنت في المكان الصحيح. في هذا الدليل سنرشدك خلال العملية باستخدام Aspose.PSD، مكتبة Java قوية لمعالجة الصور. بحلول نهاية هذا البرنامج التعليمي، ستكون قادرًا على إضافة وتخصيص وحفظ تراكبات التدرج الدائري برمجيًا.

## إجابات سريعة

- **ما الذي يمكنني تحقيقه؟** إضافة، تعديل، ومزج تراكبات التدرج الدائري على طبقات PSD.  
- **أي مكتبة مطلوبة؟** Aspose.PSD للـ Java (أحدث إصدار).  
- **هل أحتاج إلى ترخيص؟** النسخة التجريبية المجانية تكفي للتطوير؛ يلزم ترخيص تجاري للإنتاج.  
- **كم يستغرق التنفيذ؟** تقريبًا 10‑15 دقيقة لإنشاء تراكب تدرج دائري أساسي.  
- **هل هو متوافق مع Java 8+؟** نعم، الـ API يدعم Java 8 والإصدارات الأحدث.

## المتطلبات المسبقة

قبل أن نغوص في البرنامج التعليمي، تأكد من توفر المتطلبات التالية:

1. **Aspose.PSD for Java Library** – تأكد من تنزيل وتثبيت مكتبة Aspose.PSD للـ Java. يمكنك العثور على المكتبة ووثائقها [هنا](https://reference.aspose.com/psd/java/).  
2. **Java Development Environment** – قم بإعداد بيئة تطوير Java على جهازك (JDK 8 أو أعلى، IDE من اختيارك).

الآن بعد أن تم إعداد كل شيء، دعنا نتابع الدليل خطوة بخطوة.

## استيراد الحزم

ابدأ باستيراد الحزم اللازمة في مشروع Java الخاص بك. يضمن ذلك حصولك على وظائف Aspose.PSD. إليك مثالًا أساسيًا:

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

## ما هو تأثير التدرج الفوقي؟

A **gradient overlay effect** هو نمط طبقة يرسم انتقالًا سلسًا بين لونين أو أكثر عبر مساحة محددة. في Photoshop (وبالتالي في ملفات PSD)، يمكن مزج هذا التأثير، تلوينه، وتحديد موقعه لإنشاء تصاميم بصرية متقنة. Aspose.PSD يتيح هذا التأثير عبر الفئة `GradientOverlayEffect`، مما يسمح لك بقراءة وتعديل خصائصه برمجيًا.

## كيفية إنشاء تأثير تدرج دائري

أدناه نقسم التنفيذ إلى خطوات واضحة مرقمة. كل خطوة تتضمن شرحًا قصيرًا يتبعها كتلة الكود الأصلية (بدون تغيير).

### الخطوة 1: تحميل ملف PSD والوصول إلى تدرج الفوقي

```javaString dataDir = "Your Document Directory";

// Gradient overlay effect. Example
String sourceFileName = dataDir + "GradientOverlay.psd";
String exportPath = dataDir + "GradientOverlayChanged.psd";

PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);

GradientOverlayEffect gradientOverlay = (GradientOverlayEffect)im.getLayers()[1].getBlendingOptions().getEffects()[0];
```

في هذه الخطوة، نقوم بتحميل ملف PSD واسترجاع أول `GradientOverlayEffect` من الطبقة الثانية (المؤشر 1). يضمن استدعاء `loadOptions.setLoadEffectsResource(true)` توفر موارد التأثير للتحرير.

### الخطوة 2: التحقق من الإعدادات الأولية

```java
// Verify initial settings
Assert.areEqual(BlendMode.Normal, gradientOverlay.getBlendMode());
Assert.areEqual(255, gradientOverlay.getOpacity());
Assert.areEqual(true, gradientOverlay.isVisible());
// ... (additional verifications)
```

قبل إجراء أي تغييرات، من الممارسات الجيدة التأكد من وضع المزج الحالي، الشفافية، والرؤية. يساعدك ذلك على فهم الحالة الأساسية لتراكب التدرج.

### الخطوة 3: تعديل إعدادات التدرج

```java
// Modify gradient settings
settings.setColor(Color.getGreen());
gradientOverlay.setOpacity((byte)193);
gradientOverlay.setBlendMode(BlendMode.Lighten);
// ... (additional modifications)
```

هنا يمكنك تخصيص لون التدرج، الشفافية، ووضع المزج. يغيّر المثال اللون إلى الأخضر، يقلل الشفافية إلى 193 (من 255)، ويحول وضع المزج إلى **Lighten**. لا تتردد في تجربة قيم `BlendMode` أخرى مثل `Multiply` أو `Screen` أو `Overlay`.

### الخطوة 4: حفظ الصورة المعدلة

```java
// Save the edited image
im.save(exportPath);
```

بعد تطبيق التعديلات، احفظ التغييرات عن طريق حفظ ملف PSD إلى ملف جديد. تضمن هذه الخطوة بقاء الملف الأصلي دون تعديل.

### الخطوة 5: التحقق من التغييرات

```java
// Verify changes after editing
PsdImage img = (PsdImage)Image.load(sourceFileName, loadOptions);

GradientOverlayEffect gradientOverlayEffect = (GradientOverlayEffect)img.getLayers()[1].getBlendingOptions().getEffects()[0];
// ... (additional verifications)
```

أعد تحميل الملف المحفوظ (أو الأصلي، حسب سير عملك) وأعد فحص تراكب التدرج للتأكد من تطبيق التغييرات بشكل صحيح.

## لماذا إنشاء تدرجات دائرية فوقية؟

تضيف التدرجات الدائرية عمقًا وتركيزًا إلى التصاميم، مما يجعل العناصر تبدو ثلاثية الأبعاد أو مسلطة الضوء. هي مثالية لـ:

- **ملء الخلفيات** التي تجذب العين نحو العنصر المركزي.  
- **تسليط الضوء على الأزرار أو الأيقونات** حيث يلزم توهج خفيف.  
- **تأثيرات صور إبداعية** مثل الفينيت أو انفجارات الضوء.  

باستخدام Aspose.PSD يمكنك أتمتة هذه التأثيرات عبر العديد من الملفات، مما يوفر ساعات من العمل اليدوي في Photoshop.

## مشكلات شائعة ونصائح

- **التأثير غير مرئي:** تأكد من أن `gradientOverlay.isVisible()` يُعيد `true`. بعض ملفات PSD تخفي التأثيرات افتراضيًا.  
- **فهرس الطبقة غير صحيح:** الفهارس تبدأ من الصفر؛ تحقق من أنك تستهدف الطبقة الصحيحة (`im.getLayers()[1]` يشير إلى الطبقة الثانية).  
- **تحويل الشفافية:** طريقة `setOpacity` تتوقع قيمة من نوع `byte`. تمرير `int` سيسبب خطأ تجميع؛ قم بالتحويل الصريح كما هو موضح.  
- **تحميل الموارد:** إذا صادفت `null` عند الوصول إلى التأثيرات، تحقق من ضبط `loadOptions.setLoadEffectsResource(true)` قبل تحميل الصورة.

## الأسئلة المتكررة

### س1: هل يمكنني تطبيق تأثيرات تدرج متعددة على صورة واحدة؟

ج1: نعم، يمكنك تطبيق تأثيرات تدرج متعددة عن طريق تكرار خطوات التعديل لكل تأثير.

### س2: ما هي التأثيرات الأخرى التي يمكنني دمجها مع تراكب التدرج؟

ج2: توفر Aspose.PSD مجموعة متنوعة من التأثيرات، بما في ذلك الظلال، التوهجات، وأكثر. استكشف الوثائق للمزيد من الخيارات.

### س3: كيف يمكنني استكشاف الأخطاء إذا لم يتم عرض التأثيرات بشكل صحيح؟

ج3: راجع الوثائق ومنتديات المجتمع على [Aspose.PSD Support](https://forum.aspose.com/c/psd/34) للحصول على المساعدة.

### س4: هل تتوفر نسخة تجريبية من Aspose.PSD للـ Java؟

ج4: نعم، يمكنك الحصول على نسخة تجريبية مجانية [هنا](https://releases.aspose.com/).

### س5: أين يمكنني شراء ترخيص لـ Aspose.PSD للـ Java؟

ج5: زر صفحة [الشراء](https://purchase.aspose.com/buy) للحصول على معلومات الترخيص.

## أسئلة إضافية

**س: هل يمكنني تغيير اتجاه التدرج برمجيًا؟**  
ج: نعم. استخدم الطريقة `GradientOverlayEffect.setAngle(float angle)` لتحديد زاوية التدرج بالدرجات.

**س: هل يدعم Aspose.PSD التدرجات الدائرية؟**  
ج: بالتأكيد. اضبط نمط التدرج إلى `GradientStyle.Radial` عبر خصائص `GradientOverlayEffect`.

**س: هل يتم الحفاظ على تراكب التدرج عند تحويل PSD إلى صيغ أخرى (مثل PNG)؟**  
ج: عند تحويل PSD إلى صورة نقطية (مثل حفظها كـ PNG)، يُحافظ على النتيجة البصرية لتراكب التدرج، لكن يصبح التأثير جزءًا من بيانات البكسل.

**س: كيف يمكنني إزالة تراكب التدرج من طبقة؟**  
ج: استرجع `BlendingOptions` للطبقة، حدد `GradientOverlayEffect` في مجموعة `Effects`، ثم احذفه باستخدام `remove(effect)`.

**س: هل يمكن تحريك تغيّر التدرج؟**  
ج: رغم أن Aspose.PSD لا يتعامل مباشرةً مع الرسوم المتحركة، يمكنك إنشاء سلسلة من ملفات PSD بمعلمات تدرج مختلفة ثم تجميعها في فيديو أو GIF باستخدام مكتبة أخرى.

## الخلاصة

تهانينا! لقد تعلمت **كيفية إنشاء تدرج دائري** لتطبيقه على صورك باستخدام Aspose.PSD للـ Java. باتباع الخطوات أعلاه، يمكنك إضافة وتعديل وحفظ تراكبات التدرج برمجيًا، مما يمنحك سيطرة إبداعية كاملة على موارد PSD. جرّب ألوانًا مختلفة، أوضاع مزج، وقيم شفافية لتحقيق التأثير البصري الذي تحتاجه.

---

**Last Updated:** 2026-04-08  
**Tested With:** Aspose.PSD for Java 24.12 (latest at time of writing)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}