---
title: إنشاء صور مصغرة من ملفات PSD باستخدام Java
linktitle: إنشاء صور مصغرة من ملفات PSD باستخدام Java
second_title: Aspose.PSD جافا API
description: تعرف على كيفية إنشاء صور مصغرة من ملفات PSD بسهولة باستخدام Java وAspose.PSD. اتبع دليلنا خطوة بخطوة لمعالجة الصور بسلاسة.
weight: 24
url: /ar/java/modifying-converting-psd-images/create-thumbnails-psd-files/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# إنشاء صور مصغرة من ملفات PSD باستخدام Java

## مقدمة
في عالم التصميم الجرافيكي، يعد العمل باستخدام ملفات PSD (مستندات Photoshop) أمرًا شائعًا. سواء كنت مطورًا متمرسًا، أو مصمم رسومات، أو مجرد شخص يرغب في التعمق في معالجة الصور، فإن إنشاء صور مصغرة من ملفات PSD يمكن أن يوفر لك الوقت ويبسط سير عملك. سيرشدك هذا البرنامج التعليمي خلال العملية بأكملها باستخدام Aspose.PSD لـ Java. لا تعتبر Aspose.PSD مكتبة قوية لإدارة ملفات Photoshop فحسب، بل إنها تجعل المهمة التي بين يديك بديهية وسهلة الإدارة أيضًا. هل أنت مستعد لتعلم كيفية إنشاء صور مصغرة من ملفات PSD بكفاءة؟
## المتطلبات الأساسية
قبل أن نتعمق في التفاصيل الجوهرية لإنشاء الصور المصغرة، دعنا نغطي ما ستحتاج إليه للبدء.
### بيئة تطوير جافا
-  Java JDK: تأكد من تثبيت Java Development Kit (JDK) على جهاز الكمبيوتر الخاص بك. يمكنك تنزيله[هنا](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).
- IDE: بيئة التطوير المتكاملة (IDE) مثل IntelliJ IDEA أو Eclipse أو NetBeans ستجعل عملية البرمجة أسهل.
### مكتبة Aspose.PSD
- تحتاج إلى تضمين مكتبة Aspose.PSD في مشروعك. أنت تستطيع[قم بتنزيل أحدث إصدار هنا](https://releases.aspose.com/psd/java/).
### المعرفة الأساسية لجافا
- سيساعدك الإلمام بأساسيات Java على التنقل عبر رمز المثال بشكل أكثر فعالية. سيتم استخدام مفاهيم مثل الفئات والكائنات والحلقات بشكل متكرر.
## حزم الاستيراد
ابدأ باستيراد الفئات الضرورية من مكتبة Aspose.PSD. تعتبر هذه الخطوة حاسمة لأنها تمكنك من الاستفادة من وظائف المكتبة في التعليمات البرمجية الخاصة بك.
```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.ThumbnailFormat;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
```
مع انتهاء المتطلبات الأساسية، دعنا ننتقل إلى الحدث الرئيسي! يتضمن إنشاء الصور المصغرة من ملفات PSD بضع خطوات واضحة، وسأقوم بتفصيلها لك.
## الخطوة 1: إعداد بيئتك
فيما يلي كيفية بدء مشروعك والتحضير لإنشاء الصور المصغرة.
1. إنشاء مشروع جافا:
   - افتح IDE الخاص بك وقم بإنشاء مشروع Java جديد.
   - أطلق عليه اسمًا مثل "PsdThumbnailGenerator".
2. تضمين مكتبة Aspose.PSD:
   -  أضف ملف Aspose.PSD JAR إلى مسار بناء مشروعك. إذا كنت تستخدم Maven، فقم بإدراجه في ملف`pom.xml`:
     ```xml
     <dependency>
         <groupId>com.aspose</groupId>
         <artifactId>aspose-psd</artifactId>
         <version>your_version_here</version>
     </dependency>
     ```
## الخطوة 2: قم بتحميل ملف PSD
بعد ذلك، نحتاج إلى تحميل ملف PSD الذي نريد إنشاء صور مصغرة منه. 
1. حدد دليل المستندات الخاص بك:
   حدد الدليل الذي يوجد به ملف PSD الخاص بك.
   ```java
   String dataDir = "Your Document Directory"; // استبدل بمسارك
   ```
2. قم بتحميل ملف PSD:
    استخدم`PsdImage` فئة لتحميل ملف PSD الخاص بك.
   ```java
   PsdImage image = (PsdImage) Image.load(dataDir + "sample.psd");
   ```
 هنا،`sample.psd` هو اسم ملف PSD الخاص بك. اضبط هذا وفقًا لاسم ملفك.
## الخطوة 3: التكرار على موارد PSD
الآن بعد أن قمنا بتحميل صورة PSD الخاصة بنا، فإن الخطوة التالية هي فحص مواردها.
1. الحصول على عدد الموارد:
   سنقوم بتكرار جميع الموارد الموجودة في ملف PSD.
   ```java
   for (int i = 0; i < image.getImageResources().length; i++) {
       // معالجة الموارد
   }
   ```
   
2. تحديد موارد الصور المصغرة:
   داخل الحلقة، تحقق مما إذا كان المورد عبارة عن صورة مصغرة.
   ```java
   if (image.getImageResources()[i] instanceof ThumbnailResource) {
       // معالجة الصورة المصغرة
   }
   ```
## الخطوة 4: معالجة الصورة المصغرة
بمجرد تحديد مورد الصورة المصغرة، سنحتاج إلى التعامل معه وفقًا لذلك.
1. استرداد تنسيق الصورة المصغرة والتحقق منه:
   إذا كان المورد عبارة عن صورة مصغرة بالفعل، فاسترجعه وتحقق من تنسيقه.
   ```java
   ThumbnailResource thumbnail = (ThumbnailResource) image.getImageResources()[i];
   if (thumbnail.getFormat() == ThumbnailFormat.KJpegRgb) {
       // إنشاء وحفظ الصورة المصغرة
   }
   ```
## الخطوة 5: إنشاء وحفظ الصورة المصغرة
هذا هو المكان الذي يحدث فيه السحر! سنقوم بإنشاء صورة جديدة من البيانات المصغرة وحفظها.
1. إنشاء صورة جديدة:
   سنستخدم عرض المورد المصغر وارتفاعه لإنشاء صورة نقطية جديدة.
   ```java
   PsdImage thumbnailImage = new PsdImage(thumbnail.getWidth(), thumbnail.getHeight());
   ```
2. تخزين البكسلات في الصورة الجديدة:
   انقل بيانات الصورة المصغرة إلى الصورة التي تم إنشاؤها حديثًا.
   ```java
   thumbnailImage.savePixels(thumbnailImage.getBounds(), thumbnail.getThumbnailData());
   ```
3. حفظ الصورة المصغرة:
   وأخيرًا، احفظ الصورة المصغرة في دليل المستندات الخاص بك باسم فريد.
   ```java
   thumbnailImage.save(dataDir + "CreateThumbnailsFromPSDFiles_out_" + i + ".bmp");
   ```

## خاتمة
يمكن أن يكون إنشاء صور مصغرة من ملفات PSD باستخدام Java وAspose.PSD مهمة واضحة بمجرد تقسيمها إلى خطوات يمكن التحكم فيها. باستخدام هذا البرنامج التعليمي، لديك الآن القدرة على استخراج الصور المصغرة من ملفات PSD الخاصة بك بسهولة، مما يمنحك أداة رائعة لتحسين سير عملك. إذن ما الذي يمنعك؟ احصل على بعض ملفات PSD وجربها!
## الأسئلة الشائعة
### ما هو Aspose.PSD؟
Aspose.PSD هي مكتبة Java تسمح للمطورين بالعمل مع ملفات Photoshop، مما يسهل التعامل مع ملفات PSD وإدارتها برمجيًا.
### هل يمكنني استخدام Aspose.PSD مجانًا؟
نعم، يقدم Aspose نسخة تجريبية مجانية يمكنك استخدامها لاختبار المكتبة قبل شراء الترخيص.
### ما هي التنسيقات التي يمكنني حفظ الصور المصغرة بها؟
في هذا المثال، قمنا بحفظ الصور المصغرة بتنسيق BMP، لكن Aspose.PSD يدعم العديد من التنسيقات الأخرى أيضًا.
### هل أحتاج إلى تثبيت برنامج Photoshop لاستخدام Aspose.PSD؟
لا، Aspose.PSD يعمل بشكل مستقل عن Photoshop.
### أين يمكنني العثور على مزيد من المعلومات حول Aspose.PSD؟
 يمكنك الاطلاع على[وثائق Aspose.PSD](https://reference.aspose.com/psd/java/) لمزيد من التفاصيل والبرامج التعليمية والموارد.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
