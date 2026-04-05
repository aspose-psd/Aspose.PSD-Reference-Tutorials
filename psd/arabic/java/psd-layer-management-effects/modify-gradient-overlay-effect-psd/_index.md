---
date: 2026-04-05
description: تعلم كيفية تعديل تراكب التدرج في جافا لتعديل تأثير تراكب التدرج في ملف
  PSD باستخدام Aspose.PSD للغة جافا وإضافة طبقات تراكب التدرج إلى ملف PSD برمجيًا.
keywords:
- modify gradient overlay java
- add gradient overlay psd
- Aspose.PSD Java
- PSD layer effects
- gradient overlay effect
linktitle: تعديل تأثير التراكب المتدرج في PSD باستخدام جافا
second_title: Aspose.PSD Java API
title: تعديل تراكب التدرج في جافا – تعديل تأثير تراكب التدرج في PSD باستخدام جافا
url: /ar/java/psd-layer-management-effects/modify-gradient-overlay-effect-psd/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# تعديل تراكب التدرج في جافا – تعديل تأثير تراكب التدرج في PSD باستخدام جافا

## مقدمة

في هذا الدرس ستتعلم كيفية **modify gradient overlay java** لتغيير تأثير تراكب التدرج في ملف فوتوشوب (PSD) باستخدام Aspose.PSD for Java. سواءً كنت تقوم بأتمتة مهام التصميم المتكررة أو تبني خط أنابيب مخصص لمعالجة الصور، فإن إتقان هذه التقنية يتيح لك إضافة لمسة احترافية دون الحاجة لفتح فوتوشوب.

