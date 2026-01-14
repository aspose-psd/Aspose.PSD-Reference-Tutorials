---
date: 2026-01-14
description: تعلم كيفية إنشاء طبقة حد متدرج وتخصيص تدرجات الحدود في ملفات PSD باستخدام
  Aspose.PSD للغة Java من خلال هذا الدليل خطوة بخطوة.
linktitle: How to Create Gradient Stroke Layer in Java
second_title: Aspose.PSD Java API
title: كيفية إنشاء طبقة خط متدرج في جافا
url: /ar/java/java-graphics-drawing/add-stroke-layer-gradient/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# كيفية إنشاء طبقة حد تدرج لوني في Java

## مقدمة
هل تساءلت يوماً كيف **تنشئ طبقة حد تدرج لوني** في ملفات PSD باستخدام Java؟ أنت في المكان الصحيح! اليوم سنغوص في Aspose.PSD for Java—مكتبة قوية تتيح لك تعديل ملفات PSD بسهولة. سواء كنت جديدًا في برمجة الرسوميات أو تبحث عن تحسين تصاميم موجودة، سيوجهك هذا الدليل خطوة بخطوة لإضافة وتخصيص تدرجات الحدود.

## إجابات سريعة
- **ما هو الهدف الأساسي؟** إنشاء طبقة حد تدرج لوني في ملف PSD.  
- **ما المكتبة المطلوبة؟** Aspose.PSD for Java.  
- **هل أحتاج إلى ترخيص؟** نعم، يلزم وجود ترخيص صالح (أو مؤقت) للاستخدام في الإنتاج.  
- **ما نسخة Java المتوافقة؟** Java 8 أو أعلى.  
- **كم يستغرق التنفيذ؟** تقريباً 10‑15 دقيقة لإنشاء حد تدرج أساسي.

## ما هي طبقة حد تدرج لوني؟
طبقة حد تدرج لوني هي حدود متجهة حول شكل أو نص تنتقل بسلاسة بين الألوان. باستخدام Aspose.PSD يمكنك تعريف الألوان، الشفافية، الزاوية، والنوع (خطّي، شعاعي، إلخ) للحد برمجيًا.

## لماذا تستخدم Aspose.PSD for Java؟
- **دعم كامل لملفات PSD** – قراءة، تعديل، وكتابة ملفات PSD دون الحاجة إلى Photoshop.  
- **API غني للتأثيرات** – الوصول إلى حدود، ظلال، توهج، والعديد من تأثيرات الطبقات الأخرى.  
- **متعدد المنصات** – يعمل على أي نظام تشغيل يدعم Java.  
- **بدون تبعيات أصلية** – جافا صافية، سهل الدمج في خطوط CI.

