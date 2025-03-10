---
title: إضافة طبقة تعديل المستوى في PSD
linktitle: إضافة طبقة تعديل المستوى في PSD
second_title: Aspose.PSD جافا API
description: تعرف على كيفية إضافة طبقة ضبط المستوى بشكل فعال في ملفات PSD الخاصة بك باستخدام Aspose.PSD لـ Java. ارفع مهاراتك في تحرير الصور.
weight: 16
url: /ar/java/modifying-converting-psd-images/add-level-adjustment-layer-psd/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# إضافة طبقة تعديل المستوى في PSD

## مقدمة
عندما يتعلق الأمر بتحرير الصور، فإن إدارة المستويات يمكن أن تُحدث فرقًا كبيرًا في حيوية ووضوح صورك. إحدى الأدوات المفيدة في ترسانة Photoshop هي "طبقة ضبط المستوى"، والتي تسمح لك بتعديل النطاق اللوني وتوازن الألوان لصورك. في هذا الدليل، سنرشدك إلى كيفية تنفيذ طبقة ضبط المستوى في ملف PSD باستخدام Aspose.PSD لـ Java. لذا، احصل على Java IDE الخاص بك.
## المتطلبات الأساسية
قبل أن تقفز إلى عالم تعديلات المستوى، ستحتاج إلى إعداد بعض الأشياء لضمان رحلة سلسة:
1.  Java Development Kit (JDK): تأكد من تثبيت JDK على جهازك. إذا لم يكن لديك، يمكنك الحصول عليه من[موقع أوراكل](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) أو استخدم OpenJDK.
2.  Aspose.PSD لمكتبة Java: لمعالجة ملفات PSD، ستحتاج إلى تنزيل مكتبة Aspose.PSD. يمكنك الحصول على أحدث إصدار من هذا[رابط التحميل](https://releases.aspose.com/psd/java/) وتأكد من تضمين JAR في مكتبة مشروعك.
3. المعرفة الأساسية بـ Java: سيساعدك الحصول على فهم أساسي لبرمجة Java، حيث سنتعمق في مقتطفات التعليمات البرمجية خلال هذا البرنامج التعليمي.
4. إعداد IDE: يمكنك استخدام أي Java IDE تفضله — مثل IntelliJ IDEA أو Eclipse أو NetBeans — لكتابة التعليمات البرمجية وتشغيلها. فقط تأكد من إعداد مشروع Java الخاص بك وإضافة مكتبة Aspose.PSD.

## حزم الاستيراد
قبل أن نبدأ في كتابة الكود الخاص بنا، نحتاج إلى استيراد الحزم اللازمة من مكتبة Aspose.PSD. وإليك كيف يمكنك القيام بذلك:
```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.LevelsLayer;
import com.aspose.psd.fileformats.psd.layers.layerresources.LevelChannel;
```
من خلال استيراد هذه الحزم، سيكون لدينا إمكانية الوصول إلى الفئات اللازمة لتحميل ملفات PSD الخاصة بنا وتعديلها وحفظها.

الآن، دعونا نقسم العملية إلى خطوات سهلة الهضم. تابع معنا أثناء سيرنا في تحميل ملف PSD، وضبط المستويات، ثم حفظ التغييرات. 
## الخطوة 1: إعداد مسارات الملفات الخاصة بك
الخطوة الأولى هي تحديد مكان وجود ملف PSD الخاص بنا والمكان الذي نريد حفظ المخرجات المعدلة فيه. يمكنك تخصيص مسار الدليل ليناسب احتياجاتك.
```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "LevelsAdjustmentLayer.psd";
String psdPathAfterChange = dataDir + "LevelsAdjustmentLayerChanged.psd";
```
 هنا، استبدل`"Your Document Directory"`بالمسار الفعلي على نظامك حيث يتم تخزين ملف PSD الخاص بك. وهذا يمهد الطريق لكل ما سنفعله بعد ذلك.
## الخطوة 2: قم بتحميل ملف PSD
 الآن، لنقم بتحميل ملف PSD باستخدام ملف`PsdImage` فصل. هذه الخطوة ضرورية لأنها تتيح لنا الوصول إلى الطبقات ومعالجتها.
```java
PsdImage im = (PsdImage) Image.load(sourceFileName);
```
 عندما تتصل`Image.load()` ، فسوف يقرأ ملف PSD وينشئ مثيلاً له`PsdImage` التي يمكنك العمل بها.
## الخطوة 3: التكرار عبر الطبقات
نظرًا لأننا نريد ضبط طبقة ضبط المستوى، فسنحتاج إلى التكرار خلال كل طبقة في ملف PSD الخاص بنا. يساعدنا هذا في العثور على الطبقة المحددة التي نريد تعديلها.
```java
for (int i = 0; i < im.getLayers().length; i++) {
    if (im.getLayers()[i] instanceof LevelsLayer) {
        LevelsLayer levelsLayer = (LevelsLayer) im.getLayers()[i];
        // مزيد من التلاعب سوف يذهب هنا ...
    }
}
```
 في هذه الحلقة،`instanceof LevelsLayer` يتحقق مما إذا كانت الطبقة الحالية هي طبقة ضبط المستويات. إذا كان الأمر كذلك، فيمكننا المضي قدمًا في تعديل خصائصه.
## الخطوة 4: ضبط إعدادات قناة المستوى
بمجرد تحديد الطبقة الصحيحة، يمكننا تعديل مستويات الإدخال والإخراج الخاصة بها. هذا هو المكان الذي يحدث فيه السحر! اضبط المعلمات المختلفة لترى مدى تأثيرها على الصورة.
```java
LevelChannel channel = levelsLayer.getChannel(0);
channel.setInputMidtoneLevel(2.0f);
channel.setInputShadowLevel((short) 10);
channel.setInputHighlightLevel((short) 230);
channel.setOutputShadowLevel((short) 20);
channel.setOutputHighlightLevel((short) 200);
```
إليك ما تفعله كل معلمة:
- Input Midtone Level: يضبط النغمات المتوسطة.
- مستوى ظل الإدخال: يعدل المناطق الداكنة في الصورة.
- مستوى تمييز الإدخال: يغير المناطق الساطعة في الصورة.
- مستوى الظل الناتج: يضبط كيفية ظهور الظلال الداكنة.
- مستوى تمييز الإخراج: يضبط كيفية ظهور الضوء الساطع.
لا تتردد في تجربة قيم مختلفة!
## الخطوة 5: احفظ ملف PSD المعدل
الآن بعد أن أجرينا تعديلاتنا، حان الوقت لحفظ ملف PSD المعدل. هذه الخطوة ضرورية لضمان تطبيق التغييرات وتخزينها.
```java
im.save(psdPathAfterChange);
```
 يمكنك الآن العثور على ملف PSD المعدل الخاص بك في الملف المحدد`psdPathAfterChange`. 
## خاتمة
لقد تعلمت للتو كيفية إضافة طبقة ضبط المستوى إلى ملف PSD باستخدام Aspose.PSD لـ Java! باتباع هذا الدليل، يمكنك ضبط الجودة اللونية لصورك دون عناء، مما يمهد الطريق لمخرجات أكثر حيوية وجاذبية بصريًا. تذكر أن التدريب يؤدي إلى الإتقان، لذا لا تتردد في تعديل التعديلات واستكشاف ملفات PSD المختلفة لرؤية تأثيرات تغييراتك.
## الأسئلة الشائعة
### ما هي طبقة ضبط المستوى؟
تتيح لك طبقة ضبط المستوى تصحيح النطاق اللوني في صورك، وموازنة الظلال، والدرجات اللونية النصفية، والإبرازات.
### هل يمكنني استخدام Aspose.PSD بدون شراء؟
نعم! يقدم Aspose نسخة تجريبية مجانية لاختبار المكتبة قبل الشراء.
### أين يمكنني العثور على وثائق Aspose.PSD؟
 يمكنك العثور على الوثائق[هنا](https://reference.aspose.com/psd/java/).
### هل هناك أي دعم مجتمعي لمنتجات Aspose؟
 قطعاً! يمكنك طرح الأسئلة والحصول على الدعم في[منتدى Aspose](https://forum.aspose.com/c/psd/34).
### كيف يمكنني الحصول على ترخيص مؤقت لـ Aspose.PSD؟
 يمكنك التقدم بطلب للحصول على ترخيص مؤقت[هنا](https://purchase.aspose.com/temporary-license/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
