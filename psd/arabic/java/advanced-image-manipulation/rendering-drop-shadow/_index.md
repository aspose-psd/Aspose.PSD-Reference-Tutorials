---
date: 2025-12-05
description: تعلم كيفية حفظ ملف PSD كـ PNG، وتحويل PSD إلى PNG، وتطبيق طبقة ظل إسقاط
  باستخدام Aspose.PSD للغة Java – دليل كامل خطوة بخطوة.
language: ar
linktitle: Apply Rendering Drop Shadow
second_title: Aspose.PSD Java API
title: حفظ ملف PSD كـ PNG وتطبيق ظل الإسقاط أثناء العرض في Aspose.PSD للـ Java
url: /java/advanced-image-manipulation/rendering-drop-shadow/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# حفظ ملف PSD كـ PNG وتطبيق ظل إسقاط في Aspose.PSD للـ Java

## المقدمة

إذا كنت تعمل مع ملفات Photoshop في Java، فإن **حفظ PSD كـ PNG** هو أحد أكثر المهام شيوعًا التي ستواجهها. باستخدام Aspose.PSD يمكنك ليس فقط **تحويل PSD إلى PNG** بل أيضًا تحسين الصورة عن طريق **إضافة طبقة ظل إسقاط**. في هذا البرنامج التعليمي سنستعرض العملية بالكامل—تحميل ملف PSD، تطبيق ظل إسقاط أثناء العرض، وأخيرًا **حفظ PSD كملف PNG**—حتى تتمكن من دمج سير العمل في مشاريعك بثقة.

## إجابات سريعة
- **ما المكتبة التي تتعامل مع تحويل PSD إلى PNG؟** Aspose.PSD للـ Java.  
- **كم من الوقت يستغرق تنفيذ الظل الإسقاط؟** حوالي 10‑15 دقيقة لمثال أساسي.  
- **هل أحتاج إلى ترخيص لتشغيل الكود؟** النسخة التجريبية المجانية تكفي للتقييم؛ الترخيص مطلوب للإنتاج.  
- **هل يمكنني تطبيق الظل على طبقات متعددة؟** نعم—فقط قم بالتكرار عبر الطبقات المطلوبة.  
- **ما نسخة Java المطلوبة؟** Java 8 أو أعلى.

## ما هو “حفظ PSD كـ PNG” ولماذا هو مهم؟

إن حفظ PSD كـ PNG ينتج صورة غير مضغوطة تدعم الشفافية وتُعَدّ واسعة الانتشار. هذا أمر أساسي عندما تحتاج إلى عرض موارد Photoshop على الويب، في تطبيقات الهواتف المحمولة، أو كجزء من خط معالجة صور أكبر. إضافة ظل إسقاط في الوقت نفسه يتيح لك إنتاج تأثير بصري مصقول دون الحاجة لفتح Photoshop.

## المتطلبات المسبقة

قبل أن نبدأ، تأكد من وجود ما يلي:

- **بيئة تطوير Java** – JDK 8 أو أحدث مثبتة.  
- **Aspose.PSD للـ Java** – حمّل أحدث ملف JAR من [صفحة تنزيل Aspose.PSD](https://releases.aspose.com/psd/java/).  
- **ملف PSD** – يجب أن يحتوي الملف على طبقة واحدة على الأقل تريد تحسينها بظل إسقاط (مثال: *Shadow.psd*).  

## استيراد الحزم

أولاً، استورد الفئات التي سنحتاجها. سيوفر لك ذلك إمكانية تحميل الصور، تأثيرات الطبقات، وخيارات تصدير PNG.

```java
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.layereffects.DropShadowEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import com.aspose.psd.Color;

import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.imageoptions.PngOptions;
```

## دليل خطوة بخطوة

### الخطوة 1: تعريف دليل المستند  
أخبر البرنامج بمكان وجود ملف PSD المصدر.

```java
String dataDir = "Your Document Directory";
```

### الخطوة 2: تعيين مسارات ملفات PSD و PNG  
حدد كلًا من ملف PSD المدخل وملف PNG الناتج الذي سيحتوي على ظل الإسقاط المرسوم.

```java
String sourceFileName = dataDir + "Shadow.psd";
String pngExportPath = dataDir + "Shadowchanged1.png";
```

### الخطوة 3: تحميل ملف PSD مع التأثيرات  
فعّل تحميل موارد التأثير حتى نتمكن من تعديل تأثير ظل الإسقاط.

```java
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage) Image.load(sourceFileName, loadOptions);
```

### الخطوة 4: الوصول إلى تأثير ظل الإسقاط  
احصل على أول تأثير ظل إسقاط من الطبقة الثانية (الفهرس 1). هنا سنتحقق من المعلمات أو نعدلها.

```java
DropShadowEffect shadowEffect = (DropShadowEffect) (im.getLayers()[1].getBlendingOptions().getEffects()[0]);
```

### الخطوة 5: التحقق من خصائص تأثير الظل  
تأكد من أن خصائص التأثير تتطابق مع توقعاتك قبل الحفظ. يمكنك أيضًا تعديل هذه القيم للحصول على مظهر مختلف.

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

> **نصيحة احترافية:** اضبط `setSpread()` أو `setNoise()` لإنشاء ظلال أكثر نعومة أو بنسيج مختلف.

### الخطوة 6: حفظ كـ PNG – خطوة “حفظ PSD كـ PNG”  
صدّر الصورة المعدلة إلى PNG، مع الحفاظ على قناة ألفا حتى يندمج الظل بشكل صحيح.

```java
PngOptions saveOptions = new PngOptions();
saveOptions.setColorType(PngColorType.TruecolorWithAlpha);
im.save(pngExportPath, saveOptions);
```

في هذه المرحلة تكون قد نجحت في **تحويل PSD إلى PNG** وتطبيق ظل إسقاط في سير عمل واحد.

## المشكلات الشائعة والحلول

| المشكلة | السبب المحتمل | الحل |
|-------|--------------|-----|
| **الظل غير ظاهر** | تم ضبط `Opacity` على 0 أو الطبقة مخفية | تحقق من أن `shadowEffect.getOpacity()` > 0 وأن الطبقة مرئية. |
| **PNG يظهر مسطحًا (بدون شفافية)** | تم استخدام `PngColorType` غير صحيح | استخدم `PngColorType.TruecolorWithAlpha` كما هو موضح. |
| **استثناء عند التحميل** | لم يتم تحميل التأثيرات | تأكد من استدعاء `loadOptions.setLoadEffectsResource(true)`. |
| **فهرس الطبقة غير صحيح** | بنية PSD مختلفة | افحص `im.getLayers()` واختر الفهرس المناسب. |

## الأسئلة المتكررة

**س: هل يمكنني تطبيق ظلال إسقاط على طبقات متعددة في آنٍ واحد؟**  
ج: نعم. قم بالتكرار عبر `im.getLayers()` وأضف أو عدّل `DropShadowEffect` لكل طبقة مستهدفة.

**س: ما الذي يتحكم فيه معامل “Spread”؟**  
ج: `Spread` يحدد مدى حدة الانتقال بين الشفافية الكاملة والشفافية. القيمة الأعلى تنتج حافة أكثر صلابة.

**س: هل Aspose.PSD متوافق مع جميع إصدارات Photoshop؟**  
ج: يدعم Aspose.PSD ملفات PSD من Photoshop 3.0 حتى أحدث إصدار، ويتعامل مع معظم أنواع الطبقات والتأثيرات.

**س: كيف يمكنني اختبار الكود قبل شراء الترخيص؟**  
ج: حمّل النسخة التجريبية المجانية من [صفحة تنزيل Aspose.PSD](https://releases.aspose.com/psd/java/) وشغّل العينة دون مفتاح ترخيص.

**س: أين يمكنني الحصول على المساعدة إذا واجهت مشاكل؟**  
ج: انشر سؤالك على [منتدى Aspose.PSD](https://forum.aspose.com/c/psd/34) حيث يمكن للمجتمع ومهندسي Aspose مساعدتك.

## الخاتمة

أنت الآن تعرف كيف **تحفظ PSD كـ PNG**، **تحول PSD إلى PNG**، وت **طبق طبقة ظل إسقاط** باستخدام Aspose.PSD للـ Java. يتيح لك هذا الجمع أتمتة إعداد الصور عالية الجودة للويب، الهواتف المحمولة، أو تطبيقات سطح المكتب—دون الحاجة لفتح Photoshop أبداً.

---

**آخر تحديث:** 2025-12-05  
**تم الاختبار مع:** Aspose.PSD 24.11 للـ Java  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}