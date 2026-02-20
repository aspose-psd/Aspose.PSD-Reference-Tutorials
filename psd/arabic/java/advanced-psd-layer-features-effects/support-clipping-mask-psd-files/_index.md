---
date: 2026-02-20
description: تعلم كيفية تصدير ملفات PSD كـ PNG مع الحفاظ على الشفافية ودعم قناع القص
  باستخدام Aspose.PSD للغة Java. يوضح هذا الدليل خطوة بخطوة كيفية حفظ ملف PSD كـ PNG
  بسرعة.
linktitle: How to Export PSD as PNG with Clipping Mask – Aspose.PSD Java
second_title: Aspose.PSD Java API
title: كيفية تصدير ملف PSD كـ PNG مع قناع القص – Aspose.PSD Java
url: /ar/java/advanced-psd-layer-features-effects/support-clipping-mask-psd-files/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# دعم قناع القص في ملفات PSD باستخدام Aspose.PSD Java

## المقدمة
إذا كنت تبحث عن **كيفية تصدير PSD** كـ PNG مع الحفاظ على معلومات قناع القص، فإن Aspose.PSD for Java يجعل العملية سهلة. في هذا البرنامج التعليمي سنستعرض الخطوات الدقيقة للتعامل برمجياً مع ملفات PSD، وتطبيق أقنعة القص، و**حفظ PSD إلى PNG** مع دعم كامل للشفافية. في النهاية، ستحصل على مقتطف يمكن إعادة استخدامه ويتناسب مباشرة مع مشاريع Java الخاصة بك.

## إجابات سريعة
- **ماذا تفعل المكتبة؟** تقوم بقراءة وتعديل وتصدير ملفات Photoshop PSD في Java.  
- **هل يمكنها الحفاظ على أقنعة القص؟** نعم – يتم الاحتفاظ بالأقنعة عند التصدير إلى PNG.  
- **ما الصيغة المستخدمة للتصدير بدون فقدان؟** PNG مع TruecolorWithAlpha.  
- **هل أحتاج إلى ترخيص للإنتاج؟** يلزم الحصول على ترخيص تجاري؛ يتوفر نسخة تجريبية مجانية.  
- **ما نسخة Java المطلوبة؟** JDK 8 أو أعلى.

## كيفية تصدير PSD كـ PNG مع قناع القص
تحويل ملف PSD إلى PNG يحول مستند Photoshop الطبقي إلى صورة نقطية مسطحة مع الحفاظ على الشفافية. هذا مفيد بشكل خاص عندما تحتاج إلى صورة جاهزة للويب، أو تريد **الحفاظ على شفافية PNG**، أو تقوم بتحويل دفعة من PSD إلى PNG في خط أنابيب آلي.

## لماذا نستخدم Aspose.PSD لهذه المهمة؟
يتعامل Aspose.PSD مع ميزات Photoshop المعقدة—مثل أقنعة القص، طبقات التعديل، وأنماط الدمج—دون الحاجة إلى تثبيت Photoshop. إنه مثالي لتدفقات العمل الآلية، المعالجة الدفعية، أو دمج أصول التصميم في تطبيقات الخادم حيث يجب **تصدير PSD إلى PNG** بشكل موثوق.

## المتطلبات المسبقة
قبل الغوص في الشيفرة، تأكد من توفر ما يلي:

1. **Java Development Kit (JDK)** – على الأقل JDK 8. حمّله من [موقع Oracle](https://www.oracle.com/java/technologies/javase-jdk8-downloads.html).  
2. **Aspose.PSD for Java Library** – احصل على أحدث ملف JAR من [صفحة التحميل](https://releases.aspose.com/psd/java/). يمكنك أيضاً تجربة [النسخة التجريبية المجانية](https://releases.aspose.com/).  
3. **IDE** – IntelliJ IDEA، Eclipse، أو أي محرر تفضله.  
4. **معرفة أساسية بـ Java** – الإلمام بعمليات الإدخال/الإخراج والبرمجة الكائنية سيساعدك.

## تصدير PSD كـ PNG – دليل خطوة بخطوة

### الخطوة 1: تحديد دليل المستندات
أولاً، أخبر البرنامج بمكان وجود ملف PSD المصدر وأين يجب كتابة ملف PNG.

```java
String dataDir = "Your Document Directory";
```

استبدل `"Your Document Directory"` بالمسار المطلق على جهازك الذي يحتوي على ملفات PSD.

### الخطوة 2: تحميل ملف PSD
بعد ذلك، حمّل ملف PSD في كائن `PsdImage` لتتمكن من التعامل مع طبقاته وأقنانه.

```java
String sourceFileName = dataDir + "ClippingMaskComplex.psd";
PsdImage im = (PsdImage) Image.load(sourceFileName);
```

### الخطوة 3: إعداد خيارات التصدير
قم بتكوين إعدادات تصدير PNG. استخدام `TruecolorWithAlpha` يضمن بقاء أي مناطق شفافة تم إنشاؤها بواسطة أقنعة القص، وبالتالي **تحافظ على شفافية PNG**.

```java
PngOptions saveOptions = new PngOptions();
saveOptions.setColorType(PngColorType.TruecolorWithAlpha);
```

### الخطوة 4: تصدير الصورة
الآن احفظ ملف PSD (مع قناع القص) كملف PNG.

```java
String exportPath = dataDir + "ClippingMaskComplex.png";
im.save(exportPath, saveOptions);
```

يمكن استخدام ملف PNG الناتج مباشرةً في صفحات الويب، التطبيقات المحمولة، أو أي مكان يقبل الصور النقطية.

### الخطوة 5: تنظيف الموارد
دائمًا قم بتحرير `PsdImage` عند الانتهاء لتفريغ الذاكرة الأصلية.

```java
im.dispose();
```

### كيفية حفظ PSD إلى PNG في سطر واحد
إذا كنت تفضّل نسخة مختصرة، يمكن تقليل العملية بأكملها إلى:

```java
Image.load(sourceFileName).save(exportPath, new PngOptions(){{
    setColorType(PngColorType.TruecolorWithAlpha);
}});
```

*(النسخة الموسعة أعلاه موضحة للوضوح وسهولة التصحيح.)*

## المشكلات الشائعة والحلول
- **الشفافية مفقودة:** تأكد من تعيين `PngColorType.TruecolorWithAlpha`؛ وإلا سيكون PNG غير شفاف.  
- **الملف غير موجود:** تحقق من أن `dataDir` ينتهي بفاصل المسار المناسب (`/` أو `\\`).  
- **OutOfMemoryError:** حرّر `PsdImage` بسرعة، خاصةً عند معالجة ملفات كبيرة أو دفعات.  
- **تحويل دفعة من PSD إلى PNG:** عند تحويل العديد من الملفات، ضع الخطوات داخل حلقة وأعد استخدام `PngOptions` لتحسين الأداء.

## الأسئلة المتكررة

**س: ما هو قناع القص في ملفات PSD؟**  
ج: يستخدم قناع القص شفافية طبقة واحدة لتقييد رؤية طبقة أخرى، مما يسمح بإنشاء تركيبات معقدة دون تعديل دائم للطبقات.

**س: هل يمكنني استخدام Aspose.PSD لتعديل ملفات PSD؟**  
ج: نعم، يمكنك تعديل الطبقات، تطبيق التأثيرات، وتصديرها إلى صيغ مثل PNG أو JPEG.

**س: أين يمكنني العثور على وثائق Aspose.PSD؟**  
ج: يمكنك العثور على وثائق شاملة لـ Aspose.PSD for Java [هنا](https://reference.aspose.com/psd/java/).

**س: هل تتوفر نسخة تجريبية من Aspose.PSD؟**  
ج: نعم! يمكنك الوصول إلى نسخة تجريبية مجانية من Aspose.PSD [هنا](https://releases.aspose.com/).

**س: كيف أحصل على دعم لمشكلات Aspose.PSD؟**  
ج: لأي استفسارات أو مشكلات، يمكنك الحصول على الدعم عبر منتدى Aspose [هنا](https://forum.aspose.com/c/psd/34).

## الخلاصة
لقد تعلمت الآن **كيفية تصدير PSD كـ PNG** مع الحفاظ على أقنعة القص باستخدام Aspose.PSD for Java. يتيح لك هذا النهج أتمتة خطوط تصميمك، دمج أصول Photoshop في خدمات الخلفية، والحفاظ على الدقة البصرية دون خطوات تصدير يدوية. استكشف ميزات أخرى في Aspose.PSD—مثل دمج الطبقات، تعديل الألوان، والمعالجة الدفعية—لتبسيط سير العمل أكثر.

---

**آخر تحديث:** 2026-02-20  
**تم الاختبار مع:** Aspose.PSD 24.12 for Java  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}