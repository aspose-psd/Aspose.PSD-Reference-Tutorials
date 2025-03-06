---
title: عرض طبقة ضبط التعريض في ملفات PSD - Java
linktitle: عرض طبقة ضبط التعريض في ملفات PSD - Java
second_title: Aspose.PSD جافا API
description: تعرف على كيفية عرض طبقات التعريض وضبطها في ملفات PSD باستخدام Aspose.PSD لـ Java. دليل خطوة بخطوة مع أمثلة التعليمات البرمجية لتعديل طبقات التعريض وإضافتها.
weight: 15
url: /ar/java/psd-layer-management-effects/render-exposure-adjustment-layer-psd/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# عرض طبقة ضبط التعريض في ملفات PSD - Java

## مقدمة

هل تعمل باستخدام ملفات Photoshop PSD وتحتاج إلى ضبط التعريض الضوئي أو إضافة طبقة ضبط التعريض برمجيًا؟ سواء كنت تقوم بتعديل الطبقات الموجودة أو إضافة طبقات جديدة، فإن Aspose.PSD for Java يوفر طريقة قوية وبديهية للتعامل مع هذه المهام. في هذا الدليل، سنتعرف على كيفية استخدام Aspose.PSD لـ Java لعرض طبقات ضبط التعريض الضوئي وتعديلها في ملفات PSD. بنهاية هذا البرنامج التعليمي، ستعرف كيفية ضبط إعدادات التعريض الضوئي في الطبقات الموجودة وإضافة طبقات ضبط التعريض الجديدة إلى ملفات PSD الخاصة بك. دعونا الغوص في!

## المتطلبات الأساسية

قبل أن ننتقل إلى البرنامج التعليمي، تأكد من أن لديك المتطلبات الأساسية التالية:

