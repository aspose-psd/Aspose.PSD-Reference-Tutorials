---
date: 2026-10-03
description: تعلم كيفية استخراج الصورة المصغرة من PSD في Java باستخدام Aspose.PSD.
  يغطي هذا الدليل خطوة بخطوة الإعداد، مقتطفات الشيفرة، وحفظ الصورة المصغرة كملف JPEG.
keywords:
- extract thumbnail from psd
- java aspose psd
- psd thumbnail extraction
lastmod: 2026-10-03
linktitle: استخراج الصورة المصغرة من PSD في Java
og_description: تعلم كيفية استخراج الصورة المصغرة من PSD في Java باستخدام Aspose.PSD.
  يشرح هذا الدليل خطوات الإعداد، تحميل الملف، استخراج الصورة المصغرة، وحفظها كملف
  JPEG.
og_image_alt: Screenshot showing Java code extracting a thumbnail from a PSD file
  using Aspose.PSD
og_title: استخراج الصورة المصغرة من PSD في Java باستخدام Aspose.PSD
schemas:
- author: Aspose
  dateModified: '2026-10-03'
  description: Learn how to extract thumbnail from PSD in Java using Aspose.PSD. This
    step‑by‑step guide covers setup, code snippets, and saving the thumbnail as a
    JPEG image.
  headline: Extract thumbnail from PSD in Java
  type: TechArticle