## المتطلبات المسبقة
1. **Java Development Kit (JDK)** – قم بتثبيت أحدث JDK من [Oracle's website](https://www.oracle.com/java/technologies/javase-downloads.html).  
2. **Aspose.PSD for Java** – حمّل المكتبة من [Aspose.PSD download page](https://releases.aspose.com/psd/java/).  
3. **IDE** – IntelliJ IDEA، Eclipse، أو NetBeans.  
4. **License** – احصل على [temporary license](https://purchase.aspose.com/temporary-license/) إذا لم يكن لديك ترخيص كامل.

## استيراد الحزم
أولاً، استورد الفئات التي سنحتاجها لتحميل ملف PSD، الوصول إلى التأثيرات، وتكوين تعبئات التدرج.

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.examples.Utils.Assert;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.BlendMode;
import com.aspose.psd.fileformats.psd.layers.IGradientColorPoint;
import com.aspose.psd.fileformats.psd.layers.fillsettings.FillType;
import com.aspose.psd.fileformats.psd.layers.fillsettings.GradientColorPoint;
import com.aspose.psd.fileformats.psd.layers.fillsettings.GradientFillSettings;
import com.aspose.psd.fileformats.psd.layers.fillsettings.GradientTransparencyPoint;
import com.aspose.psd.fileformats.psd.layers.fillsettings.GradientType;
import com.aspose.psd.fileformats.psd.layers.fillsettings.IGradientTransparencyPoint;
import com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
```

الآن لنقسم العملية إلى خطوات واضحة.

## الخطوة 1: تحميل ملف PSD
نحمّل ملف PSD المصدر ونفعّل موارد التأثير حتى يصبح تأثير الحد متاحًا.

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "Stroke.psd";
String exportPath = dataDir + "StrokeGradientChanged.psd";
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);
PsdImage im = (PsdImage) Image.load(sourceFileName, loadOptions);
```

## الخطوة 2: الوصول إلى تأثير الحد
بافتراض أن الحد الذي نريد تعديله ينتمي إلى الطبقة الثالثة (الفهرس 2)، نسترجع `StrokeEffect` الخاص به.

```java
StrokeEffect gradientStroke = (StrokeEffect) im.getLayers()[2].getBlendingOptions().getEffects()[0];
```

## الخطوة 3: التحقق من خصائص تأثير الحد
قبل إجراء أي تغييرات، نؤكد الإعدادات الحالية حتى نعرف بالضبط ما سنحدّثه.

```java
Assert.areEqual(BlendMode.Normal, gradientStroke.getBlendMode());
Assert.areEqual(255, gradientStroke.getOpacity());
Assert.areEqual(true, gradientStroke.isVisible());
GradientFillSettings fillSettings = (GradientFillSettings) gradientStroke.getFillSettings();
Assert.areEqual(Color.getBlack(), fillSettings.getColor());
Assert.areEqual(FillType.Gradient, fillSettings.getFillType());
Assert.areEqual(true, fillSettings.getAlignWithLayer());
Assert.areEqual(GradientType.Linear, fillSettings.getGradientType());
Assert.isTrue(Math.abs(90 - fillSettings.getAngle()) < 0.001, "Angle is incorrect");
Assert.areEqual(false, fillSettings.getDither());
Assert.isTrue(Math.abs(0 - fillSettings.getHorizontalOffset()) < 0.001, "Horizontal offset is incorrect");
Assert.isTrue(Math.abs(0 - fillSettings.getVerticalOffset()) < 0.001, "Vertical offset is incorrect");
Assert.areEqual(false, fillSettings.getReverse());
```

## الخطوة 4: تعديل إعدادات تعبئة التدرج
هنا نغيّر اللون، الشفافية، وضع المزج، وغيرها من الخصائص لتحقيق المظهر المطلوب.

```java
fillSettings.setColor(Color.getGreen());
gradientStroke.setOpacity((byte) 127);
gradientStroke.setBlendMode(BlendMode.Color);
fillSettings.setAlignWithLayer(false);
fillSettings.setGradientType(GradientType.Radial);
fillSettings.setAngle(45);
fillSettings.setDither(true);
fillSettings.setHorizontalOffset(15);
fillSettings.setVerticalOffset(11);
fillSettings.setReverse(true);
```

## الخطوة 5: إضافة وتعديل نقاط اللون والشفافية
نضيف نقاط لون وشفافية جديدة، ثم نضبط النقاط الحالية لتشكيل التدرج.

```java
// Add new color point
GradientColorPoint colorPoint = fillSettings.addColorPoint();
colorPoint.setColor(Color.getGreen());
colorPoint.setLocation(4096);
colorPoint.setMedianPointLocation(75);
// Change location of previous point
fillSettings.getColorPoints()[1].setLocation(1899);
// Add new transparency point
GradientTransparencyPoint transparencyPoint = fillSettings.addTransparencyPoint();
transparencyPoint.setOpacity(25);
transparencyPoint.setMedianPointLocation(25);
transparencyPoint.setLocation(4096);
// Change location of previous transparency point
fillSettings.getTransparencyPoints()[1].setLocation(2411);
```

## الخطوة 6: حفظ ملف PSD المعدل
بعد جميع التعديلات، نكتب الملف المحدث مرة أخرى إلى القرص.

```java
im.save(exportPath);
```

## الخطوة 7: التحقق من التعديلات
نحمّل الملف المحفوظ ونؤكد أن كل خاصية تعكس التغييرات التي أجريناها.

```java
PsdImage img = (PsdImage) Image.load(exportPath, loadOptions);
StrokeEffect gradientStrokeEffect = (StrokeEffect) img.getLayers()[2].getBlendingOptions().getEffects()[0];
Assert.areEqual(BlendMode.Color, gradientStrokeEffect.getBlendMode());
Assert.areEqual(127, gradientStrokeEffect.getOpacity());
Assert.areEqual(true, gradientStrokeEffect.isVisible());
GradientFillSettings fillSetting = (GradientFillSettings) gradientStrokeEffect.getFillSettings();
Assert.areEqual(Color.getGreen(), fillSetting.getColor());
Assert.areEqual(FillType.Gradient, fillSetting.getFillType());
// Check color points
Assert.areEqual(3, fillSetting.getColorPoints().length);
IGradientColorPoint point = fillSetting.getColorPoints()[0];
Assert.areEqual(50, point.getMedianPointLocation());
Assert.areEqual(Color.getBlack(), point.getColor());
Assert.areEqual(0, point.getLocation());
point = fillSettings.getColorPoints()[1];
Assert.areEqual(50, point.getMedianPointLocation());
Assert.areEqual(Color.getWhite(), point.getColor());
Assert.areEqual(1899, point.getLocation());
point = fillSettings.getColorPoints()[2];
Assert.areEqual(75, point.getMedianPointLocation());
Assert.areEqual(Color.getGreen(), point.getColor());
Assert.areEqual(4096, point.getLocation());
// Check transparency points
Assert.areEqual(3, fillSettings.getTransparencyPoints().length);
IGradientTransparencyPoint transparencyPoint1 = fillSettings.getTransparencyPoints()[0];
Assert.areEqual(50, transparencyPoint1.getMedianPointLocation());
Assert.areEqual(100, transparencyPoint1.getOpacity());
Assert.areEqual(0, transparencyPoint1.getLocation());
transparencyPoint1 = fillSettings.getTransparencyPoints()[1];
Assert.areEqual(50, transparencyPoint.getMedianPointLocation());
Assert.areEqual(100, transparencyPoint.getOpacity());
Assert.areEqual(2411, transparencyPoint.getLocation());
transparencyPoint1 = fillSettings.getTransparencyPoints()[2];
Assert.areEqual(25, transparencyPoint.getMedianPointLocation());
Assert.areEqual(25, transparencyPoint.getOpacity());
Assert.areEqual(4096, transparencyPoint.getLocation());
```

## الخاتمة
الآن تعرف كيف **تنشئ طبقة حد تدرج لوني** في ملفات PSD باستخدام Aspose.PSD for Java. من خلال تحميل PSD، الوصول إلى تأثير الحد، تعديل إعدادات تعبئة التدرج، وحفظ النتيجة، يمكنك إنتاج رسومات احترافية برمجيًا دون الحاجة إلى فتح Photoshop.

## الأسئلة المتكررة
### ما هو Aspose.PSD for Java؟
Aspose.PSD for Java هي مكتبة تتيح للمطورين العمل مع ملفات PSD في تطبيقات Java، وتوفر ميزات لإنشاء، تعديل، وتحويل ملفات PSD.

### هل أحتاج إلى ترخيص لاستخدام Aspose.PSD for Java؟
نعم، يلزم وجود ترخيص صالح لاستخدام Aspose.PSD for Java. يمكنك الحصول على [temporary license](https://purchase.aspose.com/temporary-license/) لأغراض التقييم.

### هل يمكنني استخدام Aspose.PSD for Java لإنشاء ملفات PSD من الصفر؟
بالطبع! توفر Aspose.PSD for Java واجهات برمجة تطبيقات شاملة لإنشاء وتعديل ملفات PSD برمجيًا.

### هل يمكن تطبيق تأثيرات أخرى باستخدام Aspose.PSD for Java؟
نعم، يمكنك تطبيق تأثيرات متنوعة مثل الظل، التوهج، والمزيد باستخدام Aspose.PSD for Java.

### أين يمكنني العثور على وثائق Aspose.PSD for Java؟
يمكنك العثور على الوثائق [here](https://reference.aspose.com/psd/java/).

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**آخر تحديث:** 2026-01-14  
**تم الاختبار باستخدام:** Aspose.PSD for Java 24.11  
**المؤلف:** Aspose