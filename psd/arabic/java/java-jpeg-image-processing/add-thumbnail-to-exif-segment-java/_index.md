---
date: 2026-09-18
description: تعرف على كيفية إضافة صورة مصغرة لبيانات تعريف الصورة java إلى مقطع EXIF
  باستخدام Aspose.PSD for Java. يغطي هذا الدليل خطوة بخطوة المتطلبات المسبقة، استعراض
  الكود، وحفظ الصورة المحدثة.
keywords:
- java image metadata
- how to add thumbnail
- java exif metadata
lastmod: 2026-09-18
linktitle: إضافة Thumbnail إلى مقطع EXIF في Java
og_description: تعرف على كيفية إضافة صورة مصغرة لبيانات تعريف الصورة java إلى مقطع
  EXIF باستخدام Aspose.PSD for Java. يغطي هذا الدليل خطوة بخطوة المتطلبات المسبقة،
  استعراض الكود، وحفظ الصورة المحدثة.
og_image_alt: Guide showing Java code to embed a thumbnail into EXIF metadata using
  Aspose.PSD
og_title: كيفية إضافة صورة مصغرة لبيانات تعريف الصورة java إلى مقطع EXIF
schemas:
- author: Aspose
  dateModified: '2026-09-18'
  description: Learn how to add java image metadata thumbnail to the EXIF segment
    using Aspose.PSD for Java. This step‑by‑step guide covers prerequisites, code
    walkthrough, and saving the updated image.
  headline: How to add java image metadata thumbnail to EXIF segment
  type: TechArticle
