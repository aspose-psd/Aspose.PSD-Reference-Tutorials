---
date: 2026-06-03
description: تعلم كيفية تحويل PSD إلى PNG وإنشاء Vector Mask Java باستخدام Aspose.PSD
  for Java، إضافة Vector Mask إلى PSD، ومعالجة موارد Vmsk برمجيًا.
keywords:
- convert psd to png
- add vector mask psd
- psd vector mask tutorial
- aspose psd maven
linktitle: تحويل PSD إلى PNG وإنشاء Vector Mask Java – Vmsk Resource في ملفات PSD
schemas:
- author: Aspose
  dateModified: '2026-06-03'
  description: Learn how to convert PSD to PNG and create vector mask Java using Aspose.PSD
    for Java, add vector mask PSD, and manipulate Vmsk resources programmatically.
  headline: Convert PSD to PNG and Create Vector Mask Java – Vmsk Resource in PSD
    Files
  type: TechArticle
- questions:
  - answer: Create a `VmskResource`, populate it with the required path records (e.g.,
      `BezierKnotRecord`), and attach it to the layer’s resources collection.
    question: How do I add a new vector mask to an existing layer?
  - answer: Yes—after saving the PSD, load it again with `Image.load()` and call `im.save("output.png")`
      specifying the PNG format.
    question: Can I convert the edited PSD directly to PNG without opening Photoshop?
  - answer: Absolutely. Since the process is pure Java, you can embed it in Maven/Gradle
      builds, Docker containers, or any CI system that supports Java.
    question: Is there a way to automate this in a CI/CD pipeline?
  - answer: All recent releases (2024‑2025) support Java 8 and above, including Java
      11, 17, and newer LTS versions.
    question: What versions of Aspose.PSD are compatible with Java 11+?
  - answer: A free evaluation license works for development and testing. For production
      deployments, a commercial license is required.
    question: Do I need a license for development builds?
  type: FAQPage
second_title: Aspose.PSD Java API
title: تحويل PSD إلى PNG وإنشاء Vector Mask Java – Vmsk Resource في ملفات PSD
url: /ar/java/advanced-psd-layer-features-effects/support-vmsk-resource-psd-files/
weight: 23
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# تحويل PSD إلى PNG وإنشاء قناع متجه Java – مورد Vmsk في ملفات PSD

## المقدمة
إذا كنت بحاجة إلى **convert PSD to PNG** مع أيضًا **create vector mask** (Vmsk) داخل ملفات Photoshop، فإن Aspose.PSD for Java يوفّر لك طريقة برمجية نظيفة للقيام بالأمرين. سواءً كنت تبني أداة أتمتة تصميم، أو خط أنابيب CI يتحقق من الأصول، أو توسّع سير عمل الرسومات بأقنعة مخصصة، فإن هذا الدليل يمرّ بك عبر كل خطوة — تحميل ملف PSD، قراءة مورد Vmsk، تعديل خصائصه، تصدير النتيجة إلى PNG، وحفظ الملف المعدل. في النهاية، ستكون مرتاحًا في التعامل مع الأقنعة المتجهة، تحويل PSD → PNG، وتوسيع الملف ببيانات متجهة إضافية — جميعها باستخدام تقنيات **convert PSD to PNG**.

## إجابات سريعة
- **ما هو مورد Vmsk؟** هو بيانات القناع المتجه المخزنة داخل ملف PSD، تُعرّف أشكالًا متجهة معقدة للطبقة.  
- **أي مكتبة تدعم ذلك؟** Aspose.PSD for Java توفر وصولًا كاملاً للقراءة/الكتابة إلى موارد Vmsk.  
- **هل أحتاج إلى ترخيص؟** يتوفر إصدار تجريبي مجاني؛ الترخيص التجاري مطلوب للاستخدام في الإنتاج.  
- **هل يمكنني تحويل PSD المعدل إلى PNG؟** نعم—بعد الحفظ، يمكنك تحميل PSD وتصديره إلى PNG باستخدام نفس الـ API.  
- **هل دعم Maven متاح؟** بالطبع؛ يمكن إضافة Aspose.PSD كاعتماد Maven (انظر كلمة المفتاح “aspose psd maven”).

