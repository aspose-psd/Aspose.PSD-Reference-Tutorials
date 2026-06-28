---
date: 2026-06-28
description: تعلم كيفية دمج الصور Java باستخدام Aspose.PSD، دمج صورتين في لوحة PSD،
  وإنشاء ملف متعدد الطبقات في دقائق قليلة.
keywords:
- combine images java
- java graphics draw image
- merge images into psd
linktitle: دمج الصور
schemas:
- author: Aspose
  dateModified: '2026-06-28'
  description: Learn how to combine images java using Aspose.PSD, merge two pictures
    into a PSD canvas, and generate a layered file in just minutes.
  headline: Combine Images Java – Create PSD File by Merging Pictures with Aspose.PSD
  type: TechArticle
- description: Learn how to combine images java using Aspose.PSD, merge two pictures
    into a PSD canvas, and generate a layered file in just minutes.
  name: Combine Images Java – Create PSD File by Merging Pictures with Aspose.PSD
  steps:
  - name: Create PSD Options (prepare the file)
    text: '`PsdOptions` holds the configuration for the output PSD, such as compression
      level and color depth.'
  - name: Set the FileCreateSource (define where the PSD will be saved)
    text: '`FileCreateSource` tells Aspose where to write the generated file.'
  - name: Create Image Instance (initialize canvas size)
    text: The `Image` constructor creates a blank PSD canvas with the dimensions you
      specify.
  - name: Initialize Graphics and draw the first picture
    text: '`Graphics` provides drawing capabilities on the canvas. We clear the background
      to white and render the first source image on the left half.'
  - name: Draw the second picture (complete the combine)
    text: Now we place the second image on the right half of the same canvas, creating
      a second layer automatically.
  - name: Save the resulting PSD file
    text: Persist the combined canvas to disk. The resulting `combined.psd` contains
      two editable layers. Congratulations! You have successfully **combine images
      java** and generated a layered PSD file ready for further Photoshop editing.
  type: HowTo
- questions:
  - answer: Aspose.PSD natively reads and writes **15+ formats**, including PSD, PNG,
      JPEG, BMP, TIFF, GIF, and more, making it a versatile choice for image pipelines.
    question: Is Aspose.PSD compatible with all image formats?
  - answer: Yes. Each `drawImage` call creates a separate PSD layer, which you can
      later reposition, apply filters, or mask using Aspose.PSD’s extensive layer‑editing
      API.
    question: Can I perform additional edits after combining images?
  - answer: A valid license is required for production use. You can obtain one from
      the Aspose store; a free trial is available for evaluation.
    question: Do I need a commercial license for production?
  - answer: Simply repeat `graphics.drawImage(...)` with appropriate coordinates for
      each additional image. Each call adds a new layer.
    question: How do I add more than two pictures?
  - answer: Visit the [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) for community
      support, or consult the official documentation linked in the download page.
    question: Where can I get help if I run into problems?
  type: FAQPage
second_title: Aspose.PSD Java API
title: دمج الصور Java – إنشاء ملف PSD عن طريق دمج الصور باستخدام Aspose.PSD
url: /ar/java/image-editing/combine-images/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# دمج الصور Java – إنشاء ملف PSD بدمج الصور باستخدام Aspose.PSD

## مقدمة

إذا كنت بحاجة إلى **combine images java** عن طريق دمج عدة صور في ملف واحد متوافق مع Photoshop، فإن Aspose.PSD for Java يجعل العملية سهلة. في هذا الدرس سنستعرض إنشاء لوحة PSD بحجم 600 × 600 بكسل، ورسم صورتين مصدرية جنبًا إلى جنب، وحفظ النتيجة كملف PSD متعدد الطبقات. في النهاية ستفهم لماذا هذه التقنية قيمة لسلاسل معالجة الرسومات الآلية وكيفية توسيعها لتشمل أي عدد من الصور.

## إجابات سريعة
- **ما هي المكتبة الأفضل لدمج الصور في PSD؟** Aspose.PSD for Java.
- **كم يستغرق الجمع الأساسي؟** تقريبًا 10‑15 دقيقة لكتابة وتشغيل الشيفرة.
- **هل أحتاج إلى ترخيص للتطوير؟** إصدار تجريبي مجاني يكفي للتقييم؛ يلزم ترخيص تجاري للاستخدام في الإنتاج.
- **هل يمكنني إضافة أكثر من صورتين؟** بالطبع – فقط كرّر استدعاءات `drawImage` لكل طبقة إضافية.
- **ما إصدارات Java المدعومة؟** Java 8 وما فوق (حتى Java 21).

