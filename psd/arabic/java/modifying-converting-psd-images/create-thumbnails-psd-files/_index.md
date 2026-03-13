---
date: 2026-03-13
description: تعلم كيفية إنشاء صورة مصغرة لملف PSD باستخدام Java و Aspose.PSD. اتبع
  دليلنا خطوة بخطوة لتوليد صور مصغرة من ملفات PSD بسرعة.
linktitle: Create Thumbnails from PSD Files using Java
second_title: Aspose.PSD Java API
title: إنشاء صورة مصغرة لملف PSD باستخدام Java – توليد صور مصغرة من PSD
url: /ar/java/modifying-converting-psd-images/create-thumbnails-psd-files/
weight: 24
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# إنشاء صورة مصغرة لملف PSD باستخدام Java – إنشاء صور مصغرة من PSD

## المقدمة
إذا كنت بحاجة إلى **create PSD thumbnail Java** الذي يستخرج صور المعاينة من ملفات Photoshop، فقد وصلت إلى المكان الصحيح. سواءً كنت تبني مدير أصول رقمية، أو معرض ويب، أو خط أنابيب معالجة دفعية آلية، فإن إنشاء صور مصغرة من ملفات PSD يمكن أن يحسن الأداء وتجربة المستخدم بشكل كبير. في هذا الدليل سنستعرض العملية بالكامل باستخدام Aspose.PSD for Java، موضحين لك كيفية تحميل ملف PSD، وتحديد موارد الصورة المصغرة المدمجة، وحفظها كملفات صورة منفصلة.

## إجابات سريعة
- **ما هي المكتبة الأفضل لاستخراج صور مصغرة من PSD؟** Aspose.PSD for Java.  
- **كم من الوقت يستغرق التنفيذ؟** حوالي 10‑15 دقيقة لإعداد أساسي.  
- **هل أحتاج إلى تثبيت Photoshop؟** لا، Aspose.PSD يعمل بشكل مستقل.  
- **إلى أي صيغ صور يمكنني تصدير الصورة المصغرة؟** أي صيغة يدعمها Aspose.PSD (مثل BMP، PNG، JPEG).  
- **هل يلزم الحصول على ترخيص للاستخدام في الإنتاج؟** نعم، يلزم ترخيص تجاري للاستخدام في بيئة الإنتاج.

## ما هو “create PSD thumbnail Java”؟
إنشاء صورة مصغرة لملف PSD في Java يعني قراءة صورة المعاينة المخزنة داخل مستند Photoshop (PSD) برمجياً وكتابتها كملف صورة منفصل. هذا مفيد لتوليد معاينات سريعة دون تحميل محتوى PSD الكامل، الذي غالباً ما يكون كبيراً.

## لماذا نستخدم Aspose.PSD لهذه المهمة؟
- **بدون اعتماد على Photoshop:** يعمل على أي منصة تحتوي على JDK.  
- **دعم كامل لـ PSD:** يتعامل مع جميع إصدارات PSD والموارد، بما في ذلك الصور المصغرة.  
- **واجهة برمجة تطبيقات بسيطة:** بضع أسطر من الشيفرة لاستخراج وحفظ الصور المصغرة.  
- **محسن للأداء:** إدارة ذاكرة فعّالة للملفات الكبيرة.

## المتطلبات المسبقة
قبل الغوص في تفاصيل إنشاء الصور المصغرة، دعنا نستعرض ما ستحتاجه للبدء.

### بيئة تطوير Java
- **Java JDK:** تأكد من تثبيت مجموعة تطوير جافا (JDK) على جهازك. يمكنك تنزيلها [هنا](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).  
- **IDE:** بيئة تطوير متكاملة (IDE) مثل IntelliJ IDEA أو Eclipse أو NetBeans ستسهل عملية الترميز.

