---
date: 2026-10-03
description: تعلم كيفية قراءة بيانات تعريف الصورة وتعديل وسوم JPEG EXIF باستخدام java
  مع Aspose.PSD for Java في هذا الدليل step‑by‑step، وهو مثالي للمطورين الذين يتعاملون
  مع بيانات تعريف الصورة بكفاءة.
keywords:
- java read image metadata
- read EXIF tags Java
- modify JPEG metadata Java
- Aspose.PSD Java
lastmod: 2026-10-03
linktitle: قراءة وتعديل وسوم JPEG EXIF في Java
og_description: تعلم كيفية قراءة بيانات تعريف الصورة وتعديل وسوم JPEG EXIF باستخدام
  java مع Aspose.PSD for Java. يوضح هذا الدليل كود step‑by‑step لاستخراج وتحديث معلومات
  EXIF.
og_image_alt: Guide showing how to java read image metadata and edit JPEG EXIF tags
  using Aspose.PSD for Java
og_title: كيفية قراءة بيانات تعريف الصورة وتعديل وسوم JPEG EXIF باستخدام java
schemas:
- author: Aspose
  dateModified: '2026-10-03'
  description: Learn how to java read image metadata and modify JPEG EXIF tags with
    Aspose.PSD for Java in this step‑by‑step guide, perfect for developers handling
    image metadata efficiently.
  headline: How to java read image metadata and modify JPEG EXIF tags
  type: TechArticle