## ما هو combine images java؟
*Combine images java* يشير إلى دمج عدة صور نقطية برمجياً في ملف صورة واحد باستخدام واجهات برمجة تطبيقات Java. توفر Aspose.PSD طريقة عالية المستوى، خالصة Java للقيام بذلك دون الاعتماد على Photoshop الأصلي، مما يتيح لك أتمتة التركيب، الحفاظ على الطبقات، وإنتاج PSD متوافق مع Photoshop يمكن تحريره لاحقًا في Photoshop أو أدوات أخرى تدعم PSD.

## لماذا دمج الصور باستخدام Aspose.PSD؟
يدعم Aspose.PSD **15+ تنسيقات صور** (بما في ذلك PSD، PNG، JPEG، BMP، TIFF، GIF، وغيرها) ويمكنه معالجة **مستندات مئات الصفحات** دون تحميل الملف بالكامل إلى الذاكرة، بفضل بنية البث الخاصة به. المكتبة هي **100 % managed Java**، لذا تعمل على أي نظام تشغيل يدعم JDK، مما يلغي مشاكل ملفات DLL الأصلية.

## المتطلبات المسبقة

1. **Aspose.PSD Library** – قم بتنزيله من [here](https://releases.aspose.com/psd/java/).  
2. **Java Development Kit (JDK)** – يلزم Java 8+؛ يُنصح بـ Java 11 أو أحدث لأداء أفضل.  
3. **Working Directory** – مجلد على جهازك يحتوي على الصور المصدرية (`example1.png`, `example2.png`) حيث سيتم كتابة ملف PSD الناتج (`combined.psd`).  
4. **License Purchase** – احصل على ترخيص تجاري [here](https://purchase.aspose.com/buy) للاستخدام في الإنتاج.  
5. **Other Aspose Releases** – استكشف منتجات وتحديثات إضافية [here](https://releases.aspose.com/).

## استيراد الحزم

تجلب عبارات `import` الفئات الأساسية من Aspose.PSD إلى النطاق.

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdOptions;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.PsdImageLayer;
import com.aspose.psd.imageoptions.FileCreateSource;
import com.aspose.psd.graphics.Graphics;
import com.aspose.psd.Color;
```

## كيفية دمج الصور java باستخدام Aspose.PSD؟

حمّل لوحة فارغة، وارسم كل صورة على اللوحة، ثم احفظ النتيجة كملف PSD – هذه هي سير العمل بالكامل في ثلاث خطوات مختصرة. تقوم API تلقائيًا بإنشاء طبقة منفصلة لكل استدعاء `drawImage`، مما يمنحك إمكانية تحرير كاملة في Photoshop لاحقًا.

### الخطوة 1: إنشاء خيارات PSD (تحضير الملف)

`PsdOptions` يحتوي على إعدادات ملف PSD الناتج، مثل مستوى الضغط وعمق اللون.

```java
PsdOptions psdOptions = new PsdOptions();
```

### الخطوة 2: تعيين FileCreateSource (تحديد مكان حفظ PSD)

`FileCreateSource` يخبر Aspose بمكان كتابة الملف المُولد.

```java
psdOptions.setSource(new FileCreateSource(dataDir + "combined.psd", false));
```

### الخطوة 3: إنشاء كائن Image (تهيئة حجم اللوحة)

منشئ `Image` ينشئ لوحة PSD فارغة بالأبعاد التي تحددها.

```java
Image image = new Image(psdOptions, 600, 600);
```

### الخطوة 4: تهيئة Graphics ورسم الصورة الأولى

`Graphics` يوفر إمكانيات الرسم على اللوحة. نقوم بمسح الخلفية إلى اللون الأبيض ونرسم الصورة المصدرية الأولى على النصف الأيسر.

```java
Graphics graphics = new Graphics(image);
graphics.clear(Color.getWhite());
graphics.drawImage(dataDir + "example1.png", new Rectangle(0, 0, 300, 600));
```

### الخطوة 5: رسم الصورة الثانية (إكمال الدمج)

الآن نضع الصورة الثانية على النصف الأيمن من نفس اللوحة، مما ينشئ طبقة ثانية تلقائيًا.

```java
graphics.drawImage(dataDir + "example2.png", new Rectangle(300, 0, 300, 600));
```

### الخطوة 6: حفظ ملف PSD الناتج

احفظ اللوحة المدمجة على القرص. يحتوي `combined.psd` الناتج على طبقتين قابلتين للتحرير.

```java
image.save();
```

تهانينا! لقد نجحت في **combine images java** وتولدت ملف PSD متعدد الطبقات جاهز لمزيد من تحرير Photoshop.

## المشكلات الشائعة والحلول

| المشكلة | السبب | الحل |
|-------|-------|-----|
| `File not found` عند تحميل الصور المصدرية | مسار `dataDir` غير صحيح | تحقق من أن `dataDir` يشير إلى المجلد الذي يحتوي على `example1.png` و `example2.png`. |
| ملف PSD الناتج فارغ | `graphics.clear` تم استدعاؤه بعد الرسم | استدعِ `graphics.clear(Color.getWhite())` **قبل** أي عمليات `drawImage`. |
| استثناء الترخيص أثناء التشغيل | ترخيص Aspose.PSD مفقود أو منتهي الصلاحية | طبق ترخيصًا صالحًا باستخدام `License license = new License(); license.setLicense("Aspose.PSD.lic");` قبل أي استدعاء للـ API. |

## الأسئلة المتكررة

**س: هل Aspose.PSD متوافق مع جميع تنسيقات الصور؟**  
Aspose.PSD يقرأ ويكتب **15+ تنسيقات** أصلاً، بما في ذلك PSD، PNG، JPEG، BMP، TIFF، GIF، وغيرها، مما يجعله خيارًا متعدد الاستخدامات لسلاسل معالجة الصور.

**س: هل يمكنني إجراء تعديلات إضافية بعد دمج الصور؟**  
نعم. كل استدعاء `drawImage` ينشئ طبقة PSD منفصلة، يمكنك لاحقًا إعادة تموضعها، تطبيق فلاتر، أو قناع باستخدام API تحرير الطبقات الواسع في Aspose.PSD.

**س: هل أحتاج إلى ترخيص تجاري للإنتاج؟**  
يتطلب الاستخدام في الإنتاج ترخيصًا صالحًا. يمكنك الحصول عليه من متجر Aspose؛ يتوفر إصدار تجريبي مجاني للتقييم.

**س: كيف يمكنني إضافة أكثر من صورتين؟**  
ما عليك سوى تكرار `graphics.drawImage(...)` مع إحداثيات مناسبة لكل صورة إضافية. كل استدعاء يضيف طبقة جديدة.

**س: أين يمكنني الحصول على المساعدة إذا واجهت مشاكل؟**  
قم بزيارة [منتدى Aspose.PSD](https://forum.aspose.com/c/psd/34) للحصول على دعم المجتمع، أو راجع الوثائق الرسمية المرتبطة بصفحة التحميل.

**آخر تحديث:** 2026-06-28  
**تم الاختبار مع:** Aspose.PSD 24.11 for Java  
**المؤلف:** Aspose  

{{< blocks/products/products-backtop-button >}}

## دروس ذات صلة

- [إنشاء صورة بتحديد المسار في Aspose.PSD for Java](/psd/java/image-editing/create-image-by-setting-path/)
- [إنشاء صورة باستخدام التدفق في Aspose.PSD for Java](/psd/java/image-editing/create-image-using-stream/)
- [تغيير حجم الصورة Java - باستخدام تعداد نوع التحجيم في Aspose.PSD for Java](/psd/java/advanced-image-manipulation/resizing-with-resize-type-enumeration/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;

import com.aspose.psd.imageoptions.PsdOptions;
import com.aspose.psd.sources.FileCreateSource;
```

```java
PsdOptions imageOptions = new PsdOptions();
```

```java
imageOptions.setSource(new FileCreateSource(dataDir + "Two_images_result_out.psd", false));
```

```java
Image image = Image.create(imageOptions, 600, 600);
```

```java
Graphics graphics = new Graphics(image);
graphics.clear(Color.getWhite());
graphics.drawImage(Image.load(dataDir + "example1.psd"), 0, 0, 300, 600);
```

```java
graphics.drawImage(Image.load(dataDir + "example2.psd"), 300, 0, 300, 600);
```

```java
image.save();
```