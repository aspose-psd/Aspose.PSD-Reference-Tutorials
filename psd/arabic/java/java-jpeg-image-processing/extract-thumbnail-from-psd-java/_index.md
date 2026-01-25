---
date: 2026-01-25
description: تعلم كيفية استخراج الصورة المصغرة من ملفات PSD باستخدام Aspose.PSD للغة
  Java. اتبع هذا الدليل خطوة بخطوة لتحميل واستخراج وحفظ الصور المصغرة بسرعة.
linktitle: Extract Thumbnail from PSD in Java
second_title: Aspose.PSD Java API
title: استخراج الصورة المصغرة من ملف PSD في جافا
url: /ar/java/java-jpeg-image-processing/extract-thumbnail-from-psd-java/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# استخراج الصورة المصغرة من PSD في جافا

## Introduction
في هذا الدرس، ستتعلم **كيفية استخراج الصورة المصغرة من ملفات PSD** باستخدام مكتبة Aspose.PSD للغة جافا. الصور المصغرة هي صور معاينة صغيرة مدمجة داخل مستندات PSD، واستخراجها يمكن أن يساعدك على إنشاء معاينات سريعة، إنشاء معارض صور، أو تقليل مساحة التخزين عندما تحتاج فقط إلى تمثيل صغير للعمل الأصلي. سنستعرض كل شيء من إعداد المشروع إلى حفظ الصورة المصغرة المستخرجة كملف صورة قياسي.

## Quick Answers
- **ما الذي يغطيه هذا الدرس؟** استخراج وحفظ صورة مصغرة من ملف PSD باستخدام Aspose.PSD للغة جافا.  
- **ما المكتبة المطلوبة؟** Aspose.PSD للغة جافا (قابلة للتنزيل من الموقع الرسمي لـ Aspose).  
- **هل أحتاج إلى ترخيص؟** يلزم الحصول على ترخيص مؤقت أو كامل للاستخدام في الإنتاج؛ يتوفر نسخة تجريبية مجانية.  
- **ما هو تنسيق الإخراج المستخدم؟** المثال يحفظ الصورة المصغرة كملف JPEG، لكن يمكن اختيار أي تنسيق مدعوم.  
- **كم من الوقت يستغرق التنفيذ؟** حوالي 5‑10 دقائق للمطور المألوف بمفاهيم جافا الأساسية.

## What is “extract thumbnail from PSD”?
استخراج صورة مصغرة من PSD يعني قراءة صورة المعاينة الصغيرة التي يخزنها Photoshop داخل قسم الموارد في الملف. عادةً ما تكون هذه المعاينة نسخة منخفضة الدقة من القماش الكامل، مما يجعلها مثالية للتحميل السريع في مستعرضات الملفات أو معارض الويب.

## Why extract thumbnails with Aspose.PSD?
- **السرعة:** لا حاجة لفتح ملف PSD بالكامل في محرر رسومات؛ الصورة المصغرة مدمجة بالفعل.  
- **الأتمتة:** مثالية لمعالجة دفعات من مكتبات الصور الكبيرة.  
- **متعدد المنصات:** يعمل على أي نظام تشغيل يدعم جافا، دون الحاجة إلى Photoshop.  
- **مرونة التنسيق:** تحويل الصورة المصغرة إلى JPEG أو PNG أو أي تنسيق يدعمه Aspose.PSD.

