---
date: 2026-07-03
description: تعلم كيفية اقتصاص صورة في Java باستخدام Aspose.PSD for Java. يغطي هذا
  الدليل خطوة بخطوة لاقتصاص الصور تحميل ملفات PSD، ضبط قيم الإزاحة، وحفظ النتيجة.
keywords:
- crop image java
- how to crop image
- load psd file
- java image processing
- crop image left right
linktitle: اقتصاص الصورة بالإزاحات
schemas:
- author: Aspose
  dateModified: '2026-07-03'
  description: Learn how to crop image java using Aspose.PSD for Java. This step‑by‑step
    image cropping tutorial covers loading PSD files, setting shift values, and saving
    the result.
  headline: Crop Image Java by Shifts with Aspose.PSD
  type: TechArticle
- description: Learn how to crop image java using Aspose.PSD for Java. This step‑by‑step
    image cropping tutorial covers loading PSD files, setting shift values, and saving
    the result.
  name: Crop Image Java by Shifts with Aspose.PSD
  steps:
  - name: Load the Image
    text: '`Image` is the base class for all image types in Aspose.PSD. `RasterImage`
      represents a raster image and provides cropping capabilities.'
  - name: Cache Image Data
    text: '`cacheData()` loads the image data into memory for faster processing.'
  - name: Define Shift Values
    text: Specify the shift values for all four sides of the image (left, top, right,
      bottom) in pixels.
  - name: Apply Cropping
    text: '`crop(left, right, top, bottom)` trims the image by the specified pixel
      shifts on each side.'
  - name: Save the Results
    text: '`JpegOptions` defines JPEG encoding settings such as quality and color
      profile. Congratulations! You''ve successfully cropped an image using Aspose.PSD
      for Java.'
  type: HowTo
