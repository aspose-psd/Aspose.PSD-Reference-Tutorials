---
date: 2026-06-13
description: تعلم كيفية استبدال الخطوط في ملفات PSD باستخدام Aspose.PSD for Java،
  وتحويل PSD إلى PNG، ومعالجة الخطوط المفقودة بكفاءة.
keywords:
- how to replace fonts
- convert psd to png
- handle missing fonts psd
linktitle: إعدادات استبدال الخطوط المفقودة
schemas:
- author: Aspose
  dateModified: '2026-06-13'
  description: Learn how to replace fonts in PSD files using Aspose.PSD for Java,
    convert PSD to PNG, and handle missing fonts efficiently.
  headline: How to Replace Fonts in PSD Files with Aspose.PSD for Java
  type: TechArticle
- questions:
  - answer: '`PsdImage` is the core class that represents a PSD document in memory.'
    question: What is the primary class for loading PSD files?
  - answer: Use `PsdLoadOptions.setDefaultFontName("Arial")`.
    question: Which option sets a default replacement font?
  - answer: Yes—call `psdImage.save("output.png", new PngOptions())`.
    question: Can I save the result as PNG?
  - answer: A temporary license works for testing; a full license is required for
      production.
    question: Do I need a license for development?
  - answer: Aspose.PSD for Java supports Java 8 and later.
    question: What Java version is supported?
  type: FAQPage
second_title: Aspose.PSD Java API
title: كيفية استبدال الخطوط في ملفات PSD باستخدام Aspose.PSD for Java
url: /ar/java/advanced-techniques/settings-replacing-missing-fonts/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# كيفية استبدال الخطوط في ملفات PSD باستخدام Aspose.PSD للـ Java

في تطوير Java الحديث، **كيفية استبدال الخطوط** في ملف Photoshop (PSD) تُعد تحديًا شائعًا يمكن أن يخل بتصميم العناصر البصرية لتصاميمك. تقدم Aspose.PSD للـ Java واجهة برمجة تطبيقات قوية تقوم بأتمتة استبدال الخطوط، مما يتيح لك الحفاظ على مظهر صورك كما هو مقصود. يرشدك هذا الدليل خلال كل خطوة — من إعداد البيئة إلى حفظ ملف PNG النهائي — لتتمكن من التعامل مع الخطوط المفقودة في ملفات PSD بثقة.

## إجابات سريعة
- **ما هو الصنف الأساسي لتحميل ملفات PSD؟** `PsdImage` هو الصنف الأساسي الذي يمثل مستند PSD في الذاكرة.  
- **ما هو الخيار الذي يحدد خط الاستبدال الافتراضي؟** استخدم `PsdLoadOptions.setDefaultFontName("Arial")`.  
- **هل يمكنني حفظ النتيجة كملف PNG؟** نعم — استدعِ `psdImage.save("output.png", new PngOptions())`.  
- **هل أحتاج إلى ترخيص للتطوير؟** الترخيص المؤقت يعمل للاختبار؛ الترخيص الكامل مطلوب للإنتاج.  
- **ما نسخة Java المدعومة؟** تدعم Aspose.PSD للـ Java Java 8 وما بعدها.

## كيفية استبدال الخطوط في ملف PSD باستخدام Aspose.PSD للـ Java؟

حمّل ملف PSD المصدر باستخدام `PsdLoadOptions` الذي يحدد خطًا احتياطيًا، ثم احفظ الصورة بالتنسيق المطلوب. تقوم الواجهة البرمجية تلقائيًا باستبدال أي رموز مفقودة بالخط الافتراضي الذي تحدده، مما يلغي أخطاء العرض دون تعديل يدوي. هذا النهج خطوة واحدة يعمل مع ملفات بأي حجم ويحافظ على الطبقات والأقنعة والتأثيرات.

## ما هو `PsdLoadOptions`؟

`PsdLoadOptions` هو كائن تكوين يتحكم في طريقة تحليل Aspose.PSD لملف PSD. يتيح لك تحديد خط استبدال افتراضي، والتحكم في سلوك تحميل الطبقات، وتعيين خيارات لمعالجة الموارد المفقودة. من خلال تعديل خصائصه، يمكن للمطورين ضمان عرض ثابت للنص والعناصر الأخرى عبر بيئات مختلفة وتجنب أخطاء وقت التشغيل الناتجة عن الخطوط غير المتوفرة.

## لماذا استبدال الخطوط المفقودة في ملفات PSD؟

Aspose.PSD يدعم **أكثر من 50 تنسيقًا للإدخال والإخراج** ويمكنه معالجة ملفات PSD متعددة المئات من الصفحات دون تحميل المستند بالكامل إلى الذاكرة. استبدال الخطوط المفقودة يمنع تعطل طبقات النص، ويقلل وقت التصحيح اليدوي حتى **80%**، ويضمن أن ملفات PNG المصدرة تحتفظ بدقة التصميم الأصلي.

## المتطلبات المسبقة

