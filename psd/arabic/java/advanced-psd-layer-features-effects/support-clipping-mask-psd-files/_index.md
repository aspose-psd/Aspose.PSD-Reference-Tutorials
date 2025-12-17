---
date: 2025-12-17
description: تعلم كيفية تصدير ملفات PSD إلى PNG مع دعم قناع القص باستخدام Aspose.PSD
  للغة Java. اتبع دليلنا خطوة بخطوة لحفظ PSD كـ PNG بسرعة.
linktitle: Export PSD as PNG with Clipping Mask – Aspose.PSD Java
second_title: Aspose.PSD Java API
title: تصدير PSD كـ PNG مع قناع القص – Aspose.PSD Java
url: /ar/java/advanced-psd-layer-features-effects/support-clipping-mask-psd-files/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# دعم قناع القص في ملفات PSD باستخدام Aspose.PSD Java

## مقدمة
إذا كنت بحاجة إلى **تصدير PSD كـ PNG** مع الحفاظ على معلومات قناع القص، فإن Aspose.PSD for Java يجعل العملية سهلة. في هذا الدرس سنستعرض الخطوات الدقيقة للتعامل برمجياً مع ملفات PSD، وتطبيق أقنعة القص، و**حفظ PSD كـ PNG** مع دعم كامل للشفافية. في النهاية، ستحصل على مقطع شفرة قابل لإعادة الاستخدام يمكن دمجه مباشرةً في مشاريع Java الخاصة بك.

## إجابات سريعة
- **ماذا تفعل المكتبة؟** تقوم بقراءة وتحرير وتصدير ملفات Photoshop PSD في Java.  
- **هل يمكنها الاحتفاظ بأقنعة القص؟** نعم – يتم الاحتفاظ بالأقنعة عند التصدير إلى PNG.  
- **ما الصيغة المستخدمة للتصدير بدون فقدان؟** PNG مع TruecolorWithAlpha.  
- **هل أحتاج إلى ترخيص للإنتاج؟** يلزم الحصول على ترخيص تجاري؛ يتوفر نسخة تجريبية مجانية.  
- **ما نسخة Java المطلوبة؟** JDK 8 أو أعلى.

## ما هو “export psd as png”؟
تصدير ملف PSD إلى PNG يحول مستند Photoshop متعدد الطبقات إلى صورة نقطية مسطحة مع الحفاظ على الشفافية. هذا مفيد بشكل خاص عندما تحتاج إلى صورة جاهزة للويب أو ترغب في مشاركة التصاميم دون الحاجة إلى تطبيق Photoshop.

## لماذا نستخدم Aspose.PSD لهذه المهمة؟
تتعامل Aspose.PSD مع ميزات Photoshop المعقدة—مثل أقنعة القص، طبقات الضبط، وأنماط الدمج—دون الحاجة إلى تثبيت Photoshop. إنها مثالية لتدفقات العمل الآلية، المعالجة الدفعة، أو دمج أصول التصميم في تطبيقات الخادم.

## المتطلبات المسبقة
قبل الغوص في الشيفرة، تأكد من توفر ما يلي:

