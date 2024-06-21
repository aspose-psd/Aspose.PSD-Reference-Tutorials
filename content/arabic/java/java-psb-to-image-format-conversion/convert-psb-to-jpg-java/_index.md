---
title: تحويل PSB إلى JPG في جافا
linktitle: تحويل PSB إلى JPG في جافا
second_title: Aspose.PSD جافا API
description: قم بتحويل PSB إلى JPG بسهولة في Java باستخدام Aspose.PSD. اتبع دليلنا التفصيلي لتحويلات الصور بسلاسة. قم بتنزيل Aspose.PSD وجربه وقم بشرائه.
type: docs
weight: 10
url: /ar/java/java-psb-to-image-format-conversion/convert-psb-to-jpg-java/
---
## مقدمة
مرحبًا بك في دليلنا الشامل حول تحويل ملفات PSB إلى تنسيق JPG باستخدام Aspose.PSD لـ Java! إذا كنت تتعامل مع ملفات PSB — تلك الملفات الكبيرة ذات الطبقات Photoshop — وتحتاج إلى تحويلها إلى تنسيق JPG الأكثر دعمًا عالميًا، فأنت في المكان الصحيح. في هذا البرنامج التعليمي، سنرشدك خلال العملية خطوة بخطوة. وفي النهاية، ستتمكن من تحويل ملفات PSB إلى JPG بسلاسة.
## المتطلبات الأساسية
قبل أن نتعمق في البرنامج التعليمي، دعونا نغطي المتطلبات الأساسية. إليك ما ستحتاجه للبدء:
-  Java Development Kit (JDK): تأكد من تثبيت JDK على نظامك. يمكنك تنزيله من[موقع أوراكل](https://www.oracle.com/java/technologies/javase-downloads.html).
-  Aspose.PSD لمكتبة Java: قم بتنزيل مكتبة Aspose.PSD لـ Java من[صفحة التحميل](https://releases.aspose.com/psd/java/).
- بيئة التطوير: بيئة تطوير متكاملة (IDE) مثل IntelliJ IDEA أو Eclipse أو أي محرر نصوص من اختيارك.
- ملف PSB: ملف PSB الذي ترغب في تحويله.
## استيراد الحزم
أول الأشياء أولاً، فلنستورد الحزم الضرورية. تعتبر هذه الواردات ضرورية للعمل مع مكتبة Aspose.PSD ومعالجة تحويلات الصور.
```java
import com.aspose.psd.Image;
import com.aspose.psd.examples.Utils.Utils;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import com.aspose.psd.imageoptions.JpegOptions;
```
## الخطوة 1: قم بإعداد مشروعك
قبل البدء في البرمجة، قم بإعداد مشروع Java الخاص بك. أنشئ مشروعًا جديدًا في IDE الخاص بك وأضف مكتبة Aspose.PSD for Java إلى مسار بناء مشروعك. سيمكنك هذا من استخدام الفئات والأساليب التي يوفرها Aspose.PSD.
## الخطوة 2: قم بتحميل ملف PSB
 لتحميل ملف PSB، ستحتاج إلى تحديد المسار إلى ملفك واستخدام الملف`PsdLoadOptions` لتكوين عملية التحميل. إليك كيفية القيام بذلك:
```java
String dataDir = "Your Document Directory"; // استبدل بمسار الدليل الخاص بك
String sourceFileName = dataDir + "Simple.psb";
PsdLoadOptions options = new PsdLoadOptions();
PsdImage image = (PsdImage) Image.load(sourceFileName, options);
```
 في هذه الخطوة، نقوم بتعيين الدليل الذي يوجد به ملف PSB الخاص بك ونقوم بتحميل الملف في ملف`PsdImage` الكائن باستخدام`PsdLoadOptions`.
## الخطوة 3: تكوين خيارات JPG
الآن بعد أن تم تحميل ملف PSB الخاص بك، تحتاج إلى ضبط خيارات تحويل JPG. يتضمن ذلك تحديد جودة مخرجات JPG.
```java
JpegOptions jpgOptions = new JpegOptions();
jpgOptions.setQuality(95);
```
 هنا، نقوم بإنشاء`JpegOptions` كائن وتعيين الجودة على 95. يمكنك ضبط هذه القيمة للتحكم في ضغط الصورة الناتجة وجودتها.
## الخطوة 4: احفظ الصورة بصيغة JPG
مع تعيين الخيارات، أنت جاهز لحفظ ملف PSB الخاص بك بتنسيق JPG. هذا هو المكان الذي يحدث فيه التحويل الفعلي.
```java
image.save(dataDir + "Simple_output.jpg", jpgOptions);
```
يحفظ هذا الأمر صورة PSB المحملة بتنسيق JPG في الدليل المحدد بإعدادات الجودة المحددة.
## الخطوة 5: حفظ الصورة بتنسيق PSB (اختياري)
إذا كنت تريد أيضًا حفظ الصورة المعدلة مرة أخرى كملف PSB، فيمكنك القيام بذلك باستخدام أمر مماثل:
```java
image.save(dataDir + "Simple_output.psb");
```
هذه الخطوة اختيارية ولكنها مفيدة إذا كنت بحاجة إلى الاحتفاظ بتنسيق الطبقات لملف PSB الأصلي مع ملف JPG المحول.
## خاتمة
تهانينا! لقد نجحت في تحويل ملف PSB إلى JPG باستخدام Aspose.PSD لـ Java. يرشدك هذا البرنامج التعليمي خلال إعداد مشروعك، وتحميل ملف PSB، وتكوين خيارات JPG، وحفظ الصورة المحولة. باتباع هذه الخطوات، يمكنك بسهولة التعامل مع تحويلات PSB إلى JPG في تطبيقات Java الخاصة بك.
سواء كنت مطورًا يعمل على أحد تطبيقات معالجة الصور أو تحتاج فقط إلى تحويل ملفات PSB من حين لآخر، فإن Aspose.PSD for Java يوفر حلاً قويًا لاحتياجاتك.
## الأسئلة الشائعة
### ما هو Aspose.PSD لجافا؟
Aspose.PSD for Java هي مكتبة تسمح للمطورين بمعالجة وتحويل ملفات PSD وPSB داخل تطبيقات Java. وهو يدعم العديد من الميزات بما في ذلك تحميل ملفات Photoshop وتحريرها وحفظها.
### هل يمكنني تجربة Aspose.PSD لـ Java قبل الشراء؟
 نعم، يمكنك تنزيل نسخة تجريبية مجانية من Aspose.PSD لـ Java من[صفحة التحميل](https://releases.aspose.com/). يتيح لك ذلك تقييم المكتبة وميزاتها قبل إجراء عملية الشراء.
### كيف يمكنني الحصول على ترخيص مؤقت لـ Aspose.PSD لـ Java؟
يمكنك الحصول على ترخيص مؤقت من[صفحة الترخيص المؤقتة](https://purchase.aspose.com/temporary-license/). سيسمح لك هذا باستخدام الميزات الكاملة للمكتبة لفترة محدودة.
### هل يتوفر دعم إذا واجهت مشكلات؟
 قطعاً! يمكنك الوصول إلى الدعم من خلال[منتدى دعم Aspose.PSD](https://forum.aspose.com/c/psd/34). فريق الدعم مستجيب ومستعد لمساعدتك في أي مشاكل أو أسئلة قد تكون لديك.
### هل يمكنني ضبط جودة مخرجات JPG؟
 نعم، يمكنك ضبط جودة مخرجات JPG عن طريق ضبط`Quality` الممتلكات في`JpegOptions` هدف. تتراوح القيمة من 0 إلى 100، وتشير القيم الأعلى إلى جودة أفضل وضغط أقل.