- questions:
  - answer: Yes, Aspose.PSD supports over 30 raster formats, including PSD, JPEG,
      PNG, BMP, TIFF, and GIF, ensuring broad compatibility.
    question: Is Aspose.PSD compatible with all image formats?
  - answer: Absolutely. After each `crop` call you receive a new image object, which
      you can crop again as needed.
    question: Can I apply multiple cropping operations to the same image?
  - answer: Yes, you can find support and engage with the community at [Aspose.PSD
      Forum](https://forum.aspose.com/c/psd/34).
    question: Is there a community forum for Aspose.PSD support?
  - answer: Visit [here](https://purchase.aspose.com/temporary-license/) to obtain
      a temporary license.
    question: How can I obtain a temporary license for Aspose.PSD?
  - answer: Explore the documentation and examples at [Aspose.PSD Java Documentation](https://reference.aspose.com/psd/java/).
    question: Are there sample projects showcasing Aspose.PSD functionalities?
  type: FAQPage
second_title: Aspose.PSD Java API
title: اقتصاص الصورة في Java باستخدام الإزاحات مع Aspose.PSD
url: /ar/java/image-editing/crop-image-by-shifts/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# قص الصورة في جافا بالإزاحات باستخدام Aspose.PSD

## مقدمة

في معالجة الصور بجافا، **crop image java** هو مطلب شائع لإعداد الرسومات أو الصور المصغرة أو أصول واجهة المستخدم. تجعل Aspose.PSD for Java هذه المهمة بسيطة من خلال توفير طريقة `crop` بسيطة تعمل على أي تنسيق نقطي مدعوم. في هذا الدرس ستتعلم كيفية تحميل ملف PSD، تعريف قيم الإزاحة للجهات اليسرى‑اليمنى‑العليا‑السفلى، تطبيق القص، وحفظ النتيجة—كل ذلك دون كتابة كود مخصص لمعالجة البكسل.

## إجابات سريعة
- **ما المكتبة التي تتعامل مع القص؟** Aspose.PSD for Java provides a built‑in `crop` method.  
- **هل أحتاج إلى ترخيص؟** A temporary license works for evaluation; a full license is required for production.  
- **الصيغ المدعومة؟** Over 30 raster formats, including PSD, JPEG, PNG, BMP, and TIFF.  
- **الحد الأقصى لحجم الملف؟** Handles files up to 2 GB without loading the entire image into memory.  
- **كم عدد أسطر الكود؟** Only five logical steps—load, cache, define shifts, crop, and save.

## ما هو crop image java؟
`crop image java` يشير إلى عملية قص صورة نقطية في تطبيق جافا. باستخدام Aspose.PSD، تُجرى العملية بواسطة طريقة `crop`، التي تقبل قيم الإزاحة لكل جانب من الصورة وتُعيد كائن صورة جديد.

## لماذا تستخدم Aspose.PSD لقص الصور؟
يدعم Aspose.PSD **30+** صيغة صورة ويمكنه معالجة ملفات PSD متعددة المئات من الصفحات مع استهلاك أقل من 150 ميغابايت من الذاكرة RAM، بفضل بنية التحميل الكسول. كما تضمن المكتبة نتائج دقيقة على مستوى البكسل، مع الحفاظ على الطبقات والأقنعة وملفات تعريف الألوان—وهو ما لا تستطيع العديد من مكتبات الصور العامة ضمانه.

## المتطلبات المسبقة

### مجموعة تطوير جافا (JDK)

تأكد من أن لديك أحدث نسخة من JDK مثبتة على نظامك. يمكنك تنزيلها من [here](https://www.oracle.com/java/technologies/javase-downloads.html).

### مكتبة Aspose.PSD لجافا

للبدء، ستحتاج إلى الحصول على مكتبة Aspose.PSD لجافا. انتقل إلى [download page](https://releases.aspose.com/psd/java/) وحمّل أحدث نسخة.

### بيئة التطوير المتكاملة (IDE)

اختر بيئة التطوير المتكاملة (IDE) المفضلة لديك لجافا، مثل Eclipse أو IntelliJ، لتجربة ترميز سلسة.

## كيف تقص صورة جافا؟

حمّل ملف المصدر الخاص بك، عرّف إزاحات البكسل لكل جانب، واستدعِ طريقة `crop`—يمكن كتابة سير العمل بالكامل في خمس أسطر مختصرة من الكود. عملية `crop` تُنشئ صورة جديدة تحتوي فقط على المنطقة التي حددتها، مع ترك الملف الأصلي دون تعديل.

### الخطوة 1: تحميل الصورة

`Image` هي الفئة الأساسية لجميع أنواع الصور في Aspose.PSD.  
`RasterImage` تمثل صورة نقطية وتوفر إمكانيات القص.

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.imageoptions.JpegOptions;
```

### الخطوة 2: تخزين بيانات الصورة مؤقتًا

`cacheData()` يحمل بيانات الصورة إلى الذاكرة لمعالجة أسرع.

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// Load an existing image into an instance of RasterImage class
RasterImage rasterImage = (RasterImage)Image.load(sourceFile);
```

### الخطوة 3: تعريف قيم الإزاحة

حدد قيم الإزاحة لجميع الجوانب الأربعة للصورة (اليسار، الأعلى، اليمين، الأسفل) بوحدة البكسل.

```java
if (!rasterImage.isCached()) {
  rasterImage.cacheData();
}
```

### الخطوة 4: تطبيق القص

`crop(left, right, top, bottom)` يقتص الصورة وفقًا لإزاحات البكسل المحددة على كل جانب.

```java
int leftShift = 10;
int rightShift = 10;
int topShift = 10;
int bottomShift = 10;
```

### الخطوة 5: حفظ النتائج

`JpegOptions` يحدد إعدادات ترميز JPEG مثل الجودة وملف تعريف اللون.

```java
rasterImage.crop(leftShift, rightShift, topShift, bottomShift);
```

تهانينا! لقد قمت بقص صورة بنجاح باستخدام Aspose.PSD لجافا.

## المشكلات الشائعة والحلول

- **الصورة لا تتغير:** تحقق من أن قيم الإزاحة موجبة ولا تتجاوز أبعاد الصورة الأصلية.  
- **OutOfMemoryError على ملفات كبيرة:** فعّل التخزين المؤقت كما هو موضح في الخطوة 2؛ هذا يجبر Aspose.PSD على استخدام ملف مؤقت بدلاً من الاحتفاظ بالصورة بالكامل في الذاكرة RAM.  
- **تغيير اللون بعد القص:** تأكد من الحفاظ على ملف تعريف اللون عن طريق استدعاء `image.save(..., new JpegOptions { ColorProfile = image.ColorProfile })` إذا كنت تحتاج إلى دقة لونية مطابقة.

## الأسئلة المتكررة

**س: هل Aspose.PSD متوافق مع جميع صيغ الصور؟**  
A: نعم، يدعم Aspose.PSD أكثر من 30 صيغة نقطية، بما في ذلك PSD، JPEG، PNG، BMP، TIFF، وGIF، مما يضمن توافقًا واسعًا.

**س: هل يمكنني تطبيق عمليات قص متعددة على نفس الصورة؟**  
A: بالتأكيد. بعد كل استدعاء لـ `crop` ستحصل على كائن صورة جديد، يمكنك قصه مرة أخرى حسب الحاجة.

**س: هل هناك منتدى مجتمع لدعم Aspose.PSD؟**  
A: نعم، يمكنك العثور على الدعم والتفاعل مع المجتمع في [Aspose.PSD Forum](https://forum.aspose.com/c/psd/34).

**س: كيف يمكنني الحصول على ترخيص مؤقت لـ Aspose.PSD؟**  
A: زر [here](https://purchase.aspose.com/temporary-license/) للحصول على ترخيص مؤقت.

**س: هل هناك مشاريع مثال تُظهر وظائف Aspose.PSD؟**  
A: استكشف الوثائق والأمثلة في [Aspose.PSD Java Documentation](https://reference.aspose.com/psd/java/).

---

**Last Updated:** 2026-07-03  
**Tested With:** Aspose.PSD 24.11 for Java  
**Author:** Aspose  

{{< blocks/products/products-backtop-button >}}

```java
String destName = dataDir + "CroppingByShifts_out.jpg";
rasterImage.save(destName, new JpegOptions());
```

## دروس ذات صلة

- [قص الصورة بالمستطيل في Aspose.PSD لجافا](/psd/java/image-editing/crop-image-by-rectangle/)
- [قص الصورة جافا - توسيع وقص الصور باستخدام Aspose.PSD لجافا](/psd/java/image-editing/expand-and-crop-images/)
- [تغيير حجم الصورة جافا - استخدام تعداد نوع التحجيم في Aspose.PSD لجافا](/psd/java/advanced-image-manipulation/resizing-with-resize-type-enumeration/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}