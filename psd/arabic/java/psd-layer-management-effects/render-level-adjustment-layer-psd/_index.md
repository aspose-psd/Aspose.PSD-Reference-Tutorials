---
title: تقديم طبقة ضبط المستوى في ملفات PSD - Java
linktitle: تقديم طبقة ضبط المستوى في ملفات PSD - Java
second_title: Aspose.PSD جافا API
description: تعرف على كيفية تحسين تباين الصورة وحيويتها بسهولة باستخدام Aspose.PSD لـ Java. طبقات ضبط المستويات الرئيسية باستخدام هذا الدليل التفصيلي خطوة بخطوة.
weight: 17
url: /ar/java/psd-layer-management-effects/render-level-adjustment-layer-psd/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# تقديم طبقة ضبط المستوى في ملفات PSD - Java

## مقدمة

هل سبق لك أن فتحت ملف PSD لتجد الصورة تفتقر إلى التباين أو الحيوية؟ لا تخافوا، ومحاربي تحرير الصور! يأتي Aspose.PSD for Java إلى الإنقاذ من خلال إمكانات معالجة طبقة ضبط المستويات القوية. سيزودك هذا الدليل بالمعرفة اللازمة لضبط صورك باستخدام المستويات في غاية السهولة. 

## المتطلبات الأساسية