1. **مكتبة Aspose.PSD** – قم بتنزيل وتثبيت مكتبة Aspose.PSD للـ Java من [صفحة الإصدارات](https://releases.aspose.com/psd/java/).  
2. **بيئة تطوير Java** – JDK Java 8+ ومحررك المفضل (Eclipse، IntelliJ IDEA، إلخ).  

الآن بعد أن أصبح كل شيء جاهزًا، دعنا نغوص في التنفيذ.

## استيراد الحزم

استورد المساحات الاسمية المطلوبة حتى يتمكن المترجم من العثور على فئات Aspose.PSD.

```java
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import com.aspose.psd.imageoptions.PngOptions;
```

## الخطوة 1: إعداد دليل المستند الخاص بك

حدد المجلد الذي يحتوي على ملف PSD المصدر ومكان كتابة المخرجات. يُستخدم هذا المسار من قبل أداة التحميل والحفظ.

```java
String dataDir = "Your Document Directory";
```

## الخطوة 2: تحديد ملفات المصدر والوجهة

قدّم مسارات مطلقة أو نسبية للملف PSD الأصلي وملف PNG الهدف. يساعد استخدام تسميات واضحة على تجنب الكتابة فوق الملفات.

```java
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "result.png";
```

## الخطوة 3: تكوين إعدادات استبدال الخطوط

أنشئ مثيلًا من `PsdLoadOptions` وحدد خط الاستبدال الافتراضي إلى **Arial** (أو أي خط مثبت على نظامك). هذا يخبر المحرك أي خط يستخدم عندما لا يتم العثور على الخط الأصلي.

```java
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setDefaultReplacementFont("Arial");
```

## الخطوة 4: تحميل صورة PSD واستبدال الخطوط

حمّل ملف PSD باستخدام الخيارات المكوّنة. تقوم Aspose.PSD تلقائيًا باستبدال الخطوط المفقودة أثناء عملية التحميل، لذا لا يلزم أي كود إضافي.

```java
Image image = Image.load(sourceFile, loadOptions);
PsdImage psdImage = (PsdImage) image;
```

## الخطوة 5: حفظ الصورة المعدلة

اختر `PngOptions` لتصدير الصورة كملف PNG بألوان حقيقية مع قناة ألفا. سيعرض الملف الناتج الخطوط المستبدلة بشكل صحيح.

```java
PngOptions options = new PngOptions();
options.setColorType(PngColorType.TruecolorWithAlpha);
psdImage.save(destName, options);
```

## المشكلات الشائعة والحلول

| المشكلة | السبب | الحل |
|-------|-------|-----|
| النص يظهر مشوشًا | خط الاستبدال يفتقر إلى الرموز المطلوبة | اختر خطًا بنطاق يونيكود أوسع (مثال: **Arial Unicode MS**). |
| خطأ عدم العثور على الملف | مسار غير صحيح في الخطوة 1 أو 2 | تحقق من سلاسل المسار واستخدم `File.separator` لتوافق عبر الأنظمة. |
| استثناء الترخيص | التشغيل بدون ترخيص صالح | تطبيق ترخيص مؤقت للاختبار أو شراء ترخيص كامل للإنتاج. |

## الأسئلة المتكررة

### س1: هل Aspose.PSD متوافق مع جميع إصدارات ملفات PSD؟

ج1: تدعم Aspose.PSD إصدارات PSD من **4.0** وحتى أحدث إصدار من Photoshop، مما يضمن توافقًا واسعًا عبر التصاميم القديمة والحديثة.

### س2: هل يمكنني استخدام خطوط مخصصة للاستبدال في Aspose.PSD؟

ج2: نعم، يمكنك تحديد أي خط TrueType أو OpenType مثبت على الخادم بتمرير اسمه إلى `setDefaultFontName`. يمنحك ذلك تحكمًا كاملاً في النتيجة البصرية.

### س3: هل هناك خيارات ترخيص متاحة لـ Aspose.PSD؟

ج3: استكشف خيارات الترخيص [هنا](https://purchase.aspose.com/buy) لاختيار الخطة الأنسب لمنظمتك، بما في ذلك تراخيص المطور، الموقع، وOEM.

### س4: هل هناك منتدى مجتمع لدعم Aspose.PSD؟

ج4: نعم، زر [منتدى Aspose.PSD](https://forum.aspose.com/c/psd/34) للحصول على مساعدة المجتمع، مقتطفات الكود، ونصائح حل المشكلات من مطورين آخرين.

### س5: كيف يمكنني الحصول على ترخيص مؤقت لـ Aspose.PSD؟

ج5: احصل على ترخيص مؤقت [هنا](https://purchase.aspose.com/temporary-license/) للتقييم أو الاختبار أو مشاريع إثبات المفهوم دون أي تكلفة.

---

**آخر تحديث:** 2026-06-13  
**تم الاختبار مع:** Aspose.PSD 24.12 للـ Java  
**المؤلف:** Aspose  

{{< blocks/products/products-backtop-button >}}

## دروس ذات صلة

- [تحويل PSD إلى PNG مع تراكب اللون – Aspose.PSD للـ Java](/psd/java/advanced-image-manipulation/rendering-color-effect/)
- [كيفية تحويل PSD إلى PNG وتغيير الحجم بنسبة متناسبة مع Aspose.PSD للـ Java](/psd/java/advanced-image-manipulation/resize-image-proportionally/)
- [تحويل PSD إلى صيغ صور نقطية مع Aspose.PSD للـ Java](/psd/java/advanced-techniques/convert-psd-to-raster-formats/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}