## Prerequisites
قبل أن نبدأ، تأكد من إعداد ما يلي:
- مجموعة تطوير جافا (JDK) مثبتة على نظامك.  
- مكتبة Aspose.PSD للغة جافا. يمكنك تنزيلها من [هنا](https://releases.aspose.com/psd/java/).  
- معرفة أساسية ببرمجة جافا.

## Import Packages
لبدء العمل، قم بإضافة حزمة Aspose.PSD اللازمة في فئة جافا الخاصة بك:
```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
import com.aspose.psd.imageoptions.JpegOptions;
```

## How to extract thumbnail from PSD using Aspose.PSD for Java
فيما يلي دليل خطوة بخطوة. كل خطوة تتضمن شرحًا مختصرًا يليه الكود الدقيق الذي تحتاج إلى نسخه.

### Step 1: Load the PSD File
أولاً، قم بتحميل ملف PSD الذي يحتوي على الصورة المصغرة التي تريد استخراجها.
```java
String dataDir = "Your_Document_Directory/";
PsdImage image = (PsdImage)Image.load(dataDir + "your_file.psd");
```
استبدل `"Your_Document_Directory/"` بمسار الدليل حيث يقع ملف PSD الخاص بك، و `"your_file.psd"` باسم ملف PSD الخاص بك.

### Step 2: Iterate Over Image Resources
تجول عبر موارد الصورة للعثور على مورد الصورة المصغرة.
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

### Step 3: Save the Extracted Thumbnail
الكود في الخطوة السابقة يحفظ بالفعل الصورة المصغرة كملف JPEG باسم `extracted_thumbnail.jpg` في نفس الدليل. يمكنك تغيير اسم الملف أو التنسيق عن طريق تعديل معلمات طريقة `save`.

### Step 4: Handling Different Thumbnail Types
إذا كان ملف PSD الخاص بك قد يحتوي على أنواع متعددة من الصور المصغرة، مثل `Thumbnail4Resource`، يمكنك توسيع المنطق للتعامل مع تلك الحالات بالمثل. فقط أضف فحص `instanceof Thumbnail4Resource` داخل الحلقة وعالجها باستخدام النمط نفسه.

## Common Issues and Solutions
- **لم يتم العثور على صورة مصغرة:** ليس كل ملفات PSD تحتوي على مورد صورة مصغرة. تحقق من الملف المصدر في Photoshop (File → Export → Thumbnail) أو استخدم ملف PSD مختلف يتضمن معاينة.  
- **خطأ تنسيق صورة غير مدعوم:** تأكد من أنك تستخدم نسخة حديثة من Aspose.PSD تدعم التنسيق المستهدف.  
- **أخطاء أذونات عند الحفظ:** تأكد من أن التطبيق لديه صلاحية كتابة إلى دليل الإخراج.

## Frequently Asked Questions

**س: ما هو Aspose.PSD؟**  
ج: Aspose.PSD هي مكتبة جافا تسمح للمطورين بالعمل مع ملفات PSD وغيرها من تنسيقات الصور برمجيًا.

**س: أين يمكنني العثور على مزيد من الوثائق حول Aspose.PSD للغة جافا؟**  
ج: يمكنك الرجوع إلى [documentation](https://reference.aspose.com/psd/java/) للحصول على مراجع API مفصلة وأمثلة.

**س: هل يمكنني تجربة Aspose.PSD مجانًا قبل الشراء؟**  
ج: نعم، يمكنك تنزيل [free trial](https://releases.aspose.com/) لتقييم قدرات المكتبة.

**س: كيف يمكنني الحصول على تراخيص مؤقتة لـ Aspose.PSD؟**  
ج: يمكن الحصول على تراخيص مؤقتة من [here](https://purchase.aspose.com/temporary-license/).

**س: هل Aspose.PSD مناسب للاستخدام التجاري؟**  
ج: نعم، يمكن استخدام Aspose.PSD في المشاريع الشخصية والتجارية وفقًا لشروط الترخيص الخاصة به.

## Conclusion
في هذا الدرس، استكشفنا كيفية **استخراج الصورة المصغرة من ملفات PSD** باستخدام Aspose.PSD للغة جافا. باتباع الخطوات المذكورة أعلاه، يمكنك استرجاع وحفظ الصور المصغرة المدمجة داخل مستندات PSD بكفاءة، مما يتيح معاينات أسرع وتبسيط سير عمل الصور.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**آخر تحديث:** 2026-01-25  
**تم الاختبار مع:** Aspose.PSD for Java (latest release)  
**المؤلف:** Aspose