---
date: 2026-08-01
description: تعلم كيفية تصدير PSD إلى PNG ومعالجة تدفقات الصور غير المضغوطة باستخدام
  Aspose.PSD for Java.
keywords:
- export psd to png
- save psd as png
- java image manipulation
lastmod: 2026-08-01
linktitle: معالجة كائن تدفق الصورة غير المضغوطة في PSD - Java
og_description: تصدير PSD إلى PNG باستخدام Aspose.PSD for Java. تعلم كيفية معالجة
  تدفقات الصور غير المضغوطة، وإنشاء كائنات رسومات، وحفظ PNG بجودة عالية.
og_image_alt: 'Developer guide: Export PSD to PNG with uncompressed stream using Aspose.PSD
  Java'
og_title: تصدير PSD إلى PNG – دليل Java لتدفقات PSD غير المضغوطة
schemas:
- author: Aspose
  dateModified: '2026-08-01'
  description: Learn how to export PSD to PNG and handle uncompressed image streams
    with Aspose.PSD for Java.
  headline: Export PSD to PNG – Create PSD Graphics Object – Uncompressed Stream in
    Java
  type: TechArticle
- questions:
  - answer: Yes. After loading the PSD, retrieve the desired layer via `psdImage.getLayers().get_Item(index)`
      and pass that layer to the `Graphics` constructor.
    question: Can I use the graphics object to edit only one specific layer?
  - answer: Raw stores pixel data without any compression, so the resulting file is
      larger than a compressed PSD, but it guarantees 100 % pixel fidelity.
    question: Does the Raw compression method affect file size?
  - answer: Absolutely. After editing, call `psdImage.save("output.png", new PngOptions())`—this
      is the standard way to **export PSD to PNG** with lossless quality.
    question: Is it possible to export the edited PSD to another format (e.g., PNG)?
  - answer: Aspose.PSD for Java supports JDK 8 and later, including all LTS releases
      up to JDK 21.
    question: What Java version is required?
  - answer: Invoke `psdImage.dispose()` and close any streams (e.g., `ms.close()`)
      to free native memory and avoid leaks.
    question: How do I release resources after processing?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- export psd
- Aspose.PSD
- Java image processing
- uncompressed stream
- PSD graphics
title: تصدير PSD إلى PNG – إنشاء كائن رسومات PSD – تدفق غير مضغوط في Java
url: /ar/java/advanced-psd-layer-features-effects/handle-uncompressed-image-stream-object-psd/
weight: 26
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# تصدير PSD إلى PNG – إنشاء كائن رسومات PSD – تدفق غير مضغوط في Java

## المقدمة
في هذا الدليل خطوة بخطوة ستقوم **بتصدير PSD إلى PNG** أثناء العمل مع تدفق صورة غير مضغوط باستخدام Aspose.PSD for Java. سواءً كنت تقوم بأتمتة خط أنابيب التصميم أو بناء محرر مخصص، فإن القدرة على عرض ملف Photoshop دون فقدان الجودة أمر أساسي. سنبدأ بالإعداد المطلوب، ثم نتناول إنشاء كائن `Graphics`، وننتهي بتصدير PNG بدون فقدان. في النهاية، ستفهم لماذا يتعامل Aspose.PSD مع التدفقات الخام بكفاءة وكيفية دمجه في أي مشروع Java.

## إجابات سريعة
- **ماذا يعني “إنشاء كائن رسومات PSD”؟** يعني ذلك إنشاء سياق `Graphics` يتيح لك الرسم على صورة PSD أو تعديلها برمجياً.  
- **أي مكتبة تتعامل مع التدفقات غير المضغوطة؟** Aspose.PSD for Java توفر دعمًا كاملاً للبيانات الصورة الخام (غير المضغوطة).  
- **هل يمكنني تصدير PSD إلى PNG بعد التعديل؟** نعم—بمجرد حصولك على كائن `Graphics` يمكنك عرض PSD وحفظه كـ PNG في استدعاء واحد.  
- **هل أحتاج إلى ترخيص للتطوير؟** النسخة التجريبية المجانية تكفي للاختبار؛ يلزم الحصول على ترخيص تجاري للنشر في بيئات الإنتاج.  
- **هل التصدير بدون فقدان؟** تصدير PNG يحافظ على بيانات البكسل الأصلية، مما يوفر جودة بدون فقدان مع حجم ملف أصغر مقارنةً بـ PSD الخام.