## ما هو القناع المتجه (مورد Vmsk)؟
القناع المتجه (Vmsk) هو قناع غير مبني على البكسل يستخدم منحنيات بيزيه وسجلات المسار لتحديد المناطق الشفافة والغير شفافة على طبقة. نظرًا لأنه مبني على المتجهات، فإنه يتوسع دون فقدان الجودة—مثالي للرسومات عالية الدقة. يمكن أن يحتوي على مسارات متعددة، كل منها مكوّن من عقد بيزيه، ويدعم سمات القناع مثل الشفافية، التعبئة، وربط القناع بأقنعة الطبقة.

## لماذا إنشاء قناع متجه باستخدام Aspose.PSD؟
إنشاء أقنعة متجهة برمجيًا يلغي الحاجة إلى تحرير يدوي في Photoshop، يضمن التناسق عبر دفعات كبيرة من الملفات، ويمكّن التكامل في خطوط البناء أو النشر الآلية. باستخدام Aspose.PSD يمكنك توليد هندسة قناع دقيقة، تطبيقها على أي طبقة، والاحتفاظ بإمكانية التحرير الكاملة، وهو أمر أساسي لتوليد رسومات ديناميكية وسير عمل تصميم استجابي.

- **الأتمتة:** إضافة أو تعديل الأقنعة برمجيًا دون فتح Photoshop.  
- **التناسق:** ضمان أن كل PSD تُنشئه يتبع نفس قواعد القناع.  
- **عبر‑المنصات:** يعمل على أي نظام تشغيل يدعم Java.  
- **التكامل:** الجمع مع واجهات برمجة تطبيقات Aspose الأخرى (مثل convert PSD → PNG) لسير عمل من البداية إلى النهاية.  
- **القابلية للتوسع:** الأقنعة المتجهة تبقى حادة بأي حجم، مما يجعلها مثالية للتصاميم الاستجابية.

## لماذا هذا مهم لمطوري Java
باستخدام تقنيات **create vector mask java** يمكنك دمج منطق رسومي متقدم مباشرةً في الخدمات الخلفية، خطوط CI، أو أدوات سطح المكتب. لم تعد بحاجة إلى مصمم لإضافة الأقنعة يدويًا؛ يمكن لكودك توليدها أو تعديلها في الوقت الفعلي، مما يوفر الوقت ويقلل الأخطاء البشرية.

## المتطلبات المسبقة
قبل أن نغوص في الكود، تأكد من أن لديك ما يلي:

### ما تحتاجه
- **Java Development Kit (JDK):** ثبّت JDK 8 أو أحدث. يمكنك تنزيله من [Oracle website](https://www.oracle.com/java/technologies/javase-downloads.html).  
- **Aspose.PSD for Java Library:** هذه المكتبة القوية تدير ملفات PSD. حمّلها من [Aspose release page](https://releases.aspose.com/psd/java/). للبدء السريع، احصل على النسخة التجريبية المجانية من نفس الصفحة أو من [free trial](https://releases.aspose.com/).  
- **An IDE:** أي بيئة تطوير Java (IntelliJ IDEA، Eclipse، NetBeans) ستعمل.

### إعداد مساحة العمل الخاصة بك
1. **Create a New Java Project** – افتح بيئتك المفضلة وابدأ مشروعًا جديدًا.  
2. **Add the Aspose Library** – بعد تنزيل ملف JAR الخاص بـ Aspose، أضفه إلى مسار بناء المشروع حتى تتمكن من الوصول إلى جميع الفئات المتعلقة بـ PSD.

مع إعداد البيئة جاهز، دعنا نستعرض التنفيذ الفعلي.

## كيفية تحويل PSD إلى PNG باستخدام Aspose.PSD for Java؟
حمّل ملف PSD المصدر باستخدام `PsdImage.load()`، عدّل قناع المتجه إذا لزم الأمر، ثم استدعِ `save()` مع تحديد `ExportFormat.Png`. Aspose.PSD يتعامل تلقائيًا مع جميع ملفات التعريف اللونية، الطبقات، وبيانات القناع، منتجًا PNG مثاليًا يطابق المظهر البصري الأصلي. هذا التدفق ذو الخطوتين يعمل مع أي PSD، بغض النظر عن حجمه، ويعمل على أي منصة تدعم Java.

## استيراد الحزم
حزمة `com.aspose.psd` توفر الفئات الأساسية للتعامل مع ملفات PSD، بما في ذلك تحميل الصور، معالجة الموارد، وإمكانيات التصدير.

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

الآن بعد أن أعددنا الأساس، دعنا نستعرض كل عملية.

## الخطوة 1: تحميل ملف PSD الخاص بك
تحميل الملف يمنحك كائن `PsdImage` يمثل المستند بالكامل في الذاكرة.

```java
String dataDir = "Your Document Directory"; // Update this path
String sourceFileName = dataDir + "Rectangle.psd";
PsdImage im = (PsdImage) Image.load(sourceFileName);
```

- قمنا بتعيين `dataDir` إلى دليل ملف PSD الخاص بك.  
- أنشأنا سلسلة لـ `sourceFileName`، نجمع فيها الدليل مع اسم ملف PSD.  
- أخيرًا، حمّلنا ملف PSD إلى كائن `PsdImage` باستخدام `Image.load()`.

## الخطوة 2: استرجاع مورد Vmsk
فئة `VmskResource` تغلف بيانات القناع المتجه المخزنة داخل طبقة PSD. استرجاعها يتيح لك فحص أو تعديل مسارات القناع.

```java
VmskResource resource = getVmskResource(im);
```

- نستدعي طريقة `getVmskResource()` التي تتعامل مع البحث واسترجاع مورد Vmsk من الصورة.

## الخطوة 3: التحقق من خصائص مورد Vmsk
قبل إجراء أي تغييرات، تحقق من أن القناع مفعل، موجه بشكل صحيح، ويحتوي على العدد المتوقع من المسارات.

```java
if (resource.isDisabled() != false ||
	resource.isInverted() != false ||
	resource.isNotLinked() != false ||
	resource.getPaths().length != 7) {
	throw new RuntimeException("VmskResource was read wrong");
}
```

- هنا نتحقق من خصائص مختلفة لمورد Vmsk. نريد التأكد من أنه ليس معطلاً، غير مقلوب، أو غير مرتبط، وأنه يحتوي على العدد الصحيح من المسارات.

## الخطوة 4: الوصول إلى كل مسار والتحقق
كل سجل مسار يصف جزءًا من الشكل المتجه. فحصها يضمن أنك تعمل على الهندسة الصحيحة.

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

- نستخرج ثلاثة سجلات مسار محددة ونحقق من أنواعها وخصائصها لضمان توافقها مع معاييرنا.

## الخطوة 5: تعديل مورد Vmsk
الآن ندخل في جزء التعديل! يمكنك تبديل علامات سلوك القناع لتناسب سير عملك.

```java
resource.setDisabled(true);
resource.setInverted(true);
resource.setNotLinked(true);
```

- في هذا الجزء، نقوم بتبديل خصائص مختلفة لمورد Vmsk. بتعيينها إلى `true`، يمكننا التحكم في سلوك القناع داخل ملف PSD.

## الخطوة 6: تعديل نقاط عقد Bezier
عقد Bezier تحدد انحناء كل مقطع متجه. تعديلها يعيد تشكيل القناع دون تحويله إلى بكسل.

```java
BezierKnotRecord bezierKnot = (BezierKnotRecord) resource.getPaths()[3];
bezierKnot.getPoints()[0] = new Point(0, 0);
bezierKnot = (BezierKnotRecord) resource.getPaths()[4];
bezierKnot.getPoints()[0] = new Point(8039797, 10905190);
```

- نصل إلى مسارات `BezierKnotRecord` محددة ونغيّر نقاطها لإعادة تشكيل القناع المتجه محتملًا.

## الخطوة 7: حفظ ملف PSD المعدل
بعد إكمال جميع التعديلات، احفظ التغييرات إلى ملف PSD جديد.

```java
String exportPath = dataDir + "Rectangle_changed.psd";
im.save(exportPath);
```

- نحدد المسار لملف PSD المُصدّر ثم نستدعي `im.save()` لكتابة التغييرات إلى هذا الملف الجديد.

## الخطوة 8: تصدير PSD كـ PNG
الآن بعد أن يحتوي PSD على القناع المحدث، صدّره مباشرةً إلى PNG. تُظهر هذه الخطوة سير عمل **convert PSD to PNG**.

```java
im.dispose();
```

- استخدم `im.save("output.png", ExportFormat.Png)` لإنشاء PNG عالي الجودة يعكس القناع المتجه المعدل.

## تنظيف الموارد
أخيرًا، نحتاج إلى التأكد من أننا نتخلص من الصورة بشكل صحيح لتحرير الموارد.

CODE_BLOCK_PLACEHOLDER_9_END

- من الأفضل دائمًا التخلص من أي موارد بمجرد الانتهاء. هذا يساعد على تجنّب تسرب الذاكرة في تطبيقاتك.

## المشكلات الشائعة والحلول
| المشكلة | سبب حدوثها | كيفية الإصلاح |
|---------|------------|----------------|
| **`VmskResource` not found** | لا يحتوي PSD على طبقة قناع متجه. | تحقق من أن PSD المصدر يحتوي على قناع متجه أو أضف واحدًا يدويًا في Photoshop قبل تشغيل الكود. |
| **`ArrayIndexOutOfBoundsException` on path access** | عدد سجلات المسار المتوقعة يختلف. | افحص `resource.getPaths().length` وعدّل استخدام الفهارس وفقًا لذلك. |
| **License exception** | تشغيل بدون ترخيص Aspose.PSD صالح. | طبّق ترخيصًا تجريبيًا أو مُشتَرًى باستخدام `License license = new License(); license.setLicense("Aspose.PSD.lic");`. |
| **Memory leak** | عدم التخلص من الصورة في عمليات طويلة الأمد. | دائمًا استدعِ `im.dispose()` داخل كتلة `finally` أو استخدم try‑with‑resources إذا كان مدعومًا. |

## الأسئلة المتكررة

**س: كيف يمكنني إضافة قناع متجه جديد إلى طبقة موجودة؟**  
ج: أنشئ `VmskResource`، املأه بسجلات المسار المطلوبة (مثل `BezierKnotRecord`)، وأرفقه بمجموعة موارد الطبقة.

**س: هل يمكنني تحويل PSD المعدل مباشرةً إلى PNG دون فتح Photoshop؟**  
ج: نعم—بعد حفظ PSD، حمّله مرة أخرى باستخدام `Image.load()` واستدعِ `im.save("output.png")` مع تحديد صيغة PNG.

**س: هل هناك طريقة لأتمتة ذلك في خط أنابيب CI/CD؟**  
ج: بالتأكيد. بما أن العملية تعتمد على Java فقط، يمكنك دمجها في بناءات Maven/Gradle، حاويات Docker، أو أي نظام CI يدعم Java.

**س: ما إصدارات Aspose.PSD المتوافقة مع Java 11+؟**  
ج: جميع الإصدارات الحديثة (2024‑2025) تدعم Java 8 وما فوق، بما في ذلك Java 11، 17، والإصدارات LTS الأحدث.

**س: هل أحتاج إلى ترخيص لبناءات التطوير؟**  
ج: ترخيص تجريبي مجاني يكفي للتطوير والاختبار. للنشر في بيئات الإنتاج، يلزم ترخيص تجاري.

**آخر تحديث:** 2026-06-03  
**تم الاختبار مع:** Aspose.PSD 24.11 for Java  
**المؤلف:** Aspose

## دروس ذات صلة

- [تصدير PSD إلى PNG مع دعم قناع الطبقة في Java](/psd/java/advanced-psd-layer-features-effects/support-layer-mask-psd-files/)
- [كيفية تحويل PSD إلى PNG وإعادة التحجيم بشكل متناسب باستخدام Aspose.PSD for Java](/psd/java/advanced-image-manipulation/resize-image-proportionally/)
- [تحويل PSD إلى PNG مع تراكب اللون – Aspose.PSD for Java](/psd/java/advanced-image-manipulation/rendering-color-effect/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}