1. Java Development Kit (JDK): تحتاج إلى تثبيت JDK على جهازك. يفترض هذا الدليل أن لديك JDK 8 على الأقل.
2.  Aspose.PSD لـ Java: أنت بحاجة إلى مكتبة Aspose.PSD للعمل مع ملفات PSD. يمكنك تنزيله من[هنا](https://releases.aspose.com/psd/java/).
3. المعرفة الأساسية بـ Java: الإلمام ببرمجة Java سيساعدك على المتابعة بسهولة.
4. IDE أو محرر النصوص: استخدم أي IDE مثل IntelliJ IDEA أو Eclipse أو محرر نصوص من اختيارك لكتابة كود Java وتشغيله.

## حزم الاستيراد

أول الأشياء أولاً، لنستورد الحزم الضرورية من Aspose.PSD لـ Java. تضمن هذه الخطوة أن الكود الخاص بنا يمكنه الاستفادة من ميزات المكتبة لمعالجة ملفات PSD.

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.ExposureLayer;
import com.aspose.psd.imageoptions.PngOptions;
```

## الخطوة 1: قم بتحميل ملف PSD

للبدء، تحتاج إلى تحميل ملف PSD الخاص بك في التطبيق. وإليك كيف يمكنك القيام بذلك:

```java
String dataDir = "Your Document Directory";  // حدد دليل المستندات الخاص بك
String sourceFileName = dataDir + "ExposureAdjustmentLayer.psd";  // مسار ملف PSD المصدر

PsdImage im = (PsdImage) Image.load(sourceFileName);  // قم بتحميل ملف PSD
```

 في مقتطف الشفرة هذا، استبدل`"Your Document Directory"` بالمسار الذي توجد به ملفات PSD الخاصة بك. ال`Image.load()` تقوم الطريقة بتحميل ملف PSD إلى مثيل`PsdImage`، والذي يسمح لك بمعالجة طبقاته.

## الخطوة 2: تحرير طبقة ضبط التعريض الموجودة

بمجرد تحميل ملف PSD، يمكنك الوصول إلى الطبقات الموجودة وتعديلها. إذا كان الملف يحتوي على طبقة ضبط التعرض، فيمكنك ضبط خصائصه:

```java
for (int i = 0; i < im.getLayers().length; i++) {
    if (im.getLayers()[i] instanceof ExposureLayer) {
        ExposureLayer expLayer = (ExposureLayer) im.getLayers()[i];
        expLayer.setExposure(2);  // اضبط مستوى التعرض
        expLayer.setOffset(-0.25f);  // تعيين الإزاحة
        expLayer.setGammaCorrection(0.5f);  // ضبط تصحيح جاما
    }
}
```

في هذه الحلقة، نقوم بالتكرار على جميع طبقات ملف PSD. إذا وجدنا أ`ExposureLayer` ، نقوم بتعديله`Exposure`, `Offset` ، و`GammaCorrection` ملكيات. يتيح لك ذلك ضبط الإخراج المرئي لطبقة ضبط التعريض الضوئي.

## الخطوة 3: احفظ ملف PSD المعدل

بعد إجراء التغييرات، تحتاج إلى حفظ ملف PSD المحدث:

```java
String psdPathAfterChange = dataDir + "ExposureAdjustmentLayerChanged.psd";  // المسار لحفظ ملف PSD المعدل

im.save(psdPathAfterChange);  // احفظ التغييرات في ملف PSD
```

يحفظ هذا السطر ملف PSD المعدل في المسار المحدد، مع الحفاظ على تعديلات التعريض الضوئي.

## الخطوة 4: التصدير بصيغة PNG

لتصدير ملف PSD المحدث بصيغة PNG، اتبع الخطوات التالية:

```java
String pngExportPath = dataDir + "ExposureAdjustmentLayerChanged.png";  // المسار لحفظ ملف PNG

PngOptions saveOptions = new PngOptions();  // إنشاء خيارات PNG
saveOptions.setColorType(PngColorType.TruecolorWithAlpha);  // اضبط نوع اللون على Truecolor باستخدام Alpha

im.save(pngExportPath, saveOptions);  // حفظ بصيغة PNG
```

 هنا،`PngOptions` يُستخدم لتكوين إعدادات تصدير PNG.`PngColorType.TruecolorWithAlpha` يضمن أن ملف PNG يحتفظ بعمق الألوان والشفافية.

## الخطوة 5: إضافة طبقة ضبط التعرض الجديدة

إذا كنت تريد إضافة طبقة ضبط تعريض جديدة إلى ملف PSD موجود، فيمكنك القيام بذلك باستخدام الكود التالي:

```java
String sourceFileName = dataDir + "PhotoExample.psd";  // مسار ملف PSD المصدر

PsdImage img = (PsdImage) Image.load(sourceFileName);  // قم بتحميل ملف PSD

ExposureLayer newLayer = img.addExposureAdjustmentLayer(2, -0.25f, 2f);  // أضف طبقة ضبط التعرض الجديدة

String psdPathAfterChange = dataDir + "PhotoExampleAddedExposure.psd";  // المسار لحفظ ملف PSD المعدل
String pngExportPath = dataDir + "PhotoExampleAddedExposure.png";  // المسار لحفظ ملف PNG

img.save(psdPathAfterChange);  // احفظ التغييرات في ملف PSD

PngOptions options = new PngOptions();  // إنشاء خيارات PNG
options.setColorType(PngColorType.TruecolorWithAlpha);  // اضبط نوع اللون على Truecolor باستخدام Alpha

img.save(pngExportPath, options);  // حفظ بصيغة PNG
```

في هذه الخطوة، تتم إضافة طبقة ضبط تعريض جديدة إلى ملف PSD بقيم التعريض والإزاحة وتصحيح جاما المحددة. يتم بعد ذلك حفظ ملفات PSD وPNG المحدثة.

## خاتمة

وهنا لديك! لقد تعلمت كيفية عرض طبقات التعريض وضبطها في ملفات PSD باستخدام Aspose.PSD لـ Java. لقد تناولنا كيفية تعديل طبقات التعريض الموجودة وإضافة طبقات جديدة وتصدير عملك كملفات PNG. سواء كنت تقوم بتعديل الصور أو إعداد أصول التصميم، فإن هذه المهارات ستعزز قدرتك على إدارة ملفات PSD برمجيًا. ترميز سعيد!

## الأسئلة الشائعة

### ما هو Aspose.PSD لجافا؟

Aspose.PSD for Java هي مكتبة تتيح لك إنشاء ملفات PSD وتحريرها وتحويلها برمجيًا باستخدام Java. يوفر وظائف شاملة للعمل مع مستندات Photoshop.

### هل يمكنني استخدام Aspose.PSD لـ Java لمعالجة أنواع أخرى من الطبقات؟

نعم، يدعم Aspose.PSD for Java أنواعًا مختلفة من الطبقات، بما في ذلك طبقات النص وطبقات الضبط وطبقات الصور، مما يسمح بمعالجة واسعة النطاق لملفات PSD.

### كيف أبدأ باستخدام Aspose.PSD لـ Java؟

 يمكنك البدء بتنزيل المكتبة من[موقع إلكتروني](https://releases.aspose.com/psd/java/) والإشارة إلى[الوثائق](https://reference.aspose.com/psd/java/) للحصول على أدلة وأمثلة مفصلة.

### هل هناك نسخة تجريبية مجانية متاحة لـ Aspose.PSD لـ Java؟

 نعم، تتوفر نسخة تجريبية مجانية. يمكنك تنزيله[هنا](https://releases.aspose.com/).

### كيف يمكنني الحصول على الدعم لـ Aspose.PSD لـ Java؟

 للحصول على الدعم، يمكنك زيارة[Aspose منتدى الدعم](https://forum.aspose.com/c/psd/34) حيث يمكنك طرح الأسئلة والحصول على المساعدة من المجتمع.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
