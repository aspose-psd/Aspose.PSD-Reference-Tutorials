---
date: 2026-05-19
description: تعلم كيفية تحويل PSD إلى JPEG وتدوير الصورة 270 درجة باستخدام Aspose.PSD
  للـ Java. يوضح هذا الدليل كيفية تدوير ملفات PSD، وعكس الصور، وتحويل PSD إلى JPEG.
keywords:
- convert psd to jpeg
- how to rotate psd
- flip image java
- rotate psd layer
- rotate image without photoshop
linktitle: تدوير الصورة 270 درجة
schemas:
- author: Aspose
  dateModified: '2026-05-19'
  description: Learn how to convert PSD to JPEG and rotate image 270 degrees using
    Aspose.PSD for Java. This guide shows how to rotate PSD files, flip images, and
    convert PSD to JPEG.
  headline: Convert PSD to JPEG & Rotate 270° with Aspose.PSD for Java
  type: TechArticle
- description: Learn how to convert PSD to JPEG and rotate image 270 degrees using
    Aspose.PSD for Java. This guide shows how to rotate PSD files, flip images, and
    convert PSD to JPEG.
  name: Convert PSD to JPEG & Rotate 270° with Aspose.PSD for Java
  steps:
  - name: Load the PSD File
    text: '`Image` is Aspose.PSD''s core class that represents a single PSD document
      in memory. Instantiating it reads only the header information, keeping memory
      usage low.'
  - name: Rotate the Image 270 Degrees
    text: '`rotateFlip` performs the specified rotation and optional flip on the image.
      `RotateFlipType.Rotate270FlipNone` rotates the canvas 270 degrees clockwise
      while leaving the image orientation unchanged. > **Pro tip:** If you also need
      to flip the image horizontally or vertically, choose a different `Ro'
  - name: Convert PSD to JPEG and Save
    text: '`JpegOptions` defines JPEG‑specific parameters such as compression quality.
      The `save` method writes the transformed image to disk in the desired format.
      The file `RotatedImage_out.jpg` now contains the original PSD content rotated
      270 degrees and saved as a JPEG.'
  type: HowTo
- questions:
  - answer: Yes, Aspose.PSD supports PSD, JPEG, PNG, BMP, GIF, TIFF, and many other
      raster formats.
    question: Is Aspose.PSD compatible with different image formats?
  - answer: Absolutely! While `RotateFlipType` provides common angles, you can chain
      multiple calls or use transformation matrices for arbitrary angles.
    question: Can I apply custom rotations, not just predefined flips?
  - answer: Replace `JpegOptions` with `PngOptions` (or the appropriate options class)
      in the `save` method.
    question: How do I convert the rotated PSD to another format, such as PNG?
  - answer: For community help, visit the [Aspose.PSD Forum](https://forum.aspose.com/c/psd/34).
    question: Where can I find additional support or assistance?
  - answer: Yes, you can explore Aspose.PSD with a [free trial](https://releases.aspose.com/).
    question: Is there a free trial available?
  type: FAQPage
second_title: Aspose.PSD Java API
title: تحويل PSD إلى JPEG وتدوير 270° باستخدام Aspose.PSD للـ Java
url: /ar/java/advanced-image-manipulation/rotate-image/
weight: 19
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# تحويل PSD إلى JPEG وتدوير الصورة 270 درجة باستخدام Aspose.PSD للـ Java

## مقدمة

في هذا **دليل معالجة الصور Java**، ستتعلم كيفية **تحويل PSD إلى JPEG** مع تدوير الصورة 270 درجة باستخدام Aspose.PSD للـ Java. سواءً كنت تبني خط أنابيب معالجة دفعية، أو محررًا على الويب، أو أداة سطح مكتب، فإن المكتبة تتيح لك التعامل مع طبقات PSD دون الحاجة إلى Photoshop. سنغطي أيضًا القلب الاختياري ونظهر التدفق الكامل من تحميل ملف PSD إلى حفظه كـ JPEG.

## إجابات سريعة
- **ما المكتبة التي تتعامل مع التدوير؟** Aspose.PSD for Java  
- **ما زاوية التدوير التي يستخدمها المثال؟** 270 degrees  
- **هل يمكنني أيضًا قلب الصورة؟** Yes – use `RotateFlipType` options like `Rotate90FlipX`  
- **كيف أحفظ النتيجة؟** In the example we save as JPEG using `JpegOptions`  
- **هل أحتاج إلى ترخيص للإنتاج؟** A valid Aspose.PSD license is required for commercial use  

## ما هو “تدوير الصورة 270 درجة”؟
تدوير الصورة 270 درجة يعني تحويل الصورة بمقدار ثلاثة أرباع دورة كاملة باتجاه عقارب الساعة (أو 90 درجة عكس اتجاه عقارب الساعة). غالبًا ما يعيد هذا الاتجاه تخطيط البورتريه الأصلي بعد التحولات السابقة، ويُستخدم عادةً عندما تُلتقط الصور في وضعية أفقية ولكن تحتاج إلى عرضها في وضعية عمودية. النتيجة هي صورة موجهة بشكل صحيح دون فقدان الجودة.

## لماذا نستخدم Aspose.PSD لهذه المهمة؟
يدعم Aspose.PSD **أكثر من 50 تنسيقًا للإدخال والإخراج** — بما في ذلك PSD و JPEG و PNG و BMP و GIF و TIFF — ويمكنه معالجة ملفات تصل إلى **2 GB** دون تحميل المستند بالكامل في الذاكرة. تعمل الـ API على أي بيئة تشغيل Java (JDK 8+) ولا تتطلب تثبيت Photoshop أصلي، وتوفر استدعاءً واحدًا `rotateFlip` يتعامل مع كل من التدوير والقلب في خطوة واحدة.

## المتطلبات المسبقة

قبل أن تبدأ، تأكد من أن لديك:

- **Aspose.PSD for Java** مكتبة مثبتة. يمكنك تنزيلها وعرض مرجع الـ API الكامل [هنا](https://reference.aspose.com/psd/java/).  
- بيئة تطوير Java (JDK 8 أو أعلى).  
- ملف PSD تجريبي تريد تدويره. قم بتحديث المتغير `sourceFile` في الكود بالمسار الصحيح لملفك.

## استيراد الحزم

الفئات `Image` و `RotateFlipType` و `JpegOptions` مطلوبة لتحميل الملف وتحويله وحفظه.  
`Image` هي الفئة الأساسية التي تمثل مستند PSD في الذاكرة.  
`RotateFlipType` تُعدد عمليات التدوير والقلب المدعومة.  
`JpegOptions` تُكوّن إعدادات إخراج JPEG مثل الجودة.

```java
import com.aspose.psd.Image;
import com.aspose.psd.RotateFlipType;

