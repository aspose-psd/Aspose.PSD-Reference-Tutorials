---
date: 2026-04-05
description: تعلم كيفية عرض طبقة تعديل التعرض في ملفات PSD باستخدام Aspose.PSD للغة
  Java. دليل خطوة بخطوة مع أمثلة على الشيفرة لتعديل وإضافة طبقات التعرض.
keywords:
- render exposure adjustment layer
- exposure adjustment layer
- Aspose.PSD Java
linktitle: عرض طبقة تعديل التعرض في ملفات PSD - جافا
second_title: Aspose.PSD Java API
title: تصيير طبقة تعديل التعرض في ملفات PSD - جافا
url: /ar/java/psd-layer-management-effects/render-exposure-adjustment-layer-psd/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# عرض طبقة تعديل التعرض في ملفات PSD - Java

## مقدمة

هل تعمل مع ملفات Photoshop PSD وتحتاج إلى **render exposure adjustment layer** برمجيًا؟ سواءً كنت تقوم بتعديل الطبقات الموجودة أو إضافة طبقات جديدة، توفر Aspose.PSD for Java طريقة قوية وبديهية للتعامل مع هذه المهام. في هذا الدليل، سنستعرض كيفية استخدام Aspose.PSD for Java لعرض وتعديل طبقات تعديل التعرض في ملفات PSD. بنهاية هذا الشرح، ستعرف كيفية تعديل إعدادات التعرض في الطبقات الموجودة وإضافة طبقات تعديل تعرض جديدة إلى ملفات PSD الخاصة بك. هيا نبدأ!

## إجابات سريعة

- **ما المكتبة المطلوبة؟** Aspose.PSD for Java
- **هل يمكنني تعديل طبقة تعريض موجودة؟** نعم، يمكنك تغيير التعرض، الإزاحة، وتصحيح جاما.
- **كيف يمكنني إضافة طبقة تعديل تعريض جديدة؟** استخدم `addExposureAdjustmentLayer()` على كائن `PsdImage`.
- **هل يدعم التصدير إلى PNG؟** بالتأكيد – استخدم `PngOptions` لحفظ النتيجة كملف PNG.
- **هل أحتاج إلى ترخيص للاستخدام الإنتاجي؟** يلزم الحصول على ترخيص تجاري للاستخدام الإنتاجي؛ يتوفر نسخة تجريبية مجانية.

## ما هو render exposure adjustment layer؟

طبقة تعديل التعرض هي طبقة Photoshop غير مدمرة تقوم بتغيير السطوع، الإزاحة، وجاما الصورة الأساسية. يعني عرضها تطبيق هذه الإعدادات بحيث يعكس النتيجة البصرية التعديلات، ويمكنك بعد ذلك تصديرها إلى صيغ مثل PNG.

## لماذا نستخدم Aspose.PSD for Java لعرض طبقة تعديل التعرض؟

- **تحكم كامل** – تعديل خصائص الطبقة دون فتح Photoshop.
- **معالجة دفعة** – أتمتة التعديلات عبر العديد من الملفات.
- **متعدد المنصات** – تشغيل على أي نظام يحتوي على JDK.
- **يحافظ على بنية PSD** – إبقاء الطبقات قابلة للتحرير للتعديلات المستقبلية.

## المتطلبات المسبقة