### مكتبة Aspose.PSD
- تحتاج إلى إضافة مكتبة Aspose.PSD إلى مشروعك. يمكنك [تحميل أحدث نسخة هنا](https://releases.aspose.com/psd/java/).

### معرفة أساسية بـ Java
- الإلمام بأساسيات Java سيساعدك على متابعة مثال الشيفرة بفعالية. سيتم استخدام مفاهيم مثل الفئات، والكائنات، والحلقات بشكل متكرر.

## استيراد الحزم
ابدأ باستيراد الفئات الضرورية من مكتبة Aspose.PSD. هذه الخطوة أساسية لأنها تتيح لك الاستفادة من وظائف المكتبة في شيفرتك.

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.ThumbnailFormat;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
```

مع إتمام المتطلبات المسبقة، لننتقل إلى الحدث الرئيسي! إنشاء صور مصغرة من ملفات PSD يتضمن بضع خطوات بسيطة، وسأوضحها لك خطوة بخطوة.

## كيفية إنشاء PSD thumbnail Java – دليل خطوة بخطوة

### الخطوة 1: إعداد البيئة
إليك كيفية بدء مشروعك والتحضير لإنشاء الصور المصغرة.

1. **إنشاء مشروع Java**  
   - افتح IDE الخاص بك وأنشئ مشروع Java جديد.  
   - سمّه شيئاً مثل `"PsdThumbnailGenerator"`.

2. **إضافة مكتبة Aspose.PSD**  
   - أضف ملف JAR الخاص بـ Aspose.PSD إلى مسار بناء المشروع.  
   - إذا كنت تستخدم Maven، أدرجه في ملف `pom.xml` الخاص بك:

```xml
<dependency>
    <groupId>com.aspose</groupId>
    <artifactId>aspose-psd</artifactId>
    <version>your_version_here</version>
</dependency>
```

### الخطوة 2: تحميل ملف PSD
الخطوة التالية هي تحميل ملف PSD الذي نريد إنشاء صور مصغرة منه.

1. **تحديد مسار دليل المستندات**  
   عرّف الدليل الذي يقع فيه ملف PSD الخاص بك.

```java
String dataDir = "Your Document Directory"; // Replace with your path
```

2. **تحميل ملف PSD**  
   استخدم الفئة `PsdImage` لتحميل ملف PSD.

```java
PsdImage image = (PsdImage) Image.load(dataDir + "sample.psd");
```

> **نصيحة احترافية:** احفظ ملفات PSD في مجلد مخصص (مثلاً `src/main/resources`) لتجنب مشاكل المسارات.

### الخطوة 3: استعراض موارد PSD
الآن بعد أن تم تحميل صورة PSD، الخطوة التالية هي فحص مواردها.

1. **الحصول على عدد الموارد**  
   سنقوم بالتكرار عبر جميع الموارد في ملف PSD.

```java
for (int i = 0; i < image.getImageResources().length; i++) {
    // Processing resources
}
```

2. **تحديد موارد الصورة المصغرة**  
   داخل الحلقة، تحقق مما إذا كان المورد صورة مصغرة.

```java
if (image.getImageResources()[i] instanceof ThumbnailResource) {
    // Process the thumbnail
}
```

### الخطوة 4: معالجة الصورة المصغرة
بمجرد تحديد مورد صورة مصغرة، سنحتاج إلى التعامل معه وفقاً لذلك.

1. **استرجاع وفحص صيغة الصورة المصغرة**  
   إذا كان المورد فعلاً صورة مصغرة، استرجعه وتحقق من صيغته.

```java
ThumbnailResource thumbnail = (ThumbnailResource) image.getImageResources()[i];
if (thumbnail.getFormat() == ThumbnailFormat.KJpegRgb) {
    // Create and save the thumbnail
}
```

### الخطوة 5: إنشاء وحفظ الصورة المصغرة
هنا يحدث السحر! سننشئ صورة جديدة من بيانات الصورة المصغرة ونحفظها.

1. **إنشاء صورة جديدة**  
   سنستخدم عرض وارتفاع مورد الصورة المصغرة لإنشاء صورة bitmap جديدة.

```java
PsdImage thumbnailImage = new PsdImage(thumbnail.getWidth(), thumbnail.getHeight());
```

2. **نقل البكسلات إلى الصورة الجديدة**  
   انقل بيانات الصورة المصغرة إلى الصورة التي تم إنشاؤها حديثاً.

```java
thumbnailImage.savePixels(thumbnailImage.getBounds(), thumbnail.getThumbnailData());
```

3. **حفظ صورة المصغرة**  
   أخيراً، احفظ صورة المصغرة في دليل المستندات الخاص بك باسم فريد.

```java
thumbnailImage.save(dataDir + "CreateThumbnailsFromPSDFiles_out_" + i + ".bmp");
```

> **خطأ شائع:** نسيان إغلاق كائنات `PsdImage` قد يؤدي إلى تسرب الذاكرة. احرص على وضع شفرة التعامل مع الصورة داخل كتلة try‑with‑resources إذا كنت تستخدم Java 7+.

## الخاتمة
باتباعك لهذه الخطوات، أصبح لديك الآن طريقة ثابتة وقابلة لإعادة الاستخدام لإنشاء **create PSD thumbnail Java** التي تستخرج صور المعاينة من أي ملف Photoshop. يمكن دمج هذه التقنية في معالجات دفعية، أو خدمات ويب، أو أدوات سطح مكتب لتسريع فهرسة الصور وتحسين استجابة واجهة المستخدم. جرّبها مع مجموعة PSD الخاصة بك وشاهد مدى السرعة التي يمكنك بها توليد معاينات خفيفة الوزن!

## الأسئلة المتكررة
### ما هو Aspose.PSD؟
Aspose.PSD هي مكتبة Java تسمح للمطورين بالعمل مع ملفات Photoshop، مما يسهل تعديل وإدارة ملفات PSD برمجياً.

### هل يمكنني استخدام Aspose.PSD مجاناً؟
نعم، تقدم Aspose نسخة تجريبية مجانية يمكنك استخدامها لاختبار المكتبة قبل شراء الترخيص.

### بأي صيغ يمكنني حفظ الصور المصغرة؟
في هذا المثال، حفظنا الصور المصغرة بصيغة BMP، لكن Aspose.PSD يدعم صيغاً أخرى متعددة كذلك.

### هل أحتاج إلى تثبيت Photoshop لاستخدام Aspose.PSD؟
لا، Aspose.PSD يعمل بشكل مستقل عن Photoshop.

### أين يمكنني العثور على مزيد من المعلومات حول Aspose.PSD؟
يمكنك الاطلاع على [توثيق Aspose.PSD](https://reference.aspose.com/psd/java/) لمزيد من التفاصيل، والدروس، والموارد.

## أسئلة شائعة

**س: كيف يمكنني استخراج الصور المصغرة من PSD محمي بكلمة مرور؟**  
ج: حمّل ملف PSD باستخدام النسخة المت overloaded من `Image.load` التي تقبل معامل كلمة المرور.

**س: هل يمكنني توليد الصور المصغرة بصيغة PNG بدلاً من BMP؟**  
ج: بالتأكيد. غيّر امتداد الملف في طريقة `save` وستقوم Aspose.PSD بإجراء التحويل.

**س: هل هناك طريقة لمعالجة عدة ملفات PSD دفعة واحدة؟**  
ج: ضع الشيفرة داخل حلقة تتكرر على دليل يحتوي على ملفات PSD، مع إعادة استخدام منطق الاستخراج لكل ملف.

**س: ما نسخة Java المطلوبة؟**  
ج: تدعم Aspose.PSD Java 8 وما بعدها. يُنصح باستخدام أحدث JDK للأداء والأمان.

**س: هل تتعامل المكتبة بفعالية مع ملفات PSD الكبيرة؟**  
ج: نعم، تستخدم Aspose.PSD التحميل الكسول وإدارة الذاكرة المحسّنة للعمل مع ملفات كبيرة دون استنزاف مساحة الـ heap.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**آخر تحديث:** 2026-03-13  
**تم الاختبار مع:** Aspose.PSD 24.11 for Java (أحدث نسخة وقت الكتابة)  
**المؤلف:** Aspose  

---