- questions:
  - answer: Aspose.PSD is a Java library that enables programmatic creation, manipulation,
      and conversion of PSD and other raster image formats without requiring Adobe
      Photoshop.
    question: What is Aspose.PSD?
  - answer: You can refer to the [documentation](https://reference.aspose.com/psd/java/)
      for detailed API references and examples.
    question: Where can I find more documentation on Aspose.PSD for Java?
  - answer: Yes, you can download a [free trial](https://releases.aspose.com/) to
      evaluate the library’s capabilities.
    question: Can I try Aspose.PSD for free before purchasing?
  - answer: Temporary licenses are available from the [temporary license](https://purchase.aspose.com/temporary-license/)
      page.
    question: How can I obtain a temporary license for Aspose.PSD?
  - answer: Yes, Aspose.PSD can be used in both personal and commercial projects under
      its licensing terms.
    question: Is Aspose.PSD suitable for commercial use?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- java image processing
- aspose.psd
- thumbnail extraction
title: استخراج الصورة المصغرة من PSD في Java
url: /ar/java/java-jpeg-image-processing/extract-thumbnail-from-psd-java/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# استخراج الصورة المصغرة من PSD باستخدام Java

## مقدمة
استخراج صورة مصغرة من ملف PSD يتيح لك إنشاء معاينات سريعة دون تحميل الصورة بدقة كاملة. في Java، تجعل مكتبة Aspose.PSD هذه العملية بسيطة وعالية الأداء. في هذا الدرس ستتعلم كيفية إعداد المكتبة، تحديد مورد الصورة المصغرة، وحفظها كملف JPEG — كل ذلك ببضع أسطر من الشيفرة.

## إجابات سريعة
- **أي مكتبة تتعامل مع الصور المصغرة لملفات PSD؟** Aspose.PSD for Java.  
- **كم عدد أسطر الشيفرة المطلوبة؟** حوالي خمس أسطر للتحميل والاستخراج والحفظ.  
- **هل يمكنني استخراج الصور المصغرة من ملفات PSD الكبيرة؟** نعم، تقوم Aspose.PSD بمعالجة ملفات تصل إلى 500 MB دون تحميل كامل الذاكرة.  
- **هل أحتاج إلى ترخيص للتطوير؟** النسخة التجريبية المجانية تكفي للتقييم؛ الترخيص مطلوب للإنتاج.  
- **ما صيغ الإخراج المدعومة؟** يمكن حفظ الصورة المصغرة المستخرجة كـ JPEG أو PNG أو BMP.  

## ما هو استخراج الصورة المصغرة من PSD؟
استخراج الصورة المصغرة من PSD هو عملية قراءة صورة المعاينة الصغيرة المدمجة داخل مستند Photoshop (PSD). تُخزن هذه المعاينة كموارد ويمكن حفظها بشكل مستقل لأغراض الفهرسة أو العرض. عادةً ما تكون الصورة المصغرة تمثيلاً منخفض الدقة يستخدمه التطبيقات لإظهار ملخص بصري سريع دون تحميل الصورة بالحجم الكامل.

## لماذا نستخدم Aspose.PSD لهذه المهمة؟
تدعم Aspose.PSD **30+ صيغ صور** ويمكنها معالجة ملفات PSD تصل إلى **500 MB** مع الحفاظ على استهلاك منخفض للذاكرة لأنها تقرأ الموارد عند الطلب. كما توفر API معالجة قوية للأخطاء، مما يتيح لك استخراج الصور المصغرة بثقة حتى من الملفات التالفة.

## المتطلبات المسبقة
- مجموعة تطوير جافا (JDK) مثبتة.  
- مكتبة Aspose.PSD for Java تم تنزيلها من [تحميل Aspose.PSD for Java](https://releases.aspose.com/psd/java/).  
- إلمام أساسي بصياغة Java وإعداد المشروع.  

## كيف تستخرج صورة مصغرة من ملف PSD باستخدام Java؟
قم بتحميل ملف PSD باستخدام `PsdImage`، حدد `ThumbnailResource`، واحفظ بيانات صورته كملف JPEG. تقوم Aspose.PSD بتجريد التحليل منخفض المستوى، لذا تحتاج فقط إلى استدعاء `getResources()` ثم `save()` على الصورة المستخرجة. يعمل هذا النهج مع أي PSD يحتوي على صورة مصغرة، بغض النظر عن حجم الملف.

## استيراد الحزم
`Image` هي الفئة الأساسية لتحميل الصور. `PsdImage` تمثل مستند PSD. `ThumbnailResource` و `Thumbnail4Resource` تمثل موارد الصور المصغرة. `JpegOptions` تحدد خيارات حفظ JPEG.

```text
```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
import com.aspose.psd.imageoptions.JpegOptions;
```
```

## الخطوة 1: تحميل ملف PSD
أولاً، أنشئ كائن `PsdImage` يشير إلى ملف PSD الخاص بك. يقرأ المُنشئ فقط الرأس والموارد المطلوبة، مما يحافظ على استهلاك منخفض للذاكرة.

```text
```java
String dataDir = "Your_Document_Directory/";
PsdImage image = (PsdImage)Image.load(dataDir + "your_file.psd");
```
```

استبدل `"Your_Document_Directory/"` بمسار الدليل الذي يقع فيه ملف PSD، و `"your_file.psd"` باسم ملف PSD الخاص بك.

## الخطوة 2: التكرار على موارد الصورة
تخزن Aspose.PSD الصور المصغرة ككائنات `ThumbnailResource` داخل مجموعة موارد الصورة. قم بالتكرار عبر المجموعة، تحقق من نوع المورد، والتقط أول صورة مصغرة تصادفها.

```text
```java
for (int i = 0; i < image.getImageResources().length; i++) {
    if (image.getImageResources()[i] instanceof ThumbnailResource) {
        ThumbnailResource thumbnail = (ThumbnailResource) image.getImageResources()[i];
        
        // Extract thumbnail data
        int[] data = thumbnail.getThumbnailArgb32Data();
        
        // Create a new image with the extracted thumbnail data
        PsdImage extractedThumbnailImage = new PsdImage(thumbnail.getWidth(), thumbnail.getHeight());
        extractedThumbnailImage.saveArgb32Pixels(extractedThumbnailImage.getBounds(), data);
        
        // Save the extracted thumbnail as a separate JPEG file
        extractedThumbnailImage.save(dataDir + "extracted_thumbnail.jpg", new JpegOptions());
        
        // Output success message
        System.out.println("Thumbnail extracted and saved successfully.");
        
        break; // Exit the loop once thumbnail is found and processed
    }
}
```
```

## الخطوة 3: حفظ الصورة المصغرة المستخرجة
بمجرد حصولك على صورة المصغرة، استدعِ طريقة `save` لكتابتها إلى القرص. يمكنك اختيار JPEG أو PNG أو BMP؛ JPEG هو الأكثر شيوعًا للمعاينات على الويب.

## الخطوة 4: معالجة أنواع الصور المصغرة المختلفة
إذا كان PSD يحتوي على عدة إصدارات من الصور المصغرة، مثل `Thumbnail4Resource`, قم بتوسيع منطق التكرار للتحقق من كل نوع. توفر API فئات منفصلة لكل مورد، مما يتيح لك اختيار الدقة التي تحتاجها.

## المشكلات الشائعة والحلول
- **لم يتم العثور على صورة مصغرة:** ليس كل ملفات PSD تحتوي على معاينة. تحقق من الملف الأصلي في لوحة “File → File Info” في Photoshop.  
- **خطأ تنسيق غير مدعوم:** تأكد من أنك تستخدم أحدث نسخة من Aspose.PSD؛ الإصدارات القديمة قد لا تدعم أنواع موارد الصور المصغرة الجديدة.  
- **نفاد الذاكرة في الملفات الكبيرة:** استخدم `PsdImage.load(..., LoadOptions)` مع `LoadOptions.setLoadResourcesOnly(true)` لتجنب تحميل بيانات الصورة بالكامل عندما تحتاج فقط إلى الصورة المصغرة.  

## الأسئلة المتكررة

**س: ما هو Aspose.PSD؟**  
ج: Aspose.PSD هي مكتبة Java تمكّن من إنشاء ومعالجة وتحويل ملفات PSD وغيرها من صيغ الصور النقطية دون الحاجة إلى Adobe Photoshop.

**س: أين يمكنني العثور على مزيد من الوثائق حول Aspose.PSD for Java؟**  
ج: يمكنك الرجوع إلى [الوثائق](https://reference.aspose.com/psd/java/) للحصول على مراجع API مفصلة وأمثلة.

**س: هل يمكنني تجربة Aspose.PSD مجانًا قبل الشراء؟**  
ج: نعم، يمكنك تنزيل [نسخة تجريبية مجانية](https://releases.aspose.com/) لتقييم قدرات المكتبة.

**س: كيف يمكنني الحصول على ترخيص مؤقت لـ Aspose.PSD؟**  
ج: الترخيص المؤقت متاح من صفحة [الترخيص المؤقت](https://purchase.aspose.com/temporary-license/).

**س: هل Aspose.PSD مناسب للاستخدام التجاري؟**  
ج: نعم، يمكن استخدام Aspose.PSD في المشاريع الشخصية والتجارية وفقًا لشروط الترخيص الخاصة به.

---

**Last Updated:** 2026-10-03  
**Tested With:** Aspose.PSD for Java 24.12  
**Author:** Aspose

## دروس ذات صلة

- [كيفية تحويل PSD إلى صيغ صور نقطية باستخدام Aspose.PSD for Java](/psd/java/advanced-techniques/convert-psd-to-raster-formats/)
- [حفظ PSD كـ JPEG ودعم اللون RGB مع Aspose.PSD Java](/psd/java/advanced-psd-layer-features-effects/support-rgb-color-psd-files/)
- [تغيير حجم الصورة باستخدام Aspose.PSD for Java – رسم أشكال وعمليات صورة أساسية](/psd/java/basic-image-operations/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}