1. **Java Development Kit (JDK)** – على الأقل JDK 8. قم بتنزيله من [موقع Oracle](https://www.oracle.com/java/technologies/javase-jdk8-downloads.html).  
2. **Aspose.PSD for Java Library** – احصل على أحدث ملف JAR من [صفحة التحميل](https://releases.aspose.com/psd/java/). يمكنك أيضاً تجربة [الإصدار التجريبي المجاني](https://releases.aspose.com/).  
3. **IDE** – IntelliJ IDEA أو Eclipse أو أي محرر تفضله.  
4. **Basic Java Knowledge** – الإلمام بعمليات إدخال/إخراج الملفات ومفاهيم البرمجة الكائنية سيساعد.

## تصدير PSD كـ PNG – دليل خطوة بخطوة

### الخطوة 1: تحديد دليل المستند الخاص بك
أولاً، أخبر البرنامج بمكان وجود ملف PSD المصدر وأين يجب كتابة ملف PNG.

```java
String dataDir = "Your Document Directory";
```

استبدل `"Your Document Directory"` بالمسار المطلق على جهازك الذي يحتوي على ملفات PSD.

### الخطوة 2: تحميل ملف PSD
بعد ذلك، حمّل ملف PSD في كائن `PsdImage` حتى تتمكن من التعامل مع طبقاته وأقنانه.

```java
String sourceFileName = dataDir + "ClippingMaskComplex.psd";
PsdImage im = (PsdImage) Image.load(sourceFileName);
```

### الخطوة 3: إعداد خيارات التصدير
قم بتكوين إعدادات تصدير PNG. استخدام `TruecolorWithAlpha` يضمن الحفاظ على أي مناطق شفافة تم إنشاؤها بواسطة أقنعة القص.

```java
PngOptions saveOptions = new PngOptions();
saveOptions.setColorType(PngColorType.TruecolorWithAlpha);
```

### الخطوة 4: تصدير الصورة
الآن احفظ ملف PSD (مع قناع القص الخاص به) كملف PNG.

```java
String exportPath = dataDir + "ClippingMaskComplex.png";
im.save(exportPath, saveOptions);
```

يمكن استخدام ملف PNG الناتج مباشرةً في صفحات الويب، تطبيقات الهواتف المحمولة، أو أي مكان يقبل الصور النقطية.

### الخطوة 5: تنظيف الموارد
دائمًا قم بتحرير كائن `PsdImage` عند الانتهاء لتفريغ الذاكرة الأصلية.

```java
im.dispose();
```

### كيفية حفظ PSD كـ PNG في سطر واحد
إذا كنت تفضل نسخة مختصرة، يمكن تقليل العملية بالكامل إلى:

```java
Image.load(sourceFileName).save(exportPath, new PngOptions(){{
    setColorType(PngColorType.TruecolorWithAlpha);
}});
```

* (النسخة الموسعة أعلاه موضحة للتوضيح وتسهيل تصحيح الأخطاء.) *

## المشكلات الشائعة والحلول
- **الشفافية مفقودة:** تأكد من ضبط `PngColorType.TruecolorWithAlpha`؛ وإلا سيكون PNG غير شفاف.  
- **الملف غير موجود:** تحقق من أن `dataDir` ينتهي بفاصل المسار المناسب (`/` أو `\\`).  
- **OutOfMemoryError:** حرّر كائن `PsdImage` فورًا، خاصةً عند معالجة ملفات كبيرة أو دفعات.

## الأسئلة المتكررة

**س: ما هو قناع القص في ملفات PSD؟**  
ج: يستخدم قناع القص شفافية طبقة واحدة لتقييد ظهور طبقة أخرى، مما يسمح بإنشاء تركيبات معقدة دون تعديل دائم للطبقات.

**س: هل يمكنني استخدام Aspose.PSD لتحرير ملفات PSD؟**  
ج: نعم، يمكنك تحرير الطبقات، تطبيق التأثيرات، وتصدير إلى صيغ مثل PNG أو JPEG.

**س: أين يمكنني العثور على وثائق Aspose.PSD؟**  
ج: يمكنك العثور على وثائق شاملة لـ Aspose.PSD for Java [هنا](https://reference.aspose.com/psd/java/).

**س: هل هناك نسخة تجريبية متاحة لـ Aspose.PSD؟**  
ج: نعم! يمكنك الوصول إلى نسخة تجريبية مجانية من Aspose.PSD [هنا](https://releases.aspose.com/).

**س: كيف أحصل على دعم لمشكلات Aspose.PSD؟**  
ج: لأي استفسارات أو مشكلات، يمكنك الحصول على الدعم عبر منتدى Aspose [هنا](https://forum.aspose.com/c/psd/34).

## الخلاصة
لقد تعلمت الآن كيفية **تصدير PSD كـ PNG** مع الحفاظ على أقنعة القص باستخدام Aspose.PSD for Java. يتيح لك هذا النهج أتمتة خطوط التصميم، دمج أصول Photoshop في الخدمات الخلفية، والحفاظ على الدقة البصرية دون خطوات تصدير يدوية. استكشف ميزات Aspose.PSD الأخرى—مثل دمج الطبقات، تعديل الألوان، والمعالجة الدفعة—لتبسيط سير العمل بشكل أكبر.

---

**آخر تحديث:** 2025-12-17  
**تم الاختبار مع:** Aspose.PSD 24.12 for Java  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}