## إجابات سريعة
- **ما المكتبة التي أحتاجها؟** Aspose.PSD for Java (download **[هنا](https://releases.aspose.com/psd/java/)**).  
- **ما إصدار جافا المطلوب؟** JDK 1.8 أو أحدث.  
- **هل يمكنني إضافة تراكب تدرج إلى أي طبقة؟** نعم – فقط استهدف فهرس الطبقة المطلوب.  
- **هل تحتاج إلى ترخيص للإنتاج؟** نعم، يلزم ترخيص تجاري للاستخدام غير التجريبي.  
- **كم من الوقت تستغرق العملية؟** تقريبًا 10‑15 دقيقة للإعداد الأساسي.

## ما هو “modify gradient overlay java”؟

تعديل تراكب التدرج في جافا يعني تعديل التدرج البصري برمجيًا والذي يقع فوق طبقة PSD. يتيح لك ذلك تغيير الألوان، الشفافية، وضع المزج، الزاوية، والحجم دون الحاجة إلى تحرير يدوي في فوتوشوب.

## لماذا تستخدم Aspose.PSD لإضافة تراكب تدرج إلى طبقات PSD؟

- **الأتمتة:** معالجة العشرات من ملفات PSD في مهمة دفعة.  
- **الدقة:** تعيين قيم عددية دقيقة للشفافية، الزاوية، ونقاط ألوان التدرج.  
- **متعدد المنصات:** تشغيل نفس الشيفرة على Windows أو Linux أو macOS.  
- **بدون الحاجة إلى فوتوشوب:** مثالي للتصوير على الخادم أو خطوط أنابيب CI.

## المتطلبات المسبقة

- مكتبة Aspose.PSD for Java – تحميل من الرابط أعلاه.  
- Java Development Kit (JDK) 1.8+ مثبت.  
- بيئة تطوير متكاملة مثل IntelliJ IDEA أو Eclipse.  
- ملف PSD تجريبي يحتوي على طبقة واحدة على الأقل تريد تعديلها.  
- إلمام أساسي بصياغة جافا.

بمجرد التأكد من القائمة، يمكننا الغوص في الشيفرة.

## استيراد الحزم

أولاً، استورد الفئات التي تمنحنا الوصول إلى معالجة PSD، تأثيرات الطبقة، وإعدادات التدرج.

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.BlendMode;
import com.aspose.psd.fileformats.psd.layers.IGradientColorPoint;
import com.aspose.psd.fileformats.psd.layers.fillsettings.GradientColorPoint;
import com.aspose.psd.fileformats.psd.layers.fillsettings.GradientFillSettings;
import com.aspose.psd.fileformats.psd.layers.fillsettings.GradientType;
import com.aspose.psd.fileformats.psd.layers.layereffects.BlendingOptions;
import com.aspose.psd.fileformats.psd.layers.layereffects.GradientOverlayEffect;
import com.aspose.psd.fileformats.psd.layers.layereffects.ILayerEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
```

## كيفية تعديل تراكب التدرج في جافا – الخطوة 1: تحميل ملف PSD

تحميل الملف باستخدام `PsdLoadOptions` يضمن الحفاظ على أي تأثيرات موجودة.

```java
String sourceDir = "Your Source Directory";
String inPsdFilePath = sourceDir + "psdnet256.psd";

// Enable support for existing layer effects
PsdLoadOptions psdLoadOptions = new PsdLoadOptions();
psdLoadOptions.setLoadEffectsResource(true);

// Load the PSD file
PsdImage psdImage = (PsdImage) Image.load(inPsdFilePath, psdLoadOptions);
```

## كيفية إضافة تراكب تدرج إلى PSD – الخطوة 2: تحديد الطبقة المستهدفة

حدد الطبقة التي تريد تعديلها. في هذا المثال نعمل مع الطبقة الثانية (`[1]`).

```java
BlendingOptions layerBlendOptions = psdImage.getLayers()[1].getBlendingOptions();
```

## الخطوة 3: البحث عن تأثير تراكب التدرج الموجود

نسترجع إما التأثير الموجود أو ننشئ واحدًا جديدًا إذا لم يكن موجودًا.

```java
GradientOverlayEffect gradientOverlayEffect = null;
for (ILayerEffect effect : layerBlendOptions.getEffects()) {
    if (effect instanceof GradientOverlayEffect) {
        gradientOverlayEffect = (GradientOverlayEffect) effect;
        break;
    }
}

if (gradientOverlayEffect == null) {
    // Create a new GradientOverlayEffect if it doesn't exist
    gradientOverlayEffect = layerBlendOptions.addGradientOverlay();
}
```

## الخطوة 4: تعديل تأثير تراكب التدرج

### تعيين الشفافية ووضع المزج

```java
gradientOverlayEffect.setOpacity((byte) 200);
gradientOverlayEffect.setBlendMode(BlendMode.Hue);
```

### تخصيص ألوان التدرج والإعدادات

```java
GradientFillSettings settings = gradientOverlayEffect.getSettings();
settings.setColorPoints(new IGradientColorPoint[]{
        new GradientColorPoint(Color.getGreenYellow(), 0, 50),
        new GradientColorPoint(Color.getBlueViolet(), 4096, 50),
});
settings.setAngle(80);
settings.setScale(150);
settings.setGradientType(GradientType.Linear);
settings.getTransparencyPoints()[0].setOpacity(100);
settings.getTransparencyPoints()[1].setOpacity(100);
```

## الخطوة 5: حفظ ملف PSD المعدل

أخيرًا، احفظ التغييرات في ملف جديد ونظف الموارد.

```java
String outputDir = "Your Document Directory";
String outPsdFilePath = outputDir + "psdnet256.psd_output.psd";

psdImage.save(outPsdFilePath);
psdImage.dispose();
```

## المشكلات الشائعة والحلول

- **التأثير غير مرئي بعد الحفظ:** تحقق من أن فهرس الطبقة صحيح وأن وضع المزج ليس مضبوطًا على وضع يخفي التدرج (مثلاً، `Normal` بنسبة شفافية 0 %).  
- **نقاط اللون تظهر معكوسة:** ترتيب كائنات `GradientColorPoint` يحدد البداية إلى النهاية؛ قم بتبديلها إذا كان اتجاه التدرج عكس المتوقع.  
- **استثناء عند التحميل:** تأكد من استدعاء `psdLoadOptions.setLoadEffectsResource(true)`؛ وإلا قد يتم تجاهل التأثيرات الموجودة، مما يؤدي إلى مراجع `null`.

## الأسئلة المتكررة

### هل يمكنني تطبيق عدة تراكبات تدرج على طبقة واحدة؟

نعم، يمكنك تطبيق عدة تراكبات تدرج على طبقة واحدة عن طريق إضافة مثيلات جديدة من `GradientOverlayEffect` إلى خيارات المزج للطبقة.

### هل يمكن إزالة تأثير تراكب التدرج من طبقة؟

بالطبع! يمكنك إزالة تأثير تراكب التدرج الموجود ببساطة بحذف التأثير المقابل من خيارات المزج للطبقة.

### ما هي التأثيرات الأخرى التي يمكنني تطبيقها باستخدام Aspose.PSD for Java؟

تتيح لك Aspose.PSD for Java تطبيق تأثيرات مختلفة، مثل الظلال، التوهجات الداخلية، التوهجات الخارجية، والمزيد. يمكنك تخصيص كل تأثير ليناسب احتياجاتك.

### كيف يمكنني التراجع عن التغييرات التي تم إجراؤها على ملف PSD؟

إذا لم تقم بحفظ الملف بعد، يمكنك ببساطة إعادة تحميل ملف PSD الأصلي. إذا قمت بحفظه بالفعل، ستحتاج إلى الاستعادة من نسخة احتياطية أو التراجع عن التغييرات برمجيًا.

## أسئلة شائعة

**س: هل يعمل هذا مع ملفات PSD التي تحتوي على كائنات ذكية؟**  
**ج:** نعم، لكن الكائنات الذكية تُعامل كطبقات عادية؛ سيتأثر تراكب التدرج بالتمثيل النقطي.

**س: هل يمكنني ربط عدة تراكبات تدرج بوضعات مزج مختلفة؟**  
**ج:** بالتأكيد. كل `GradientOverlayEffect` يمكن أن يكون له وضع مزج خاص به، مما يسمح بتركيبات بصرية معقدة.

**س: هل هناك طريقة لقراءة إعدادات التدرج الحالية قبل تعديلها؟**  
**ج:** نعم. استخدم `gradientOverlayEffect.getSettings()` لاسترجاع `GradientFillSettings` الحالية وفحص خصائصها.

**س: هل سيحافظ ملف PSD المعدل على التوافق مع فوتوشوب؟**  
**ج:** الملف المحفوظ يلتزم بمواصفات PSD، لذا سيفتحه فوتوشوب دون مشاكل، مع الحفاظ على تراكب التدرج المضاف أو المعدل حديثًا.

**س: هل أحتاج إلى ترخيص تجاري لبنات التطوير؟**  
**ج:** ترخيص تجريبي مجاني يكفي للاختبار، لكن الترخيص المشتراة مطلوب للنشر في بيئة الإنتاج.

---

**آخر تحديث:** 2026-04-05  
**تم الاختبار مع:** Aspose.PSD for Java 24.11  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}