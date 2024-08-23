---
title: استخراج الصورة المصغرة من PSD في جافا
linktitle: استخراج الصورة المصغرة من PSD في جافا
second_title: Aspose.PSD جافا API
description: تعرف على كيفية استخراج الصور المصغرة من ملفات PSD باستخدام Aspose.PSD لـ Java. يغطي هذا الدليل التفصيلي كل شيء بدءًا من الإعداد وحتى حفظ الصور المستخرجة.
type: docs
weight: 15
url: /ar/java/java-jpeg-image-processing/extract-thumbnail-from-psd-java/
---
## مقدمة
في هذا البرنامج التعليمي، سنستكشف كيفية استخراج الصور المصغرة من ملفات PSD باستخدام Aspose.PSD لـ Java. يمكن أن تكون الصور المصغرة مفيدة للمعاينات السريعة أو لإنشاء إصدارات أصغر من الصور المضمنة في مستندات PSD. دعنا نتعمق في الخطوات المطلوبة لتحقيق ذلك باستخدام Aspose.PSD.
## المتطلبات الأساسية
قبل أن نبدأ، تأكد من أن لديك الإعداد التالي:
- تم تثبيت Java Development Kit (JDK) على نظامك.
-  Aspose.PSD لمكتبة جافا. يمكنك تنزيله من[هنا](https://releases.aspose.com/psd/java/).
- المعرفة الأساسية ببرمجة جافا.
## حزم الاستيراد
للبدء، قم بتضمين حزمة Aspose.PSD الضرورية في فئة Java الخاصة بك:
```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
import com.aspose.psd.imageoptions.JpegOptions;
```
## الخطوة 1: قم بتحميل ملف PSD
أولاً، قم بتحميل ملف PSD الذي يحتوي على الصورة المصغرة التي تريد استخراجها.
```java
String dataDir = "Your_Document_Directory/";
PsdImage image = (PsdImage)Image.load(dataDir + "your_file.psd");
```
 يستبدل`"Your_Document_Directory/"` باستخدام مسار الدليل حيث يوجد ملف PSD الخاص بك، و`"your_file.psd"` مع اسم ملف PSD الخاص بك.
## الخطوة 2: التكرار على موارد الصورة
قم بالتكرار عبر موارد الصورة للعثور على مورد الصورة المصغرة.
```java
for (int i = 0; i < image.getImageResources().length; i++) {
    if (image.getImageResources()[i] instanceof ThumbnailResource) {
        ThumbnailResource thumbnail = (ThumbnailResource) image.getImageResources()[i];
        
        // استخراج البيانات المصغرة
        int[] data = thumbnail.getThumbnailArgb32Data();
        
        // قم بإنشاء صورة جديدة باستخدام البيانات المصغرة المستخرجة
        PsdImage extractedThumbnailImage = new PsdImage(thumbnail.getWidth(), thumbnail.getHeight());
        extractedThumbnailImage.saveArgb32Pixels(extractedThumbnailImage.getBounds(), data);
        
        // احفظ الصورة المصغرة المستخرجة كملف JPEG منفصل
        extractedThumbnailImage.save(dataDir + "extracted_thumbnail.jpg", new JpegOptions());
        
        // رسالة نجاح الإخراج
        System.out.println("Thumbnail extracted and saved successfully.");
        
        break; // اخرج من الحلقة بمجرد العثور على الصورة المصغرة ومعالجتها
    }
}
```
## الخطوة 3: احفظ الصورة المصغرة المستخرجة
احفظ الصورة المصغرة المستخرجة كملف صورة منفصل (في هذه الحالة، كملف JPEG).
## الخطوة 4: التعامل مع أنواع الصور المصغرة المختلفة
 إذا كان ملف PSD الخاص بك يحتوي على أنواع متعددة من الصور المصغرة، مثل`Thumbnail4Resource`، يمكنك توسيع المنطق للتعامل مع هذه الحالات بالمثل.

## خاتمة
في هذا البرنامج التعليمي، اكتشفنا كيفية استخراج الصور المصغرة من ملفات PSD باستخدام Aspose.PSD لـ Java. باتباع الخطوات الموضحة أعلاه، يمكنك استرداد الصور المصغرة المضمنة في مستندات PSD وحفظها بكفاءة.

## الأسئلة الشائعة
### ما هو Aspose.PSD؟
Aspose.PSD هي مكتبة Java تسمح للمطورين بالعمل مع PSD وتنسيقات ملفات الصور الأخرى برمجيًا.
### أين يمكنني العثور على مزيد من الوثائق حول Aspose.PSD لـ Java؟
 يمكنك الرجوع إلى[الوثائق](https://reference.aspose.com/psd/java/) للحصول على مراجع وأمثلة تفصيلية لواجهة برمجة التطبيقات.
### هل يمكنني تجربة Aspose.PSD مجانًا قبل الشراء؟
 نعم يمكنك تحميل أ[تجربة مجانية](https://releases.aspose.com/) لتقييم إمكانيات المكتبة.
### كيف يمكنني الحصول على تراخيص مؤقتة لـ Aspose.PSD؟
 يمكن الحصول على التراخيص المؤقتة من[هنا](https://purchase.aspose.com/temporary-license/).
### هل Aspose.PSD مناسب للاستخدام التجاري؟
نعم، يمكن استخدام Aspose.PSD لكل من المشاريع الشخصية والتجارية بموجب شروط الترخيص الخاصة به.