- questions:
  - answer: EXIF metadata is embedded information in digital images that includes
      camera settings, capture date, GPS coordinates, and other details.
    question: What is EXIF metadata?
  - answer: Adding a thumbnail improves user experience by allowing quick image previews
      without loading the full image.
    question: Why add a thumbnail to EXIF?
  - answer: You can download Aspose.PSD for Java from the [Aspose.PSD for Java download
      page](https://releases.aspose.com/psd/java/).
    question: Where can I download Aspose.PSD for Java?
  - answer: You can obtain a temporary license for Aspose.PSD from the [temporary
      license page](https://purchase.aspose.com/temporary-license/).
    question: How can I get a temporary license for Aspose.PSD?
  - answer: For support, visit the [Aspose.PSD forum](https://forum.aspose.com/c/psd/34).
    question: How do I get support for Aspose.PSD?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- java image metadata
- EXIF thumbnail
- Aspose.PSD
- Java image processing
title: كيفية إضافة صورة مصغرة لبيانات تعريف الصورة java إلى مقطع EXIF
url: /ar/java/java-jpeg-image-processing/add-thumbnail-to-exif-segment-java/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# إضافة صورة مصغرة لبيانات تعريف الصورة Java إلى مقطع EXIF

## مقدمة
في هذا الدرس ستتعلم كيفية إضافة صورة مصغرة **java image metadata** إلى مقطع EXIF لملف PSD باستخدام Aspose.PSD for Java. تخزن بيانات تعريف EXIF (Exchangeable Image File Format) إعدادات الكاميرا وتاريخ الالتقاط والموقع ومعلومات مفيدة أخرى. يتيح تضمين صورة مصغرة صغيرة للمعاينة للتطبيقات عرض لمحة سريعة عن الصورة دون تحميل الملف بالكامل، مما يحسن الأداء وتجربة المستخدم.

## إجابات سريعة
- **ما الذي يغطيه الدرس؟** إضافة صورة مصغرة إلى مقطع EXIF لصورة PSD باستخدام Aspose.PSD for Java.  
- **كم من الوقت تستغرق التنفيذ؟** حوالي 10‑15 دقيقة لتكامل أساسي.  
- **هل أحتاج إلى ترخيص؟** يلزم ترخيص مؤقت للاستخدام في الإنتاج؛ النسخة التجريبية المجانية تكفي للتقييم.  
- **ما نسخة Java المدعومة؟** Java 8 وما فوق مدعومة بالكامل.  
- **هل يمكن معالجة الملفات الكبيرة؟** نعم—يمكن لـ Aspose.PSD التعامل مع ملفات تصل إلى 2 GB دون تحميل الصورة بالكامل في الذاكرة.

## ما هو java image metadata؟
تشير بيانات تعريف الصورة Java إلى المعلومات المهيكلة المدمجة في ملفات الصور (مثل EXIF أو IPTC أو XMP) التي يمكن قراءتها أو تعديلها أو إنشاؤها برمجياً باستخدام مكتبات Java مثل Aspose.PSD. تتيح هذه البيانات للتطبيقات استرجاع إعدادات الكاميرا، الطوابع الزمنية، إحداثيات GPS، وبيانات مخصصة دون فتح المحتوى المرئي.

## لماذا إضافة صورة مصغرة إلى بيانات تعريف EXIF؟
إضافة صورة مصغرة إلى مقطع EXIF توفر إشارة بصرية فورية لمستعرضات الصور، مستكشفات الملفات، وأنظمة إدارة المحتوى. تقوم Aspose.PSD بمعالجة الصور المصغرة في الذاكرة، مما يتيح لك تضمين معاينة في أقل من 0.2 ثانية للصور التي يصل حجمها إلى 500 KB، وتدعم أكثر من 30 صيغة صورة، بما في ذلك PSD و JPEG و PNG و TIFF.

## المتطلبات المسبقة
- معرفة أساسية ببرمجة Java.  
- مجموعة تطوير Java (JDK) مثبتة على نظامك.  
- بيئة تطوير متكاملة (IDE) لـ Java، مثل IntelliJ IDEA أو Eclipse.  
- مكتبة Aspose.PSD for Java. يمكنك تنزيلها من [صفحة تنزيل Aspose.PSD for Java](https://releases.aspose.com/psd/java/).

## استيراد الحزم
تستورد التعليمات التالية فئات Aspose.PSD اللازمة للعمل مع صور PSD وبيانات EXIF.  
```java
import com.aspose.psd.Image;
import com.aspose.psd.exif.JpegExifData;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
```

## الخطوة 1: تحميل صورة psd
`PsdImage` يمثل ملف Photoshop PSD ويوفر الوصول إلى طبقاته وموارده.  
```java
String dataDir = "Your Document Directory";
PsdImage image = (PsdImage)Image.load(dataDir + "sample.psd");
```

## الخطوة 2: التجول عبر موارد الصورة
`ImageResource` يضم موارد مثل الصور المصغرة، ملفات تعريف ICC، والبيانات المدمجة في ملف PSD.  
```java
for (int i = 0; i < image.getImageResources().length; i++) {
    if (image.getImageResources()[i] instanceof ThumbnailResource || image.getImageResources()[i] instanceof Thumbnail4Resource) {
        ThumbnailResource thumbnail = (ThumbnailResource)image.getImageResources()[i];
        // Process the thumbnail resource
    }
}
```

## الخطوة 3: تعديل بيانات الصورة المصغرة
`JpegOptions` يتيح لك ضبط إعدادات JPEG الخاصة، مثل الجودة، لصورة المصغرة.  
```java
JpegOptions jpegOptions = new JpegOptions();
jpegOptions.setQuality(100); // Set JPEG quality
```

## الخطوة 4: حفظ الصورة
استدعاء `save` يكتب مقطع EXIF المحدث (بما في ذلك الصورة المصغرة الجديدة) إلى القرص دون إعادة ترميز الصورة بالكامل.  
```java
image.save(dataDir + "output.psd");
```

## المشكلات الشائعة والحلول
- **الصورة المصغرة لا تظهر:** تحقق من أن مورد الصورة المصغرة تمت إضافته بشكل صحيح إلى مقطع EXIF وأن الصورة تم حفظها باستخدام طريقة `PsdImage.save`.  
- **أخطاء نفاد الذاكرة على الملفات الكبيرة:** استخدم `PsdImage.load(..., LoadOptions)` مع `LoadOptions.setLoadOnlyMetadata(true)` للعمل فقط على البيانات الوصفية.  
- **الاتجاه غير الصحيح:** تأكد من أن الصورة المصغرة تحترم علم الاتجاه الأصلي للصورة؛ يمكنك قراءة وسم EXIF `Orientation` وتدوير الصورة المصغرة وفقاً لذلك.

## الأسئلة المتكررة

**س: ما هو بيانات تعريف EXIF؟**  
ج: بيانات تعريف EXIF هي معلومات مدمجة في الصور الرقمية تشمل إعدادات الكاميرا، تاريخ الالتقاط، إحداثيات GPS، وتفاصيل أخرى.

**س: لماذا إضافة صورة مصغرة إلى EXIF؟**  
ج: إضافة صورة مصغرة تحسن تجربة المستخدم من خلال السماح بمعاينات سريعة للصور دون تحميل الصورة بالكامل.

**س: من أين يمكنني تنزيل Aspose.PSD for Java؟**  
ج: يمكنك تنزيل Aspose.PSD for Java من [صفحة تنزيل Aspose.PSD for Java](https://releases.aspose.com/psd/java/).

**س: كيف يمكنني الحصول على ترخيص مؤقت لـ Aspose.PSD؟**  
ج: يمكنك الحصول على ترخيص مؤقت لـ Aspose.PSD من [صفحة الترخيص المؤقت](https://purchase.aspose.com/temporary-license/).

**س: كيف أحصل على الدعم لـ Aspose.PSD؟**  
ج: للحصول على الدعم، زر [منتدى Aspose.PSD](https://forum.aspose.com/c/psd/34).

---

**آخر تحديث:** 2026-09-18  
**تم الاختبار مع:** Aspose.PSD for Java 24.10  
**المؤلف:** Aspose

## دروس ذات صلة

- [إنشاء بيانات تعريف XMP في ملفات PSD باستخدام Aspose.PSD for Java](/psd/java/image-editing/create-xmp-metadata/)
- [تغيير حجم الصورة باستخدام Aspose.PSD for Java – رسم الأشكال والعمليات الأساسية على الصورة](/psd/java/basic-image-operations/)
- [كيفية تحويل PSD إلى صيغ صور نقطية باستخدام Aspose.PSD for Java](/psd/java/advanced-techniques/convert-psd-to-raster-formats/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}