---
date: 2026-04-22
description: تعلم كيفية حفظ ملف PSD كـ PNG، وتصدير PNG مع قناة ألفا، وإضافة طبقة ظل
  إسقاط باستخدام Aspose.PSD للغة Java – دليل كامل خطوة بخطوة.
keywords:
- save psd as png
- convert psd to png
- export png with alpha
- batch psd to png
- preserve png transparency
linktitle: تطبيق ظل الإسقاط في التصيير
second_title: Aspose.PSD Java API
title: حفظ ملف PSD كـ PNG وتطبيق ظل الإسقاط في Aspose.PSD للـ Java
url: /ar/java/advanced-image-manipulation/rendering-drop-shadow/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# حفظ PSD كـ PNG وتطبيق ظل إسقاط التقديم في Aspose.PSD للـ Java

## مقدمة

إذا كنت تعمل مع ملفات Photoshop في Java، فإن **حفظ PSD كـ PNG** هو أحد أكثر المهام شيوعًا التي ستواجهها. في العديد من المشاريع ستحتاج إلى **save psd as png** لتسليم الأصول إلى الويب أو تطبيقات الهواتف المحمولة، مع الحفاظ على الشفافية والتأثيرات البصرية. باستخدام Aspose.PSD يمكنك ليس فقط **convert PSD to PNG** بل أيضًا تحسين الصورة عن طريق **adding a drop shadow layer**. في هذا الدرس سنستعرض العملية بالكامل—تحميل PSD، تطبيق ظل إسقاط مرفق، وأخيرًا **saving the PSD as a PNG** file—حتى تتمكن من دمج سير العمل في مشاريعك بثقة.

## إجابات سريعة
- **ما المكتبة التي تتعامل مع تحويل PSD إلى PNG؟** Aspose.PSD for Java.  
- **كم من الوقت يستغرق تنفيذ ظل الإسقاط؟** حوالي 10‑15 دقيقة لمثال أساسي.  
- **هل أحتاج إلى ترخيص لتشغيل الكود؟** نسخة تجريبية مجانية تكفي للتقييم؛ الترخيص مطلوب للإنتاج.  
- **هل يمكنني تطبيق الظل على طبقات متعددة؟** نعم—فقط قم بالتكرار عبر الطبقات المطلوبة، وهذا يتيح لك أيضًا إجراء تحويل دفعة من PSD إلى PNG.  
- **ما نسخة Java المطلوبة؟** Java 8 أو أعلى.

## ما هو “حفظ PSD كـ PNG” ولماذا هو مهم؟

**حفظ PSD كـ PNG** ينتج صورة غير مضغوطة مدعومة على نطاق واسع تحتفظ بالشفافية. هذا أمر أساسي عندما تحتاج إلى عرض أصول Photoshop على الويب، في تطبيقات الهواتف المحمولة، أو كجزء من خط أنابيب معالجة صور أكبر. إضافة ظل إسقاط في الوقت نفسه يتيح لك إنتاج تأثير بصري مصقول دون الحاجة لفتح Photoshop.

## لماذا نستخدم Aspose.PSD لهذا سير العمل؟

* **تحكم كامل من الكود** – لا حاجة لتشغيل Photoshop أو الاعتماد على أدوات خارجية.  
* **يحافظ على تأثيرات الطبقة** – ظلال الإسقاط، التوهجات، وغيرها من التأثيرات تُعرض تمامًا كما تظهر في الملف الأصلي.  
* **تصدير PNG مع قناة ألفا** – ناتج PNG يحتفظ بالخلفية الشفافة، مما يضمن **الحفاظ على شفافية PNG** للاستخدام في واجهة المستخدم أو الويب.  
* **متعدد المنصات** – يعمل على أي نظام تشغيل يدعم Java 8+.

## المتطلبات المسبقة