1. **Java Development Kit (JDK)** – على الأقل JDK 8.
2. **Aspose.PSD for Java** – قم بتنزيله من [here](https://releases.aspose.com/psd/java/).
3. **Basic Java knowledge** – يجب أن تكون مرتاحًا مع بنية Java القياسية.
4. **IDE or Text Editor** – IntelliJ IDEA، Eclipse، VS Code، أو أي محرر تفضله.

## استيراد الحزم

أولاً، استورد الفئات المطلوبة من Aspose.PSD:

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.ExposureLayer;
import com.aspose.psd.imageoptions.PngOptions;
```

## كيفية عرض طبقة تعديل التعرض – دليل خطوة بخطوة

### الخطوة 1: تحميل ملف PSD

استبدل `"Your Document Directory"` بالمجلد الذي يحتوي على ملفات PSD الخاصة بك. تُعيد طريقة `Image.load()` كائن `PsdImage` الذي يمنحك وصولًا كاملاً إلى طبقات المستند.

```java
String dataDir = "Your Document Directory";  // Define your document directory
String sourceFileName = dataDir + "ExposureAdjustmentLayer.psd";  // Source PSD file path

PsdImage im = (PsdImage) Image.load(sourceFileName);  // Load the PSD file
```

### الخطوة 2: تعديل طبقة تعديل التعرض الموجودة

تقوم الحلقة بالمرور عبر كل طبقة، وتبحث عن أي `ExposureLayer`، وتحدّث ثلاثتها المعلمات الرئيسية. هذا هو جوهر **rendering the exposure adjustment layer** باستخدام القيم المخصصة الخاصة بك.

```java
for (int i = 0; i < im.getLayers().length; i++) {
    if (im.getLayers()[i] instanceof ExposureLayer) {
        ExposureLayer expLayer = (ExposureLayer) im.getLayers()[i];
        expLayer.setExposure(2);  // Adjust the exposure level
        expLayer.setOffset(-0.25f);  // Set the offset
        expLayer.setGammaCorrection(0.5f);  // Adjust the gamma correction
    }
}
```

### الخطوة 3: حفظ ملف PSD المعدل

يحافظ ملف PSD المعدل على جميع الطبقات الأصلية دون تغيير، لكن تعديل التعرض الآن يعكس الإعدادات الجديدة.

```java
String psdPathAfterChange = dataDir + "ExposureAdjustmentLayerChanged.psd";  // Path to save the modified PSD file

im.save(psdPathAfterChange);  // Save the changes to the PSD file
```

### الخطوة 4: تصدير النتيجة كـ PNG

استخدام `PngOptions` مع `TruecolorWithAlpha` يضمن أن PNG المُصدَّر يحتفظ بعمق اللون الكامل وأي شفافية من PSD.

```java
String pngExportPath = dataDir + "ExposureAdjustmentLayerChanged.png";  // Path to save the PNG file

PngOptions saveOptions = new PngOptions();  // Create PNG options
saveOptions.setColorType(PngColorType.TruecolorWithAlpha);  // Set color type to Truecolor with Alpha

im.save(pngExportPath, saveOptions);  // Save as PNG
```

### الخطوة 5: إضافة طبقة تعديل تعرض جديدة

إذا كنت بحاجة إلى **add a new exposure adjustment layer** إلى مستند موجود، استخدم الشيفرة التالية:

```java
String sourceFileName = dataDir + "PhotoExample.psd";  // Source PSD file path

PsdImage img = (PsdImage) Image.load(sourceFileName);  // Load the PSD file

ExposureLayer newLayer = img.addExposureAdjustmentLayer(2, -0.25f, 2f);  // Add new exposure adjustment layer

String psdPathAfterChange = dataDir + "PhotoExampleAddedExposure.psd";  // Path to save the modified PSD file
String pngExportPath = dataDir + "PhotoExampleAddedExposure.png";  // Path to save the PNG file

img.save(psdPathAfterChange);  // Save the changes to the PSD file

PngOptions options = new PngOptions();  // Create PNG options
options.setColorType(PngColorType.TruecolorWithAlpha);  // Set color type to Truecolor with Alpha

img.save(pngExportPath, options);  // Save as PNG
```

## المشكلات الشائعة والنصائح

- **Layer not found** – تأكد من أن PSD يحتوي فعليًا على `ExposureLayer`. استخدم `instanceof ExposureLayer` كما هو موضح لتجنب `ClassCastException`.
- **File path errors** – استخدم مسارات مطلقة أو تحقق من أن `dataDir` ينتهي بفاصل ملفات (`/` أو `\`).
- **License exception** – تشغيل البرنامج بدون ترخيص صالح سيضيف علامة مائية إلى الناتج. سجِّل ترخيصك مبكرًا في الشيفرة (`License license = new License(); license.setLicense("Aspose.PSD.lic");`).

## الأسئلة المتكررة

### ما هو Aspose.PSD for Java؟

Aspose.PSD for Java هي مكتبة تتيح لك إنشاء وتعديل وتحويل ملفات PSD برمجيًا باستخدام Java. توفر وظائف شاملة للعمل مع مستندات Photoshop.

### هل يمكنني استخدام Aspose.PSD for Java للتعامل مع أنواع أخرى من الطبقات؟

نعم، يدعم Aspose.PSD for Java أنواعًا مختلفة من الطبقات، بما في ذلك طبقات النص، طبقات التعديل، وطبقات الصورة، مما يتيح تعديلًا واسعًا لملفات PSD.

### كيف أبدأ باستخدام Aspose.PSD for Java؟

يمكنك البدء بتنزيل المكتبة من [website](https://releases.aspose.com/psd/java/) والاطلاع على [documentation](https://reference.aspose.com/psd/java/) للحصول على أدلة مفصلة وأمثلة.

### هل تتوفر نسخة تجريبية مجانية لـ Aspose.PSD for Java؟

نعم، تتوفر نسخة تجريبية مجانية. يمكنك تنزيلها من [here](https://releases.aspose.com/).

### كيف يمكنني الحصول على الدعم لـ Aspose.PSD for Java؟

للحصول على الدعم، يمكنك زيارة [Aspose support forum](https://forum.aspose.com/c/psd/34) حيث يمكنك طرح الأسئلة والحصول على مساعدة من المجتمع.

**أسئلة إضافية**

**س: هل يمكنني معالجة دفعة من ملفات PSD متعددة؟**  
ج: بالتأكيد. ضع منطق التحميل، التعديل، والحفظ داخل حلقة تتكرر على قائمة مسارات الملفات.

**س: هل تحتفظ المكتبة بهيكل الطبقات عند إضافة طبقة تعريض جديدة؟**  
ج: نعم. تُضاف الطبقة الجديدة فوق الطبقات الموجودة، مع الحفاظ على الهيكل الأصلي.

**س: ما هي صيغ الصور التي يمكنني التصدير إليها بخلاف PNG؟**  
ج: يدعم Aspose.PSD صيغ JPEG، BMP، TIFF، والعديد من الصيغ الأخرى عبر الفئات المقابلة `*Options`.

---

**آخر تحديث:** 2026-04-05  
**تم الاختبار مع:** Aspose.PSD for Java 24.10  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}