## ما هو تصدير PSD إلى PNG؟
تصدير PSD إلى PNG يحول مستند Photoshop متعدد الطبقات إلى صورة نقطية ذات طبقة واحدة، غير مضغوطة، يمكن عرضها في أي متصفح ويب أو عارض صور. العملية تحتفظ بالشفافية، عمق اللون، وتأثيرات الطبقات مع حذف البيانات الوصفية الخاصة بـ Photoshop. كما تحافظ على ملف تعريف اللون الأصلي لضمان دقة الألوان.

## لماذا تستخدم Aspose.PSD for Java لمعالجة الصور؟
يدعم Aspose.PSD **أكثر من 50** تنسيق إدخال وإخراج—بما في ذلك PSD، PNG، JPEG، BMP، وTIFF—ويمكنه معالجة ملفات تحتوي على **أكثر من 200 طبقة** دون تحميل المستند بالكامل إلى الذاكرة. خيار الضغط `Raw` يخزن بيانات البكسل غير مضغوطة، مما يضمن دقة بكسل‑بكسل للتحرير أو الأرشفة اللاحقة.

## المتطلبات المسبقة
قبل الغوص في الكود، تأكد من وجود ما يلي:

- **مجموعة تطوير جافا (JDK)** – JDK 8 أو أحدث مثبت.  
- **Aspose.PSD for Java** – قم بتنزيل أحدث ملف JAR من صفحة الإصدار الرسمية: [Aspose.PSD Java download](https://releases.aspose.com/psd/java/). يمكنك أيضًا الوصول إليه عبر [this link](https://releases.aspose.com/psd/java/) أو صفحة [release page](https://releases.aspose.com/psd/java/). لمنتجات Aspose الأخرى، اضغط [here](https://releases.aspose.com/).  
- **بيئة تطوير متكاملة (IDE)** – IntelliJ IDEA أو Eclipse أو أي محرر متوافق مع Java.  
- **معرفة أساسية بجافا** – الإلمام بالفئات والطرق ومعالجة الاستثناءات.

مع توفر هذه المتطلبات، أنت جاهز للبدء في كتابة الكود.

## استيراد الحزم
فئة `Graphics` هي سطح الرسم في Aspose.PSD الذي يتيح لك عرض أو تعديل بيانات البكسل مباشرة. فئة `PsdImage` تمثل ملف PSD في الذاكرة، بينما تتحكم `PsdOptions` في كيفية حفظ الصورة.

```java
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.CompressionMethod;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PsdOptions;
import java.io.ByteArrayInputStream;
import java.io.ByteArrayOutputStream;
```

الآن، دعنا نفصل الكود إلى خطوات قابلة للفهم حتى تتمكن من المتابعة بسهولة. سنقوم بإعداد البيئة، تحميل ملف PSD، تعديلّه، وأخيرًا حفظ النتيجة.

## الخطوة 1: تحديد دليل المستند الخاص بك
قبل أي عمليات ملف، تحتاج إلى إخبار البرنامج بمكان البحث عن موارد PSD الخاصة بك. يُستخدم مسار الدليل هذا طوال الدرس.

```java
String dataDir = "Your Document Directory";
```

استبدل `"Your Document Directory"` بالمسار المطلق الذي يحتوي على `layers.psd`. جعل المسار قابلاً للتكوين يجعل الكود قابلًا لإعادة الاستخدام عبر المشاريع.

## الخطوة 2: إنشاء تدفق إخراج مصفوفة بايت
`ByteArrayOutputStream` هو تدفق Java يحتفظ بالبيانات في الذاكرة كمصفوفة بايت. يعمل كمنفذ مؤقت في الذاكرة للصورة المعدلة، مما يتيح لك التقاط البايتات الخام قبل كتابتها إلى القرص أو إرسالها عبر الشبكة.

```java
ByteArrayOutputStream ms = new ByteArrayOutputStream();
```

المتغير `ms` سيحتوي على بيانات الصورة غير المضغوطة بعد عملية `save`.

## الخطوة 3: تحميل ملف PSD
فئة `PsdImage` تقوم بتحميل ملف PSD إلى الذاكرة للمعالجة. تحويل الملف من القرص إلى كائن `PsdImage` يتيح لك تعديل محتواه. هذه الخطوة هي التي يقرأ فيها Aspose.PSD رأس الملف، الطبقات، والموارد.

```java
PsdImage psdImage = (PsdImage) Image.load(dataDir + "layers.psd");
```

إذا كان المسار غير صحيح، سيطرح Aspose.PSD استثناء `FileNotFoundException`، ويجب عليك معالجته في كود الإنتاج.

## الخطوة 4: إعداد PsdOptions للحفظ
`PsdOptions` يحدد معلمات الحفظ لملفات PSD. تعيين طريقة الضغط إلى `Raw` يعني أن بيانات البكسل يجب أن تُخزن بدون ضغط، مما يحافظ على كل بكسل كما هو في الذاكرة.

```java
PsdOptions saveOptions = new PsdOptions();
saveOptions.setCompressionMethod(CompressionMethod.Raw);
```

خيار `CompressionMethod.Raw` يخزن بيانات البكسل دون أي ضغط، وهو مثالي عندما تخطط لإجراء تعديلات إضافية لاحقًا.

## الخطوة 5: حفظ الصورة إلى تدفق الإخراج
الآن تقوم بحفظ الـ PSD (مع أي تعديلات) في `ByteArrayOutputStream` الذي أنشأته مسبقًا. طريقة `save` تحترم `PsdOptions` التي قمت بتكوينها.

```java
psdImage.save(ms, saveOptions);
```

في هذه المرحلة، يحتوي `ms` على التمثيل الثنائي الكامل للـ PSD غير المضغوط.

## الخطوة 6: إعادة ضبط تدفق الإخراج
بعد الكتابة، يكون مؤشر التدفق الداخلي في النهاية. إعادة ضبطه يعيد المؤشر إلى البداية حتى تتمكن من القراءة من البداية.

```java
ms.reset();
```

فكر في ذلك كإعادة رأس الشريط إلى البداية قبل التشغيل.

## الخطوة 7: تحميل الصورة التي تم إنشاؤها حديثًا
يمكنك الآن إنشاء كائن `PsdImage` جديد مباشرة من مصفوفة البايت. هذه الخطوة تتحقق من أن البيانات المحفوظة يمكن إعادة تحميلها دون فساد.

```java
PsdImage img = (PsdImage) Image.load(new ByteArrayInputStream(ms.toByteArray()));
```

إذا تم تحميل الصورة بنجاح، فأنت تعلم أن التدفق غير المضغوط تم كتابته بشكل صحيح.

## الخطوة 8: إنشاء كائن رسومات
فئة `Graphics` هي لوحة الرسم في Aspose.PSD. توفر طرقًا لرسم الأشكال، النص، وتطبيق الفلاتر مباشرة على مصفوفة بكسلات `PsdImage`.

```java
Graphics graphics = new Graphics(psdImage);
```

مع هذا الكائن `Graphics` يمكنك رسم محتوى جديد، مسح أجزاء، أو دمج طبقات إضافية.

## كيف يمكنني تصدير PSD إلى PNG باستخدام Aspose.PSD for Java؟
حمّل الـ PSD باستخدام `new PsdImage(dataDir + "layers.psd")`، أنشئ كائن `Graphics`، نفّذ أي رسومات تحتاجها، ثم استدعِ `psdImage.save("output.png", new PngOptions())`. هذه السلسلة تقوم بعرض الـ PSD المعدل وتكتب PNG غير مضغوط في خطوة واحدة، مستفيدةً من محرك التحويل المدمج في Aspose.PSD.

## تعديل طبقات PSD باستخدام كائن الرسومات
وجود كائن `Graphics` يمنحك تحكمًا على مستوى البكسل لكل طبقة. يمكنك رسم أشكال هندسية، عرض نص، أو تطبيق فلاتر مخصصة. نظرًا لأن سياق الرسومات يعمل على العرض النقطي للطبقة، فإن التغييرات تظهر فورًا عند حفظ الصورة.

## المشكلات الشائعة والحلول
- **NullPointerException عند تحميل الملف** – تحقق من مسار `dataDir` وتأكد من أن اسم الملف مطابق تمامًا، بما في ذلك حساسية الأحرف.  
- **إخراج مضغوط رغم استخدام Raw** – تأكد من استدعاء `saveOptions.setCompressionMethod(CompressionMethod.Raw);` **قبل** استدعاء `save`.  
- **كائن الرسومات يظهر فارغًا** – تأكد من أنك ترسم على كائن `PsdImage` الصحيح (الذي تم تحميله، وليس صورة جديدة فارغة).  
- **OutOfMemoryError في الملفات الكبيرة** – استخدم `PsdImage.load(dataDir, LoadOptions)` مع `loadOptions.setLoadMode(LoadMode.Memory)` لتدفق الملفات الكبيرة دون تحميل المستند بالكامل إلى الذاكرة.

## الأسئلة المتكررة
### ما هو Aspose.PSD؟
Aspose.PSD هي مكتبة Java تمكّن المطورين من إنشاء، تعديل، وتحويل ملفات Photoshop PSD برمجيًا دون الحاجة إلى Adobe Photoshop. تدعم القراءة والكتابة لملفات PSD، معالجة الطبقات، الأقنعة، القنوات، والموارد المختلفة، وتوفر واجهات برمجة تطبيقات للعمليات النقطية والمتجهة، مما يجعلها مناسبة لمعالجة الصور على الخادم وأتمتة المهام.

### كيف يمكنني تنزيل Aspose.PSD for Java؟
يمكنك تنزيله من صفحة الإصدار الرسمية: [Aspose.PSD Java download](https://releases.aspose.com/psd/java/).

### هل هناك نسخة تجريبية مجانية لـ Aspose.PSD؟
نعم، نسخة تجريبية كاملة الوظائف متاحة على نفس صفحة التنزيل. يمكن استخدامها لأغراض التطوير والتقييم.

### هل يمكنني الحصول على دعم لـ Aspose.PSD؟
بالطبع! يوفر منتدى دعم Aspose إجابات من فريق المنتج والمجتمع: [Aspose support forum](https://forum.aspose.com/c/psd/34).

### كيف يمكنني الحصول على ترخيص مؤقت لـ Aspose.PSD؟
يمكنك طلب ترخيص مؤقت مباشرةً من بوابة الترخيص الخاصة بـ Aspose، والتي توفر مفتاحًا محدودًا زمنيًا صالحًا لمدة 30 يومًا. يتيح لك ذلك تقييم جميع وظائف Aspose.PSD دون شراء ترخيص تجاري. بعد انتهاء الفترة التجريبية، يجب استبدال المفتاح المؤقت بترخيص دائم للاستمرار في استخدام المكتبة في بيئات الإنتاج. زر صفحة الترخيص المؤقت لتوليد المفتاح: [temporary license page](https://purchase.aspose.com/temporary-license/).

## الأسئلة المتكررة

**س: هل يمكنني استخدام كائن الرسومات لتعديل طبقة محددة واحدة فقط؟**  
ج: نعم. بعد تحميل الـ PSD، احصل على الطبقة المطلوبة عبر `psdImage.getLayers().get_Item(index)` ومرّر تلك الطبقة إلى مُنشئ `Graphics`.

**س: هل يؤثر أسلوب الضغط Raw على حجم الملف؟**  
ج: يخزن Raw بيانات البكسل دون أي ضغط، لذا يكون حجم الملف الناتج أكبر من PSD المضغوط، لكنه يضمن دقة 100 % للبكسل.

**س: هل من الممكن تصدير PSD المعدل إلى تنسيق آخر (مثل PNG)؟**  
ج: بالتأكيد. بعد التعديل، استدعِ `psdImage.save("output.png", new PngOptions())`—هذه هي الطريقة القياسية **لتصدير PSD إلى PNG** بجودة غير مضغوطة.

**س: ما إصدار Java المطلوب؟**  
ج: يدعم Aspose.PSD for Java JDK 8 وما بعده، بما في ذلك جميع إصدارات LTS حتى JDK 21.

**س: كيف يمكنني تحرير الموارد بعد المعالجة؟**  
ج: استدعِ `psdImage.dispose()` وأغلق أي تدفقات (مثل `ms.close()`) لتحرير الذاكرة الأصلية وتجنب التسريبات.

**آخر تحديث:** 2026-08-01  
**تم الاختبار مع:** Aspose.PSD for Java (latest release)  
**المؤلف:** Aspose  

{{< blocks/products/products-backtop-button >}}

## الدروس ذات الصلة

- [حفظ الصور إلى تدفق باستخدام Aspose.PSD for Java](/psd/java/advanced-techniques/save-images-to-stream/)
- [تصدير مجموعة طبقات PSD إلى صورة باستخدام Java](/psd/java/working-with-psd-files/export-psd-layer-group-to-image/)
- [إنشاء صورة باستخدام تدفق في Aspose.PSD for Java](/psd/java/image-editing/create-image-using-stream/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}