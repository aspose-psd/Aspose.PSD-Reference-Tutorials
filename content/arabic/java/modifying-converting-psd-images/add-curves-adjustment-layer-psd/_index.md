---
title: أضف طبقة ضبط المنحنيات في PSD باستخدام Java
linktitle: أضف طبقة ضبط المنحنيات في PSD باستخدام Java
second_title: Aspose.PSD جافا API
description: تعرف على كيفية إضافة طبقة ضبط المنحنيات إلى ملف PSD باستخدام Aspose.PSD لـ Java في هذا البرنامج التعليمي المفصل. تعزيز الصور الخاصة بك بسهولة.
type: docs
weight: 11
url: /ar/java/modifying-converting-psd-images/add-curves-adjustment-layer-psd/
---
## مقدمة
هل وجدت نفسك عالقًا أثناء محاولتك معالجة الصور بتنسيق PSD؟ سواء كنت مصمم رسومات ناشئًا أو محترفًا متمرسًا، فإن العمل باستخدام ملفات Photoshop قد يبدو أحيانًا وكأنه يتنقل في متاهة. لحسن الحظ، هناك أداة تعمل على تبسيط هذه العملية - Aspose.PSD لـ Java. في هذا البرنامج التعليمي، سنتعمق في كيفية إضافة طبقة ضبط المنحنيات إلى ملف PSD باستخدام Aspose.PSD، مما يجعل مهام تحرير الصور الخاصة بك أسهل وأكثر كفاءة. من خلال التوجيه خطوة بخطوة، ستتمكن من تحسين صورك مثل المحترفين دون التورط في التعقيدات المرتبطة تقليديًا بمعالجة الصور.
## المتطلبات الأساسية
قبل أن نتعمق في الكود، دعنا نتأكد من أنك جاهز تمامًا. فيما يلي المتطلبات الأساسية التي ستحتاج إليها:
1. Java Development Kit (JDK): ستحتاج إلى تثبيت JDK على جهاز الكمبيوتر الخاص بك. تأكد من أنه الإصدار الأحدث للحصول على أفضل توافق.
2. Aspose.PSD لمكتبة Java: لمعالجة ملفات PSD، ستحتاج إلى تنزيل مكتبة Aspose.PSD وتضمينها في مشروعك. يمكنك الاستيلاء عليها[هنا](https://releases.aspose.com/psd/java/).
3. IDE: استخدم أي Java IDE مثل IntelliJ IDEA أو Eclipse أو حتى محرر نص بسيط لكتابة التعليمات البرمجية الخاصة بك.
4. الفهم الأساسي لجافا: الإلمام ببرمجة جافا سيساعدك على المتابعة بسلاسة.
حصلت على كل شيء؟ مذهل! دعونا ندخل في الجزء الممتع.
## استيراد الحزم
أول الأشياء أولاً، تحتاج إلى استيراد الحزم المطلوبة. إليك كيفية القيام بذلك:
```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.CurvesLayer;
import com.aspose.psd.fileformats.psd.layers.layerresources.CurvesContinuousManager;
import com.aspose.psd.fileformats.psd.layers.layerresources.CurvesDiscreteManager;
```
من خلال استيراد هذه الحزم، فإنك تخبر تطبيق Java الخاص بك عن الفئات التي يحتاجها لمعالجة ملفات PSD والعمل بشكل خاص مع طبقات Curves Adjustment.
الآن بعد أن قمنا بإعداد كل شيء، دعونا نقسم الكود ونرى كيفية إضافة طبقة ضبط المنحنيات خطوة بخطوة.
## الخطوة 1: تحديد دليل البيانات الخاص بك
الخطوة الأولى هي تحديد مكان تخزين ملفات PSD الخاصة بك. قم بتعيين دليل للحفاظ على كل شيء منظمًا.
```java
String dataDir = "Your Document Directory"; // قم بتحديث هذا المسار
```
 فكر في`dataDir`كمساحة العمل الخاصة بك؛ إنه المكان الذي يحدث فيه كل السحر! تأكد من استبدال`Your Document Directory` بالمسار الفعلي حيث توجد أو ستوجد ملفات PSD الخاصة بك.
## الخطوة 2: قم بتحميل ملف PSD الخاص بك
بعد ذلك، ستحتاج إلى تحميل ملف PSD الذي تريد تحريره. ويتم ذلك باستخدام الكود التالي:
```java
String sourceFileName = dataDir + "CurvesAdjustmentLayer";
String psdPathAfterChange = dataDir + "CurvesAdjustmentLayerChanged";
```
 في مقتطف الكود هذا،`sourceFileName` يشير إلى ملف PSD الأصلي، بينما`psdPathAfterChange` هو المكان الذي ستحفظ فيه ملفك المعدل. لا تنسى أن إلحاق`.psd` لاحقًا في الكود.
## الخطوة 3: التكرار على الطبقات
حان الوقت الآن للبحث في طبقات ملف PSD الخاص بك. سنقوم بالتكرار خلال كل طبقة بحثًا عن طبقات ضبط المنحنيات.
```java
for (int j = 1; j < 2; j++) {
    String fileName = sourceFileName + ".psd";
    PsdImage im = (PsdImage) Image.load(fileName);
    
    for(int k = 0; k < im.getLayers().length; k++) {
        if (im.getLayers()[k] instanceof CurvesLayer) {
            // ستتم معالجة طبقة المنحنيات هنا
        }
    }
}
```
وفيما يلي تفصيل لما يحدث:
-  نبدأ بتحميل ملف PSD إلى ملف`PsdImage` الكائن المسمى`im`.
-  بعد ذلك، نقوم بتمرير جميع الطبقات الموجودة في الصورة باستخدام`im.getLayers().length` . وهذا يتيح لنا الوصول إلى كل طبقة، مما يسمح لنا بالتحقق مما إذا كانت طبقة`CurvesLayer`.
## الخطوة 4: تعديل طبقة المنحنيات
 داخل الحلقة التي تتحقق من`CurvesLayer`، ستضيف منطقًا لتعديل المنحنيات. إليك كيفية القيام بذلك:
```java
if (curvesLayer.isDiscreteManagerUsed()) {
    CurvesDiscreteManager manager = (CurvesDiscreteManager) curvesLayer.getCurvesManager();
    for (int i = 10; i < 50; i++) {
        manager.setValueInPosition(0, (byte) i, (byte) (15 + (i * 2)));
    }
} else {
    CurvesContinuousManager manager = (CurvesContinuousManager) curvesLayer.getCurvesManager();
    manager.addCurvePoint((byte) 0, (byte) 50, (byte) 100);
    manager.addCurvePoint((byte) 0, (byte) 150, (byte) 130);
}
```
في هذا الجزء:
- نتحقق مما إذا كانت طبقة المنحنيات تستخدم مديرًا منفصلاً أو مديرًا مستمرًا.
- إذا كان مديرًا منفصلاً، فسنضع قيمًا جديدة لكل منصب من 10 إلى 49.
- على العكس من ذلك، مع المدير المستمر، نضيف نقاط منحنى لضبط المنحنيات حسب الحاجة.
## الخطوة 5: احفظ ملف PSD المعدل
بعد إجراء التعديلات، الخطوة الأخيرة هي حفظ ملف PSD المعدل.
```java
im.save(psdPathAfterChange + Integer.toString(j) + ".psd");
```
 يحفظ هذا الخط ملف PSD المعدل في المسار الذي حددته مسبقًا. في كل مرة تقوم فيها بالتعديل، سيتم إنشاء ملف جديد بلاحقة مختلفة بناءً على عداد الحلقة`j`.
## خاتمة
تهانينا! لقد تعلمت بنجاح كيفية إضافة طبقة ضبط المنحنيات إلى ملف PSD باستخدام Aspose.PSD لـ Java. من خلال بضع خطوات فقط، يمكنك تحسين صورك ومعالجتها وفقًا لاحتياجاتك. المرونة التي توفرها هذه المكتبة تجعلها أداة لا تقدر بثمن لأي شخص يعمل مع ملفات PSD. والآن قم بتجربة منحنيات مختلفة، ودع إبداعك يتدفق.
## الأسئلة الشائعة
### ما هو Aspose.PSD؟
Aspose.PSD هي مكتبة لمعالجة ملفات Photoshop PSD بلغات البرمجة المختلفة، بما في ذلك Java.
### هل يمكنني استخدام Aspose.PSD مجانًا؟
 نعم، يقدم Aspose نسخة تجريبية مجانية يمكنك استكشافها قبل الشراء. تحقق من[تنزيل تجريبي مجاني](https://releases.aspose.com/) وصلة.
### هل من الضروري تثبيت الفوتوشوب؟
لا، لا تحتاج إلى تثبيت Photoshop على جهازك للعمل مع Aspose.PSD.
### هل يمكنني التعامل مع طبقات أخرى غير طبقات ضبط المنحنيات؟
قطعاً! يسمح Aspose.PSD بمعالجة أنواع الطبقات المختلفة في ملفات PSD.
### أين يمكنني العثور على المزيد من الوثائق؟
 للحصول على وثائق مفصلة، قم بزيارة[Aspose.PSD لمستندات جافا](https://reference.aspose.com/psd/java/).