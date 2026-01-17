---
date: 2026-01-17
description: تعلم كيفية إضافة نمط الخط في جافا باستخدام Aspose.PSD للغة جافا. اتبع
  هذا الدليل خطوة بخطوة لتعزيز صور PSD الخاصة بك بسرعة.
linktitle: How to Add Stroke Layer Pattern in Java
second_title: Aspose.PSD Java API
title: كيفية إضافة نمط الحد في جافا باستخدام Aspose.PSD
url: /ar/java/java-graphics-drawing/add-stroke-layer-pattern/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# كيفية إضافة نمط الحد Java باستخدام Aspose.PSD

## المقدمة
إذا كنت بحاجة إلى **add stroke pattern java** إلى ملف Photoshop، فإن Aspose.PSD for Java يجعل العملية بسيطة بشكل مفاجئ. سواءً كنت تبني أداة تصميم جرافيكي، أو تقوم بأتمتة تعديلات دفعية، أو مجرد تجربة تأثيرات الطبقات، فإن هذا الدليل يرافقك في كل خطوة—من تحميل ملف PSD إلى التحقق من النمط الجديد. لنبدأ ونرى مدى السرعة التي يمكنك بها تحسين صورك.

## إجابات سريعة
- **ما المكتبة التي أحتاجها؟** Aspose.PSD for Java  
- **ما نسخة Java المدعومة؟** JDK 8 أو أحدث  
- **هل أحتاج إلى ترخيص للاختبار؟** النسخة التجريبية المجانية تكفي للتطوير؛ الترخيص مطلوب للإنتاج  
- **كم يستغرق التنفيذ؟** تقريباً 10‑15 دقيقة لنمط حد أساسي  
- **هل يمكن إعادة استخدام النمط على طبقات متعددة؟** نعم، فقط عيّن نفس `PattResource` للطبقات الأخرى  

## ما هو إضافة نمط الحد Java؟
إضافة نمط حد في Java تعني تطبيق تعبئة مخصصة (غالباً صورة متكررة) على تأثير حد الطبقة. تتيح لك هذه التقنية إنشاء حدود مُصممة—مثل خط متقطع، أو نسيج طوب، أو إطار رسومي مخصص—مباشرة داخل ملف PSD دون الحاجة لفتح Photoshop.

## لماذا تستخدم Aspose.PSD لإضافة نمط الحد Java؟
- **دقة كاملة للـ PSD** – جميع تأثيرات الطبقات والموارد وأنماط المزج محفوظة.  
- **لا حاجة إلى Photoshop الأصلي** – يعمل على أي نظام تشغيل مع JDK.  
- **تحكم برمجي** – أتمتة المعالجة الدفعية أو دمجها في خدمات الخادم.  
- **API غني** – الوصول إلى الموارد العامة، تعبئة الأنماط، وأنماط المزج في واجهة واحدة سلسة.  

## المتطلبات المسبقة
- **مجموعة تطوير Java (JDK)** – تأكد من تثبيت JDK 8 أو أحدث.  
- **Aspose.PSD for Java** – قم بتحميل المكتبة من [here](https://releases.aspose.com/psd/java/) وأضف ملف JAR إلى مسار الفئة في مشروعك.  
- **بيئة التطوير المتكاملة (IDE)** – IntelliJ IDEA أو Eclipse أو أي محرر تفضله.  

## استيراد الحزم
أولاً، استورد الفئات التي ستحتاجها للتعامل مع ملفات PSD، الألوان، المستطيلات، وتأثيرات الحد.

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

## الخطوة 1: تحميل ملف PSD
حمّل ملف PSD المصدر حتى تتمكن من العمل مع طبقاته وموارده.

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "Stroke.psd";
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);
PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);
```

## الخطوة 2: إعداد بيانات النمط الجديد
أنشئ نمطًا بسيطًا بحجم 4 × 4 بكسل سيُستخدم للحد.

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

## الخطوة 3: الوصول إلى تأثير الحد
حدد تأثير الحد على الطبقة المستهدفة (في هذا المثال، الطبقة الرابعة).

```java
StrokeEffect patternStroke = (StrokeEffect)im.getLayers()[3].getBlendingOptions().getEffects()[0];
Assert.areEqual(BlendMode.Normal, patternStroke.getBlendMode());
Assert.areEqual(255, patternStroke.getOpacity());
Assert.areEqual(true, patternStroke.isVisible());
PatternFillSettings fillSettings = (PatternFillSettings)patternStroke.getFillSettings();
Assert.areEqual(FillType.Pattern, fillSettings.getFillType());
```

## الخطوة 4: تعديل تأثير الحد
### تحديث خصائص تأثير الحد
عدّل الشفافية ووضع المزج لرؤية الأثر البصري للنمط الجديد.

```java
patternStroke.setOpacity((byte)127);
patternStroke.setBlendMode(BlendMode.Color);
```

### تحديث مورد النمط
استبدل مورد النمط العالمي الحالي بالذي أنشأته للتو.

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

## الخطوة 5: تطبيق النمط الجديد
اربط مورد النمط المحدث بتأثير الحد واحفظ ملف PSD.

```java
((PatternFillSettings)patternStroke.getFillSettings()).setPatternName("$$/Presets/Patterns/HorizontalLine1=Horizontal Line 9\0");
((PatternFillSettings)patternStroke.getFillSettings()).setPatternId(guid.toString() + "\0");
im.save(exportPath);
```

## الخطوة 6: التحقق من التغييرات
أعد تحميل الملف وتأكد من أن النمط الجديد، الشفافية، ووضع المزج تم تطبيقها بشكل صحيح.

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

## المشكلات الشائعة والحلول
| المشكلة | السبب | الحل |
|---------|-------|------|
| النمط لا يظهر | إشارة `PatternId` غير صحيحة | تأكد من أن `PatternId` المعين على `PattResource` يطابق ما يُستخدم في `PatternFillSettings`. |
| الحد يختفي بعد الحفظ | تم ضبط الشفافية على 0 أو تم إخفاء التأثير | تحقق من أن `setOpacity` بين 0‑255 وأن `isVisible()` تُعيد `true`. |
| ألوان غير متوقعة | عدم توافق وضع المزج | استخدم `BlendMode.Color` (أو وضع آخر) يتوافق مع هدف التصميم الخاص بك. |

## الأسئلة المتكررة
### ما هو Aspose.PSD for Java؟
Aspose.PSD for Java هي مكتبة تتيح للمطورين إنشاء، تعديل، وتحويل ملفات PSD (Photoshop Document) برمجيًا.

### هل يمكنني استخدام Aspose.PSD for Java في مشروع تجاري؟
نعم، يمكنك استخدامها في المشاريع التجارية. يمكنك شراء ترخيص من [here](https://purchase.aspose.com/buy).

### هل تتوفر نسخة تجريبية مجانية لـ Aspose.PSD for Java؟
نعم، يمكنك تنزيل نسخة تجريبية مجانية من [here](https://releases.aspose.com/).

### كيف يمكنني الحصول على الدعم لـ Aspose.PSD for Java؟
يمكنك الحصول على الدعم من منتديات مجتمع Aspose [here](https://forum.aspose.com/c/psd/34).

### ما هي متطلبات النظام لـ Aspose.PSD for Java؟
تحتاج إلى تثبيت JDK وبيئة تطوير (IDE). المكتبة تدعم أنظمة تشغيل متعددة بما فيها Windows وLinux وmacOS.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Last Updated:** 2026-01-17  
**Tested With:** Aspose.PSD for Java 24.12 (latest at time of writing)  
**Author:** Aspose