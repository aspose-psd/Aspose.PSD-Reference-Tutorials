---
date: 2025-12-18
description: تعلم كيفية إنشاء قناع متجه (مورد Vmsk) في ملفات PSD باستخدام Aspose.PSD
  للغة Java. يوضح هذا الدليل خطوة بخطوة كيفية إضافة قناع متجه، وتحويل PSD إلى PNG،
  والمزيد.
linktitle: Create Vector Mask (Vmsk Resource) in PSD Files with Java
second_title: Aspose.PSD Java API
title: إنشاء قناع متجه (مورد Vmsk) في ملفات PSD باستخدام Java
url: /ar/java/advanced-psd-layer-features-effects/support-vmsk-resource-psd-files/
weight: 23
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# إنشاء قناع متجه (مورد Vmsk) في ملفات PSD باستخدام Java

## المقدمة
إذا كنت بحاجة إلى **إنشاء قناع متجه** (Vmsk) داخل ملفات Photoshop (PSD)، فإن Aspose.PSD for Java يوفّر لك طريقة برمجية نظيفة للقيام بذلك. سواءً كنت تبني أداة أتمتة تصميم أو تضيف دعم قناع مخصص إلى خط أنابيب رسومي موجود، فإن هذا الدليل يمرّ بك عبر كل خطوة—تحميل ملف PSD، قراءة مورد Vmsk، تعديل خصائصه، وحفظ النتيجة. في النهاية، ستكون مرتاحًا في التعامل مع الأقنعة المتجهة، تحويل PSD إلى PNG، وتوسيع الملف ببيانات متجهية إضافية.

## إجابات سريعة
- **ما هو مورد Vmsk؟** هو بيانات القناع المتجه المخزنة داخل ملف PSD، تُعرّف أشكالًا متجهة معقدة لطبقة ما.  
- **أي مكتبة تدعم ذلك؟** Aspose.PSD for Java يوفّر وصولًا كاملاً للقراءة والكتابة لموارد Vmsk.  
- **هل أحتاج إلى ترخيص؟** يتوفر إصدار تجريبي مجاني؛ الترخيص التجاري مطلوب للاستخدام في الإنتاج.  
- **هل يمكنني تحويل PSD المعدل إلى PNG؟** نعم—بعد الحفظ، يمكنك تحميل PSD وتصديره إلى PNG باستخدام نفس الـ API.  
- **هل الدعم متاح لـ Maven؟** بالطبع؛ يمكن إضافة Aspose.PSD كاعتماد Maven (انظر كلمة المفتاح “aspose psd maven”).

## ما هو القناع المتجه (مورد Vmsk)؟
القناع المتجه (Vmsk) هو قناع غير مبني على البكسل يستخدم منحنيات بيزييه وسجلات المسار لتحديد المناطق الشفافة والغير شفافة على طبقة. نظرًا لأنه مبني على المتجهات، فإنه يتوسع دون فقدان الجودة—مثالي للرسومات عالية الدقة.

## لماذا ننشئ قناعًا متجهًا باستخدام Aspose.PSD؟
- **الأتمتة:** إضافة أو تعديل الأقنعة برمجيًا دون فتح Photoshop.  
- **الاتساق:** ضمان أن كل ملف PSD تُنشئه يتبع نفس قواعد القناع.  
- **متعدد المنصات:** يعمل على أي نظام تشغيل يدعم Java.  
- **التكامل:** دمجه مع واجهات برمجة تطبيقات Aspose الأخرى (مثل تحويل PSD → PNG) لإنشاء سير عمل شامل من البداية إلى النهاية.

## المتطلبات المسبقة
قبل الغوص في الكود، تأكد من توفر ما يلي:

