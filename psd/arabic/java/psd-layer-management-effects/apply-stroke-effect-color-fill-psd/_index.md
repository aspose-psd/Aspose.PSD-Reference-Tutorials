---
date: 2026-04-03
description: تعلم كيفية حفظ ملف PSD كـ PNG مع تأثير الحد وتعبئة اللون باستخدام Aspose.PSD
  للغة Java. يوضح هذا الدليل خطوة بخطوة كيفية تصدير PSD إلى PNG بسرعة.
keywords:
- save psd as png
- export psd to png
- set stroke color
- apply layer effects
- customize stroke width
linktitle: حفظ PSD كـ PNG مع تأثير الحد – جافا
second_title: Aspose.PSD Java API
title: حفظ PSD كـ PNG مع تأثير الحد – Java
url: /ar/java/psd-layer-management-effects/apply-stroke-effect-color-fill-psd/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# احفظ PSD كـ PNG مع تأثير الحد وتعبئة اللون – Java

## مقدمة

في هذا الدليل، ستتعلم كيفية **حفظ PSD كـ PNG** مع تطبيق تأثير الحد وتعبئة اللون باستخدام Aspose.PSD للغة Java. سواء كنت مطورًا متمرسًا أو مبتدئًا، سيسهل عليك هذا الشرح خطوة بخطوة إنجاز المهمة. سنغطي كل شيء من إعداد بيئتك إلى تصدير الصورة النهائية، حتى تتمكن من **تصدير PSD إلى PNG** بسرعة في مشاريعك.

## إجابات سريعة
- **ما الذي يحققه هذا الدليل؟** يوضح كيفية حفظ ملف PSD كـ PNG بعد تطبيق تأثير حد قابل للتخصيص.  
- **ما المكتبة المستخدمة؟** Aspose.PSD للغة Java.  
- **هل أحتاج إلى ترخيص؟** النسخة التجريبية المجانية تكفي للاختبار؛ الترخيص مطلوب للإنتاج.  
- **هل يمكنني تغيير لون الحد؟** نعم – يمكنك تعيين أي لون عبر `ColorFillSettings`.  
- **هل المعالجة الدفعة ممكنة؟** بالتأكيد – يمكنك وضع الكود داخل حلقة لمعالجة ملفات PSD متعددة.

## ما هو “حفظ PSD كـ PNG”؟
يعني حفظ PSD كـ PNG تحويل ملف Photoshop الأصلي متعدد الطبقات إلى تنسيق صورة مسطح صديق للويب مع الحفاظ على الدقة البصرية. هذا مفيد عندما تحتاج إلى عرض محتوى PSD على مواقع الويب أو التطبيقات المحمولة أو أي منصة لا تدعم ملفات PSD مباشرة.

## لماذا تطبيق تأثير الحد مع تعبئة اللون؟
يضيف الحد حدودًا واضحة حول محتويات الطبقة، مما يجعل الرسومات تبرز أمام الخلفيات المعقدة. الجمع بينه وبين لون تعبئة مخصص يتيح لك وضع علامة تجارية على الصور، إبراز عناصر واجهة المستخدم، أو إنشاء صور مصغرة جذابة دون الحاجة إلى Photoshop.

## المتطلبات المسبقة

