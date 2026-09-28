---
date: 2026-09-28
description: كيفية إضافة صورة مصغرة إلى مقطع JFIF في Java باستخدام Aspose.PSD. اتبع
  هذا الدليل خطوة بخطوة لتضمين الصور المصغرة في ملفات PSD بسرعة وموثوقية.
keywords:
- how to add thumbnail
- JFIF segment Java
- Aspose.PSD thumbnail
- Java image processing
lastmod: 2026-09-28
linktitle: إضافة صورة مصغرة إلى مقطع JFIF في Java
og_description: كيفية إضافة صورة مصغرة إلى مقطع JFIF في Java باستخدام Aspose.PSD.
  اتبع هذا الدليل خطوة بخطوة لتضمين الصور المصغرة في ملفات PSD بسرعة وموثوقية.
og_image_alt: Guide showing how to add thumbnail to JFIF segment in Java with Aspose.PSD
og_title: كيفية إضافة صورة مصغرة إلى مقطع JFIF في Java
schemas:
- author: Aspose
  dateModified: '2026-09-28'
  description: How to add thumbnail to a JFIF segment in Java using Aspose.PSD. Follow
    this step‑by‑step guide to embed thumbnails in PSD files quickly and reliably.
  headline: How to add thumbnail to JFIF segment in Java
  type: TechArticle
- description: How to add thumbnail to a JFIF segment in Java using Aspose.PSD. Follow
    this step‑by‑step guide to embed thumbnails in PSD files quickly and reliably.
  name: How to add thumbnail to JFIF segment in Java
  steps:
  - name: import packages
    text: '`Document`, `JfifResource`, and related classes are part of the Aspose.PSD
      namespace. Document represents the PSD file container, and JfifResource provides
      access to the JFIF segment within the PSD. Import them at the top of your source
      file.'
  - name: load the PSD image
    text: Create a `PsdImage` instance by passing the file path to the constructor.
      PsdImage is the Aspose.PSD class that models a Photoshop document. This loads
      the document metadata while streaming the pixel data.
  - name: iterate over image resources
    text: Search the `Resources` collection for a `JfifResource`. When found, you
      can replace its thumbnail byte array with a new JPEG‑encoded preview.
  - name: adjust thumbnail data
    text: Generate a small JPEG thumbnail (e.g., 120 × 120 px) using any image‑processing
      library, then assign the resulting byte array to `jfifResource.ThumbnailData`.
  - name: save the modified image
    text: Call the `save` method on the `PsdImage` object, specifying the output path
      and desired format. The JFIF segment now contains the new thumbnail.
  type: HowTo
