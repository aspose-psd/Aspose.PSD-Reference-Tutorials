---
date: 2025-12-04
description: تعلم كيفية حفظ ملف PSD كـ PNG وتطبيق ظل إسقاط معروض باستخدام Aspose.PSD
  للغة Java. يغطي هذا الدليل كيفية إضافة الظل، تحويل PSD إلى PNG، وتطبيق ظل الإسقاط
  في Java.
language: ar
linktitle: Apply Rendering Drop Shadow
second_title: Aspose.PSD Java API
title: حفظ ملف PSD كـ PNG وإضافة ظل إسقاط باستخدام Aspose.PSD Java
url: /java/advanced-image-manipulation/rendering-drop-shadow/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# حفظ PSD كـ PNG وإضافة ظل إسقاط باستخدام Aspose.PSD Java

## المقدمة

إذا كنت تعمل مع ملفات Photoshop في Java، فإن **حفظ PSD كـ PNG** مع إضافة ظل إسقاط بمظهر احترافي هو طلب شائع. تجعل Aspose.PSD هذه المهمة سهلة، حيث تتيح لك **تحويل PSD إلى PNG** و**تطبيق ظل إسقاط Java** في بضع أسطر من الشيفرة فقط. في هذا الدرس سنستعرض العملية بالكامل، من تحميل ملف PSD إلى تصدير PNG النهائي مع تأثير الظل المرسوم.

## الإجابات السريعة
- **ماذا يعني “حفظ PSD كـ PNG”؟** إنه يحول ملف Photoshop متعدد الطبقات إلى صورة PNG مسطحة، مع الحفاظ على الشفافية.  
- **هل يمكنني إضافة ظل إسقاط أثناء التحويل؟** نعم—تتيح لك Aspose.PSD تعديل تأثيرات الطبقة قبل التصدير.  
- **هل أحتاج إلى ترخيص لتشغيل الشيفرة؟** النسخة التجريبية المجانية تكفي للتقييم؛ الترخيص مطلوب للإنتاج.  
- **ما نسخة Java المدعومة؟** Java 8 أو أعلى.  
- **هل يمكن تخصيص تأثير ظل الإسقاط؟** بالتأكيد—يمكنك تعديل اللون، الشفافية، المسافة، الحجم، الزاوية، وأكثر.

## المتطلبات المسبقة

قبل أن نبدأ، تأكد من أن لديك:

- **بيئة تطوير Java** – JDK 8 أو أحدث مثبت.  
- **مكتبة Aspose.PSD** – حمّل أحدث JAR من الموقع الرسمي [هنا](https://releases.aspose.com/psd/java/).  
- **ملف PSD** – ملف يحتوي على طبقة واحدة على الأقل تريد تحسينها بظل.

## كيفية حفظ PSD كـ PNG مع ظل إسقاط في Java؟

فيما يلي دليل خطوة بخطوة. كل خطوة تتضمن شرحًا مختصرًا يليه الشيفرة الدقيقة التي تحتاج إلى نسخها.

### الخطوة 1: استيراد الحزم المطلوبة

نبدأ باستيراد الفئات التي توفر تحميل الصور، معالجة التأثيرات، وإمكانيات تصدير PNG.

```java
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.layereffects.DropShadowEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import com.aspose.psd.Color;

import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.imageoptions.PngOptions;
```

### الخطوة 2: تعريف دليل المستند

حدد المجلد الذي سيحتوي على ملف PSD المصدر وملف PNG الناتج.

```java
String dataDir = "Your Document Directory";
```

### الخطوة 3: تعيين مسارات ملفات PSD و PNG

حدد المسارات الكاملة لملف PSD المدخل وملف PNG المخرج.

```java
String sourceFileName = dataDir + "Shadow.psd";
String pngExportPath = dataDir + "Shadowchanged1.png";
```

### الخطوة 4: تحميل ملف PSD مع تمكين التأثيرات

تمكين **loadEffectsResource** يضمن أن تأثيرات الطبقة (مثل الظلال) متاحة للتعديل.

```java
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage) Image.load(sourceFileName, loadOptions);
```

### الخطوة 5: الوصول إلى تأثير ظل الإسقاط

هنا نسترجع أول تأثير مطبق على الطبقة الثانية (الفهرس 1). هذا هو المكان الذي سنقرأ أو نعدل فيه معلمات الظل.

```java
DropShadowEffect shadowEffect = (DropShadowEffect) (im.getLayers()[1].getBlendingOptions().getEffects()[0]);
```

### الخطوة 6: التحقق من خصائص تأثير الظل (اختياري لكن مفيد)

التحقق من الخصائص الحالية يساعدك على تحديد ما إذا كنت بحاجة لتغيير أي شيء. التأكيدات أدناه تؤكد القيم الافتراضية.

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

> **نصيحة احترافية:** إذا كنت تريد **كيفية إضافة ظل** بإعدادات مخصصة، عدّل الخصائص على `shadowEffect` قبل الحفظ (مثال: `shadowEffect.setColor(Color.getRed());`).

### الخطوة 7: حفظ الصورة المعدلة كـ PNG

أخيرًا، نقوم بتصدير PSD (مع الظل المرسوم) إلى ملف PNG. خيار `TruecolorWithAlpha` يحافظ على الشفافية.

```java
PngOptions saveOptions = new PngOptions();
saveOptions.setColorType(PngColorType.TruecolorWithAlpha);
im.save(pngExportPath, saveOptions);
```

وهكذا تحصل على سير عمل كامل **لتحويل PSD إلى PNG** يضيف أيضًا **تطبيق ظل إسقاط Java** في خطوة واحدة.

## لماذا تستخدم Aspose.PSD لهذا المهمة؟

- **لا حاجة لبرنامج Photoshop الأصلي** – يعمل على أي منصة تدعم Java.  
- **دقة PSD كاملة** – جميع معلومات الطبقة، الأقنعة، والتأثيرات محفوظة.  
- **تحكم دقيق** – تعديل كل معلمة من ظل الإسقاط قبل التصدير.  
- **أداء عالي** – مُحسّن للملفات الكبيرة ومعالجة الدُفعات.

## المشكلات الشائعة & استكشاف الأخطاء

| العَرَض | السبب المحتمل | الحل |
|---------|--------------|-----|
| `NullPointerException` على `shadowEffect` | الطبقة المستهدفة لا تحتوي على تأثيرات أو الفهرس غير صحيح. | تحقق من فهرس الطبقة (`im.getLayers()[i]`) وتأكد من وجود تأثير. |
| PNG المُصدَّر فارغ | خيارات PNG غير مضبوطة بشكل صحيح أو الصورة لم تُحفظ. | استخدم `PngColorType.TruecolorWithAlpha` وتأكد من أن مسار `im.save()` قابل للكتابة. |
| لون الظل غير مرئي | تم ضبط شفافية الظل إلى 0 أو اللون يطابق الخلفية. | عيّن `shadowEffect.setOpacity(255);` واختر لونًا متباينًا. |

## الأسئلة المتكررة

**س: هل يمكنني تطبيق ظلال إسقاط على عدة طبقات في آن واحد؟**  
ج: نعم. قم بتكرار `im.getLayers()` وعدّل `DropShadowEffect` لكل طبقة حسب الحاجة.

**س: ماذا يفعل معامل “Spread”؟**  
ج: يتحكم في مدى حدة انتقال الظل من غير شفاف بالكامل إلى شفاف. كلما زاد الـ spread، يصبح الحافة أكثر صلابة.

**س: هل Aspose.PSD متوافق مع جميع إصدارات Photoshop؟**  
ج: يدعم مجموعة واسعة من إصدارات PSD، من الإصدارات القديمة حتى أحدث ملفات Photoshop CC.

**س: كيف يمكنني الحصول على مساعدة إذا واجهت مشاكل؟**  
ج: زر [منتدى Aspose.PSD](https://forum.aspose.com/c/psd/34) للحصول على دعم المجتمع والمساعدة الرسمية.

**س: هل يمكنني تجربة Aspose.PSD قبل الشراء؟**  
ج: بالطبع. حمّل نسخة تجريبية مجانية من [موقع Aspose](https://releases.aspose.com/).

---

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

**آخر تحديث:** 2025-12-04  
**تم الاختبار باستخدام:** Aspose.PSD 24.12 for Java  
**المؤلف:** Aspose  

---