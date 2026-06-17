---
date: 2026-03-28
description: تعلم كيفية إنشاء طبقة التعرض باستخدام Aspose.PSD للغة جافا – دليل خطوة
  بخطوة لإضافة وتعديل وحفظ طبقات تعديل التعرض في ملفات PSD.
linktitle: How to create exposure layer java with Aspose.PSD
second_title: Aspose.PSD Java API
title: كيفية إنشاء طبقة التعرض في جافا باستخدام Aspose.PSD
url: /ar/java/psd-image-modification-conversion/manage-exposure-adjustment-layer-psd/
weight: 23
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# إدارة طبقة تعديل التعرض في PSD باستخدام Java

## مقدمة
عندما يتعلق الأمر بالعمل مع ملفات Photoshop برمجيًا، فإن تعلم كيفية **create exposure layer java** باستخدام Aspose.PSD يُعد تغييرًا حقيقيًا في اللعبة. تسمح لك طبقة تعديل التعرض بضبط السطوع والإزاحة والجاما ببضع أسطر من الشيفرة فقط. في هذا الدرس سنستعرض كل خطوة ضرورية لإضافة وتعديل وحفظ طبقات تعديل التعرض داخل ملف PSD باستخدام Java.

## إجابات سريعة
- **أي مكتبة؟** Aspose.PSD for Java  
- **المهمة الأساسية؟** Create exposure layer java and adjust its properties  
- **الوقت النموذجي للتنفيذ؟** 10–15 دقيقة لبرنامج أساسي  
- **المتطلبات المسبقة؟** JDK 11+, IDE، و Aspose.PSD JAR  
- **هل تحتاج إلى ترخيص؟** ترخيص مؤقت أو كامل لـ Aspose.PSD للاستخدام الإنتاجي  

## ما هو create exposure layer java؟
إنشاء طبقة التعرض في Java يعني إدراج **Exposure Adjustment Layer** برمجيًا في مستند Photoshop (PSD). تتصرف هذه الطبقة مثل تعديل “Exposure” الذي تضيفه يدويًا في Photoshop، مما يتيح لك التحكم في التعرض والإزاحة والجاما دون تحويل الصورة إلى نقطية.

## لماذا نستخدم Aspose.PSD لهذه المهمة؟
- **No Photoshop required** – العمل بالكامل على الخادم أو في خطوط أنابيب CI.  
- **Full layer fidelity** – الحفاظ على جميع الطبقات الأصلية دون تعديل أثناء تعديل التعرض.  
- **Cross‑platform** – تشغيل على Windows أو Linux أو macOS باستخدام نفس شفرة Java.  

## المتطلبات المسبقة
قبل أن نبدأ هذه الرحلة المثيرة في تعديل ملفات PSD، ستحتاج إلى إعداد بعض الأشياء على جانبك:

### بيئة Java
1. Java Development Kit (JDK): تأكد من تثبيت JDK على جهازك. إذا لم يكن مثبتًا، قم بتنزيله من [Oracle website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).  
2. IDE of Your Choice: استخدم أي بيئة تطوير مثل IntelliJ IDEA أو Eclipse أو حتى محرر نصوص بسيط لكتابة شفرة Java الخاصة بك.  
3. Aspose.PSD Library: ستحتاج إلى مكتبة Aspose.PSD لـ Java. يمكنك تنزيلها من [Aspose release page](https://releases.aspose.com/psd/java/).  
4. Basic Knowledge of Java: فهم أساسي لبرمجة Java سيساعدك كثيرًا في استيعاب المفاهيم التي يغطيها هذا الدرس.  

بمجرد أن تكون جاهزًا، يمكننا الغوص في تفاصيل إضافة وتعديل وحفظ طبقات تعديل التعرض في ملفات PSD الخاصة بك!

## استيراد الحزم
قبل أن نتمكن من البدء في تحرير ملفات PSD، سنحتاج إلى استيراد الحزم الضرورية التي توفرها Aspose.PSD. إليك الطريقة:
```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.ExposureLayer;
```
تتيح لنا هذه الاستيرادات الوصول إلى الوظائف الأساسية التي نحتاجها لتعديل ملفات PSD.

## الخطوة 1: إعداد دليل المستند الخاص بك
أولاً، دعنا نحدد الدليل الذي توجد فيه ملفات PSD الخاصة بك. ستحتاج إلى استبدال `"Your Document Directory"` بالمسار إلى الدليل المحلي الخاص بك.
```java
String dataDir = "Your Document Directory";
```
هنا، نحن في الأساس نجهز مساحة العمل لتطبيقنا. إنه مثل إعداد محطة عملك قبل بدء مشروع DIY — يجب أن يكون كل شيء جاهزًا تمامًا!

## الخطوة 2: تحميل ملف PSD للتحرير
الآن، لنحمّل ملف PSD الذي نريد تعديل التعرض فيه. سنعمل على ملف مثال يُدعى `ExposureAdjustmentLayer.psd`.
```java
String sourceFileName = dataDir + "ExposureAdjustmentLayer.psd";
PsdImage im = (PsdImage) Image.load(sourceFileName);
```
هذه هي اللحظة التي نتفاعل فيها مع ملفنا! إنه كفتح كتاب والاستعداد للغوص في صفحاته — كل طبقة هي قصة تنتظر أن تُروى.

## الخطوة 3: تعديل طبقات تعديل التعرض الحالية
بعد ذلك، سنقوم بالتكرار عبر كل طبقة في ملف PSD للتحقق مما إذا كان هناك طبقة تعديل التعرض. إذا وجدنا واحدة، سنقوم بتعديل خصائصها!
```java
for (int i = 0; i < im.getLayers().length; i++) {
    if (im.getLayers()[i] instanceof ExposureLayer) {
        ExposureLayer expLayer = (ExposureLayer) im.getLayers()[i];
        expLayer.setExposure(2);
        expLayer.setOffset(-0.25f);
        expLayer.setGammaCorrection(0.5f);
    }
}
```
هنا يحدث السحر. فكر فيها كضبط أزرار راديو قديم للحصول على الصوت المثالي — الآن، أنت تضبط مستويات التعرض!

## الخطوة 4: حفظ ملف PSD المعدل
بعد أن تقوم بضبط التعرض حسب رغبتك، حان الوقت لحفظ الملف المعدل. سنحفظه باسم `ExposureAdjustmentLayerChanged.psd`.
```java
String psdPathAfterChange = dataDir + "ExposureAdjustmentLayerChanged.psd";
im.save(psdPathAfterChange);
```
إنه كإغلاق الوصفة المثالية التي أعددتها للتو — حفظها يضمن أن كل جهدك لن يذهب سدى!

## الخطوة 5: إضافة طبقة تعديل التعرض جديدة
الآن بعد أن عدلنا واحدة موجودة، دعنا نضيف طبقة تعديل التعرض جديدة إلى ملف PSD آخر، `PhotoExample.psd`.
```java
sourceFileName = dataDir + "PhotoExample.psd";
PsdImage img = (PsdImage) Image.load(sourceFileName);
```
مثل اختيار لوحة أخرى للرسم عليها، نحن نجهز مستند PSD آخر!

## الخطوة 6: تكوين طبقة التعرض الجديدة
سنقوم بإنشاء وتكوين طبقة التعرض الجديدة بالإعدادات التي تريدها.
```java
ExposureLayer newlayer = img.addExposureAdjustmentLayer(10, -0.25f, 2f);
```
هذا مشابه لإضافة طبقة طلاء جديدة إلى تحفتك — فهو يعزز الصورة ويجددها، مضيفًا عمقًا وطابعًا.

## الخطوة 7: حفظ ملف PSD الجديد
أخيرًا، دعنا نحفظ الصورة التي عدلناها حديثًا باسم `PhotoExampleAddedExposure.psd`.
```java
String psdPathAfterChange = dataDir + "PhotoExampleAddedExposure.psd";
img.save(psdPathAfterChange);
```
وبذلك، نكون قد أنهينا مشروعًا آخر، جاهزًا لعرض إبداعنا الجديد!

## الخاتمة
إدارة طبقات تعديل التعرض في ملفات PSD باستخدام Aspose.PSD for Java ليست فقط فعّالة؛ بل هي تمكينية. يمكنك تعديل الطبقات الموجودة أو حتى إضافة طبقات جديدة، مع ضمان بروز رؤيتك الإبداعية. باتباع الخطوات المذكورة أعلاه، يمكنك تعديل صورك بفعالية باستخدام بضع أسطر من الشيفرة فقط.

مع استمرارك في استكشاف إمكانيات إدارة وتعديل الصور مع Aspose، تذكر أن كل تعديل هو خطوة نحو إنشاء الصورة المثالية.

## الأسئلة المتكررة

**س: ما هو Aspose.PSD for Java?**  
A: Aspose.PSD for Java هي مكتبة تتيح لك العمل مع ملفات Photoshop برمجيًا، مما يتيح ميزات مثل تعديل الطبقات، والتصيير، والتحويل.

**س: هل يمكنني استخدام Aspose.PSD في تطبيق ويب؟**  
A: نعم، يمكن دمج Aspose.PSD في تطبيقات الويب، مما يسمح بتعديل الصور على جانب الخادم.

**س: هل أحتاج إلى ترخيص لاستخدام Aspose.PSD؟**  
A: نعم، رغم توفر نسخة تجريبية مجانية، إلا أن الترخيص الصالح مطلوب للاستخدام الممتد. يمكنك الحصول على ترخيص مؤقت [here](https://purchase.aspose.com/temporary-license/).

**س: كيف يمكنني الحصول على دعم لـ Aspose.PSD؟**  
A: يمكنك الوصول إلى دعم المجتمع في منتديات Aspose [here](https://forum.aspose.com/c/psd/34).

**س: هل هناك مشروع مثال متاح للبدء؟**  
A: نعم، يمكنك العثور على مشاريع مثال وثائقية على [Aspose.PSD Reference page](https://reference.aspose.com/psd/java/).

---

**آخر تحديث:** 2026-03-28  
**تم الاختبار مع:** Aspose.PSD for Java 24.12 (latest)  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}