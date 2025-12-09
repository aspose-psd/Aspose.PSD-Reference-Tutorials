---
date: 2025-11-30
description: تعلم كيفية إضافة حد وتغيير لون حد PSD باستخدام Aspose.PSD للغة Java.
  اتبع هذا الدليل خطوة بخطوة لتعديل لون طبقة الحد والشفافية.
linktitle: Add Stroke Layer Color
second_title: Aspose.PSD Java API
title: كيفية إضافة لون طبقة الحد في Aspose.PSD للغة Java
url: /ar/java/advanced-image-effects/add-stroke-layer-color/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# كيفية إضافة لون طبقة الحد في Aspose.PSD للـ Java

## المقدمة

إذا كنت بحاجة إلى **كيفية إضافة الحد** إلى مستند Photoshop برمجياً، فإن Aspose.PSD للـ Java يجعل العملية بسيطة. في هذا الدرس سنستعرض إضافة لون طبقة الحد، تعديل شفافيته، وحفظ النتيجة. في النهاية ستتعرف أيضاً على **كيفية تغيير لون الحد** (أو *تغيير لون حد PSD*) لأي طبقة موجودة، مما يمنحك سيطرة إبداعية كاملة من خلال كود Java الخاص بك.

## إجابات سريعة
- **ما المكتبة المطلوبة؟** Aspose.PSD للـ Java (الإصدار الأحدث).  
- **هل يمكنني تغيير لون الحد؟** نعم – استخدم `ColorFillSettings` لتعيين أي `Color`.  
- **هل أحتاج إلى ترخيص؟** الترخيص المؤقت يعمل للتقييم؛ الترخيص الكامل مطلوب للإنتاج.  
- **ما نسخة Java المدعومة؟** Java 8 أو أعلى.  
- **كم من الوقت تستغرق العملية؟** عادةً أقل من 10 دقائق لتغيير حد أساسي.

## ما هي طبقة الحد في ملف PSD؟
طبقة الحد هي تأثير متجهي يرسم خطًا حول محتويات الطبقة. يمكن تخصيصه باللون، السماكة، الشفافية، ووضع الدمج. تعديل هذا التأثير برمجياً يتيح أتمتة العلامة التجارية، المعالجة الدفعية، أو إنشاء رسومات ديناميكية.

## لماذا نستخدم Aspose.PSD لتغيير لون الحد؟
- **لا حاجة لبرنامج Photoshop** – العمل بالكامل في Java.  
- **الامتثال الكامل لمواصفات PSD** – جميع ميزات PSD الحديثة مدعومة.  
- **أداء عالي** – معالجة الملفات الكبيرة بسرعة.  
- **متعدد المنصات** – تشغيل على أي نظام تشغيل يحتوي على JVM.

## المتطلبات المسبقة

