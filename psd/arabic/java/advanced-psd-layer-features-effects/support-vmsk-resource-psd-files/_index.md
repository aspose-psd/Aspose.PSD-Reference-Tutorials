---
date: 2026-02-22
description: تعلم كيفية إنشاء قناع متجه في جافا باستخدام Aspose.PSD للغة جافا، إضافة
  قناع متجه إلى ملف PSD، ومعالجة موارد Vmsk برمجياً.
linktitle: Create Vector Mask Java – Vmsk Resource in PSD Files
second_title: Aspose.PSD Java API
title: إنشاء قناع متجه جافا – مورد Vmsk في ملفات PSD
url: /ar/java/advanced-psd-layer-features-effects/support-vmsk-resource-psd-files/
weight: 23
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# إنشاء قناع متجه Java – مورد Vmsk في ملفات PSD

## المقدمة
إذا كنت بحاجة إلى **إنشاء قناع متجه** (Vmsk) داخل ملفات Photoshop (PSD)، فإن Aspose.PSD for Java يوفّر لك طريقة برمجية نظيفة للقيام بذلك. سواءً كنت تبني أداة أتمتة تصميم أو تضيف دعم قناع مخصص إلى خط أنابيب رسومات موجود، فإن هذا الدليل يمرّ بك عبر كل خطوة—تحميل ملف PSD، قراءة مورد Vmsk، تعديل خصائصه، وحفظ النتيجة. في النهاية، ستكون مرتاحًا في التعامل مع الأقنعة المتجهة، تحويل PSD إلى PNG، وتوسيع الملف ببيانات متجهة إضافية—كل ذلك باستخدام تقنيات **create vector mask java**.

## إجابات سريعة
- **ما هو مورد Vmsk؟** هو بيانات القناع المتجه المخزّنة داخل ملف PSD، تُعرّف أشكالًا متجهة معقدة لطبقة.
- **أي مكتبة تدعم ذلك؟** Aspose.PSD for Java يوفّر وصولًا كاملاً للقراءة/الكتابة لموارد Vmsk.
- **هل أحتاج إلى ترخيص؟** يتوفر نسخة تجريبية مجانية؛ الترخيص التجاري مطلوب للاستخدام في الإنتاج.
- **هل يمكنني تحويل PSD المعدل إلى PNG؟** نعم—بعد الحفظ، يمكنك تحميل PSD وتصديره إلى PNG باستخدام نفس الـ API.
- **هل دعم Maven متاح؟** بالطبع؛ يمكن إضافة Aspose.PSD كاعتماد Maven (انظر كلمة “aspose psd maven”).

## ما هو قناع المتجه (مورد Vmsk)؟
قناع المتجه (Vmsk) هو قناع غير مبني على البكسل يستخدم منحنيات بيزيه وسجلات المسار لتحديد المناطق الشفافة والغير شفافة على طبقة. وبما أنه متجه، فإنه يتكّون من دون فقدان جودة عند التكبير—مناسب للرسومات عالية الدقة.

## لماذا إنشاء قناع متجه باستخدام Aspose.PSD؟
- **الأتمتة:** إضافة أو تعديل الأقنعة برمجيًا دون فتح Photoshop.  
- **الاتساق:** ضمان أن كل ملف PSD تُنشئه يتبع نفس قواعد القناع.  
- **متعدد الأنظمة:** يعمل على أي نظام تشغيل يدعم Java.  
- **التكامل:** دمجه مع واجهات برمجة تطبيقات Aspose الأخرى (مثل تحويل PSD → PNG) لإنشاء سير عمل كامل.  
- **القابلية للتوسع:** الأقنعة المتجهة تبقى واضحة بأي حجم، مما يجعلها مثالية للتصاميم المتجاوبة.

## لماذا هذا مهم لمطوري Java
باستخدام تقنيات **create vector mask java** يمكنك دمج منطق رسومي متقدم مباشرةً في الخدمات الخلفية، خطوط أنابيب CI، أو الأدوات المكتبية. لم تعد بحاجة إلى مصمم لإضافة الأقنعة يدويًا؛ يمكن لكودك توليدها أو تعديلها فورًا، مما يوفر الوقت ويقلل الأخطاء البشرية.