import com.aspose.psd.imageoptions.JpegOptions;
```

## كيفية تحويل PSD إلى JPEG بعد التدوير؟

حمّل ملف PSD المصدر، طبّق تدويرًا بزاوية 270 درجة، واحفظه فورًا كـ JPEG. هذا التدفق المكوّن من ثلاث خطوات يُنفّذ في أقل من ثانية للصور ذات 10 ميغابكسل تقريبًا على معالج حديث، مما يجعله مثاليًا للوظائف الدفعية عالية الإنتاجية. من خلال معالجة البيانات الضرورية فقط للصورة، يبقى استهلاك الذاكرة منخفضًا، ويحافظ JPEG الناتج على جودة الصورة مع تقليل حجم الملف.

### الخطوة 1: تحميل ملف PSD

`Image` هي الفئة الأساسية في Aspose.PSD التي تمثل مستند PSD واحد في الذاكرة. عند إنشاء كائن منها يتم قراءة معلومات الرأس فقط، مما يحافظ على انخفاض استهلاك الذاكرة.

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";
Image image = Image.load(sourceFile);
```

### الخطوة 2: تدوير الصورة 270 درجة

`rotateFlip` تنفّذ التدوير المحدد والقلب الاختياري على الصورة. `RotateFlipType.Rotate270FlipNone` يدور القماش 270 درجة باتجاه عقارب الساعة مع ترك اتجاه الصورة دون تغيير.

