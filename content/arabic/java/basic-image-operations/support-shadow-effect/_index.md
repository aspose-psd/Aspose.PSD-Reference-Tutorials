---
title: دعم تأثير الظل في Aspose.PSD لجافا
linktitle: دعم تأثير الظل
second_title: Aspose.PSD جافا API
description: تعرف على كيفية إضافة تأثيرات الظل الجذابة إلى الصور باستخدام Aspose.PSD لـ Java. ارفع مستوى تصميمك الجرافيكي من خلال هذا البرنامج التعليمي خطوة بخطوة.
type: docs
weight: 13
url: /ar/java/basic-image-operations/support-shadow-effect/
---
## مقدمة

يعد تحسين الصور بتأثيرات الظل ممارسة شائعة في التصميم الجرافيكي، مما يضيف العمق والواقعية. يوفر Aspose.PSD for Java دعمًا قويًا لتأثيرات الظل، مما يسمح للمطورين بدمج هذه التأثيرات بسهولة في تطبيقات Java الخاصة بهم. في هذا البرنامج التعليمي، سنستكشف كيفية دعم تأثيرات الظل باستخدام Aspose.PSD، خطوة بخطوة.

## المتطلبات الأساسية

قبل الغوص في البرنامج التعليمي، تأكد من توفر المتطلبات الأساسية التالية:

- المعرفة الأساسية ببرمجة جافا.
-  تم تثبيت Aspose.PSD لـ Java. يمكنك تنزيله[هنا](https://releases.aspose.com/psd/java/).

## حزم الاستيراد

تأكد من قيامك باستيراد الحزم اللازمة للاستفادة من وظائف Aspose.PSD في تطبيق Java الخاص بك. استخدم مقتطف الشفرة التالي كدليل:

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;


import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.layereffects.DropShadowEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
```

## الخطوة 1: قم بتحميل صورة PSD

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "Shadow.psd";
String psdPathAfterChange = dataDir + "ShadowChanged.psd";

PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);
```

## الخطوة 2: استرداد تأثير الظل

```java
DropShadowEffect shadowEffect = (DropShadowEffect)(im.getLayers()[1].getBlendingOptions().getEffects()[0]);
```

## الخطوة 3: التحقق من الإعدادات الافتراضية

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

## الخطوة 4: تخصيص تأثير الظل

```java
shadowEffect.setColor(Color.getGreen());
shadowEffect.setOpacity((byte)128);
shadowEffect.setDistance(11);
shadowEffect.setUseGlobalLight(false);
shadowEffect.setSize(9);
shadowEffect.setAngle(45);
shadowEffect.setSpread(3);
shadowEffect.setNoise(50);
```

## الخطوة 5: احفظ الصورة المعدلة

```java
im.save(psdPathAfterChange);
```

## خاتمة

من خلال هذه الخطوات البسيطة، يمكنك بسهولة دعم تأثيرات الظل في Aspose.PSD لـ Java، مما يعزز المظهر المرئي لصورك.

## الأسئلة الشائعة

### س1: هل Aspose.PSD for Java مناسب لمشاريع التصميم الجرافيكي الاحترافية؟

ج1: بالتأكيد! Aspose.PSD for Java هي مكتبة قوية مصممة لمهام التصميم الجرافيكي الاحترافية.

### س2: هل يمكنني استخدام Aspose.PSD لـ Java في التطبيقات التجارية؟

 ج2: نعم، Aspose.PSD لـ Java هو منتج تجاري. يمكنك شرائه[هنا](https://purchase.aspose.com/buy).

### س3: هل هناك نسخة تجريبية مجانية متاحة؟

 ج3: نعم، يمكنك استكشاف نسخة تجريبية مجانية.[هنا](https://releases.aspose.com/).

### س4: أين يمكنني العثور على وثائق مفصلة؟

 ج4: راجع الوثائق الشاملة[هنا](https://reference.aspose.com/psd/java/).

### س5: كيف يمكنني الحصول على دعم Aspose.PSD لـ Java؟

 ج5: انضم إلى منتدى المجتمع.[هنا](https://forum.aspose.com/c/psd/34) لأية استفسارات الدعم.