- **مكتبة Aspose.PSD** – تحميل من [الوثائق الرسمية](https://reference.aspose.com/psd/java/).  
- **مجموعة تطوير Java (JDK)** – الإصدار 8 أو أحدث.  
- **بيئة التطوير المتكاملة (IDE)** – Eclipse، IntelliJ IDEA، أو أي محرر متوافق مع Java.

## استيراد الحزم

أولاً، استورد الفئات التي ستحتاجها. هذا يمنح مشروعك إمكانية الوصول إلى معالجة PSD وواجهات برمجة تطبيقات تأثير الحد.

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;


import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.BlendMode;
import com.aspose.psd.fileformats.psd.layers.fillsettings.ColorFillSettings;
import com.aspose.psd.fileformats.psd.layers.fillsettings.FillType;
import com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
```

## الخطوة 1: إعداد مشروعك

أنشئ مشروع Java جديد، أضف ملف JAR الخاص بـ Aspose.PSD إلى مسار البناء، وتأكد من تحميل المكتبة دون أخطاء.

## الخطوة 2: تحميل ملف PSD

فعّل تحميل موارد التأثير بحيث تكون معلومات الحد متاحة.

```java
String dataDir = "Your Document Directory";

String sourceFileName = dataDir + "Stroke.psd";
String exportPath = dataDir + "StrokeGradientChanged.psd";

PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);
```

## الخطوة 3: الوصول إلى طبقة تأثير الحد

استرجع أول تأثير حد من الطبقة الثانية (الفهرس 1).

```java
StrokeEffect colorStroke = (StrokeEffect)im.getLayers()[1].getBlendingOptions().getEffects()[0];
```

## الخطوة 4: التحقق من خصائص الحد

تأكد من الخصائص الحالية قبل إجراء أي تغييرات. هذا يساعد على تجنب النتائج غير المتوقعة.

```java
Assert.areEqual(BlendMode.Normal, colorStroke.getBlendMode());
Assert.areEqual(255, colorStroke.getOpacity());
Assert.areEqual(true, colorStroke.isVisible());
```

## الخطوة 5: تعيين اللون والشفافية (كيفية تغيير لون الحد)

هنا **نقوم بتغيير لون حد PSD** إلى الأصفر ونقلل الشفافية إلى 50 % (127 / 255).

```java
ColorFillSettings fillSettings = (ColorFillSettings)colorStroke.getFillSettings();
fillSettings.setColor(Color.getYellow());

colorStroke.setOpacity((byte)127);
```

## الخطوة 6: حفظ ملف PSD المعدل

اكتب الصورة المحدثة مرة أخرى إلى القرص. الملف الجديد الآن يحتوي على الحد المعدل.

```java
im.save(exportPath);
```

## المشكلات الشائعة والنصائح

- **التحقق من القيم الفارغة** – تحقق دائمًا أن `getEffects()` تُرجع مصفوفة غير فارغة قبل التحويل.  
- **فهرس الطبقة** – طبقات PSD تبدأ من الصفر؛ تأكد من استهداف الطبقة الصحيحة.  
- **تنسيق اللون** – `Color.getYellow()` مجرد مثال؛ يمكنك إنشاء ألوان مخصصة باستخدام `new Color(r, g, b)`.  
- **نطاق الشفافية** – الشفافية هي بايت (0–255)؛ القيم فوق 255 سيتم تقليمها.

## الخلاصة

لقد تعلمت الآن **كيفية إضافة حد** إلى ملف PSD و**كيفية تغيير لون الحد** باستخدام Aspose.PSD للـ Java. جرّب ألوانًا مختلفة، أوضاع دمج، وشفافية لتحقيق النمط البصري الدقيق الذي يحتاجه مشروعك.

## الأسئلة المتكررة

**س: هل يمكنني استخدام Aspose.PSD مع مكتبات رسومية أخرى للـ Java؟**  
ج: نعم، يمكن دمج Aspose.PSD مع مكتبات مثل Apache Commons Imaging أو Java2D لتوسيع الوظائف.

**س: هل Aspose.PSD متوافق مع أحدث صيغة ملفات PSD؟**  
ج: بالتأكيد. يتم تحديث المكتبة بانتظام لدعم أحدث مواصفات Photoshop.

**س: كيف أتعامل مع الاستثناءات أثناء استخدام Aspose.PSD؟**  
ج: راجع [منتدى الدعم](https://forum.aspose.com/c/psd/34) للحصول على حلول مفصلة وأمثلة على معالجة الأخطاء.

**س: هل يمكنني تجربة Aspose.PSD قبل الشراء؟**  
ج: بالطبع! احصل على [نسخة تجريبية مجانية](https://releases.aspose.com/) لاستكشاف جميع الميزات.

**س: أين يمكنني الحصول على ترخيص مؤقت لـ Aspose.PSD؟**  
ج: احصل على [ترخيص مؤقت](https://purchase.aspose.com/temporary-license/) لتقييم المكتبة في بيئة التطوير الخاصة بك.

---

**آخر تحديث:** 2025-11-30  
**تم الاختبار مع:** Aspose.PSD 24.11 للـ Java  
**المؤلف:** Aspose

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}