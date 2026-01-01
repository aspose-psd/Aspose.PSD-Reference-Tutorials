---
date: 2026-01-01
description: أتقن معالجة الصور في جافا من خلال تعلم كيفية قص الصورة باستخدام Aspose.PSD
  لجافا. دليل شامل لتعديل الصور بسلاسة.
linktitle: Crop Image by Shifts
second_title: Aspose.PSD Java API
title: معالجة الصور في جافا – قص الصورة بالإزاحات باستخدام Aspose.PSD
url: /ar/java/image-editing/crop-image-by-shifts/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# معالجة الصور في جافا – قص الصورة بالتحولات باستخدام Aspose.PSD

## المقدمة

إذا كنت تعمل على **java image processing**، ستكتشف سريعًا أن القص الدقيق هو عنصر أساسي لأي سير عمل رسومي. سواء كنت بحاجة إلى قص الحدود، أو إزالة الخلفية غير المرغوب فيها، أو إعداد الأصول للتسليم عبر الويب، فإن معرفة **how to crop image** برمجيًا توفر ساعات لا تحصى من العمل اليدوي. في هذا الدرس سنستعرض قص صورة نقطية عن طريق تحديد قيم التحول لكل جانب، باستخدام مكتبة **Aspose.PSD for Java** القوية. في النهاية ستكون قادرًا على **use the crop method** بثقة وحتى **optimize image cropping** لأداء أفضل.

## إجابات سريعة
- **ما المكتبة التي تتعامل مع java image processing؟** Aspose.PSD for Java  
- **ما الطريقة التي تقص صورة نقطية؟** `RasterImage.crop(left, right, top, bottom)`  
- **هل أحتاج إلى تخزين البيانات مؤقتًا أولاً؟** Yes – caching improves speed for large PSD files  
- **هل يمكنني تعيين هوامش قص مخصصة؟** Absolutely – specify left, right, top, and bottom shifts  
- **ما صيغ الإخراج المدعومة؟** JPEG, PNG, BMP, and many more via `ImageOptions`

## ما هو java image processing؟
يشير java image processing إلى معالجة صور البت‌ماب والرسومات المتجهية باستخدام واجهات برمجة تطبيقات مبنية على Java. تشمل المهام تغيير الحجم، الترشيح، تحويل الصيغ، وتعديلات **image cropping margins** — جميعها يمكن أتمتتها في تطبيقات الخادم أو سطح المكتب.

## لماذا تستخدم Aspose.PSD لمعالجة الصور في java؟
توفر Aspose.PSD حلاً مكتوبًا بالكامل بلغة Java يفهم ملفات PSD المتوافقة مع Photoshop، الطبقات، القنوات، والأقنعة. يلغي الحاجة إلى المكتبات الأصلية، يعمل عبر الأنظمة، ويوفر واجهة برمجة تطبيقات **crop raster image** بسيطة يمكن دمجها بسهولة مع مشاريع Java الحالية.

## المتطلبات المسبقة