1. **مجموعة تطوير جافا (JDK) 8+** – تأكد من وجود `java` في PATH.  
2. **Aspose.PSD للغة Java** – قم بتنزيله من [الموقع](https://releases.aspose.com/psd/java/).  
3. **بيئة تطوير متكاملة (IDE)** – IntelliJ IDEA أو Eclipse أو أي محرر تفضله.  
4. **ملف PSD تجريبي** – ملف يحتوي بالفعل على تأثير حد (أو أضف واحدًا في Photoshop).  
5. **معرفة أساسية بجافا** – ستكتب بضع أسطر من الكود، لكن لا شيء معقد.

بمجرد أن تكون هذه العناصر جاهزة، يمكننا البدء بالبرمجة.

## استيراد الحزم

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.fillsettings.ColorFillSettings;
import com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.imageoptions.PsdOptions;
```

هذه الاستيرادات تجلب جميع الفئات اللازمة لتحميل ملف PSD، تعديل حدّه، وحفظ مخرجات PSD و PNG.

## كيفية حفظ PSD كـ PNG مع تأثير الحد

### الخطوة 1: تحميل ملف PSD

أولاً، حدد المجلد الذي يحتوي على ملف PSD المصدر.

```java
String dataDir = "Your Document Directory";
```

استبدل `"Your Document Directory"` بالمسار الفعلي على جهازك.

الآن قم بتحميل الملف مع الحفاظ على أي موارد تأثير موجودة:

```java
String sourceFileName = dataDir + "StrokeComplex.psd";

PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage) Image.load(sourceFileName, loadOptions);
```

### الخطوة 2: تعيين لون الحد (وإمكانية تخصيص العرض اختياريًا)

الحلقة أدناه تتنقل عبر كل طبقة، تلتقط أول `StrokeEffect`، وتغيّر لون التعبئة. يمكنك أيضًا تعديل `setWidth` أو `setPosition` على كائن `StrokeEffect` إذا كنت بحاجة إلى **تخصيص عرض الحد**.

```java
for (int i = 0; i < im.getLayers().length; i++) {
    StrokeEffect effect = (StrokeEffect) im.getLayers()[i].getBlendingOptions().getEffects()[0];
    ColorFillSettings settings = (ColorFillSettings) effect.getFillSettings();
    // Set the stroke color – change to any Color you like
    settings.setColor(Color.getDeepPink());
}
```

> **نصيحة احترافية:** `Color.getDeepPink()` مجرد مثال. استخدم `new Color(r, g, b)` للقيم RGB المخصصة.

### الخطوة 3: حفظ PSD المعدل (اختياري)

إذا كنت ترغب في الاحتفاظ بنسخة PSD مع الحد المحدث، احفظها هكذا:

```java
String exportPath = dataDir + "StrokeComplexRendering.psd";
im.save(exportPath, new PsdOptions());
```

### الخطوة 4: تصدير الصورة كـ PNG (خطوة “حفظ PSD كـ PNG” الأساسية)

أخيرًا، حوّل PSD المعدل إلى ملف PNG جاهز للاستخدام على الويب:

```java
String exportPathPng = dataDir + "StrokeComplexRendering.png";
PngOptions option = new PngOptions();
option.setColorType(PngColorType.TruecolorWithAlpha);

im.save(exportPathPng, option);
```

يحافظ PNG على الحد الوردي العميق الذي حددته مسبقًا، وخيار `TruecolorWithAlpha` يضمن الحفاظ على الشفافية.

## المشكلات الشائعة والحلول

| المشكلة | السبب | الحل |
|-------|--------|-----|
| **`ArrayIndexOutOfBoundsException`** | الطبقة لا تحتوي على تأثيرات أو التأثير الأول ليس `StrokeEffect`. | تحقق من أن الطبقة تحتوي فعلاً على حد أو قم بالتكرار عبر `getEffects()` للعثور على النوع المناسب. |
| **اللون لا يتغير** | قد تكون تقوم بتحرير نسخة من الإعدادات بدلاً من الأصل. | تأكد من التحويل إلى `ColorFillSettings` مباشرةً من `effect.getFillSettings()`. |
| **PNG يظهر فارغًا** | تم تحميل PSD دون تحويل الطبقة إلى نقطية. | استدعِ `im.save(..., new PngOptions())` بعد جميع التعديلات؛ تجنّب حفظ الـ `im` الأصلي قبل التغييرات. |

## الأسئلة المتكررة

**س: هل يمكنني تطبيق تأثيرات متعددة على طبقة واحدة باستخدام Aspose.PSD للغة Java؟**  
نعم، يمكنك الوصول إلى خيارات الدمج للطبقة وإضافة عدد غير محدود من التأثيرات حسب الحاجة، بما في ذلك الظلال، والتوهجات، والحدود.

**س: هل من الممكن أتمتة العملية لمجموعة من ملفات PSD؟**  
بالطبع. ضع منطق التحميل، وتطبيق التأثير، والحفظ داخل حلقة `for‑each` التي تتنقل عبر الملفات في دليل.

**س: كيف يمكنني التراجع عن التغييرات التي تم إجراؤها على ملف PSD؟**  
أعد تحميل الملف الأصلي قبل حفظ أي تعديل؛ لا توفر Aspose.PSD ميزة التراجع.

**س: هل يمكنني تخصيص عرض وموقع الحد؟**  
نعم. استخدم `effect.setWidth(float)` و `effect.setPosition(StrokeEffect.Position)` للتحكم في السماكة والموقع (داخل، خارج، أو مركزي).

**س: هل مكتبة Aspose.PSD للغة Java مجانية للاستخدام؟**  
تتوفر نسخة تجريبية مجانية للتقييم. تتطلب الوظائف الكاملة ترخيصًا مدفوعًا. راجع [خيارات الشراء](https://purchase.aspose.com/buy) للمزيد من التفاصيل.

---

**آخر تحديث:** 2026-04-03  
**تم الاختبار مع:** Aspose.PSD 24.12 للغة Java  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}