```java
image.rotateFlip(RotateFlipType.Rotate270FlipNone);
```

> **نصيحة احترافية:** إذا كنت بحاجة أيضًا إلى قلب الصورة أفقيًا أو عموديًا، اختر `RotateFlipType` مختلفًا مثل `Rotate90FlipX` أو `Rotate180FlipY`.

### الخطوة 3: تحويل PSD إلى JPEG وحفظه

`JpegOptions` تُعرّف معلمات JPEG الخاصة مثل جودة الضغط. طريقة `save` تكتب الصورة المُحوّلة إلى القرص بالتنسيق المطلوب.

```java
String destName = dataDir + "RotatedImage_out.jpg";
image.save(destName, new JpegOptions());
```

الملف `RotatedImage_out.jpg` الآن يحتوي على محتوى PSD الأصلي مدورًا بزاوية 270 درجة ومُحفظًا كـ JPEG.

## المشكلات الشائعة والحلول

| المشكلة | الحل |
|-------|----------|
| **الصورة تظهر مقلوبة رأسًا على عقب** | Verify you used `Rotate270FlipNone`. For a 90‑degree clockwise rotation use `Rotate90FlipNone`. |
| **ملف الإخراج تالف** | Ensure the destination folder exists and you have write permissions. |
| **استثناء الترخيص** | Install a temporary or permanent Aspose.PSD license before loading the image in production. |

## الأسئلة المتكررة

**س: هل Aspose.PSD متوافق مع صيغ صور مختلفة؟**  
ج: نعم، يدعم Aspose.PSD صيغ PSD و JPEG و PNG و BMP و GIF و TIFF والعديد من صيغ الرسوم النقطية الأخرى.

**س: هل يمكنني تطبيق تدويرات مخصصة، وليس فقط القلب المسبق التعريف؟**  
ج: بالتأكيد! بينما توفر `RotateFlipType` الزوايا الشائعة، يمكنك ربط عدة استدعاءات أو استخدام مصفوفات التحويل للزوايا العشوائية.

**س: كيف أحول الـ PSD المدور إلى صيغة أخرى، مثل PNG؟**  
ج: استبدل `JpegOptions` بـ `PngOptions` (أو الفئة المناسبة) في طريقة `save`.

**س: أين يمكنني العثور على دعم إضافي أو مساعدة؟**  
ج: للحصول على مساعدة المجتمع، زر [Aspose.PSD Forum](https://forum.aspose.com/c/psd/34).

**س: هل هناك نسخة تجريبية مجانية متاحة؟**  
ج: نعم، يمكنك استكشاف Aspose.PSD عبر [free trial](https://releases.aspose.com/).

**س: كيف أحصل على ترخيص مؤقت؟**  
ج: إذا كنت بحاجة إلى ترخيص مؤقت، يمكنك الحصول عليه [here](https://purchase.aspose.com/temporary-license/).

---

**آخر تحديث:** 2026-05-19  
**تم الاختبار باستخدام:** Aspose.PSD for Java 24.12  
**المؤلف:** Aspose  

{{< blocks/products/products-backtop-button >}}

## دروس ذات صلة

- [تحويل PSD إلى صيغ صور نقطية باستخدام Aspose.PSD للـ Java](/psd/java/advanced-techniques/convert-psd-to-raster-formats/)
- [تحويل PSD إلى PNG وتدوير الطبقات في ملفات PSD باستخدام Java](/psd/java/advanced-psd-layer-features-effects/rotate-layers-psd-files/)
- [كيفية تدوير الصورة في Java باستخدام Aspose.PSD](/psd/java/advanced-image-manipulation/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}