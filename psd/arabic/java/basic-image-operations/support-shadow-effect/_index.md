---
date: 2025-12-30
description: تعلم كيفية تغيير لون الظل وتخصيص تأثيرات الظل باستخدام Aspose.PSD للغة
  Java. اتبع هذا الدليل خطوة بخطوة لتأثير الظل.
linktitle: Support Shadow Effect
second_title: Aspose.PSD Java API
title: كيفية تغيير لون الظل باستخدام Aspose.PSD للغة Java
url: /ar/java/basic-image-operations/support-shadow-effect/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# تغيير لون الظل باستخدام Aspose.PSD للـ Java

## المقدمة

إضافة العمق إلى رسوماتك غالبًا ما يعني **تغيير لون الظل** ليتناسب مع مزاج التصميم. باستخدام Aspose.PSD للـ Java يمكنك بسهولة إضافة أو تعديل تأثيرات الظل الساقط، التحكم في الشفافية، وضبط المعلمات الأخرى بدقة — كل ذلك من خلال كود Java. في هذا **الدليل الخاص بتأثير الظل** سنستعرض خطوات تحميل ملف PSD، قراءة الظل الموجود، تخصيص لونه، شفافيته، مسافته، وأخيرًا حفظ الملف المحدث.

## إجابات سريعة
- **ماذا يعني “تغيير لون الظل”؟** يعني تحديث خاصية اللون لتأثير DropShadowEffect المطبق على طبقة PSD.  
- **أي مكتبة تدعم ذلك؟** Aspose.PSD للـ Java توفر دعمًا كاملاً لتأثيرات الظل.  
- **هل أحتاج إلى ترخيص؟** النسخة التجريبية تعمل للتطوير؛ الترخيص التجاري مطلوب للإنتاج.  
- **هل يمكنني ضبط شفافية الظل؟** نعم – استخدم `setOpacity(byte)` لتحديد الشفافية (0‑255).  
- **هل الكود متوافق مع Java 8+؟** بالتأكيد، الـ API تستهدف Java 8 وما بعدها.

## ما هو “تغيير لون الظل” في ملفات PSD؟

تغيير لون الظل ي modifies اللون البصري للظل الساقط الذي يظهر خلف الطبقة. هذا مفيد لإنشاء إضاءة واقعية، مطابقة ألوان العلامة التجارية، أو ببساطة لإضافة لمسة فنية.

## لماذا نستخدم Aspose.PSD للـ Java لتخصيص تأثيرات الظل؟

- **دقة كاملة للـ PSD** – جميع تأثيرات الطبقات، بما فيها الظلال، تُحافظ عليها.  
- **لا حاجة لبرنامج Photoshop** – يمكن معالجة الملفات برمجيًا على أي خادم.  
- **تحكم دقيق** – ضبط اللون، الشفافية، المسافة، الزاوية، الانتشار، والضوضاء.  
- **متعدد المنصات** – يعمل على JVMs في Windows، Linux، و macOS.

## المتطلبات المسبقة

- معرفة أساسية ببرمجة Java.  
- تثبيت Aspose.PSD للـ Java. يمكنك تنزيله [هنا](https://releases.aspose.com/psd/java/).  

## استيراد الحزم

قبل البدء، استورد الفئات المطلوبة لتتمكن من العمل مع الصور وتأثيرات الظل:

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;


import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.layereffects.DropShadowEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
```

## دليل خطوة بخطوة

### الخطوة 1: تحميل صورة PSD

أولًا، حمّل ملف PSD المصدر مع تمكين تحميل موارد التأثير:

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "Shadow.psd";
String psdPathAfterChange = dataDir + "ShadowChanged.psd";

PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);
```

### الخطوة 2: استرجاع تأثير الظل الساقط الموجود

حدد تأثير الظل على الطبقة المطلوبة (في هذا المثال، الطبقة الثانية):

```java
DropShadowEffect shadowEffect = (DropShadowEffect)(im.getLayers()[1].getBlendingOptions().getEffects()[0]);
```

### الخطوة 3: التحقق من الإعدادات الافتراضية (اختياري)

تشغيل هذه التأكيدات يساعدك على فهم القيم الأصلية قبل تعديلها:

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

### الخطوة 4: **تغيير لون الظل** وتخصيص الخصائص الأخرى

الآن نقوم فعليًا **بتغيير لون الظل** إلى الأخضر، وضبط الشفافية، المسافة، الحجم، وغيرها من السمات. هذا يوضح قدرات **تخصيص تأثير الظل** في Aspose.PSD:

```java
shadowEffect.setColor(Color.getGreen());          // change shadow color
shadowEffect.setOpacity((byte)128);               // set shadow opacity (50% transparent)
shadowEffect.setDistance(11);                     // move shadow farther from the object
shadowEffect.setUseGlobalLight(false);            // use local lighting
shadowEffect.setSize(9);                          // adjust blur radius
shadowEffect.setAngle(45);                        // rotate light source
shadowEffect.setSpread(3);                        // increase spread
shadowEffect.setNoise(50);                        // add texture noise
```

### الخطوة 5: حفظ الصورة المعدلة

أخيرًا، اكتب ملف PSD المحدث إلى القرص:

```java
im.save(psdPathAfterChange);
```

## المشكلات الشائعة والنصائح

- **NullPointerException عند استرجاع التأثيرات** – تأكد من استدعاء `setLoadEffectsResource(true)`؛ وإلا لن تُحمَّل التأثيرات.  
- **اللون لا يتغير** – تحقق من أنك تعدل الفهرس الصحيح للطبقة (`im.getLayers()[1]` في هذا المثال).  
- **الشفافية تبدو غير متغيرة** – تذكر أن الشفافية هي بايت (0‑255). يلزم التحويل إلى `(byte)`.  

## الخاتمة

باتباع هذه الخطوات يمكنك **تغيير لون الظل**، **ضبط شفافية الظل**، وتخصيص جميع معلمات **تأثير الظل** في أي ملف PSD باستخدام Aspose.PSD للـ Java. هذا يمكّنك من إنشاء رسومات أغنى برمجيًا دون الحاجة إلى العمل اليدوي في Photoshop.

## الأسئلة المتكررة

**س: هل Aspose.PSD للـ Java مناسب لمشاريع التصميم الجرافيكي الاحترافية؟**  
ج: بالتأكيد! Aspose.PSD للـ Java مكتبة قوية صُممت لمهام التصميم الجرافيكي الاحترافية.

**س: هل يمكنني استخدام Aspose.PSD للـ Java في التطبيقات التجارية؟**  
ج: نعم، Aspose.PSD للـ Java هو منتج تجاري. يمكنك شراؤه [هنا](https://purchase.aspose.com/buy).

**س: هل تتوفر نسخة تجريبية مجانية؟**  
ج: نعم، يمكنك تجربة النسخة التجريبية المجانية [هنا](https://releases.aspose.com/).

**س: أين يمكنني العثور على الوثائق التفصيلية؟**  
ج: راجع الوثائق الشاملة [هنا](https://reference.aspose.com/psd/java/).

**س: كيف يمكنني الحصول على الدعم لـ Aspose.PSD للـ Java؟**  
ج: انضم إلى منتدى المجتمع [هنا](https://forum.aspose.com/c/psd/34) لأي استفسارات دعم.

---

**آخر تحديث:** 2025-12-30  
**تم الاختبار مع:** Aspose.PSD للـ Java 24.10  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}