- Java Development Kit (JDK): تأكد من تثبيت إصدار حديث من JDK على نظامك. يمكنك تحميله من موقع أوراكل ([https://www.Oracle.com/java/technologies/javase-downloads.html](https://www.oracle.com/java/technologies/javase-downloads.html)).
- Aspose.PSD لمكتبة Java: قم بتنزيل مكتبة Aspose.PSD لـ Java من صفحة التنزيل ([https://releases.aspose.com/psd/Java/](https://releases.aspose.com/psd/java/)). ستحتاج إلى ترخيص صالح لاستخدام الميزات الكاملة، ولكن تتوفر نسخة تجريبية مجانية للبدء ([https://releases.aspose.com/](https://releases.aspose.com/)).

## حزم الاستيراد

قبل الغوص في التعليمات البرمجية، نحتاج إلى استيراد فئات Aspose.PSD الضرورية للتفاعل مع ملفات PSD. إليك ما ستحتاج إليه:

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.LevelsLayer;
import com.aspose.psd.fileformats.psd.layers.layerresources.LevelChannel;
import com.aspose.psd.imageoptions.PngOptions;
```

 ال`com.aspose.psd` توفر الحزمة إمكانية الوصول إلى وظائف معالجة PSD، بينما`com.aspose.psd.imaging.PngOptions` يتيح لنا تحديد الخيارات عند حفظ الصورة بتنسيق PNG.

الآن، دعونا نشرع في مغامرة تعديل المستويات:

## الخطوة 1: إعداد مسارات الملفات:

- تحديد المتغيرات لدليل المستند الخاص بك (`dataDir`)، اسم ملف PSD المصدر (`sourceFileName`)، اسم ملف PSD المستهدف بعد التعديل (`psdPathAfterChange`)، ومسار تصدير PNG النهائي (`pngExportPath`). فكر في استخدام أسماء وصفية لتحسين إمكانية قراءة التعليمات البرمجية.

```java
String dataDir = "Your Document Directory";

String sourceFileName = dataDir + "LevelsAdjustmentLayer.psd";
String psdPathAfterChange = dataDir + "LevelsAdjustmentLayerChanged.psd";
String pngExportPath = dataDir + "LevelsAdjustmentLayerChanged.png";
```

## الخطوة 2: تحميل صورة PSD:

-  استخدم`Image.load` طريقة لفتح ملف PSD المصدر وتخزينه في ملف`PsdImage`هدف (`im`). يكتشف Aspose.PSD تنسيق الملف تلقائيًا.

```java
PsdImage im = (PsdImage)Image.load(sourceFileName);
```

## الخطوة 3: التكرار عبر الطبقات:

- نحن بحاجة إلى العثور على طبقة تعديل المستويات داخل ملف PSD الخاص بك. يوفر Aspose طريقة ملائمة للتكرار عبر جميع الطبقات باستخدام حلقة.

```java
for (int i = 0; i < im.getLayers().length; i++) {
   // ... (ستتم إضافة رمز التحقق من طبقة المستويات هنا)
}
```

## الخطوة 4: تحديد طبقة المستويات:

- داخل الحلقة، تحقق مما إذا كانت الطبقة الحالية (`im.getLayers()[i]` ) هو مثال على`LevelsLayer` الطبقة باستخدام`instanceof` مشغل. 
-  إذا كان الأمر كذلك، فقم بإلقاء الطبقة على أ`LevelsLayer` كائن لمزيد من التلاعب.

```java
for (int i = 0; i < im.getLayers().length; i++) {
   if (im.getLayers()[i] instanceof LevelsLayer) {
	   LevelsLayer levelsLayer = (LevelsLayer) im.getLayers()[i];
	   // ... (ستتم إضافة كود ضبط المستويات هنا)
   }
}
```
## الخطوة 5: مستويات الضبط الدقيق (تابع):

-  اضبط مستويات الإخراج باستخدام`setOutputShadowLevel` و`setOutputHighlightLevel` للتحكم في عتمة وخفة الصورة الناتجة. تحدد هذه القيم نطاق مستويات الإدخال التي سيتم تعيينها إلى نطاق الإخراج.

```java
for (int i = 0; i < im.getLayers().length; i++) {
   if (im.getLayers()[i] instanceof LevelsLayer) {
	   LevelsLayer levelsLayer = (LevelsLayer) im.getLayers()[i];
	   LevelChannel channel = levelsLayer.getChannel(0);

	   // ضبط مستويات الإدخال (0-255):
	   channel.setInputShadowLevel((short) 10); // أغمق الظلال قليلاً
	   channel.setInputMidtoneLevel(2.0f);     // زيادة الدرجات اللونية النصفية
	   channel.setInputHighlightLevel((short) 230); // تقليل النقاط البارزة

	   // ضبط مستويات الإخراج (0-255):
	   channel.setOutputShadowLevel((short) 20); // أغمق الظلال أكثر
	   channel.setOutputHighlightLevel((short) 200); //سطع الضوء
   }
}
```

## الخطوة 6: حفظ ملف PSD المعدل:

-  استخدم`save` طريقة`PsdImage` كائن لحفظ الصورة المعدلة في المسار المحدد (`psdPathAfterChange`).

```java
im.save(psdPathAfterChange);
```

## الخطوة 7: التصدير بصيغة PNG (اختياري):

-  إذا كنت بحاجة إلى إصدار PNG من الصورة المعدلة، فقم بإنشاء ملف`PngOptions` كائن وتعيين نوع اللون ل`TruecolorWithAlpha` . ثم استخدم`save` الطريقة مرة أخرى باستخدام مسار وخيارات تصدير PNG.

```java
PngOptions saveOptions = new PngOptions();
saveOptions.setColorType(PngColorType.TruecolorWithAlpha);
im.save(pngExportPath, saveOptions);
```

وهنا لديك! لقد نجحت في ضبط طبقة ضبط المستويات في ملف PSD الخاص بك باستخدام Aspose.PSD لـ Java. من خلال فهم هذه الخطوات وتجربة القيم المختلفة، يمكنك تحسين التباين والمظهر العام لصورك.

## خاتمة

يمكّنك Aspose.PSD for Java من التحكم في عملية تحرير الصور الخاصة بك. من خلال إتقان طبقة ضبط المستويات، يمكنك بث حياة جديدة في صورك وتصميماتك. تذكر أن الممارسة تؤدي إلى الكمال، لذا لا تتردد في تجربة واستكشاف الإمكانات الكاملة لهذه الأداة القوية.
 
## الأسئلة الشائعة

### هل يمكنني ضبط قنوات الألوان الفردية (RGB) بشكل منفصل؟ 
نعم، يمكنك الوصول إلى كل قناة ألوان باستخدام`getChannel` طريقة`LevelsLayer` الكائن وتعديل مستوياته بشكل مستقل.

### كيف يمكنني التعامل مع طبقات ضبط المستويات المتعددة في ملف PSD؟
يتكرر الكود عبر جميع الطبقات، لذلك سيعالج تلقائيًا أي طبقات مستويات إضافية موجودة في الصورة.

### هل هناك طرق أخرى لضبط تباين الصورة إلى جانب المستويات؟
قطعاً! يقدم Aspose.PSD أدوات متنوعة لضبط الصورة مثل Curves وBrightness/Contrast والمزيد.

### هل يمكنني أتمتة هذه العملية لصور متعددة؟ 
نعم، يمكنك دمج هذا الرمز في برنامج نصي للمعالجة الحلقية أو المجمعة لمعالجة ملفات PSD المتعددة بكفاءة.

### أين يمكنني العثور على مزيد من المعلومات والدعم؟
يوفر Aspose وثائق واسعة النطاق ([https://reference.aspose.com/psd/Java/](https://reference.aspose.com/psd/java/)) ومنتدى الدعم ([https://forum.aspose.com/c/psd/34](https://forum.aspose.com/c/psd/34)) لأية أسئلة أو مشاكل قد تواجهها.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
