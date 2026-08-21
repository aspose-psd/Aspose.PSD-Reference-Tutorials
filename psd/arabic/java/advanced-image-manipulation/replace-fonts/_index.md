---
date: 2026-06-23
description: تعلم كيفية حفظ ملف PSD كـ PNG، استبدال الخطوط المفقودة، وتصدير الصور
  باستخدام Aspose.PSD for Java – التعامل بسرعة مع ملفات PSD التي تحتوي على خطوط مفقودة.
keywords:
- save psd as png
- how to replace fonts
- convert psd to bmp
- export psd to jpeg
- handle missing fonts psd
linktitle: استبدال الخطوط
schemas:
- author: Aspose
  dateModified: '2026-06-23'
  description: Learn how to save PSD as PNG, replace missing fonts, and export images
    using Aspose.PSD for Java – handle missing fonts PSD files quickly.
  headline: How to Save PSD as PNG and Replace Missing Fonts in Java with Aspose
  type: TechArticle
- questions:
  - answer: Yes. While the primary use‑case is PSD, Aspose.PSD also supports PNG,
      JPEG, BMP, and TIFF, allowing font replacement wherever text layers exist.
    question: Can I replace fonts in other image formats besides PSD?
  - answer: No. You can set any TrueType font you prefer, or omit the setting to let
      Aspose use its internal default.
    question: Is the default replacement font mandatory?
  - answer: A commercial license is required for production deployments. See the [purchase
      page](https://purchase.aspose.com/buy) for details.
    question: Are there licensing requirements for using Aspose.PSD?
  - answer: Absolutely. Aspose offers free temporary licenses for evaluation – visit
      the [temporary license page](https://purchase.aspose.com/temporary-license/).
    question: Can I obtain a temporary license for testing?
  - answer: 'The community forum is a great place to ask questions: [Aspose.PSD forum](https://forum.aspose.com/c/psd/34).'
    question: Where can I find additional support or discuss Aspose.PSD‑related issues?
  type: FAQPage
second_title: Aspose.PSD Java API
title: كيفية حفظ ملف PSD كـ PNG واستبدال الخطوط المفقودة في Java باستخدام Aspose
url: /ar/java/advanced-image-manipulation/replace-fonts/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# حفظ PSD كـ PNG – استبدال الخطوط المفقودة في Java

## مقدمة

إذا كنت بحاجة إلى **حفظ PSD كـ PNG** مع استبدال الخطوط المفقودة أو غير المرغوب فيها داخل ملف Photoshop (PSD)، فإن استبدال الخطوط في Aspose PSD يجعل العملية سهلة. في تطبيقات Java يمكنك تحميل ملف PSD، وإخبار Aspose بالخط الاحتياطي الذي تريد استخدامه، ثم تصدير الصورة المصححة بأي تنسيق تريده. يشرح هذا البرنامج التعليمي سير العمل الكامل — من إعداد المشروع إلى تصدير PNG المحدث — بحيث يمكنك التعامل مع سيناريوهات **missing fonts PSD** بثقة دون الحاجة إلى فتح Photoshop.

## إجابات سريعة
- **ما المكتبة التي تتعامل مع استبدال الخطوط؟** Aspose.PSD for Java  
- **كم من الوقت تستغرق عملية التنفيذ؟** حوالي 5‑10 دقائق للسيناريو الأساسي  
- **ما هو الخط المستخدم كبديل افتراضي؟** يمكنك تعيين أي خط TrueType، مثل “Arial”  
- **هل يمكنني الحفظ إلى صيغ أخرى غير PNG؟** نعم – يدعم PSD و JPEG و BMP والمزيد  
- **هل أحتاج إلى ترخيص للإنتاج؟** يلزم وجود ترخيص Aspose.PSD صالح للاستخدام غير التجريبي  

## ما هو استبدال خطوط Aspose PSD؟

استبدال خطوط Aspose PSD هو عملية تحديد خط بديل ستستخدمه المكتبة كلما صادفت خطًا مفقودًا أو غير مدعوم في ملف PSD. يضمن ذلك عرض طبقات النص بشكل صحيح دون تعديل يدوي في Photoshop ويسمح لك **بمعالجة missing fonts PSD** تلقائيًا.

## لماذا تستخدم Aspose.PSD للـ Java؟

توفر Aspose.PSD للـ Java حلاً شاملاً وعالي الأداء للعمل مع ملفات Photoshop مباشرة من كود Java، مما يلغي الحاجة إلى Photoshop نفسه. تدعم مجموعة واسعة من أنواع الطبقات، التأثيرات، وحجم الملفات الكبيرة مع توفير واجهات برمجة تطبيقات بسيطة لمهام مثل استبدال الخطوط، تحويل الصور، ومعالجة البيانات الوصفية.

- **معالجة PSD كاملة المميزات** – تدعم Aspose.PSD **أكثر من 30 نوع طبقة**، **أكثر من 20 تأثيرًا**، ويمكنها معالجة ملفات تصل إلى **2 GB** دون تحميل المستند بالكامل في الذاكرة.  
- **متعددة المنصات** – تعمل على أي نظام تشغيل يدعم Java 8+.  
- **بدون تبعيات خارجية** – تتعامل المكتبة مع استبدال الخطوط داخليًا، لذا لا تحتاج إلى شحن خطوط إضافية مع تطبيقك.  

## كيفية استبدال الخطوط المفقودة في PSD باستخدام Aspose PSD

لإستبدال الخطوط المفقودة، أولاً قم بتحميل ملف PSD مع تحديد خط احتياطي في خيارات التحميل، ثم قم بعملية العرض أو الحفظ. تقوم المكتبة تلقائيًا باستبدال الخطوط المفقودة بالخط الذي تحدده، مما يضمن أن النتيجة البصرية تتطابق مع توقعاتك دون تعديل يدوي.

## المتطلبات المسبقة

قبل أن نبدأ، تأكد من أن لديك:

- **Java Development Kit (JDK)** – الإصدار 8 أو أعلى مثبتًا.  
- **Aspose.PSD for Java** – حمّل أحدث ملف JAR من [صفحة الإصدار](https://releases.aspose.com/psd/java/).  
- **IDE** – IntelliJ IDEA أو Eclipse أو أي محرر تفضله.  

## استيراد الحزم

فئة `PsdImage` تمثل مستند Photoshop في الذاكرة، وتوفر الوصول إلى الطبقات، النص، وإمكانيات العرض. `PsdLoadOptions` تتحكم في طريقة قراءة الملف، بما في ذلك الخط الاحتياطي، بينما `SaveOptions` (أو الفئات الفرعية الخاصة بالتنسيق) تحدد كيفية كتابة الصورة.

```java
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import com.aspose.psd.imageoptions.PngOptions;
```

## الخطوة 1: تعيين دليل المستند

حدد المجلد الذي يحتوي على ملف PSD المصدر. استبدل العنصر النائب بالمسار الفعلي على جهازك.

كائن `File` يشير ببساطة إلى ملف PSD الذي تريد معالجته؛ لا يلزم أي تكوين إضافي هنا.  

```java
String dataDir = "Your Document Directory";
```

## الخطوة 2: تحميل الصورة بخط بديل

أنشئ مثيلًا من `PsdLoadOptions`، حدد الخط البديل الافتراضي (مثل **Arial**)، ثم حمّل ملف PSD. سيطبق Aspose الخط الاحتياطي تلقائيًا كلما صادف خطًا مفقودًا.

`PsdLoadOptions` يتيح لك تعريف سلوك التحميل، بما في ذلك الخط الاحتياطي الذي يستبدل أي خط مفقود أثناء مرحلة الاستيراد.  

```java
PsdLoadOptions psdLoadOptions = new PsdLoadOptions(); 
psdLoadOptions.setDefaultReplacementFont("Arial");

PsdImage psdImage = (PsdImage)Image.load(dataDir + "Cloud_AzPlat_Banner3A_SB_EN_US_160x600_chinese_font.psd", psdLoadOptions);
```

## الخطوة 3: حفظ الصورة المستبدلة كـ PNG

بعد استبدال الخطوط، يمكنك تصدير الصورة بأي تنسيق مدعوم. هنا نحفظها كـ PNG، لكن يمكنك أيضًا اختيار JPEG أو BMP أو حتى إعادتها كـ PSD.

طريقة `save` في `PsdImage` تقبل كائن `SaveOptions`؛ استخدام `PngOptions` يضمن أن الناتج هو PNG غير مضغوط مناسب للويب أو المعالجة الإضافية.  

```java
PngOptions pngOptions = new PngOptions();
psdImage.save(dataDir + "replaced_font.png", pngOptions);
```

## كيف أحفظ PSD كـ PNG بعد استبدال الخطوط؟

حمّل ملف PSD مع خط احتياطي، ثم استدعِ `psdImage.save("output.png", new PngOptions())`. هذه العملية ذات السطر الواحد تكتب PNG مكتمل العرض يعكس الخط المستبدل، مما يتيح لك تضمين الصورة في أي مكان دون القلق بشأن الخطوط المفقودة. تأكد من تطبيق الخط البديل قبل الحفظ، ويمكنك تعديل إعدادات ضغط PNG عبر كائن `PngOptions` للحصول على حجم ملف مثالي.

## المشكلات الشائعة والحلول

| المشكلة | السبب | الحل |
|-------|-------|-----|
| النص يظهر مشوّشًا بعد الاستبدال | خط الاستبدال لا يحتوي على الأحرف المطلوبة | اختر خطًا يدعم نطاق Unicode المطلوب (مثل “Arial Unicode MS”). |
| `OutOfMemoryError` على ملفات PSD الكبيرة | تحميل ملف عالي الدقة جدًا دون مساحة كافية في الذاكرة | زيادة حجم ذاكرة JVM (`-Xmx2g`) أو تحميل الصورة في وضع البث إذا كان متاحًا. |
| استثناء الترخيص | استخدام النسخة التجريبية في الإنتاج | تطبيق ترخيص دائم أو مؤقت صالح قبل تحميل الصورة. |

## الأسئلة المتكررة

**س: هل يمكنني استبدال الخطوط في صيغ صور أخرى غير PSD؟**  
ج: نعم. بينما الحالة الأساسية هي PSD، يدعم Aspose.PSD أيضًا PNG و JPEG و BMP و TIFF، مما يسمح باستبدال الخطوط حيثما توجد طبقات نصية.

**س: هل الخط البديل الافتراضي إلزامي؟**  
ج: لا. يمكنك تعيين أي خط TrueType تفضله، أو إهمال الإعداد للسماح لـ Aspose باستخدام الافتراضي الداخلي.

**س: هل هناك متطلبات ترخيص لاستخدام Aspose.PSD؟**  
ج: يتطلب ترخيص تجاري للنشر في بيئات الإنتاج. راجع [صفحة الشراء](https://purchase.aspose.com/buy) للتفاصيل.

**س: هل يمكنني الحصول على ترخيص مؤقت للاختبار؟**  
ج: بالطبع. تقدم Aspose تراخيص مؤقتة مجانية للتقييم – زر [صفحة الترخيص المؤقت](https://purchase.aspose.com/temporary-license/).

**س: أين يمكنني العثور على دعم إضافي أو مناقشة مشكلات Aspose.PSD؟**  
ج: منتدى المجتمع هو مكان ممتاز لطرح الأسئلة: [منتدى Aspose.PSD](https://forum.aspose.com/c/psd/34).

**س: كيف أتعامل مع ملفات PSD التي تحتوي على خطوط مفقودة متعددة؟**  
ج: حدد الخط البديل الافتراضي مرة واحدة (كما هو موضح) – سيُطبق على *جميع* الخطوط المفقودة أثناء عملية التحميل.

**س: هل يمكن استبدال الخطوط بعد حفظ الصورة؟**  
ج: يجب أن يحدث استبدال الخطوط أثناء مرحلة التحميل. لتغيير الخطوط لاحقًا، أعد تحميل PSD بخط بديل مختلف وأعد الحفظ.

## الخلاصة

لقد رأيت الآن سير عمل كامل لـ **حفظ PSD كـ PNG** في Java — من استيراد الفئات الصحيحة، تكوين خط احتياطي، تحميل PSD، إلى تصدير PNG المصحح. دمج هذا النمط في خطوط معالجة الصور الخاصة بك يضمن تناسق الطباعة عبر جميع أصول PSD الخاصة بك و**معالجة missing fonts PSD** تلقائيًا.

**آخر تحديث:** 2026-06-23  
**تم الاختبار مع:** Aspose.PSD for Java 24.12 (latest at time of writing)  
**المؤلف:** Aspose

## دروس ذات صلة

- [إعدادات استبدال الخطوط المفقودة في Aspose.PSD للـ Java](/psd/java/advanced-techniques/settings-replacing-missing-fonts/)
- [حفظ PSD كـ PNG وتطبيق ظل التقديم في Aspose.PSD للـ Java](/psd/java/advanced-image-manipulation/rendering-drop-shadow/)
- [كيفية تحويل PSD إلى PNG وتغيير الحجم بنسبة متناسبة مع Aspose.PSD للـ Java](/psd/java/advanced-image-manipulation/resize-image-proportionally/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< blocks/products/products-backtop-button >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}