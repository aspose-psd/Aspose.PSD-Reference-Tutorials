---
title: إدارة السطوع والتباين في طبقات PSD - Java
linktitle: إدارة السطوع والتباين في طبقات PSD - Java
second_title: Aspose.PSD جافا API
description: تعلم كيفية ضبط السطوع والتباين في ملفات PSD باستخدام Aspose.PSD لـ Java دون عناء. مثالية للمطورين ومصممي الجرافيك.
weight: 21
url: /ar/java/psd-image-modification-conversion/manage-brightness-contrast-psd-layers/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# إدارة السطوع والتباين في طبقات PSD - Java

## مقدمة

هل أنت مصمم جرافيك أو مطور يعمل بشكل متكرر مع ملفات PSD (مستندات Photoshop)؟ هل تجد نفسك بحاجة إلى ضبط السطوع والتباين للطبقات في هذه الملفات ولكنك تفتقر إلى المعرفة اللازمة لأتمتة هذه المهمة باستخدام Java؟ حسنًا، أنت محظوظ! في هذا البرنامج التعليمي، سنتعمق في كيفية إدارة السطوع والتباين في طبقات PSD باستخدام مكتبة Aspose.PSD لـ Java. لن يوفر لك هذا الوقت فحسب، بل سيعزز أيضًا سير عملك الإبداعي. دعونا نشمر عن سواعدنا ونبدأ!

## المتطلبات الأساسية

قبل أن نبدأ هذه الرحلة المثيرة لمعالجة ملفات PSD باستخدام Java، من الضروري التأكد من إعداد كل ما تحتاجه بشكل صحيح. إليك ما ستحتاجه لإكمال هذا البرنامج التعليمي بنجاح:

