---
date: 2025-12-25
description: تعلم كيفية استبدال الخطوط في ملفات PSD باستخدام Aspose.PSD للغة Java
  – دليل خطوة بخطوة يوضح أيضًا كيفية حفظ ملف PSD كـ PNG والتعامل مع الخطوط المفقودة.
linktitle: Settings for Replacing Missing Fonts
second_title: Aspose.PSD Java API
title: كيفية استبدال الخطوط في Aspose.PSD لجافا
url: /ar/java/advanced-techniques/settings-replacing-missing-fonts/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# كيفية استبدال الخطوط في Aspose.PSD لـ Java

## المقدمة

إذا كنت تتعامل مع ملفات Photoshop (PSD) في تطبيق Java، فإن فقدان الخطوط قد يفسد تخطيط التصميم ويتسبب في أخطاء العرض. **كيفية استبدال الخطوط** بسرعة وبشكل موثوق أمر أساسي للحفاظ على دقة التصميم. في هذا الدرس ستتعلم كيفية استخدام Aspose.PSD لـ Java لاستبدال الخطوط المفقودة، وتحويل النتيجة إلى PNG، والحفاظ على سلاسة سير عمل تحويل الصور. في النهاية، ستكون قادرًا على استبدال الخطوط في الصور، حفظ PSD كـ PNG، وتجنب المشكلات الشائعة التي يواجهها المطورون.

## إجابات سريعة
- **ماذا يعني “استبدال الخطوط” في معالجة PSD؟** يستبدل الخطوط المفقودة أو غير المتوفرة بخط احتياطي تحدده.  
- **أي مكتبة تتعامل مع ذلك تلقائيًا؟** توفر Aspose.PSD لـ Java الخاصية `PsdLoadOptions.setDefaultReplacementFont`.  
- **هل يمكنني أيضًا تحويل PSD إلى PNG بعد الاستبدال؟** نعم – استخدم `PngOptions` واستدعِ `psdImage.save`.  
- **هل أحتاج إلى ترخيص للاستخدام في الإنتاج؟** يلزم وجود ترخيص صالح لـ Aspose.PSD للبنيات غير التجريبية.  
- **ما نسخة Java المدعومة؟** أي بيئة تشغيل Java 8+ تعمل مع إصدار Aspose.PSD الحالي.

## ما هو استبدال الخطوط في ملفات PSD؟

عندما يشير PSD إلى خط غير مثبت على الجهاز المضيف، يلجأ محرك العرض إلى خط عام، مما يؤدي غالبًا إلى نص غير محاذٍ. يتيح لك استبدال الخطوط تحديد خط افتراضي (مثل Arial) سيستخدمه المكتبة كلما صادفت خطًا مفقودًا، مما يضمن مخرجات بصرية متسقة.

## لماذا نستبدل الخطوط المفقودة باستخدام Aspose.PSD؟

- **حل بدون تبعيات** – لا حاجة إلى Photoshop الأصلي أو أدوات خارجية.  
- **جاهز للمعالجة الدفعية** – يمكن معالجة عشرات الملفات في حلقة بنفس الإعدادات.  
- **جاهز لتحويل الصور** – بعد الاستبدال يمكنك مباشرة **حفظ PSD كـ PNG** أو **تحويل PSD إلى PNG** دون خطوات إضافية.  
- **متعدد المنصات** – يعمل على بيئات Java في Windows وLinux وmacOS.

## المتطلبات المسبقة

