---
title: أضف تأثير طبقة الظل الداخلي في PSD باستخدام Java
linktitle: أضف تأثير طبقة الظل الداخلي في PSD باستخدام Java
second_title: Aspose.PSD جافا API
description: تعرف على كيفية إضافة تأثير الظل الداخلي إلى ملفات PSD باستخدام Aspose.PSD لـ Java من خلال هذا البرنامج التعليمي خطوة بخطوة، بما في ذلك النصائح وأفضل الممارسات.
weight: 12
url: /ar/java/advanced-psd-layer-features-effects/add-inner-shadow-layer-effect-psd/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# أضف تأثير طبقة الظل الداخلي في PSD باستخدام Java

## مقدمة
هل أنت مستعد للغوص في عالم برمجة التصميم الجرافيكي؟ إذا كنت ترغب في التعامل مع ملفات PSD برمجيًا، فأنت في المكان الصحيح! سنستكشف اليوم كيفية إضافة تأثير طبقة الظل الداخلي إلى ملف PSD (مستند Photoshop) باستخدام Aspose.PSD لـ Java. تسمح هذه المكتبة القوية لمطوري Java بالعمل مع ملفات PSD بكفاءة، مما يتيح مجموعة من عمليات معالجة الصور، بدءًا من التعديلات البسيطة وحتى التأثيرات المعقدة.
## المتطلبات الأساسية
قبل أن نتعمق في عملية الترميز، دعنا نجهزك. إليك ما تحتاج إلى وضعه في مكانه:
1.  Java Development Kit (JDK): تأكد من تثبيت JDK على نظامك. إنه ضروري لتجميع وتشغيل كود Java. إذا لم يكن لديك بعد، يمكنك تنزيله من[موقع أوراكل](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).
2. مكتبة Aspose.PSD: ستحتاج إلى الوصول إلى مكتبة Aspose.PSD. يمكنك تنزيله بسهولة من[النشرات Aspose](https://releases.aspose.com/psd/java/). إنها أداة قوية للتعامل مع ملفات PSD، لذا تأكد من الحصول على أحدث إصدار.
3. بيئة تطوير متكاملة (IDE): بينما يمكنك استخدام أي محرر نصوص، فمن المستحسن استخدام بيئة تطوير متكاملة مثل IntelliJ IDEA أو Eclipse أو NetBeans. توفر هذه ميزات مفيدة مثل أدوات تمييز بناء الجملة وتصحيح الأخطاء.
4. معرفة Java الأساسية: سيساعدك الإلمام بأساسيات Java مثل المتغيرات والفئات والأساليب على المتابعة بسلاسة.
5. نموذج ملف PSD: لاختبار الكود، تأكد من أن لديك نموذج ملف PSD. يمكنك إنشاء واحدة في Adobe Photoshop أو تنزيل عينة مجانية عبر الإنترنت.
## حزم الاستيراد
بمجرد الانتهاء من إعداد كل شيء وجاهز للاستخدام، فإن الخطوة الأولى هي استيراد الحزم الضرورية في فئة Java الخاصة بك. يعد هذا أمرًا بالغ الأهمية للوصول إلى وظائف Aspose.PSD. 
## استيراد الحزم المطلوبة
```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
import com.aspose.psd.fileformats.psd.layers.layereffects.IShadowEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import com.aspose.psd.imageoptions.PsdOptions;
```
في هذه السطور، نحضر الفصول التي نحتاجها من مكتبة Aspose.
الآن بعد أن قمنا باستيراد حزمنا وإعداد بيئتنا، فلننتقل إلى التفاصيل الجوهرية للتعليمات البرمجية. سأقسمها إلى خطوات يمكن التحكم فيها.
## الخطوة 1: تحديد الدلائل
في هذه الخطوة، سنحدد مكان وجود ملف PSD المصدر والمكان الذي نريد حفظ النسخة المعدلة فيه. 
```java
String sourceDir = "Your Source Directory";
String outputDir = "Your Document Directory";
String sourceFile = sourceDir + "sample.psd";
String destName = outputDir + "sample_out.psd";
```
 يستبدل`"Your Source Directory"` و`"Your Document Directory"` مع المسارات الفعلية على جهاز الكمبيوتر الخاص بك. هذا هو المكان الذي تخبر فيه برنامجك بمكان البحث عن ملف PSD ومكان حفظ الإصدار الجديد.
## الخطوة 2: قم بتحميل ملف PSD
 بعد ذلك، نحتاج إلى تحميل ملف PSD الموجود في ملف`PsdImage` هدف. سنقوم أيضًا بتكوين خيارات التحميل لتشمل التأثيرات.
```java
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);
PsdImage image = (PsdImage) Image.load(sourceFile, loadOptions);
```
 هنا، نقوم بإنشاء مثيل لـ`PsdLoadOptions` ، وإعداده لتحميل موارد التأثير، ثم تحميل نموذج ملف PSD الخاص بنا إلى كائن يسمى`image`. إنه مثل فتح كتاب قبل القراءة!
## الخطوة 3: الوصول إلى طبقة التأثير
الآن، دعنا نصل إلى الطبقة الأخيرة في ملف PSD الخاص بنا (بافتراض أن هذه هي الطبقة التي نريد تطبيق تأثيرنا عليها).
```java
try {
    Layer layer = image.getLayers()[image.getLayers().length - 1];
```
يصل هذا الخط إلى الطبقة الأخيرة من صورة PSD الخاصة بنا. في Photoshop، تكون الطبقات مثل الأوراق الشفافة المكدسة فوق بعضها البعض، وغالبًا ما يكون الجزء العلوي هو ما تراه أولاً.
## الخطوة 4: تكوين تأثير الظل الداخلي
سيطبق مقتطف الكود هذا تأثير الظل الداخلي على طبقتنا. 
```java
    IShadowEffect shadowEffect = (IShadowEffect) layer.getBlendingOptions().getEffects()[0];
    shadowEffect.setColor(Color.getGreen());
    shadowEffect.setOpacity((byte) 128);
    shadowEffect.setDistance(1);
    shadowEffect.setUseGlobalLight(false);
    shadowEffect.setSize(2);
    shadowEffect.setAngle(45);
    shadowEffect.setSpread(50);
    shadowEffect.setNoise(5);
```
هنا يحدث السحر! يلتقط هذا الكود تأثير الظل من خيارات مزج الطبقة ويضبط خصائصه:
- اللون: يضبط الظل على اللون الأخضر.
- العتامة: تجعلها شبه شفافة.
- المسافة: لتحريك الظل قليلاً من حافة الطبقة.
- الحجم: يحدد حجم الظل.
- الزاوية: تحدد اتجاه مصدر الضوء.
- الانتشار والضوضاء: افتح الخيارات الإبداعية لكيفية ظهور الظل.
## الخطوة 5: احفظ ملف PSD المعدل
بمجرد تطبيق جميع الإعدادات، فإن الخطوة التالية هي حفظ ملف PSD المعدل.
```java
    image.save(destName, new PsdOptions(image));
```
هذا الخط يحفظ تغييراتنا. يتم تسمية ملف الإخراج`sample_out.psd`، ويتضمن جميع التأثيرات التي تم تطبيقها للتو. إنه مثل النقر على "حفظ" في Photoshop بعد إجراء التعديلات.
## الخطوة 6: تنظيف الموارد
وأخيرًا، سنتأكد من تحرير أي موارد استخدمناها.
```java
} finally {
    image.dispose();
}
```
 يعد هذا ممارسة جيدة لمنع تسرب الذاكرة. من خلال التخلص من`image` الكائن، ونحن نضمن أن تطبيقنا يعمل بسلاسة وكفاءة.
## خاتمة
وهنا لديك! في بضع خطوات بسيطة، تعلمت كيفية إضافة تأثير الظل الداخلي إلى الطبقات في ملف PSD باستخدام Aspose.PSD لـ Java. توفر هذه المكتبة إمكانات رائعة لأي شخص يتطلع إلى أتمتة مهام التصميم الجرافيكي أو دمج ميزات معالجة الصور في تطبيقات Java الخاصة به. 

## الأسئلة الشائعة
### ما هو Aspose.PSD؟  
Aspose.PSD هي مكتبة Java للعمل مع ملفات PSD، مما يسمح للمطورين بمعالجة تأثيرات الطبقة والأقنعة وخصائص الصورة برمجيًا.
### هل أحتاج إلى Photoshop لاستخدام Aspose.PSD؟  
لا، لا تحتاج إلى Photoshop لاستخدام Aspose.PSD. تعمل المكتبة بشكل مستقل لمعالجة ملفات PSD.
### هل يمكنني تطبيق تأثيرات متعددة على نفس الطبقة؟  
قطعاً! يمكنك تطبيق تأثيرات متعددة عن طريق الوصول إلى كل نوع تأثير بشكل مشابه لكيفية وصولنا إلى تأثير الظل الداخلي.
### هل Aspose.PSD مجاني؟  
Aspose.PSD هو منتج تجاري؛ ومع ذلك، يمكنك استخدام النسخة التجريبية المجانية المتاحة من خلال Aspose.
### أين يمكنني العثور على المزيد من الوثائق؟  
 يمكنك العثور على وثائق شاملة لـ Aspose.PSD[هنا](https://reference.aspose.com/psd/java/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