### ما تحتاجه
- **مجموعة تطوير جافا (JDK):** تأكد من تثبيت JDK على جهازك. إذا لم يكن مثبتًا، يمكنك تنزيله من [موقع Oracle](https://www.oracle.com/java/technologies/javase-downloads.html).  
- **مكتبة Aspose.PSD for Java:** مكتبة قوية لإدارة ملفات PSD. يمكنك تنزيلها من [صفحة إصدارات Aspose](https://releases.aspose.com/psd/java/). لمن يرغب في التجربة قبل الشراء، يمكنك البدء بـ [الإصدار التجريبي المجاني](https://releases.aspose.com/).  
- **بيئة تطوير متكاملة (IDE):** أي IDE لجافا (مثل IntelliJ IDEA، Eclipse، إلخ) سيعمل مع هذا المشروع.

### إعداد مساحة العمل
1. **إنشاء مشروع جافا جديد** – افتح IDE المفضلة لديك وابدأ مشروعًا جديدًا.  
2. **إضافة مكتبة Aspose** – بعد تنزيل ملف JAR الخاص بـ Aspose، أضفه إلى مسار بناء المشروع حتى تتمكن من الوصول إلى جميع الفئات المتعلقة بـ PSD.

مع إعداد البيئة جاهزًا، لننتقل إلى التنفيذ الفعلي.

## كيفية إنشاء قناع متجه في ملفات PSD باستخدام Java
فيما يلي دليل خطوة بخطوة. كتل الشيفرة تبقى كما هي من الدليل الأصلي؛ أضفنا فقط نصًا توضيحيًا لجعل كل خطوة واضحة تمامًا.

## استيراد الحزم
قبل أن نتمكن من العمل على ملفات PSD، نحتاج إلى استيراد الفئات الضرورية من مكتبة Aspose.PSD.

```java
import com.aspose.psd.Image;
import com.aspose.psd.Point;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
import com.aspose.psd.fileformats.psd.layers.LayerResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.VmskResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.BezierKnotRecord;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.InitialFillRuleRecord;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.LengthRecord;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.PathFillRuleRecord;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathType;
```

الآن بعد أن أعددنا الأساس، دعونا نستعرض كل عملية.

## الخطوة 1: تحميل ملف PSD الخاص بك
أول شيء تريد القيام به هو تحميل ملف PSD. هنا يبدأ كل السحر.

```java
String dataDir = "Your Document Directory"; // Update this path
String sourceFileName = dataDir + "Rectangle.psd";
PsdImage im = (PsdImage) Image.load(sourceFileName);
```

- نحدد `dataDir` إلى دليل ملف PSD الخاص بك.  
- ننشئ سلسلة `sourceFileName` بدمج الدليل مع اسم ملف PSD.  
- أخيرًا، نحمل ملف PSD في كائن `PsdImage` باستخدام `Image.load()`.

## الخطوة 2: استرجاع مورد Vmsk
الآن بعد أن تم تحميل صورة PSD، لنستخرج مورد Vmsk.

```java
VmskResource resource = getVmskResource(im);
```

- نستدعي طريقة `getVmsقResource()` التي تتولى البحث واسترجاع مورد Vmsk من الصورة.

## الخطوة 3: التحقق من خصائص مورد Vmsk
قبل المتابعة مع التعديلات، من الضروري التحقق من أن مورد Vmsk في الحالة المتوقعة.

```java
if (resource.isDisabled() != false ||
	resource.isInverted() != false ||
	resource.isNotLinked() != false ||
	resource.getPaths().length != 7) {
	throw new RuntimeException("VmskResource was read wrong");
}
```

- هنا نتحقق من خصائص مختلفة لمورد Vmsk. نريد التأكد من أنه ليس معطلاً، أو مقلوبًا، أو غير مرتبط، وأنه يحتوي على العدد الصحيح من المسارات.

## الخطوة 4: الوصول إلى كل مسار والتحقق منه
دعنا نتعمق أكثر ونفحص المسارات داخل مورد Vmsk.

```java
PathFillRuleRecord pathFillRule = (PathFillRuleRecord) resource.getPaths()[0];
InitialFillRuleRecord initialFillRule = (InitialFillRuleRecord) resource.getPaths()[1];
LengthRecord subpathLength = (LengthRecord) resource.getPaths()[2];
if (pathFillRule.getType() != VectorPathType.PathFillRuleRecord ||
	initialFillRule.getType() != VectorPathType.InitialFillRuleRecord ||
	initialFillRule.isFillStartsWithAllPixels() != false ||
	subpathLength.getType() != VectorPathType.ClosedSubpathLengthRecord ||
	subpathLength.isClosed() != true) {
	throw new RuntimeException("VmskResource paths were read wrong");
}
```

- نستخرج ثلاث سجلات مسار محددة ونتحقق من أنواعها وخصائصها للتأكد من مطابقتها للمعايير المطلوبة.

## الخطوة 5: تعديل مورد Vmsk
الآن ندخل في جزء التعديل! يمكنك تعديل خصائص مورد Vmsk حسب الحاجة.

```java
resource.setDisabled(true);
resource.setInverted(true);
resource.setNotLinked(true);
```

- في هذه الكتلة، نقوم بتبديل خصائص مختلفة لمورد Vmsk. بتعيينها إلى `true`، يمكننا التحكم في سلوك القناع داخل ملف PSD.

## الخطوة 6: تعديل نقاط عقد بيزييه
عقد بيزييه حاسمة للمسارات المتجهة. لنغيّر بعض القيم هنا.

```java
BezierKnotRecord bezierKnot = (BezierKnotRecord) resource.getPaths()[3];
bezierKnot.getPoints()[0] = new Point(0, 0);
bezierKnot = (BezierKnotRecord) resource.getPaths()[4];
bezierKnot.getPoints()[0] = new Point(8039797, 10905190);
```

- نصل إلى سجلات `BezierKnotRecord` محددة ونغيّر نقاطها لإعادة تشكيل القناع المتجه إذا لزم الأمر.

## الخطوة 7: حفظ ملف PSD المعدل
بعد إكمال جميع التعديلات، حان وقت حفظ ملف PSD المعدل.

```java
String exportPath = dataDir + "Rectangle_changed.psd";
im.save(exportPath);
```

- نحدد مسار ملف PSD المُصدَّر ثم نستدعي `im.save()` لكتابة التغييرات إلى هذا الملف الجديد.

## الخطوة 8: تنظيف الموارد
أخيرًا، نحتاج إلى التأكد من تحرير الصورة بشكل صحيح لتحرير الموارد.

```java
im.dispose();
```

- من الممارسات الجيدة دائمًا تحرير أي موارد بمجرد الانتهاء. هذا يساعد على تجنّب تسرب الذاكرة في تطبيقاتك.

## الخلاصة
تهانينا! لقد مررت الآن بعملية مفصلة لإنشاء **قناع متجه** (Vmsk) في ملفات PSD باستخدام Aspose.PSD for Java. من تحميل الصورة، استرجاع والتحقق من مورد Vmsk، تعديل خصائصه، إلى حفظ ملف PSD المعدل، لديك الآن أساس قوي لأتمتة سير عمل الأقنعة المتجهة. استخدم هذه التقنيات لإثراء خطوط تصميمك، دمجها مع واجهات Aspose الأخرى (مثل تحويل PSD إلى PNG)، أو بناء أدوات رسومية مخصصة.

## الأسئلة المتكررة
### ما هو مورد Vmsk؟
مورد Vmsk هو قناع متجه داخل ملف PSD يتيح إنشاء أشكال متجهة معقدة وميزات تحرير متقدمة.

### هل يمكنني استخدام Aspose.PSD في مشروع Maven؟
نعم، يمكنك تضمين Aspose.PSD كاعتماد في مشروع Maven باستخدام إحداثياته من المستودع.

### بأي صيغة يمكنني حفظ ملفات PSD المعدلة؟
يمكنك حفظها مرة أخرى كملفات PSD أو تصديرها إلى صيغ أخرى مثل PNG، JPEG، إلخ.

### هل هناك نسخة تجريبية مجانية متاحة لـ Aspose.PSD؟
نعم، يمكنك الحصول على نسخة تجريبية مجانية من Aspose.PSD لاختبار ميزاته. زر [رابط النسخة التجريبية](https://releases.aspose.com/).

### كيف يمكنني الحصول على دعم لـ Aspose.PSD؟
يمكنك الانضمام إلى [منتدى Aspose](https://forum.aspose.com/c/psd/34) للحصول على الدعم ومساعدة في حل المشكلات.

## أسئلة شائعة
**س: كيف أضيف قناعًا متجهًا جديدًا إلى طبقة موجودة؟**  
ج: أنشئ `VmskResource`، املأه بسجلات المسار المطلوبة (مثل `BezierKnotRecord`)، وأرفقه بمجموعة موارد الطبقة.

**س: هل يمكنني تحويل PSD المعدل مباشرة إلى PNG دون فتح Photoshop؟**  
ج: نعم—بعد حفظ PSD، حمّله مرة أخرى باستخدام `Image.load()` واستدعِ `im.save("output.png")` مع تحديد صيغة PNG.

**س: هل هناك طريقة لأتمتة ذلك في خط أنابيب CI/CD؟**  
ج: بالتأكيد. بما أن العملية تعتمد على Java فقط، يمكنك دمجها في بناء Maven/Gradle، حاويات Docker، أو أي نظام CI يدعم Java.

**س: ما إصدارات Aspose.PSD المتوافقة مع Java 11+؟**  
ج: جميع الإصدارات الحديثة (2024‑2025) تدعم Java 8 وما فوق، بما في ذلك Java 11، 17، والإصدارات LTS الأحدث.

**س: هل أحتاج إلى ترخيص للبناء التجريبي؟**  
ج: ترخيص تجريبي مجاني يكفي للتطوير والاختبار. بالنسبة للنشر في بيئات الإنتاج، يلزم الحصول على ترخيص تجاري.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**آخر تحديث:** 2025-12-18  
**تم الاختبار مع:** Aspose.PSD 24.11 for Java  
**المؤلف:** Aspose  

---