- description: Learn how to java read image metadata and modify JPEG EXIF tags with
    Aspose.PSD for Java in this step‑by‑step guide, perfect for developers handling
    image metadata efficiently.
  name: How to java read image metadata and modify JPEG EXIF tags
  steps:
  - name: '**Java Development Kit (JDK)** – make sure you have JDK 11 or newer. You
      can download it from the [Oracle website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).'
    text: '**Java Development Kit (JDK)** – make sure you have JDK 11 or newer. You
      can download it from the [Oracle website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).'
  - name: '**Aspose.PSD for Java library** – obtain the latest JAR from the [Aspose
      releases page](https://releases.aspose.com/psd/java/).'
    text: '**Aspose.PSD for Java library** – obtain the latest JAR from the [Aspose
      releases page](https://releases.aspose.com/psd/java/).'
  - name: '**IDE** – IntelliJ IDEA, Eclipse, or any editor you prefer.'
    text: '**IDE** – IntelliJ IDEA, Eclipse, or any editor you prefer.'
  - name: '**Basic Java knowledge** – you should be comfortable with creating projects
      and adding external JARs.'
    text: '**Basic Java knowledge** – you should be comfortable with creating projects
      and adding external JARs.'
  type: HowTo
- questions:
  - answer: EXIF (Exchangeable Image File Format) metadata stores camera settings,
      timestamps, GPS coordinates, and other information embedded in JPEG and other
      image files.
    question: What is EXIF data?
  - answer: You can get a free trial from the [Aspose releases page](https://releases.aspose.com/).
    question: Can I use Aspose.PSD for Java for free?
  - answer: Aspose.PSD for Java supports Java SE 7 and above.
    question: Is Aspose.PSD for Java compatible with all versions of Java?
  - answer: Check out the [documentation](https://reference.aspose.com/psd/java/)
      for more details.
    question: Where can I find more documentation on Aspose.PSD for Java?
  - answer: You can get support from the [Aspose PSD support forum](https://forum.aspose.com/c/psd/34/).
    question: How do I get support for Aspose.PSD for Java?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- java image metadata
- exif tags
- aspose psd
- jpeg metadata
- java tutorial
title: كيفية قراءة بيانات تعريف الصورة وتعديل وسوم JPEG EXIF باستخدام java
url: /ar/java/java-jpeg-image-processing/read-modify-jpeg-exif-tags-java/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# قراءة وتعديل وسوم EXIF لملفات JPEG في Java

## مقدمة
إذا كنت بحاجة إلى **java read image metadata** من ملفات JPEG وتغييرها برمجياً، فقد وصلت إلى المكان الصحيح. في هذا الدرس سنستعرض استخراج وتحديث وسوم EXIF باستخدام Aspose.PSD for Java. في النهاية ستتمكن من سحب تفاصيل الكاميرا، الاتجاه، والحقول المخصصة، ثم كتابة هذه البيانات مرة أخرى إلى الملف—كل ذلك دون الحاجة إلى محرر رسومي.

## إجابات سريعة
- **أي مكتبة تتعامل مع JPEG EXIF في Java؟** Aspose.PSD for Java.
- **كم عدد أسطر الكود لقراءة EXIF؟** About three lines after loading the image.
- **هل يمكنك تعديل وسوم EXIF؟** Yes, you can change any standard or custom tag and save the result.
- **ما هي صيغ الصور المدعومة؟** Over 150 formats, including PSD, JPEG, PNG, TIFF, and BMP.
- **ما هو الحد الأدنى لإصدار Java؟** Java 7 or higher.

## لماذا تستخدم Aspose.PSD for Java؟
يدعم Aspose.PSD **150+ صيغ صور** ويمكنه معالجة الملفات حتى **2 GB** دون تحميل المستند بالكامل في الذاكرة، مما يمنحك عمليات بيانات تعريف سريعة وقليلة الذاكرة على مجموعات الصور الكبيرة. كما يوفر واجهة برمجة تطبيقات بسيطة لقراءة وكتابة بيانات EXIF وIPTC وXMP، مما يجعل معالجة الدفعات لآلاف الصور فعّالة وموثوقة.

## المتطلبات المسبقة
1. **Java Development Kit (JDK)** – تأكد من أن لديك JDK 11 أو أحدث. يمكنك تنزيله من [Oracle website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).  
2. **Aspose.PSD for Java library** – احصل على أحدث ملف JAR من [Aspose releases page](https://releases.aspose.com/psd/java/).  
3. **IDE** – IntelliJ IDEA أو Eclipse أو أي محرر تفضله.  
4. **Basic Java knowledge** – يجب أن تكون مرتاحاً لإنشاء المشاريع وإضافة ملفات JAR الخارجية.

## ما هو Java read image metadata؟
يشير Java read image metadata إلى عملية الوصول برمجياً إلى المعلومات المدمجة مثل EXIF وIPTC وXMP المخزنة داخل ملفات الصور باستخدام كود Java. يمكن أن تشمل هذه البيانات إعدادات الكاميرا، الطوابع الزمنية، إحداثيات GPS، إشعارات حقوق النشر، وتعليقات المستخدم، مما يمكّن التطبيقات من تنظيم، البحث، ومعالجة الصور بناءً على بياناتها الوصفية.

## استيراد الحزم
أولاً، أضف ملف Aspose.PSD JAR إلى مسار الفئة (classpath) في مشروعك واستورد الفئات المطلوبة.

توفر الحزمة `com.aspose.psd` واجهة برمجة التطبيقات الأساسية لتحميل الصور والوصول إلى مواردها.

```java
import com.aspose.psd.Image;
import com.aspose.psd.exif.JpegExifData;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
```

## كيفية قراءة بيانات تعريف الصورة من ملفات JPEG في Java؟
حمّل ملف JPEG باستخدام `PsdImage.load("image.jpg")`، حدد مورد الصورة المصغرة (thumbnail) الذي يحتوي على بيانات EXIF، ثم استدعِ `ExifData.read()` للحصول على كائن `ExifData` مُعبأ. هذه الطريقة خطوة واحدة تمنحك وصولاً كاملاً إلى جميع حقول EXIF القياسية وأي وسوم مخصصة قد تكون أضفتها.

## الخطوة 1: تحميل صورة PSD
PsdImage هي الفئة في Aspose.PSD التي تمثل ملف PSD وتوفر طرقاً للوصول إلى موارده وبياناته الوصفية.  
في هذه الخطوة، سنحمّل صورة PSD التي نريد قراءة بيانات EXIF منها. تأكد من أن صورتك موجودة في الدليل الصحيح.

```java
String dataDir = "Your Document Directory";
PsdImage image = null;
try {
    image = (PsdImage) Image.load(dataDir + "1280px-Zebras_Serengeti.psd");
} catch (IOException e) {
    e.printStackTrace();
}
```

## الخطوة 2: تكرار موارد الصورة
ThumbnailResource تمثل صورة مصغرة مخزنة في ملف PSD، غالباً ما تحتوي على بيانات EXIF مدمجة.  
بعد تحميل الصورة، الخطوة التالية هي تكرار موارده للعثور على مورد الصورة المصغرة، الذي عادةً ما يحتوي على بيانات EXIF.

```java
for (int i = 0; i < image.getImageResources().length; i++) {
    if (image.getImageResources()[i] instanceof ThumbnailResource) {
        ThumbnailResource thumbnail = (ThumbnailResource) image.getImageResources()[i];
        // Proceed to next step
    }
}
```

## الخطوة 3: استخراج بيانات EXIF
JpegExifData هي الفئة التي تحتفظ بمعلومات EXIF المستخرجة من صورة JPEG، مما يتيح لك قراءة وتعديل الوسوم الفردية.  
الآن بعد أن حصلنا على مورد الصورة المصغرة، يمكننا استخراج بيانات EXIF منه. تشمل بيانات EXIF معلومات قيمة مثل اسم مالك الكاميرا، قيمة الفتحة، الاتجاه، والمزيد.

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
بعد قراءة بيانات EXIF، قد ترغب في تعديل بعض حقوله. إليك كيفية القيام بذلك:

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
أخيراً، بعد تعديل بيانات EXIF، احفظ التغييرات إلى ملف PSD جديد.

```java
try {
    image.save(dataDir + "Modified_Zebras_Serengeti.psd");
} catch (IOException e) {
    e.printStackTrace();
}
```

## المشكلات الشائعة والحلول
- **Missing thumbnail resource** – بعض ملفات JPEG تخزن EXIF مباشرةً في رأس الصورة الرئيسي. إذا كان مورد الصورة المصغرة غير موجود، استخدم `image.getExifData()` بدلاً من ذلك.  
- **Large files cause OutOfMemoryError** – تأكد من تشغيل JVM بذاكرة كافية (`-Xmx2g`) أو معالجة الصورة في وضع البث باستخدام `PsdImage.load(inputStream, loadOptions)`.  
- **Unsupported tag types** – يدعم Aspose.PSD جميع وسوم EXIF القياسية؛ قد تتطلب الوسوم المخصصة معالجة يدوية على مستوى البايت.

## الأسئلة المتكررة
**Q: ما هي بيانات EXIF؟**  
A: بيانات EXIF (Exchangeable Image File Format) تخزن إعدادات الكاميرا، الطوابع الزمنية، إحداثيات GPS، ومعلومات أخرى مدمجة في ملفات JPEG وغيرها من ملفات الصور.

**Q: هل يمكنني استخدام Aspose.PSD for Java مجاناً؟**  
A: يمكنك الحصول على نسخة تجريبية مجانية من [Aspose releases page](https://releases.aspose.com/).

**Q: هل Aspose.PSD for Java متوافق مع جميع إصدارات Java؟**  
A: Aspose.PSD for Java يدعم Java SE 7 وما فوق.

**Q: أين يمكنني العثور على مزيد من الوثائق حول Aspose.PSD for Java؟**  
A: اطلع على [documentation](https://reference.aspose.com/psd/java/) للمزيد من التفاصيل.

**Q: كيف أحصل على الدعم لـ Aspose.PSD for Java؟**  
A: يمكنك الحصول على الدعم من [Aspose PSD support forum](https://forum.aspose.com/c/psd/34/).

## الخلاصة
باتباع هذه الخطوات يمكنك **java read image metadata** من أي ملف JPEG، تعديل حقول EXIF التي تحتاجها، وكتابة البيانات المحدثة مرة أخرى إلى الملف—كل ذلك باستخدام بضع أسطر من كود Java النظيف. تجعل واجهة برمجة التطبيقات الغنية في Aspose.PSD معالجة البيانات الوصفية موثوقة وعالية الأداء، بحيث يمكنك دمجها في خطوط معالجة الدفعات، أدوات إدارة الصور، أو أي تطبيق يحتاج إلى التعامل مع معلومات الصور.

---

**آخر تحديث:** 2026-10-03  
**تم الاختبار مع:** Aspose.PSD for Java 24.5  
**المؤلف:** Aspose

## دروس ذات صلة

- [قراءة معلومات وسوم EXIF المحددة في Java باستخدام Aspose (asp)](/psd/java/java-jpeg-image-processing/read-specific-exif-tags-info-java/)
- [إنشاء بيانات XMP الوصفية في ملفات PSD باستخدام Aspose.PSD for Java](/psd/java/image-editing/create-xmp-metadata/)
- [تغيير حجم الصورة باستخدام Aspose.PSD for Java – رسم الأشكال والعمليات الأساسية على الصورة](/psd/java/basic-image-operations/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}