- **بيئة تطوير Java** – JDK 8 أو أحدث مثبت.  
- **Aspose.PSD للـ Java** – حمّل أحدث JAR من [Aspose.PSD download page](https://releases.aspose.com/psd/java/).  
- **ملف PSD** – يجب أن يحتوي الملف على طبقة واحدة على الأقل تريد تحسينها بظل إسقاط (مثال: *Shadow.psd*).  

## استيراد الحزم

أولاً، استورد الفئات التي سنحتاجها. هذا يمنحنا الوصول إلى تحميل الصور، تأثيرات الطبقات، وخيارات تصدير PNG.

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

### الخطوة 1: تحديد دليل المستند  
أخبر البرنامج بمكان وجود ملف PSD المصدر.

```java
String dataDir = "Your Document Directory";
```

### الخطوة 2: تعيين مسارات ملفات PSD و PNG  
حدد كلًا من PSD الإدخالي و PNG الناتج الذي سيحتوي على ظل الإسقاط المرسوم.

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
احصل على أول تأثير ظل إسقاط من الطبقة الثانية (الفهرس 1). هذا هو المكان الذي سنتحقق فيه من المعلمات أو نعدّلها.

```java
DropShadowEffect shadowEffect = (DropShadowEffect) (im.getLayers()[1].getBlendingOptions().getEffects()[0]);
```

### الخطوة 5: التحقق من خصائص تأثير الظل  
تأكد من أن خصائص التأثير تتطابق مع ما تتوقعه قبل الحفظ. يمكنك أيضًا تعديل هذه القيم للحصول على مظهر مختلف.

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
صدّر الصورة المعدلة إلى PNG، مع الحفاظ على قناة ألفا بحيث يندمج الظل بشكل صحيح.

```java
PngOptions saveOptions = new PngOptions();
saveOptions.setColorType(PngColorType.TruecolorWithAlpha);
im.save(pngExportPath, saveOptions);
```

في هذه المرحلة، لقد نجحت في **تحويل PSD إلى PNG**، **تصدير PNG مع ألفا**، وتطبيق ظل إسقاط مرفّق في سير عمل واحد.

## تصدير PNG مع شفافية ألفا

عندما تحتاج إلى أن يحتفظ ناتج PNG بخلفيته الشفافة—خاصةً لتراكبات واجهة المستخدم أو رسومات الويب—تأكد من استخدام `PngColorType.TruecolorWithAlpha` كما هو موضح في خطوة الحفظ أعلاه. هذا يضمن أن ظل الإسقاط يجلس على لوحة شفافة بدلاً من خلفية صلبة، مما يساعدك على **الحفاظ على شفافية PNG**.

## إضافة طبقة ظل إسقاط باستخدام Java

إذا كان PSD الخاص بك يحتوي على طبقات متعددة تحتاج إلى ظلال، ببساطة كرّر **الخطوة 4** و**الخطوة 5** داخل حلقة تتكرر على `im.getLayers()`. كل تكرار يمكنه إنشاء أو تعديل كائن `DropShadowEffect`، مما يمنحك تحكمًا دقيقًا في الشفافية، المسافة، الحجم، والزاوية لكل طبقة. هذا النهج يتيح أيضًا **batch psd to png** حيث يحصل كل ملف على نفس معالجة الظل.

## حالات الاستخدام الشائعة لحفظ PSD كـ PNG

* **سلاسل أصول الويب** – تحويل ملفات PSD المقدمة من المصمم إلى PNG جاهزة للويب مع ظلال مدمجة.  
* **موارد تطبيقات الجوال** – إنشاء أيقونات PNG شفافة مباشرةً، لتجنب التصدير اليدوي.  
* **معالجة دفعات** – أتمتة تحويل مئات ملفات PSD في مهمة على الخادم، مع ضمان احتفاظ كل PNG بقناة ألفا وتأثيراته البصرية.  

## المشكلات الشائعة والحلول

| المشكلة | السبب المحتمل | الحل |
|-------|--------------|-----|
| **Shadow not visible** | `Opacity` set to 0 or layer is hidden | Verify `shadowEffect.getOpacity()` > 0 and layer visibility. |
| **PNG appears flat (no transparency)** | Wrong `PngColorType` used | Use `PngColorType.TruecolorWithAlpha` as shown. |
| **Exception on loading** | Effects not loaded | Ensure `loadOptions.setLoadEffectsResource(true)` is called. |
| **Incorrect layer index** | PSD structure differs | Inspect `im.getLayers()` and pick the correct index. |

## الأسئلة المتكررة

**س: هل يمكنني تطبيق ظلال إسقاط على طبقات متعددة في آن واحد؟**  
ج: نعم. قم بالتكرار عبر `im.getLayers()` وأضف أو عدل `DropShadowEffect` لكل طبقة مستهدفة، مما يتيح لك أيضًا إجراء تحويل دفعة من PSD إلى PNG.

**س: ما الذي يتحكم فيه معامل “Spread”؟**  
ج: `Spread` يحدد مدى حدة انتقال الظل من الشفافية الكاملة إلى الشفافية. قيمة أعلى تُنتج حافة أكثر صلابة.

**س: هل Aspose.PSD متوافق مع جميع إصدارات Photoshop؟**  
ج: Aspose.PSD يدعم ملفات PSD من Photoshop 3.0 حتى أحدث إصدار، مع معالجة معظم أنواع الطبقات والتأثيرات.

**س: كيف يمكنني اختبار الكود قبل شراء الترخيص؟**  
ج: حمّل النسخة التجريبية المجانية من [Aspose.PSD download page](https://releases.aspose.com/psd/java/) وشغّل العينة دون مفتاح ترخيص.

**س: أين يمكنني الحصول على مساعدة إذا واجهت مشاكل؟**  
ج: انشر سؤالك على [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) حيث يمكن للمجتمع ومهندسي Aspose المساعدة.

## الخلاصة

أنت الآن تعرف كيف **save psd as png**، **export PNG with alpha**، **convert PSD to PNG**، و**apply a drop shadow layer** باستخدام Aspose.PSD للـ Java. يتيح لك هذا الجمع أتمتة إعداد صور عالية الجودة للويب، الهواتف المحمولة، أو تطبيقات سطح المكتب—دون الحاجة لفتح Photoshop أبداً.

---

**Last Updated:** 2026-04-22  
**Tested With:** Aspose.PSD 24.11 for Java  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}