1. **مكتبة Aspose.PSD** – قم بتنزيل وتثبيت مكتبة Aspose.PSD لـ Java من [صفحة الإصدارات](https://releases.aspose.com/psd/java/).  
2. **بيئة تطوير Java** – يجب تثبيت JDK 8 أو أحدث وتكوينه.  

الآن بعد أن لدينا الأساسيات، دعنا نتعمق في الكود.

## استيراد الحزم

ابدأ باستيراد الفئات الضرورية من Aspose.PSD. سيمكنك ذلك من تحميل الصور، إعداد خيارات استبدال الخطوط، وتصدير PNG.

```java
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import com.aspose.psd.imageoptions.PngOptions;
```

## الخطوة 1: إعداد دليل المستندات

حدد المجلد الذي يحتوي على ملف PSD المصدر وأين سيتم حفظ PNG الناتج.

```java
String dataDir = "Your Document Directory";
```

## الخطوة 2: تحديد ملفات المصدر والوجهة

قدم المسارات الكاملة لملف PSD المدخل وملف PNG المخرج. هذا يجعل سير العمل واضحًا ويسهل صيانة الكود.

```java
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "result.png";
```

## الخطوة 3: تكوين إعدادات استبدال الخطوط

أنشئ كائن `PsdLoadOptions` وحدد للـ Aspose.PSD الخط الذي سيستخدمه عندما يصادف خطًا مفقودًا. في هذا المثال نستخدم **Arial**، لكن يمكنك استبداله بأي خط مثبت على نظامك.

```java
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setDefaultReplacementFont("Arial");
```

## الخطوة 4: تحميل صورة PSD واستبدال الخطوط

حمّل ملف PSD باستخدام الخيارات التي عرّفتها أعلاه. تقوم المكتبة تلقائيًا بتبديل أي خطوط مفقودة بالخط الافتراضي الذي حددته.

```java
Image image = Image.load(sourceFile, loadOptions);
PsdImage psdImage = (PsdImage) image;
```

## الخطوة 5: حفظ الصورة المعدلة

قم بتكوين خيارات تصدير PNG – ألوان حقيقية مع قناة ألفا – للحفاظ على الشفافية. تُظهر هذه الخطوة أيضًا **تحويل صورة PSD إلى PNG** بعد استبدال الخطوط.

```java
PngOptions options = new PngOptions();
options.setColorType(PngColorType.TruecolorWithAlpha);
psdImage.save(destName, options);
```

### ماذا حدث؟

- تم فتح ملف PSD بخط احتياطي (Arial).  
- جميع طبقات النص التي كانت تشير إلى خطوط مفقودة الآن تُعرض باستخدام Arial.  
- تم حفظ الصورة النهائية كملف PNG، مما يعني **حفظ PSD كـ PNG** مع الحفاظ على الدقة البصرية.

## المشكلات الشائعة & استكشاف الأخطاء

| المشكلة | السبب | الحل |
|-------|-------|----------|
| النص لا يزال غير صحيح | اختلاف مقاييس الخط (الحجم، الوزن) | اضبط حجم الخط البديل برمجيًا أو اختر خطًا له مقاييس مشابهة. |
| حجم PNG أكبر من المتوقع | خيارات PNG الافتراضية تستخدم ألوان 32‑bit | غيّر `PngColorType` إلى `Truecolor` إذا لم تكن الشفافية مطلوبة. |
| استثناء الترخيص | تشغيل بدون ترخيص صالح | طبّق ترخيص Aspose.PSD مؤقت أو دائم قبل تحميل الصورة. |

## الأسئلة المتكررة

**س: هل Aspose.PSD متوافق مع جميع إصدارات ملفات PSD؟**  
ج: يدعم Aspose.PSD مجموعة واسعة من إصدارات PSD، من إصدارات Photoshop القديمة حتى أحدث الميزات.

**س: هل يمكنني استخدام خطوط مخصصة للاستبدال في Aspose.PSD؟**  
ج: نعم، ما عليك سوى تمرير اسم الخط المخصص إلى `setDefaultReplacementFont`. تأكد من أن الخط متاح للـ JVM.

**س: هل هناك خيارات ترخيص متاحة لـ Aspose.PSD؟**  
ج: استكشف خيارات الترخيص [هنا](https://purchase.aspose.com/buy) لاختيار الخطة الأنسب لاحتياجاتك.

**س: هل هناك منتدى مجتمع لدعم Aspose.PSD؟**  
ج: نعم، زر [منتدى Aspose.PSD](https://forum.aspose.com/c/psd/34) للحصول على دعم المجتمع والنقاشات.

**س: كيف يمكنني الحصول على ترخيص مؤقت لـ Aspose.PSD؟**  
ج: احصل على ترخيص مؤقت [هنا](https://purchase.aspose.com/temporary-license/) لأغراض الاختبار والتقييم.

---

**آخر تحديث:** 2025-12-25  
**تم الاختبار مع:** Aspose.PSD 24.11 لـ Java (أحدث نسخة وقت الكتابة)  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}