- **Java Development Kit (JDK)** – قم بتنزيل أحدث نسخة من [here](https://www.oracle.com/java/technologies/javase-downloads.html).  
- **Aspose.PSD for Java Library** – احصل على أحدث إصدار من [download page](https://releases.aspose.com/psd/java/).  
- **Integrated Development Environment (IDE)** – Eclipse، IntelliJ IDEA، أو أي محرر تفضله.

## استيراد الحزم

في مشروع Java الخاص بك، استورد الفئات اللازمة لبدء سير عمل القص:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.imageoptions.JpegOptions;
```

## دليل خطوة بخطوة

### الخطوة 1: تحميل الصورة (how to crop image)

أولاً، قم بتحميل ملف PSD المصدر إلى كائن `RasterImage`. يمنحك ذلك وصولًا مباشرًا إلى مستوى البكسل.

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// Load an existing image into an instance of RasterImage class
RasterImage rasterImage = (RasterImage)Image.load(sourceFile);
```

### الخطوة 2: تخزين بيانات الصورة مؤقتًا (optimize image cropping)

تخزين بيانات الصورة مؤقتًا في الذاكرة يقلل من عبء الإدخال/الإخراج عند تنفيذ عمليات متعددة مثل القص.

```java
if (!rasterImage.isCached()) {
  rasterImage.cacheData();
}
```

### الخطوة 3: تحديد هوامش القص (image cropping margins)

حدد عدد البكسلات التي تريد قصها من كل جانب. اضبط هذه القيم لتتناسب مع **image cropping margins** المطلوبة.

```java
int leftShift = 10;
int rightShift = 10;
int topShift = 10;
int bottomShift = 10;
```

### الخطوة 4: تطبيق القص (use crop method)

الآن استدعِ طريقة `crop` مع قيم التحول. هذه العملية **crop raster image** تعدل البت‌ماب الأساسي.

```java
rasterImage.crop(leftShift, rightShift, topShift, bottomShift);
```

### الخطوة 5: حفظ النتائج (how to crop image to a new format)

أخيرًا، احفظ الصورة المقتصة إلى القرص. في هذا المثال نختار JPEG، لكن يمكن استخدام أي صيغة يدعمها Aspose.PSD.

```java
String destName = dataDir + "CroppingByShifts_out.jpg";
rasterImage.save(destName, new JpegOptions());
```

تهانينا! لقد قمت بنجاح **cropped an image by shifts** باستخدام Aspose.PSD for Java، وهي مهارة أساسية في أي مجموعة أدوات **java image processing**.

## المشكلات الشائعة والحلول

| المشكلة | الحل |
|-------|----------|
| **`OutOfMemoryError` on large PSD files** | تأكد من استدعاء `cacheData()` (الخطوة 2) وفكر في زيادة حجم الذاكرة المخصصة للـ JVM (`-Xmx`). |
| **Unexpected transparent borders** | تحقق من أن قيم التحول تعكس الهوامش المطلوبة بدقة؛ القيم السالبة قد توسع بدلاً من القص. |
| **Saving in the wrong format** | استخدم الفئة الفرعية المناسبة من `ImageOptions` (مثال: `PngOptions`) عند استدعاء `save`. |

## الأسئلة المتكررة

**س: هل Aspose.PSD متوافق مع جميع صيغ الصور؟**  
ج: نعم، يدعم Aspose.PSD مجموعة واسعة من الصيغ النقطية والمتجهة، مما يضمن مرونة في مشاريعك.

**س: هل يمكنني تطبيق عمليات قص متعددة على نفس الصورة؟**  
ج: بالطبع. يمكنك استدعاء `crop` عدة مرات؛ كل استدعاء يعمل على الحالة الحالية للصورة.

**س: هل هناك منتدى مجتمع لدعم Aspose.PSD؟**  
ج: نعم، يمكنك العثور على الدعم والتفاعل مع المجتمع في [Aspose.PSD Forum](https://forum.aspose.com/c/psd/34).

**س: كيف يمكنني الحصول على ترخيص مؤقت لـ Aspose.PSD؟**  
ج: قم بزيارة [here](https://purchase.aspose.com/temporary-license/) للحصول على ترخيص مؤقت.

**س: هل هناك مشاريع نموذجية تُظهر وظائف Aspose.PSD؟**  
ج: استكشف الوثائق والأمثلة في [Aspose.PSD Java Documentation](https://reference.aspose.com/psd/java/).

## الخاتمة

في هذا الدليل غطينا كل ما تحتاج معرفته ل**crop raster image** الملفات عن طريق تحديد قيم التحول، وهي تقنية أساسية لمعالجة **java image processing** الدقيقة. الآن لديك أساس قوي لدمج عملية القص في سير عمل أكبر، سواء كنت تُعد الأصول للويب، أو تُنشئ صورًا مصغرة، أو تُنظف المستندات الممسوحة.

---

**آخر تحديث:** 2026-01-01  
**تم الاختبار مع:** Aspose.PSD 24.11 for Java  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}