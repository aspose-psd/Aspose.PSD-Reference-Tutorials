---
title: أضف طبقة ضبط تشبع اللون إلى PSD
linktitle: أضف طبقة ضبط تشبع اللون إلى PSD
second_title: Aspose.PSD جافا API
description: تعرف على كيفية إضافة طبقات ضبط تشبع اللون إلى PSD باستخدام Aspose.PSD لـ Java في هذا البرنامج التعليمي الشامل خطوة بخطوة. تعزيز سير عمل التصميم الجرافيكي الخاص بك.
weight: 14
url: /ar/java/modifying-converting-psd-images/add-hue-saturation-adjustment-layer-psd/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# أضف طبقة ضبط تشبع اللون إلى PSD

## مقدمة
عندما يتعلق الأمر بالتصميم الجرافيكي، يلعب التلاعب بالألوان دورًا محوريًا - على وجه التحديد، يمكن أن يؤدي تغيير اللون والتشبع والخفة إلى تغيير الحالة المزاجية وجودة أي صورة بشكل جذري. إحدى الطرق الفعالة لتحقيق ذلك هي استخدام طبقات الضبط في Photoshop (ملفات PSD). إذا كنت تتطلع إلى تحسين ملفات PSD الخاصة بك برمجيًا باستخدام Java، فإن مكتبة Aspose.PSD موجودة لمساعدتك! سيأخذك هذا البرنامج التعليمي عبر خطوات إضافة طبقة ضبط تشبع اللون إلى ملفات PSD الخاصة بك، مما يجعل سير العمل الخاص بك أكثر إنتاجية وكفاءة.
في هذا الدليل، سنغطي كل شيء بدءًا من استيراد الحزم الضرورية وحتى التفاصيل الدقيقة لأمثلة التعليمات البرمجية.
## المتطلبات الأساسية
قبل أن ننتقل إلى الكود، تأكد من أن لديك ما يلي:
1.  Java Development Kit (JDK): تأكد من تثبيت JDK 8 أو أعلى على جهازك. يمكنك تنزيله من[تحميل مجموعة أدوات تطوير Java SE](https://www.oracle.com/java/technologies/javase-downloads.html).
2.  Aspose.PSD لمكتبة Java: ستحتاج إلى مكتبة Aspose.PSD، وهو ما يمكنك فعله[تحميل هنا](https://releases.aspose.com/psd/java/). 
3. IDE: بيئة تطوير متكاملة مناسبة (IDE) مثل IntelliJ IDEA أو Eclipse لتطوير Java.
4. المعرفة الأساسية بجافا: الإلمام ببرمجة جافا يعد ميزة إضافية، لكن لا تقلق؛ سنرشدك عبر الكود خطوة بخطوة.
الآن بعد أن قمنا بفرز المتطلبات الأساسية، دعنا ننتقل إلى الجزء الممتع - البرمجة!
## حزم الاستيراد
لبدء العمل مع مكتبة Aspose.PSD، الخطوة الأولى هي استيراد الفئات الضرورية. إليك كيفية القيام بذلك في ملف Java الخاص بك:
```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.HueSaturationLayer;
import com.aspose.psd.fileformats.psd.layers.layerresources.ColorRangeHsl;
```
تأكد من إضافة المكتبات المناسبة إلى مشروعك حتى تعمل هذه الواردات بسلاسة.
## الخطوة 1: قم بإعداد دليل المستندات الخاص بك
كل مشروع يحتاج إلى نقطة بداية، ومشروعنا ليس استثناءً. تحتاج إلى تحديد دليل حيث يتم تخزين ملفات PSD الخاصة بك. يعد هذا أمرًا بالغ الأهمية لتحميل الصور وحفظها بشكل صحيح.
```java
String dataDir = "Your Document Directory"; // قم بتحديث هذا المسار إلى الدليل الفعلي الخاص بك
```
## الخطوة 2: تحميل ملف PSD موجود
لمعالجة ملف PSD موجود، نحتاج أولاً إلى تحميله في برنامجنا. وإليك كيف يمكنك القيام بذلك:
```java
String sourceFileName = dataDir + "HueSaturationAdjustmentLayer.psd";
PsdImage im = (PsdImage) Image.load(sourceFileName);
```
 في هذا الكود قم بالتحديث`"HueSaturationAdjustmentLayer.psd"` إلى اسم ملف PSD الموجود لديك والذي تريد تحريره.
## الخطوة 3: تحرير طبقة هوى / تشبع
بعد ذلك، سنقوم بالتمرير عبر طبقات صورة PSD المحملة للعثور على أي طبقات Hue/Saturation موجودة وتحريرها. تتضمن هذه الخطوة تعديل قيم الصبغة والتشبع والخفة.
```java
for (int i = 0; i < im.getLayers().length; i++) {
    if (im.getLayers()[i] instanceof HueSaturationLayer) {
        HueSaturationLayer hueLayer = (HueSaturationLayer) im.getLayers()[i];
        hueLayer.setHue((short) -25);
        hueLayer.setSaturation((short) -12);
        hueLayer.setLightness((short) 67);
        ColorRangeHsl colorRange = hueLayer.getRange(2);
        colorRange.setHue((short) -40);
        colorRange.setSaturation((short) 50);
        colorRange.setLightness((short) -20);
        colorRange.setMostLeftBorder((short) 300);
    }
}
```
في هذا المثال:
- نقوم بضبط درجة اللون إلى -25، والتشبع إلى -12، والخفة إلى +67.
-  ال`getRange(2)` تسمح لنا الطريقة بتعديل نطاقات ألوان معينة حسب الرغبة.
## الخطوة 4: احفظ ملف PSD المعدل
بعد إجراء التعديلات، الخطوة التالية هي حفظ الملف. يعد هذا جزءًا حيويًا من عمليتنا، مما يضمن عدم ضياع التغييرات التي أجريناها.
```java
String psdPathAfterChange = dataDir + "HueSaturationAdjustmentLayerChanged.psd";
im.save(psdPathAfterChange);
```
## الخطوة 5: إضافة طبقة هوى / تشبع جديدة
بعد ذلك، قد ترغب في إضافة طبقة ضبط Hue/Saturation جديدة إلى ملف PSD آخر. ما عليك سوى اتباع نفس الطريقة التي استخدمتها سابقًا ولكن مع ملفات PSD مختلفة.
```java
sourceFileName = dataDir + "PhotoExample.psd";
PsdImage img = (PsdImage) Image.load(sourceFileName);
HueSaturationLayer hueLayerNew = img.addHueSaturationAdjustmentLayer();
```
## الخطوة 6: قم بتعيين قيم هوى / تشبع جديدة للطبقة الجديدة
الآن بعد أن قمت بإنشاء هذه الطبقة الجديدة، قم بتطبيق إعدادات الصبغة والتشبع والخفة المطلوبة تمامًا كما كان من قبل.
```java
hueLayerNew.setHue((short) -25);
hueLayerNew.setSaturation((short) -12);
hueLayerNew.setLightness((short) 67);
ColorRangeHsl newColorRange = hueLayerNew.getRange(2);
newColorRange.setHue((short) -160);
newColorRange.setSaturation((short) 100);
newColorRange.setLightness((short) 20);
newColorRange.setMostLeftBorder((short) 300);
```
## الخطوة 7: احفظ ملف PSD المحدث
أخيرًا، احفظ ملف PSD مع طبقة Hue/Saturation المضافة حتى تتمكن من رؤية تغييراتك.
```java
String psdPathAfterNewLayerChange = dataDir + "PhotoExampleAddedHueSaturation.psd";
img.save(psdPathAfterNewLayerChange);
```
تهانينا! لقد نجحت في معالجة ملفات PSD باستخدام Aspose.PSD لـ Java. الآن، يمكنك تجربة صور مختلفة وتعديلات أعمق، لإضفاء الحيوية على مشاريع التصميم الجرافيكي الخاصة بك.
## خاتمة
يفتح العمل مع الرسومات برمجيًا عالمًا من الإمكانيات. يوفر استخدام Aspose.PSD لـ Java لإضافة طبقات ضبط Hue Saturation وتعديلها المرونة والكفاءة التي يمكنها تبسيط سير عمل التصميم الخاص بك. سواء كنت تقوم بتحسين الصور لمشروع ما أو إنشاء محتوى مرئي مذهل، فإن إتقان هذه الأدوات يمكن أن يؤدي إلى تحسين مخرجاتك بشكل كبير.
 لا تتردد في استكشاف المزيد من وظائف Aspose.PSD من خلال الغوص فيها[الوثائق](https://reference.aspose.com/psd/java/) أو فكر في التمزق أ[ترخيص مؤقت](https://purchase.aspose.com/temporary-license/) لاختبار القوة الكاملة للمكتبة.
## الأسئلة الشائعة
### ما هي طبقة تعديل تشبع هوى؟
تسمح لك طبقة ضبط تشبع اللون بتعديل خصائص لون الصورة دون تغيير وحدات البكسل الأصلية بشكل دائم.
### هل أحتاج إلى تثبيت برنامج Photoshop لاستخدام Aspose.PSD؟
لا، Aspose.PSD هي مكتبة مستقلة تعمل بشكل مستقل عن Photoshop.
### هل يمكنني استخدام Aspose.PSD لمعالجة الدفعات؟
نعم، يمكنك أتمتة ومعالجة ملفات PSD متعددة باستخدام Aspose.PSD.
### هل Aspose.PSD مجاني؟
يقدم Aspose.PSD نسخة تجريبية مجانية، ولكن يلزم الحصول على ترخيص للاستخدام على المدى الطويل. يمكنك عرض التسعير[هنا](https://purchase.aspose.com/buy).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