## المتطلبات المسبقة
قبل الغوص في الكود، تأكد من توفر ما يلي:

### ما تحتاجه
- Java Development Kit (JDK): تأكد من تثبيت JDK على جهازك. إذا لم يكن مثبتًا، يمكنك تنزيله من [موقع Oracle](https://www.oracle.com/java/technologies/javase-downloads.html).
- Aspose.PSD for Java Library: مكتبة قوية لإدارة ملفات PSD. يمكنك تنزيلها من [صفحة إصدارات Aspose](https://releases.aspose.com/psd/java/). لمن يرغب في التجربة قبل الشراء، يمكنك البدء بالـ [نسخة التجريبية المجانية](https://releases.aspose.com/).
- IDE: أي بيئة تطوير متكاملة للـ Java (مثل IntelliJ IDEA، Eclipse، إلخ) ستعمل مع هذا المشروع.

### إعداد مساحة العمل الخاصة بك
1. **إنشاء مشروع Java جديد** – افتح IDE المفضلة لديك وابدأ مشروعًا جديدًا.  
2. **إضافة مكتبة Aspose** – بعد تنزيل ملف JAR الخاص بـ Aspose، أضفه إلى مسار بناء المشروع حتى تتمكن من الوصول إلى جميع الفئات المتعلقة بـ PSD.

مع جاهزية البيئة، لننتقل إلى التنفيذ الفعلي.

## كيفية إنشاء قناع متجه في ملفات PSD باستخدام Java
فيما يلي دليل خطوة بخطوة. كتل الشيفرة تبقى كما هي من الدليل الأصلي؛ أضفنا نصًا توضيحيًا لجعل كل خطوة واضحة تمامًا.

### استيراد الحزم
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

الآن بعد أن أعددنا الأساس، دعنا نتبع كل عملية.

### الخطوة 1: تحميل ملف PSD الخاص بك
أول شيء تريد القيام به هو تحميل ملف PSD. هنا يبدأ كل السحر.

```java
String dataDir = "Your Document Directory"; // Update this path
String sourceFileName = dataDir + "Rectangle.psd";
PsdImage im = (PsdImage) Image.load(sourceFileName);
```

- نحدد المتغيّر `dataDir` إلى دليل ملف PSD الخاص بك.  
- ننشئ سلسلة `sourceFileName`، نجمع فيها الدليل مع اسم ملف PSD.  
- أخيرًا، نحمل ملف PSD في كائن `PsdImage` باستخدام `Image.load()`.

### الخطوة 2: استرجاع مورد Vmsk
الآن بعد أن تم تحميل صورة PSD، لنستخرج مورد Vmsk.

```java
VmskResource resource = getVmskResource(im);
```

- نستدعي الطريقة `getVmskResource()` التي تتولى البحث واسترجاع مورد Vmsk من الصورة.

### الخطوة 3: التحقق من خصائص مورد Vmsk
قبل المتابعة مع التعديلات، من الضروري التحقق من أن مورد Vmsk في الحالة المتوقعة.

```java
if (resource.isDisabled() != false ||
	resource.isInverted() != false ||
	resource.isNotLinked() != false ||
	resource.getPaths().length != 7) {
	throw new RuntimeException("VmskResource was read wrong");
}
```

- هنا نتحقق من خصائص مختلفة لمورد Vmsk. نريد التأكد من أنه ليس معطَّلًا، أو مقلوبًا، أو غير مرتبط، وأنه يحتوي على العدد الصحيح من المسارات.

### الخطوة 4: الوصول إلى كل مسار والتحقق منه
دعنا نتعمق قليلًا ونفحص المسارات داخل مورد Vmsk.

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

- نستخرج ثلاثة سجلات مسار محددة ونتحقق من أنواعها وخصائصها للتأكد من مطابقتها للمعايير المطلوبة.

### الخطوة 5: تعديل مورد Vmsk
الآن ندخل في جزء التعديل! يمكنك تعديل خصائص مورد Vmsk حسب الحاجة.

```java
resource.setDisabled(true);
resource.setInverted(true);
resource.setNotLinked(true);
```

- في هذا الجزء، نقوم بتبديل عدة خصائص لمورد Vmsk. عن طريق ضبطها على `true`، يمكننا التحكم في سلوك القناع داخل ملف PSD.

### الخطوة 6: تعديل نقاط عقد Bezier
عقد Bezier حاسمة للمسارات المتجهة. لنغيّر بعض القيم هنا.

```java
BezierKnotRecord bezierKnot = (BezierKnotRecord) resource.getPaths()[3];
bezierKnot.getPoints()[0] = new Point(0, 0);
bezierKnot = (BezierKnotRecord) resource.getPaths()[4];
bezierKnot.getPoints()[0] = new Point(8039797, 10905190);
```

- نصل إلى سجلات `BezierKnotRecord` المحددة ونغيّر نقاطها لتغيير شكل القناع المتجه ربما.

### الخطوة 7: حفظ ملف PSD المعدل
بعد إكمال جميع التعديلات، حان وقت حفظ ملف PSD المعدل.

```java
String exportPath = dataDir + "Rectangle_changed.psd";
im.save(exportPath);
```

- نحدد مسار ملف PSD المُصدَّر ثم نستدعي `im.save()` لكتابة التغييرات إلى هذا الملف الجديد.

### الخطوة 8: تنظيف الموارد
أخيرًا، نحتاج إلى التأكد من تحرير الصورة بشكل صحيح لتفادي استهلاك الموارد.

```java
im.dispose();
```

- من الممارسات الجيدة دائمًا التخلص من أي موارد بمجرد الانتهاء. هذا يساعد على تجنّب تسرب الذاكرة في تطبيقاتك.

## المشكلات الشائعة والحلول
| المشكلة | سبب حدوثها | كيفية الإصلاح |
|-------|----------------|------------|
| **`VmskResource` not found** | ملف PSD لا يحتوي على طبقة قناع متجه. | تحقق من أن ملف PSD المصدر يحتوي على قناع متجه أو أضف واحدًا يدويًا في Photoshop قبل تشغيل الكود. |
| **`ArrayIndexOutOfBoundsException` on path access** | عدد سجلات المسار المتوقعة يختلف. | افحص `resource.getPaths().length` وعدّل استخدام الفهارس وفقًا لذلك. |
| **License exception** | تشغيل بدون ترخيص Aspose.PSD صالح. | طبّق ترخيص تجريبي أو مرخص باستخدام `License license = new License(); license.setLicense("Aspose.PSD.lic");`. |
| **Memory leak** | عدم تحرير الصورة في عمليات طويلة الأمد. | دائمًا استدعِ `im.dispose()` داخل كتلة `finally` أو استخدم try‑with‑resources إذا كان مدعومًا. |

## الأسئلة المتكررة

**س: كيف يمكنني إضافة قناع متجه جديد إلى طبقة موجودة؟**  
ج: أنشئ كائن `VmskResource`، املأه بسجلات المسار المطلوبة (مثل `BezierKnotRecord`)، وأرفقه بمجموعة موارد الطبقة.

**س: هل يمكنني تحويل PSD المعدل مباشرةً إلى PNG دون فتح Photoshop؟**  
ج: نعم—بعد حفظ PSD، حمّله مرة أخرى باستخدام `Image.load()` واستدعِ `im.save("output.png")` مع تحديد صيغة PNG.

**س: هل هناك طريقة لأتمتة ذلك في خط أنابيب CI/CD؟**  
ج: بالتأكيد. بما أن العملية تعتمد على Java فقط، يمكنك دمجها في بناء Maven/Gradle، حاويات Docker، أو أي نظام CI يدعم Java.

**س: ما إصدارات Aspose.PSD المتوافقة مع Java 11+؟**  
ج: جميع الإصدارات الحديثة (2024‑2025) تدعم Java 8 وما فوق، بما فيها Java 11، 17، والإصدارات LTS الأحدث.

**س: هل أحتاج إلى ترخيص لبنات التطوير؟**  
ج: ترخيص تجريبي مجاني يكفي للتطوير والاختبار. بالنسبة للنشر في بيئات الإنتاج، يلزم ترخيص تجاري.

---

**آخر تحديث:** 2026-02-22  
**تم الاختبار مع:** Aspose.PSD 24.11 for Java  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}