---
date: 2026-03-13
description: تعلم كيفية إضافة طبقة صبغة وتشبّع إلى ملفات PSD باستخدام Aspose.PSD للغة
  Java. يوضح هذا الدليل أيضًا كيفية معالجة ملفات PSD دفعيًا وإنشاء طبقة تعديل الصبغة
  برمجيًا.
linktitle: Add Hue Saturation Layer to PSD
second_title: Aspose.PSD Java API
title: إضافة طبقة تشبع اللون إلى ملف PSD باستخدام Aspose.PSD للـ Java
url: /ar/java/modifying-converting-psd-images/add-hue-saturation-adjustment-layer-psd/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# إضافة طبقة تشبع اللون إلى PSD

## المقدمة
عند الحديث عن التصميم الجرافيكي، يلعب تعديل الألوان دورًا حيويًا—وبشكل خاص، تعديل الصبغة (Hue)، التشبع (Saturation)، والسطوع (Lightness) يمكن أن يغيّر بشكل جذري مزاج وجودة أي صورة. إحدى الطرق الفعّالة لتحقيق ذلك هي استخدام طبقات الضبط في برنامج فوتوشوب (ملفات PSD). إذا كنت ترغب في **إضافة طبقة تشبع اللون** برمجيًا باستخدام Java، فإن مكتبة Aspose.PSD موجودة لمساعدتك! سيقودك هذا البرنامج التعليمي خلال الخطوات لإضافة طبقة ضبط تشبع اللون إلى ملفات PSD الخاصة بك، مما يجعل سير العمل أكثر إنتاجية وكفاءة.

## إجابات سريعة
- **ما المكتبة التي تسمح لك بإضافة طبقة تشبع اللون في Java؟** Aspose.PSD for Java.  
- **هل أحتاج إلى تثبيت Photoshop؟** لا، المكتبة تعمل بشكل مستقل عن Photoshop.  
- **هل يمكنني معالجة ملفات PSD دفعيًا باستخدام هذه الطريقة؟** نعم—بمجرد أتمتة الخطوات يمكنك تطبيقها على العديد من الملفات.  
- **ما إصدار Java المطلوب؟** JDK 8 أو أحدث.  
- **هل تحتاج إلى ترخيص للاستخدام في الإنتاج؟** نعم، يلزم الحصول على ترخيص تجاري بعد فترة التجربة.

## ما هي عملية “إضافة طبقة تشبع اللون”؟
عملية **إضافة طبقة تشبع اللون** تُنشئ طبقة ضبط غير مدمرة تسمح لك بتعديل قيم الصبغة (Hue)، التشبع (Saturation)، والسطوع (Lightness) دون تغيير بيانات البكسل الأصلية. هذا مثالي لضبط الألوان بدقة عبر التركيبة بأكملها أو نطاقات ألوان محددة.

## لماذا تستخدم Aspose.PSD لـ Java؟
- **عدم الاعتماد على Photoshop** – يعمل على أي منصة تدعم Java.  
- **دقة PSD كاملة** – يحافظ على جميع معلومات الطبقات، الأقنعة، والتأثيرات.  
- **جاهز للمعالجة الدفعية** – يمكنك التكرار عبر المجلدات وتطبيق نفس الضبط على العشرات من الملفات.  
- **مركز على الأداء** – مُحسّن للوثائق الكبيرة والأتمتة على الخادم.

## المتطلبات المسبقة
قبل أن نبدأ في كتابة الكود، تأكد من توفر ما يلي:

1. **مجموعة تطوير Java (JDK):** تأكد من تثبيت JDK 8 أو أعلى على جهازك. يمكنك تنزيله من [Java SE Development Kit Downloads](https://www.oracle.com/java/technologies/javase-downloads.html).  
2. **مكتبة Aspose.PSD لـ Java:** ستحتاج إلى مكتبة Aspose.PSD، والتي يمكنك [تنزيلها هنا](https://releases.aspose.com/psd/java/).  
3. **IDE:** بيئة تطوير متكاملة مناسبة مثل IntelliJ IDEA أو Eclipse لتطوير Java.  
4. **معرفة أساسية بـ Java:** الإلمام ببرمجة Java يُعتبر ميزة، لكن لا تقلق—سنشرح لك كل سطر.

الآن بعد أن رتبنا المتطلبات المسبقة، لننتقل إلى الجزء الممتع—البرمجة!

## استيراد الحزم
لبدء العمل مع مكتبة Aspose.PSD، الخطوة الأولى هي استيراد الفئات اللازمة. إليك كيفية القيام بذلك في ملف Java الخاص بك:

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.HueSaturationLayer;
import com.aspose.psd.fileformats.psd.layers.layerresources.ColorRangeHsl;
```

تأكد من إضافة المكتبات المناسبة إلى مشروعك حتى تعمل هذه الاستيرادات بسلاسة.

## الخطوة 1: إعداد دليل المستندات الخاص بك
كل مشروع يحتاج إلى نقطة بداية، ومشروعنا ليس استثناءً. عليك تحديد دليل تخزين ملفات PSD الخاصة بك. هذا أمر حاسم لتحميل وحفظ الصور بشكل صحيح.

```java
String dataDir = "Your Document Directory"; // Update this path to your actual directory
```

## الخطوة 2: تحميل ملف PSD موجود
للتعامل مع ملف PSD موجود، نحتاج أولاً إلى تحميله إلى برنامجنا. إليك كيفية القيام بذلك:

```java
String sourceFileName = dataDir + "HueSaturationAdjustmentLayer.psd";
PsdImage im = (PsdImage) Image.load(sourceFileName);
```

في هذا الكود، قم بتحديث `"HueSaturationAdjustmentLayer.psd"` إلى اسم ملف PSD الموجود الذي تريد تحريره.

## الخطوة 3: تعديل طبقة الصبغة/التشبع
بعد ذلك، سنقوم بالتكرار عبر طبقات صورة PSD التي تم تحميلها للعثور على أي طبقة صبغة/تشبع موجودة وتعديلها. تتضمن هذه الخطوة تعديل قيم الصبغة، التشبع، والسطوع.

```java
for (int i = 0; i < im.getLayers().length; i++) {
    if (im.getLayers()[i] instanceof HueSaturationLayer) {
        HueSaturationLayer hueLayer = (HueSaturationLayer) im.getLayers()[i];
        hueLayer.setHue((short) -25);
        hueLayer.setSaturation((short) -12);
        hueLayer.setLightness((short) 67);
        ColorRangeHsl colorRange = hueLayer.getRange(2);
        colorRange.setHue((short) -40);
        colorRange.setSaturation((short) 50);
        colorRange.setLightness((short) -20);
        colorRange.setMostLeftBorder((short) 300);
    }
}
```

في هذا المثال:  
- نقوم بضبط الصبغة إلى **-25**، التشبع إلى **-12**، والسطوع إلى **+67**.  
- تسمح طريقة `getRange(2)` لنا بتعديل نطاقات ألوان محددة حسب الرغبة.

## الخطوة 4: حفظ ملف PSD المعدل
بعد إجراء التعديلات، الخطوة التالية هي حفظ الملف. هذه خطوة أساسية في عمليتنا لضمان عدم فقدان التغييرات التي أجريناها.

```java
String psdPathAfterChange = dataDir + "HueSaturationAdjustmentLayerChanged.psd";
im.save(psdPathAfterChange);
```

## الخطوة 5: إضافة طبقة صبغة/تشبع جديدة
إذا كنت بحاجة إلى **إنشاء طبقة ضبط صبغة** من الصفر، يمكنك إضافة طبقة ضبط صبغة/تشبع جديدة إلى ملف PSD آخر. اتبع نمط التحميل نفسه لكن استخدم طريقة `addHueSaturationAdjustmentLayer()`.

```java
sourceFileName = dataDir + "PhotoExample.psd";
PsdImage img = (PsdImage) Image.load(sourceFileName);
HueSaturationLayer hueLayerNew = img.addHueSaturationAdjustmentLayer();
```

## الخطوة 6: تعيين قيم صبغة/تشبع جديدة للطبقة الجديدة
الآن بعد أن أنشأت هذه الطبقة الجديدة، قم بتطبيق إعدادات الصبغة، التشبع، والسطوع المطلوبة كما فعلت من قبل.

```java
hueLayerNew.setHue((short) -25);
hueLayerNew.setSaturation((short) -12);
hueLayerNew.setLightness((short) 67);
ColorRangeHsl newColorRange = hueLayerNew.getRange(2);
newColorRange.setHue((short) -160);
newColorRange.setSaturation((short) 100);
newColorRange.setLightness((short) 20);
newColorRange.setMostLeftBorder((short) 300);
```

## الخطوة 7: حفظ ملف PSD المحدث
أخيرًا، احفظ ملف PSD مع طبقة الصبغة/التشبع المضافة حتى تتمكن من رؤية التغييرات.

```java
String psdPathAfterNewLayerChange = dataDir + "PhotoExampleAddedHueSaturation.psd";
img.save(psdPathAfterNewLayerChange);
```

تهانينا! لقد نجحت في تعديل ملفات PSD باستخدام Aspose.PSD لـ Java. الآن يمكنك تجربة صور مختلفة وتعديلات أعمق، مما يحيي مشاريع التصميم الجرافيكي الخاصة بك.

## كيفية معالجة ملفات PSD دفعيًا مع تعديلات الصبغة
نظرًا لأن الكود أعلاه قابل للبرمجة بالكامل، يمكنك تغليف التسلسل الكامل في حلقة تتكرر على كل ملف `.psd` في مجلد. يتيح لك ذلك **معالجة ملفات psd دفعيًا** وتطبيق نفس تعديلات الصبغة، التشبع، والسطوع في تشغيل واحد—مثالي لتحديثات العلامة التجارية على نطاق واسع.

## المشكلات الشائعة والحلول
- **NullPointerException عند تحميل ملف:** تأكد من أن `dataDir` ينتهي بالفاصل المناسب للملفات (`/` أو `\`) وأن اسم الملف صحيح.  
- **قيم الضبط خارج النطاق:** الصبغة، التشبع، والسطوع تقبل قيمًا من -255 إلى 255. حافظ على أرقامك ضمن هذا النطاق.  
- **الطبقة غير موجودة:** إذا لم يحتوي PSD على طبقة صبغة/تشبع، سيتخطى فحص `instanceof` الكتلة. استخدم `addHueSaturationAdjustmentLayer()` لإنشاء واحدة أولاً.

## الأسئلة المتكررة

**Q: ما هي طبقة Hue Saturation Adjustment Layer؟**  
A: تسمح لك بتعديل خصائص اللون في الصورة دون تغيير البكسلات الأصلية بشكل دائم.

**Q: هل أحتاج إلى تثبيت Photoshop لاستخدام Aspose.PSD؟**  
A: لا، Aspose.PSD هي مكتبة مستقلة تعمل دون الاعتماد على Photoshop.

**Q: هل يمكنني استخدام Aspose.PSD للمعالجة الدفعية؟**  
A: نعم، يمكنك أتمتة ومعالجة عدة ملفات PSD دفعيًا باستخدام Aspose.PSD.

**Q: هل Aspose.PSD مجانية؟**  
A: توفر Aspose.PSD نسخة تجريبية مجانية، لكن يلزم الحصول على ترخيص للاستخدام طويل الأمد. يمكنك الاطلاع على الأسعار [هنا](https://purchase.aspose.com/buy).

## الخاتمة
العمل مع الرسومات برمجيًا يفتح أمامك عالماً من الإمكانيات. استخدام Aspose.PSD لـ Java **لإضافة طبقة تشبع اللون** و**لإنشاء طبقة ضبط صبغة** يوفر مرونة وكفاءة يمكن أن تُبسّط سير عمل التصميم الخاص بك. سواءً كنت تُحسّن الصور لمشروع ما أو تُنشئ محتوى بصري مذهل، فإن إتقان هذه الأدوات يمكن أن يُحسّن مخرجاتك بشكل كبير.

لا تتردد في استكشاف المزيد من وظائف Aspose.PSD من خلال الاطلاع على [التوثيق](https://reference.aspose.com/psd/java/) أو التفكير في الحصول على [ترخيص مؤقت](https://purchase.aspose.com/temporary-license/) لتجربة القوة الكاملة للمكتبة.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**آخر تحديث:** 2026-03-13  
**تم الاختبار مع:** Aspose.PSD for Java 24.12 (latest at time of writing)  
**المؤلف:** Aspose  

---