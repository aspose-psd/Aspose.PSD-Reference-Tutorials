---
title: قراءة وتعديل علامات JPEG EXIF في Java
linktitle: قراءة وتعديل علامات JPEG EXIF في Java
second_title: Aspose.PSD جافا API
description: تعرف على كيفية قراءة علامات JPEG EXIF وتعديلها باستخدام Aspose.PSD لـ Java في هذا الدليل التفصيلي خطوة بخطوة. مثالي للمطورين الذين يتطلعون إلى التعامل مع البيانات الوصفية للصور دون عناء.
type: docs
weight: 18
url: /ar/java/java-jpeg-image-processing/read-modify-jpeg-exif-tags-java/
---
## مقدمة
مرحبًا يا من هناك! هل تساءلت يومًا كيف يمكنك قراءة علامات JPEG EXIF وتعديلها باستخدام Java؟ إذا كان الأمر كذلك، فأنت في المكان الصحيح! سيرشدك هذا البرنامج التعليمي خلال العملية خطوة بخطوة باستخدام Aspose.PSD لـ Java. سواء كنت مطورًا متمرسًا أو مبتدئًا، بنهاية هذا الدليل، ستتمكن من التعامل مع علامات JPEG EXIF مثل المحترفين. لذا، دعونا نتعمق!
## المتطلبات الأساسية
قبل أن نبدأ، تأكد من أن لديك ما يلي:
1.  Java Development Kit (JDK): تأكد من تثبيت JDK على نظامك. يمكنك تنزيله من[موقع أوراكل](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).
2.  Aspose.PSD لمكتبة Java: أنت بحاجة إلى تنزيل Aspose.PSD لمكتبة Java. احصل عليه من[صفحة الإصدارات Aspose](https://releases.aspose.com/psd/java/).
3. بيئة التطوير المتكاملة (IDE): بيئة تطوير متكاملة مثل IntelliJ IDEA أو Eclipse ستجعل تجربة البرمجة الخاصة بك أكثر سلاسة.
4. المعرفة الأساسية لجافا: مطلوب فهم أساسي لجافا لمتابعة هذا البرنامج التعليمي.
## حزم الاستيراد
أول الأشياء أولاً، فلنستورد الحزم الضرورية. افتح Java IDE الخاص بك وقم بإنشاء مشروع Java جديد. بعد ذلك، قم بتضمين مكتبة Aspose.PSD لـ Java في تبعيات مشروعك.
```java
import com.aspose.psd.Image;
import com.aspose.psd.exif.JpegExifData;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
```
## الخطوة 1: قم بتحميل صورة PSD
في هذه الخطوة، سنقوم بتحميل صورة PSD التي نريد قراءة بيانات EXIF منها. تأكد من أن صورتك موجودة في الدليل الصحيح.
```java
String dataDir = "Your Document Directory";
PsdImage image = null;
try {
    image = (PsdImage) Image.load(dataDir + "1280px-Zebras_Serengeti.psd");
} catch (IOException e) {
    e.printStackTrace();
}
```
## الخطوة 2: التكرار على موارد الصورة
بمجرد تحميل الصورة، فإن الخطوة التالية هي تكرار مواردها للعثور على مورد الصورة المصغرة، والذي يحتوي عادةً على بيانات EXIF.
```java
for (int i = 0; i < image.getImageResources().length; i++) {
    if (image.getImageResources()[i] instanceof ThumbnailResource) {
        ThumbnailResource thumbnail = (ThumbnailResource) image.getImageResources()[i];
        // انتقل إلى الخطوة التالية
    }
}
```
## الخطوة 3: استخراج بيانات EXIF
الآن بعد أن أصبح لدينا مورد الصورة المصغرة، يمكننا استخراج بيانات EXIF منه. تتضمن بيانات EXIF معلومات قيمة مثل اسم مالك الكاميرا وقيمة فتحة العدسة والاتجاه والمزيد.
```java
JpegExifData exifData = thumbnail.getJpegOptions().getExifData();
if (exifData != null) {
    System.out.println("Camera Owner Name: " + exifData.getCameraOwnerName());
    System.out.println("Aperture Value: " + exifData.getApertureValue());
    System.out.println("Orientation: " + exifData.getOrientation());
    System.out.println("Focal Length: " + exifData.getFocalLength());
    System.out.println("Compression: " + exifData.getCompression());
}
```
## الخطوة 4: تعديل بيانات EXIF
بعد قراءة بيانات EXIF، قد ترغب في تعديل بعض حقولها. وإليك كيف يمكنك القيام بذلك:
```java
if (exifData != null) {
    exifData.setCameraOwnerName("New Camera Owner");
    exifData.setApertureValue(3.5);
    exifData.setOrientation(1);
    exifData.setFocalLength(35.0);
    exifData.setCompression(6);
    thumbnail.getJpegOptions().setExifData(exifData);
}
```
## الخطوة 5: حفظ التغييرات
أخيرًا، بعد تعديل بيانات EXIF، احفظ التغييرات في ملف PSD جديد.
```java
try {
    image.save(dataDir + "Modified_Zebras_Serengeti.psd");
} catch (IOException e) {
    e.printStackTrace();
}
```

## خاتمة
وهنا لديك! باتباع هذه الخطوات، يمكنك بسهولة قراءة علامات JPEG EXIF وتعديلها باستخدام Aspose.PSD لـ Java. هذه المكتبة القوية تجعل التعامل مع البيانات الوصفية للصور أمرًا سهلاً. لذا، تفضل وجرب ذلك في مشاريعك الخاصة. ترميز سعيد!
## الأسئلة الشائعة
### ما هي بيانات EXIF؟
تحتوي بيانات EXIF (تنسيق ملف الصورة القابل للتبديل) على بيانات تعريف حول الصورة، مثل إعدادات الكاميرا واتجاهها.
### هل يمكنني استخدام Aspose.PSD لـ Java مجانًا؟
 يمكنك الحصول على نسخة تجريبية مجانية من[صفحة الإصدارات Aspose](https://releases.aspose.com/).
### هل Aspose.PSD لـ Java متوافق مع جميع إصدارات Java؟
يدعم Aspose.PSD لـ Java Java SE 7 وما فوق.
### أين يمكنني العثور على مزيد من الوثائق حول Aspose.PSD لـ Java؟
 تحقق من[الوثائق](https://reference.aspose.com/psd/java/) لمزيد من التفاصيل.
### كيف يمكنني الحصول على الدعم لـ Aspose.PSD لـ Java؟
 يمكنك الحصول على الدعم من[Aspose منتدى دعم PSD](https://forum.aspose.com/c/psd/34).