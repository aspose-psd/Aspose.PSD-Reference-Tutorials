---
title: إضافة تأثيرات النمط في Aspose.PSD لـ Java
linktitle: إضافة تأثيرات النمط
second_title: Aspose.PSD جافا API
description: قم بتحسين أنماط صور Java الخاصة بك بسهولة باستخدام Aspose.PSD لـ Java. اتبع البرنامج التعليمي خطوة بخطوة لإضافة تأثيرات نمط آسرة.
type: docs
weight: 12
url: /ar/java/advanced-image-effects/add-pattern-effects/
---
## مقدمة

في عالم تطوير Java، يعد تحسين أنماط الصور مهمة شائعة، ويوفر Aspose.PSD for Java حلاً قويًا لذلك. سيرشدك هذا البرنامج التعليمي خلال عملية إضافة تأثيرات النمط باستخدام Aspose.PSD، مما يضمن أن صورك تتميز بتراكبات وتحسينات فريدة.

## المتطلبات الأساسية

قبل الغوص في البرنامج التعليمي، تأكد من توفر المتطلبات الأساسية التالية:

- تم تثبيت Java Development Kit (JDK) على نظامك.
-  تم تنزيل Aspose.PSD لمكتبة Java وإضافتها إلى مشروعك. يمكنك تنزيله من[موقع Aspose.PSD](https://releases.aspose.com/psd/java/).

## حزم الاستيراد

في مشروع Java الخاص بك، قم باستيراد الحزم اللازمة للعمل مع Aspose.PSD. قم بتضمين الكود التالي في بداية فصل Java الخاص بك:

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.Rectangle;


import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.BlendMode;
import com.aspose.psd.fileformats.psd.layers.fillsettings.FillType;
import com.aspose.psd.fileformats.psd.layers.fillsettings.PatternFillSettings;
import com.aspose.psd.fileformats.psd.layers.layereffects.PatternOverlayEffect;
import com.aspose.psd.fileformats.psd.layers.layerresources.PattResource;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;

import java.util.UUID;
```

## الخطوة 1: تحميل الصورة

```java
// قم بتحميل صورة PSD
String sourceFileName = "YourImagePath/PatternOverlay.psd";
String exportPath = "YourExportPath/PatternOverlayChanged.psd";

PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);
```

تأكد من استبدال "YourImagePath" و"YourExportPath" بالمسارات الفعلية في مشروعك.

## الخطوة 2: استخراج معلومات تراكب النمط

```java
// استخراج المعلومات حول تراكب النمط
PatternOverlayEffect patternOverlay = (PatternOverlayEffect)im.getLayers()[1].getBlendingOptions().getEffects()[0];
```

## الخطوة 3: تعديل إعدادات تراكب النمط

```java
// تعديل إعدادات تراكب النمط
PatternFillSettings settings = patternOverlay.getSettings();
settings.setColor(Color.getGreen());
patternOverlay.setOpacity((byte)193);
patternOverlay.setBlendMode(BlendMode.Difference);
settings.setHorizontalOffset(15);
settings.setVerticalOffset(11);
```

## الخطوة 4: تحرير بيانات النمط

```java
// تحرير بيانات النمط
PattResource resource;
UUID guid = UUID.randomUUID();
String newPatternName = "$$/Presets/Patterns/Pattern=Some new pattern name\0";

for (int i = 0; i < im.getGlobalLayerResources().length; i++) {
    if (im.getGlobalLayerResources()[i] instanceof PattResource) {
        resource = (PattResource)im.getGlobalLayerResources()[i];
        resource.setPatternId(guid.toString());
        resource.setName(newPatternName);
        resource.setPattern(new int[]{Color.getAqua().toArgb(), Color.getRed().toArgb(),
                        Color.getRed().toArgb(), Color.getAqua().toArgb(),
                        Color.getAqua().toArgb(), Color.getWhite().toArgb(),
                        Color.getWhite().toArgb(), Color.getAqua().toArgb()}, new Rectangle(0, 0, 4, 2));
    }
}
```

## الخطوة 5: احفظ الصورة المعدلة

```java
// احفظ الصورة المعدلة
settings.setPatternName(newPatternName);
settings.setPatternId(guid.toString() + "\0");
im.save(exportPath);
```

## الخطوة 6: التحقق من التغييرات

```java
// التحقق من التغييرات في الملف المحرر
PsdImage img = (PsdImage)Image.load(sourceFileName, loadOptions);
PatternOverlayEffect patternOverlayEffect = (PatternOverlayEffect)img.getLayers()[1].getBlendingOptions().getEffects()[0];

// أضف تأكيدات للتأكد من تطبيق التغييرات بنجاح
```

## خاتمة

تهانينا! لقد تعلمت بنجاح كيفية إضافة تأثيرات النمط باستخدام Aspose.PSD لـ Java. تتيح لك هذه المكتبة القوية إنشاء صور جذابة بصريًا بأنماط مخصصة، مما يوفر إمكانيات لا حصر لها لمشاريعك المستندة إلى Java.

## الأسئلة الشائعة

### س1: هل يمكنني استخدام Aspose.PSD لـ Java مع مكتبات معالجة صور Java الأخرى؟

ج1: تم تصميم Aspose.PSD for Java للعمل بشكل مستقل، ولكن يمكنك دمجه مع مكتبات Java الأخرى إذا لزم الأمر.

### س2: أين يمكنني العثور على الوثائق التفصيلية لـ Aspose.PSD لـ Java؟

 ج2: راجع[Aspose.PSD لوثائق جافا](https://reference.aspose.com/psd/java/) للحصول على معلومات شاملة.

### س3: هل هناك نسخة تجريبية مجانية متاحة لـ Aspose.PSD لـ Java؟

 ج3: نعم، يمكنك الوصول إلى النسخة التجريبية المجانية[هنا](https://releases.aspose.com/).

### س4: كيف يمكنني الحصول على دعم Aspose.PSD لـ Java؟

 ج4: قم بزيارة[منتدى Aspose.PSD](https://forum.aspose.com/c/psd/34) للحصول على دعم المجتمع أو فكر في شراء خطة دعم.

### س5: هل يمكنني الحصول على ترخيص مؤقت لـ Aspose.PSD لـ Java؟

ج5: نعم، يمكنك الحصول على ترخيص مؤقت[هنا](https://purchase.aspose.com/temporary-license/).