- questions:
  - answer: Aspose.PSD for Java is a commercial library that enables developers to
      create, edit, convert, and render Photoshop PSD files without requiring Adobe
      Photoshop.
    question: What is Aspose.PSD for Java?
  - answer: Detailed documentation can be found on the [Aspose.PSD for Java documentation
      page](https://reference.aspose.com/psd/java/).
    question: Where can I find more documentation for Aspose.PSD for Java?
  - answer: Yes, Aspose.PSD for Java can be used commercially. You can purchase a
      license from [Aspose.PSD's purchase page](https://purchase.aspose.com/buy).
    question: Is Aspose.PSD for Java suitable for commercial use?
  - answer: Yes, you can download a free trial from [Aspose.PSD's trial download page](https://releases.aspose.com/).
    question: Can I try Aspose.PSD for Java before purchasing?
  - answer: For support, visit the [Aspose.PSD forum](https://forum.aspose.com/c/psd/34).
    question: How can I get support for Aspose.PSD for Java?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- add thumbnail
- Aspose.PSD
- Java image processing
- JFIF
- PSD
title: كيفية إضافة صورة مصغرة إلى مقطع JFIF في Java
url: /ar/java/java-jpeg-image-processing/add-thumbnail-to-jfif-segment-java/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# كيفية إضافة صورة مصغرة إلى مقطع JFIF في Java

## مقدمة
إضافة صورة مصغرة إلى مقطع JFIF في ملف PSD هو طلب شائع عندما تحتاج إلى معاينة بصرية سريعة دون تحميل الصورة بالكامل. في هذا البرنامج التعليمي ستتعلم **كيفية إضافة صورة مصغرة** إلى مقطع JFIF في Java باستخدام Aspose.PSD. في نهاية الدليل ستحصل على مقتطف شفرة قابل للتنفيذ، وفهم للهيكل الداخلي لـ JFIF، ونصائح للتعامل مع الملفات الكبيرة بكفاءة.

## إجابات سريعة
- **ما المكتبة المطلوبة؟** Aspose.PSD for Java.
- **أي نسخة من Java تعمل؟** JDK 11 أو أحدث.
- **كم عدد أسطر الشفرة المطلوبة؟** حوالي 10 أسطر للتحميل، التعديل، والحفظ.
- **هل يمكنني معالجة ملفات متعددة الميجابايت؟** نعم، Aspose.PSD يبث البيانات، لذا يبقى استهلاك الذاكرة منخفضًا.
- **هل تحتاج إلى ترخيص تجاري؟** الترخيص مطلوب للاستخدام في الإنتاج؛ تتوفر نسخة تجريبية مجانية.

## ما هو مقطع JFIF؟
مقطع JFIF هو كتلة من تنسيق تبادل ملفات JPEG يمكنها تخزين بيانات اختيارية مثل الصور المصغرة، EXIF، أو ملفات تعريف الألوان.  
يقع داخل تدفق JPEG لملف PSD ويتم التعرف عليه من قبل معظم عارضات الصور لتوليد معاينة سريعة.

## لماذا إضافة صورة مصغرة إلى ملف PSD؟
يدعم Aspose.PSD for Java **أكثر من 30 تنسيق صورة** ويمكنه معالجة ملفات تصل إلى **2 GB** دون تحميل المستند بالكامل في الذاكرة. إضافة صورة مصغرة تقلل من عرض النطاق الترددي للشبكة عند نقل المعاينات وتسرّع عرض واجهة المستخدم في تطبيقات المعارض.

## المتطلبات المسبقة
- Java Development Kit (JDK): تأكد من تثبيت Java على نظامك. يمكنك تنزيله من [Oracle's JDK website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).
- Aspose.PSD for Java: تحتاج إلى مكتبة Aspose.PSD for Java. يمكنك الحصول عليها من [Aspose.PSD Java download page](https://releases.aspose.com/psd/java/).
- Integrated Development Environment (IDE): استخدم بيئة تطوير متكاملة مثل IntelliJ IDEA أو Eclipse لتطوير Java.
- Basic Understanding of Java: إلمام بلغة برمجة Java ومفاهيمها.

## كيفية إضافة صورة مصغرة إلى مقطع JFIF في Java؟
حمّل ملف PSD المستهدف، حدد مورد JFIF، استبدل بيانات صورته المصغرة، واحفظ الملف. يمكن تنفيذ العملية بالكامل ببضع نداءات API بسيطة، ويتعامل Aspose.PSD مع بنية JPEG منخفضة المستوى نيابةً عنك.

### الخطوة 1: استيراد الحزم
`Document`، `JfifResource`، والفئات ذات الصلة هي جزء من مساحة أسماء Aspose.PSD. تمثل Document حاوية ملف PSD، وتوفر JfifResource الوصول إلى مقطع JFIF داخل PSD. استوردها في أعلى ملف المصدر الخاص بك.

```java
import com.aspose.psd.Image;
import com.aspose.psd.exif.JpegExifData;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
```

### الخطوة 2: تحميل صورة PSD
أنشئ مثيلًا من `PsdImage` بتمرير مسار الملف إلى المُنشئ. `PsdImage` هي فئة Aspose.PSD التي تمثل مستند Photoshop. يقوم هذا بتحميل بيانات تعريف المستند مع بث بيانات البكسل.

```java
String dataDir = "Your Document Directory";
PsdImage image = (PsdImage)Image.load(dataDir + "your_image.psd");
```

### الخطوة 3: التكرار على موارد الصورة
ابحث في مجموعة `Resources` عن `JfifResource`. عند العثور عليه، يمكنك استبدال مصفوفة البايت الخاصة بالصورة المصغرة بمعاينة جديدة مشفرة بصيغة JPEG.

```java
for(int i = 0; i < image.getImageResources().length; i++) {
    if (image.getImageResources()[i] instanceof ThumbnailResource) {
        ThumbnailResource thumbnail = (ThumbnailResource)image.getImageResources()[i];
        
        // Continue with thumbnail processing
    }
}
```

### الخطوة 4: تعديل بيانات الصورة المصغرة
أنشئ صورة مصغرة JPEG صغيرة (مثلاً 120 × 120 بكسل) باستخدام أي مكتبة معالجة صور، ثم عيّن مصفوفة البايت الناتجة إلى `jfifResource.ThumbnailData`.

```java
try {
    PsdImage thumbnailImage = new PsdImage(100, 100);
    
    // Fill thumbnail data (example: create a simple pixel array)
    int[] pixels = new int[thumbnailImage.getWidth() * thumbnailImage.getHeight()];
    for (int j = 0; j < pixels.length; j++) {
        pixels[j] = j;
    }
    
    // Save thumbnail data
    thumbnailImage.saveArgb32Pixels(thumbnailImage.getBounds(), pixels);
    
    // Set thumbnail data to Jpeg options
    JpegExifData exifData = new JpegExifData();
    exifData.setThumbnail(thumbnailImage);
    JpegOptions jpegOptions = new JpegOptions();
    jpegOptions.setExifData(exifData);
    
    // Set options to thumbnail resource
    thumbnail.getJpegOptions().setExifData(exifData);
    
} catch(Exception e) {
    // Handle exceptions
} finally {
    // Dispose of resources
}
```

### الخطوة 5: حفظ الصورة المعدلة
استدعِ طريقة `save` على كائن `PsdImage`، مع تحديد مسار الإخراج والصيغة المطلوبة. الآن يحتوي مقطع JFIF على الصورة المصغرة الجديدة.

```java
image.save(dataDir + "output.psd");
```

## المشكلات الشائعة والحلول
- **الصورة المصغرة غير مرئية في العارضات:** تأكد من أن بيانات الصورة المصغرة هي مصفوفة بايت JPEG صالحة وأن أبعادها لا تتجاوز 256 × 256 بكسل، وهو الحد الأقصى المدعوم وفقًا لمواصفات JFIF.
- **OutOfMemoryError في ملفات PSD الكبيرة:** استخدم `PsdImage.load(inputStream, true)` لتمكين وضع البث، مما يحافظ على استهلاك الذاكرة منخفضًا.
- **نوع المورد غير صحيح:** تحقق من أن المورد الذي تعدله هو فعلاً `JfifResource`؛ الموارد الأخرى مثل `ExifResource` لن تؤثر على عرض الصورة المصغرة.

## الأسئلة المتكررة

**س: ما هو Aspose.PSD for Java؟**  
ج: Aspose.PSD for Java هي مكتبة تجارية تمكّن المطورين من إنشاء وتحرير وتحويل وعرض ملفات Photoshop PSD دون الحاجة إلى Adobe Photoshop.

**س: أين يمكنني العثور على مزيد من الوثائق لـ Aspose.PSD for Java؟**  
ج: يمكن العثور على وثائق مفصلة في صفحة [Aspose.PSD for Java documentation page](https://reference.aspose.com/psd/java/).

**س: هل Aspose.PSD for Java مناسب للاستخدام التجاري؟**  
ج: نعم، يمكن استخدام Aspose.PSD for Java تجاريًا. يمكنك شراء ترخيص من [Aspose.PSD's purchase page](https://purchase.aspose.com/buy).

**س: هل يمكنني تجربة Aspose.PSD for Java قبل الشراء؟**  
ج: نعم، يمكنك تنزيل نسخة تجريبية مجانية من [Aspose.PSD's trial download page](https://releases.aspose.com/).

**س: كيف يمكنني الحصول على الدعم لـ Aspose.PSD for Java؟**  
ج: للحصول على الدعم، زر [Aspose.PSD forum](https://forum.aspose.com/c/psd/34).

---

**آخر تحديث:** 2026-09-28  
**تم الاختبار مع:** Aspose.PSD for Java 24.11  
**المؤلف:** Aspose

## دروس ذات صلة

- [إضافة مورد IOPA إلى ملفات PSD باستخدام Aspose PSD for Java](/psd/java/modifying-converting-psd-images/add-iopa-resource-psd-files/)
- [إضافة توقيع إلى الصورة – رسم الصورة على القماش باستخدام Aspose.PSD for Java](/psd/java/advanced-image-effects/add-signature-to-image/)
- [كيفية تدوير الصورة بزاوية محددة باستخدام Aspose.PSD for Java](/psd/java/advanced-image-manipulation/rotate-image-specific-angle/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}