1.  Java Development Kit (JDK): تأكد من تثبيت JDK 8 أو أعلى على جهازك. يمكنك تنزيله من[موقع أوراكل](https://www.oracle.com/java/technologies/javase-jdk8-downloads.html).

2. Aspose.PSD لمكتبة Java: للعمل مع ملفات PSD، ستحتاج إلى مكتبة Aspose.PSD. يمكنك تنزيل أحدث إصدار من[صفحة الإصدار](https://releases.aspose.com/psd/java/).

3. بيئة تطوير متكاملة (IDE) من اختيارك: تُفضل بيئة التطوير المتكاملة (IDE) مثل IntelliJ IDEA أو Eclipse أو NetBeans لكتابة تعليمات Java البرمجية وتشغيلها.

4. المعرفة الأساسية بجافا: الإلمام ببرمجة جافا سيساعدك على فهم مقتطفات التعليمات البرمجية التي سنعمل معها.

بمجرد استيفاء هذه المتطلبات الأساسية، نكون جاهزين للمضي قدمًا. الآن، احصل على محرر الأكواد المفضل لديك ودعنا نبدأ في البرمجة!

## حزم الاستيراد

الخطوة الأولى في رحلة البرمجة لدينا هي استيراد الحزم اللازمة. قبل أن تتمكن من الاستفادة من الوظائف التي يوفرها Aspose.PSD، ستحتاج إلى التأكد من وجود المكتبة في مسار الفصل الدراسي الخاص بك. وإليك كيف يمكنك القيام بذلك:

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.BrightnessContrastLayer;
```

من خلال إكمال هذه الخطوات، فإنك تقوم بإعداد المشهد للعمل مع ملفات PSD بفعالية!

الآن بعد أن قمنا بإعداد كل شيء، حان الوقت للدخول في جوهر البرنامج التعليمي: ضبط السطوع والتباين في طبقات PSD. سنقوم بتقسيم هذه العملية إلى خطوات واضحة للتأكد من أنه يمكنك المتابعة بسهولة.

## الخطوة 1: تحديد دليل المستندات الخاص بك

ابدأ بتحديد الدليل الذي توجد به ملفات PSD الخاصة بك. تساعد هذه الخطوة في تنظيم ملفاتك بكفاءة.

```java
String dataDir = "Your Document Directory";
```

 يستبدل`"Your Document Directory"` مع المسار الفعلي إلى دليل ملف PSD الخاص بك.

## الخطوة 2: تحديد أسماء الملفات المصدر والوجهة

بعد ذلك، تحتاج إلى تحديد اسم الملف المصدر لملف PSD الخاص بك والملف الوجهة الذي سيتم حفظ ملف PSD المعدل فيه.

```java
String sourceFileName = dataDir + "BrightnessContrastModern.psd";
String psdPathAfterChange = dataDir + "BrightnessContrastModernChanged.psd";
```

 في هذا المثال، نفترض أن لديك ملف PSD باسم`BrightnessContrastModern.psd` في الدليل الخاص بك.

## الخطوة 3: قم بتحميل ملف PSD

حان الوقت الآن لتحميل ملف PSD في تطبيقك حتى تتمكن من معالجته.

```java
PsdImage im = (PsdImage) Image.load(sourceFileName);
```

 يقوم هذا السطر من التعليمات البرمجية بإنشاء مثيل لـ`PsdImage` يمثل ملف PSD الخاص بك. وبهذا، يمكنك الآن الوصول إلى جميع طبقات PSD.

## الخطوة 4: التكرار عبر الطبقات

تتضمن الخطوة التالية التكرار خلال كل طبقة من ملف PSD الخاص بك للعثور على إعدادات السطوع والتباين ومعالجتها.

```java
for(int i = 0; i < im.getLayers().length; i++) {
    if (im.getLayers()[i] instanceof BrightnessContrastLayer) {
        BrightnessContrastLayer brightnessContrastLayer = (BrightnessContrastLayer)im.getLayers()[i];
```

 ال`for` تمر الحلقة عبر كل طبقة من PSD. نحن نتحقق مما إذا كانت الطبقة هي مثيل لـ`BrightnessContrastLayer`. يعد هذا ضروريًا لضمان محاولتك فقط تغيير السطوع والتباين في الطبقات الصحيحة.

## الخطوة 5: ضبط السطوع والتباين

 داخل الحلقة، يمكنك الآن ضبط السطوع والتباين لكل منها`BrightnessContrastLayer`. 

```java
        brightnessContrastLayer.setBrightness(50);
        brightnessContrastLayer.setContrast(50);
    }
}
```

 في هذا المثال، قمنا بتعيين السطوع والتباين ل`50`. يمكنك ضبط هذه القيم بناءً على متطلباتك. يؤدي الرقم الأعلى إلى زيادة السطوع/التباين، بينما يؤدي الرقم الأقل إلى تقليله.

## الخطوة 6: حفظ التغييرات

الخطوة الأخيرة هي حفظ التغييرات في ملف PSD. ستحتاج إلى إعادة كتابة الصورة المعدلة إلى الوجهة المحددة.

```java
im.save(psdPathAfterChange);
```

يحفظ سطر التعليمات البرمجية هذا ملف PSD المعدل بإعدادات السطوع والتباين الجديدة.

## خاتمة

تهانينا! لقد تعلمت بنجاح كيفية إدارة السطوع والتباين في طبقات PSD باستخدام Aspose.PSD لـ Java. ومن خلال أتمتة هذه التعديلات، فإنك لا تحسن سير عملك فحسب، بل تزيد إنتاجيتك أيضًا. في المرة القادمة التي تحتاج فيها إلى تعديل تلك الصور، ستكون مجهزًا جيدًا للتعامل مع المهمة باستخدام مهارات Java الجديدة لديك. إذن، ما الذي ستنشئه بعد ذلك؟

## الأسئلة الشائعة

### ما هو Aspose.PSD لجافا؟
Aspose.PSD for Java هي مكتبة تسمح للمطورين بمعالجة ملفات PSD برمجيًا، مما يتيح أتمتة المهام المتعلقة بـ Photoshop.

### هل يمكنني ضبط السطوع والتباين لطبقات متعددة في وقت واحد؟
 نعم، يتكرر الأسلوب المستخدم في هذا البرنامج التعليمي عبر جميع الطبقات في ملف PSD، مما يسمح لك بضبط عدة طبقات`BrightnessContrastLayer` الحالات.

### كيف يمكنني الحصول على ترخيص مؤقت لـ Aspose.PSD؟
 يمكنك الحصول على ترخيص مؤقت بزيارة[صفحة الترخيص المؤقتة](https://purchase.aspose.com/temporary-license/).

### هل هناك نسخة تجريبية مجانية متاحة لـ Aspose.PSD؟
 نعم، يمكنك تنزيل نسخة تجريبية مجانية من Aspose.PSD من الموقع[صفحة الإصدار](https://releases.aspose.com/).

### أين يمكنني العثور على دعم إضافي لـ Aspose.PSD؟
 يمكنك الحصول على الدعم لـ Aspose.PSD على موقعهم[منتدى الدعم](https://forum.aspose.com/c/psd/34).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
