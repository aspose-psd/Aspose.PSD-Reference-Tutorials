---
title: التصحيح التلقائي لاتجاه صورة JPEG في Java
linktitle: التصحيح التلقائي لاتجاه صورة JPEG في Java
second_title: Aspose.PSD جافا API
description: تعلم كيفية تصحيح اتجاه صورة JPEG تلقائيًا في Java باستخدام Aspose.PSD. تعزيز مهارات معالجة الصور الخاصة بك دون عناء.
type: docs
weight: 12
url: /ar/java/java-jpeg-image-processing/auto-correct-jpeg-image-orientation-java/
---
## مقدمة
في العصر الرقمي الحالي، أصبحت معالجة الصور وتحسينها برمجيًا مهمة حاسمة للمطورين عبر مختلف المجالات. يعمل Aspose.PSD for Java على تمكين المطورين بأدوات قوية للتعامل مع تنسيقات PSD وJPEG وتنسيقات الصور الأخرى بكفاءة. يتعمق هذا البرنامج التعليمي في مهمة محددة: تصحيح اتجاه صورة JPEG تلقائيًا باستخدام Aspose.PSD لـ Java. سواء كنت تقوم بإنشاء تطبيق لتحرير الصور، أو إدارة موارد الصور في نظام إدارة المحتوى، أو أتمتة سير عمل معالجة الصور، فإن هذا الدليل سيزودك بالمعرفة اللازمة لدمج هذه الوظيفة بسلاسة في تطبيقات Java الخاصة بك.
## المتطلبات الأساسية
قبل الغوص في هذا البرنامج التعليمي، تأكد من إعداد المتطلبات الأساسية التالية:
- بيئة تطوير Java: تأكد من تثبيت Java Development Kit (JDK) على نظامك.
-  Aspose.PSD لـ Java JAR: قم بتنزيل مكتبة Aspose.PSD لـ Java من[هنا](https://releases.aspose.com/psd/java/).
- بيئة التطوير المتكاملة (IDE): استخدم IntelliJ IDEA أو Eclipse أو أي بيئة تطوير متكاملة من اختيارك لتطوير Java.
- الفهم الأساسي لـ Java ومعالجة الصور: سيكون الإلمام ببرمجة Java والمفاهيم الأساسية لمعالجة الصور مفيدًا.

## حزم الاستيراد
قبل البدء بالمثال، تأكد من استيراد الحزم الضرورية من Aspose.PSD لـ Java:
```java
import com.aspose.psd.Image;
import com.aspose.psd.examples.Utils.Utils;
import com.aspose.psd.exif.JpegExifData;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
```
## الخطوة 1: قم بتحميل صورة PSD
أولاً، قم بتحميل صورة PSD التي تحتوي على الصورة المصغرة بتنسيق JPEG والتي يحتاج اتجاهها إلى التصحيح:
```java
String dataDir = "Your Document Directory";
PsdImage image = (PsdImage)Image.load(dataDir + "1280px-Zebras_Serengeti.psd");
```
 يستبدل`"Your Document Directory"` باستخدام مسار الدليل الفعلي حيث يوجد ملف PSD الخاص بك.
## الخطوة 2: التكرار على موارد الصورة
بعد ذلك، قم بالتكرار خلال موارد الصورة للعثور على مورد الصورة المصغرة لـ JPEG:
```java
for (int i = 0; i < image.getImageResources().length; i++) {
    // البحث عن الموارد المصغرة. عادةً ما تكون بتنسيق ملف Jpeg.
    if (image.getImageResources()[i] instanceof ThumbnailResource || image.getImageResources()[i] instanceof Thumbnail4Resource) {
        // ضبط بيانات الصورة المصغرة.
        ThumbnailResource thumbnail = (ThumbnailResource) image.getImageResources()[i];
        JpegExifData exifData = thumbnail.getJpegOptions().getExifData();
        if (exifData != null && exifData.getThumbnail() != null) {
            // إذا كانت هناك صورة مصغرة مخزنة، فقم بتدويرها تلقائيًا.
            PsdImage jpegImage = (PsdImage) exifData.getThumbnail();
            if (jpegImage != null) {
                jpegImage.autoRotate();
            }
        }
    }
}
```
## الخطوة 3: احفظ الصورة
وأخيرًا، احفظ الصورة المصححة بعد تطبيق التدوير التلقائي:
```java
image.save();
```
تضمن هذه الخطوة استمرار التغييرات التي تم إجراؤها على الصورة.

## خاتمة
في الختام، يوفر استخدام Aspose.PSD لـ Java حلاً قويًا لتصحيح اتجاهات صور JPEG تلقائيًا داخل ملفات PSD. باتباع الخطوات الموضحة في هذا البرنامج التعليمي، يمكن للمطورين تحسين سير عمل معالجة الصور لديهم، مما يضمن عرض الصور بشكل صحيح عبر الأنظمة الأساسية والأجهزة المختلفة.
## الأسئلة الشائعة
### ما هو Aspose.PSD لجافا؟
Aspose.PSD for Java هي مكتبة قوية تتيح لمطوري Java العمل مع تنسيقات PSD وJPEG وتنسيقات الصور الأخرى برمجيًا.
### كيف يمكنني تنزيل Aspose.PSD لـ Java؟
 يمكنك تحميل المكتبة من[هنا](https://releases.aspose.com/psd/java/).
### هل يدعم Aspose.PSD لـ Java معالجة الصور؟
نعم، فهو يدعم العديد من مهام معالجة الصور مثل تغيير الحجم، والاقتصاص، وضبط الاتجاه.
### أين يمكنني العثور على وثائق Aspose.PSD لـ Java؟
 الوثائق الشاملة متاحة[هنا](https://reference.aspose.com/psd/java/).
### هل يمكنني تجربة Aspose.PSD لـ Java مجانًا؟
 نعم، يمكنك الحصول على نسخة تجريبية مجانية من[هنا](https://releases.aspose.com/).