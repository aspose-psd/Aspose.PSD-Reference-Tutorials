---
date: 2026-03-13
description: تعلم كيفية إنشاء مشاريع جافا لمعالجة صور PSD مع إدارة إعادة تخصيص الذاكرة
  المؤقتة باستخدام Aspose.PSD للغة جافا. قم بتحسين استخدام الذاكرة والقرص بكفاءة.
linktitle: Create PSD Image Java – Control Cache Reallocation
second_title: Aspose.PSD Java API
title: إنشاء صورة PSD بجافا – التحكم في إعادة تخصيص الذاكرة المؤقتة
url: /ar/java/modifying-converting-psd-images/control-cache-reallocation-psd-files/
weight: 22
---

 keep bold markup **...** with Arabic inside.

Now craft final answer.{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# التحكم في إعادة تخصيص الذاكرة المؤقتة في ملفات PSD

## مقدمة
إذا كنت بحاجة إلى **create PSD image java** مشاريع بكفاءة، فإن التحكم في إعادة تخصيص الذاكرة المؤقتة أمر أساسي. عند العمل مع الصور وملفات Photoshop برمجيًا، تُعد الكفاءة عاملًا رئيسيًا. تقدم Aspose.PSD for Java ميزات قوية لإدارة ومعالجة ملفات PSD بسلاسة. أحد الجوانب الأساسية لتحسين الأداء هو التحكم في إعادة تخصيص الذاكرة المؤقتة. يساعد إدارة الذاكرة المؤقتة في الحفاظ على التوازن بين استخدام الذاكرة والقرص، مما يضمن تشغيل تطبيقك بسلاسة دون تعطل غير متوقع أو بطء.

## إجابات سريعة
- **ماذا تفعل إعادة تخصيص الذاكرة المؤقتة؟** إنها توازن بين استخدام الذاكرة والقرص أثناء معالجة ملفات PSD الكبيرة.  
- **ما هو نوع الذاكرة المؤقتة الأفضل للصور الكبيرة؟** `CacheOnDiskOnly` يبقي الذاكرة حرة عن طريق تخزين الذاكرة المؤقتة على القرص.  
- **كم مساحة القرص التي يمكنني تخصيصها؟** حتى 1 GB (أو أي حجم تحدده باستخدام `setMaxDiskSpaceForCache`).  
- **هل أحتاج إلى ترخيص لاستخدام هذه الميزات؟** الترخيص يزيل قيود النسخة التجريبية؛ راجع صفحة شراء Aspose.  
- **هل يمكنني مراقبة استخدام الذاكرة المؤقتة أثناء التشغيل؟** نعم، استخدم `Cache.getAllocatedDiskBytesCount()` و `Cache.getAllocatedMemoryBytesCount()`.

## لماذا التحكم في إعادة تخصيص الذاكرة المؤقتة؟
إدارة الذاكرة المؤقتة أمر حاسم عندما تقوم بـ **create PSD image java** تطبيقات تتعامل مع ملفات عالية الدقة أو متعددة الطبقات. تمنع إعدادات الذاكرة المؤقتة المناسبة أخطاء نفاد الذاكرة، وتقلل من توقفات GC، وتوفر لك أداءً متوقعًا على الخوادم أو تطبيقات سطح المكتب.

## المتطلبات المسبقة
قبل الانتقال إلى جزء الترميز، هناك بعض الأشياء التي تحتاج إلى التأكد منها لضمان سير كل شيء بسلاسة:
1. **مجموعة تطوير جافا (JDK):** تأكد من تثبيت JDK على جهازك. يمكنك تنزيله من [Oracle's website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).
2. **Aspose.PSD for Java:** تحتاج إلى تنزيل مكتبة Aspose.PSD. يمكنك العثور على أحدث إصدار [هنا](https://releases.aspose.com/psd/java/).
3. **إعداد بيئة التطوير المتكاملة (IDE):** بيئة تطوير متكاملة مثل IntelliJ IDEA أو Eclipse ستسهل عليك إدارة الكود.
4. **فهم أساسي لجافا:** الإلمام ببرمجة جافا سيساعدك على فهم المفاهيم ومقاطع الكود بشكل أفضل.
5. **ترخيص Aspose (اختياري):** إذا رغبت في إزالة العلامات المائية والحصول على الوظائف الكاملة، فكر في شراء ترخيص [هنا](https://purchase.aspose.com/buy) أو تجربة النسخة التجريبية المجانية [هنا](https://releases.aspose.com/).

## استيراد الحزم
قبل أن نبدأ بكتابة الكود، دعنا نتأكد من استيراد الحزم الضرورية. أدناه قائمة مختصرة بما يجب تضمينه في بداية ملف Java الخاص بك:
```java
import com.aspose.psd.Cache;
import com.aspose.psd.CacheType;
import com.aspose.psd.Color;
import com.aspose.psd.ColorPalette;
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;
import com.aspose.psd.imageoptions.GifOptions;
import com.aspose.psd.imageoptions.PsdOptions;
import com.aspose.psd.sources.StreamSource;
import com.aspose.psd.system.io.MemoryStream;
```

## كيفية إنشاء صورة PSD في جافا مع التحكم في الذاكرة المؤقتة
فيما يلي دليل خطوة بخطوة يربط تكوين الذاكرة المؤقتة مباشرةً بعملية إنشاء صورة PSD في جافا.

### الخطوة 1: إعداد دليل البيانات الخاص بك
أولًا، ستحتاج إلى إعداد دليل حيث تريد تخزين ملفات الذاكرة المؤقتة. هذا ضروري لإدارة الذاكرة المؤقتة بفعالية.
```java
String dataDir = "Your Document Directory";
Cache.setCacheFolder(dataDir);
```

- `String dataDir`: تعريف الدليل لذاكرة التخزين المؤقتة للمستند.  
- `Cache.setCacheFolder(dataDir)`: هذه الطريقة تحدد مجلد الذاكرة المؤقتة إلى الدليل المحدد. أي ذاكرة مؤقتة تُنشئها Aspose ستُخزن الآن هنا بدلاً من الدليل المؤقت الافتراضي.

### الخطوة 2: تكوين الذاكرة المؤقتة على القرص
بعد ذلك، سنحدد أننا نريد تخزين الذاكرة المؤقتة على القرص فقط. هذا مفيد خصوصًا إذا كان تطبيقك يستخدم ملفات كبيرة وتريد التأكد من بقاء الذاكرة حرة.
```java
Cache.setCacheType(CacheType.CacheOnDiskOnly);
```

- `Cache.setCacheType(CacheType.CacheOnDiskOnly)`: هذا الخيار يضمن عدم احتفاظ الذاكرة المؤقتة في الذاكرة، وهو مفيد لمعالجة ملفات PSD الكبيرة دون استهلاك الكثير من الذاكرة العشوائية.

### الخطوة 3: تحديد الحد الأقصى لحجم الذاكرة المؤقتة على القرص والذاكرة
الآن، لنقيد أحجام الذاكرة المؤقتة. هذا أمر حاسم لأن الذاكرة غير المحدودة قد تؤدي إلى مشاكل في الأداء.
```java
Cache.setMaxDiskSpaceForCache(1073741824); // 1 gigabyte
Cache.setMaxMemoryForCache(1073741824); // 1 gigabyte
```

- `Cache.setMaxDiskSpaceForCache(1073741824)`: يحدد حدًا قدره 1 GB للذاكرة المؤقتة على القرص. يمكنك تعديل هذا الحجم حسب احتياجاتك.  
- `Cache.setMaxMemoryForCache(1073741824)`: بالمثل، يحد هذا من الذاكرة المؤقتة في الذاكرة، مما يضمن عدم استخدام تطبيقك للذاكرة بشكل مفرط.

### الخطوة 4: إدارة استراتيجية إعادة تخصيص الذاكرة المؤقتة
إدارة كيفية إعادة تخصيص الذاكرة المؤقتة أمر أساسي للحفاظ على الأداء. إليك كيفية إعداد ذلك.
```java
Cache.setExactReallocateOnly(false);
```

- `Cache.setExactReallocateOnly(false)`: عندما تُضبط على `false`، يسمح ذلك لـ Aspose بإدارة إعادة تخصيص الذاكرة المؤقتة بمرونة أكبر، مما قد يؤدي إلى أداء أفضل.

### الخطوة 5: التحقق من حجم الذاكرة المؤقتة المخصصة
هذه الخطوة تتعلق بمراقبة عدد البايتات المخصصة حاليًا للذاكرة المؤقتة في الذاكرة أو على القرص. لنقم بتنفيذ ذلك:
```java
long l1 = Cache.getAllocatedDiskBytesCount();
long l2 = Cache.getAllocatedMemoryBytesCount();
```

- `long l1`: يخزن عدد البايتات المخصصة على القرص.  
- `long l2`: يخزن عدد البايتات المخصصة في الذاكرة.  
يمكنك التحقق من هذه القيم في أي وقت لضمان أن تطبيقك يدير استخدام الذاكرة والقرص كما هو متوقع.

### الخطوة 6: إنشاء صورة PSD
الآن بعد أن أعددنا تكوينات الذاكرة المؤقتة، لننشئ صورة PSD بسيطة.
```java
PsdOptions options = new PsdOptions();
Color[] color = { Color.getRed(), Color.getBlue(), Color.getBlack(), Color.getWhite() };
options.setPalette(new ColorPalette(color));
options.setSource(new StreamSource(new ByteArrayInputStream(new byte[0])));
RasterImage image = (RasterImage) Image.create(options, 100, 100);
```

- `PsdOptions options`: هذا الكائن يتيح لك تحديد الخيارات عند إنشاء صورة Photoshop.  
- `Color[] color`: مصفوفة تحتوي على الألوان التي ستُستخدم في لوحة ألوان الصورة.

### الخطوة 7: حفظ بيانات البكسل إلى الصورة
الآن، لنملأ صورتنا ببيانات البكسل ونحفظها.
```java
Color[] pixels = new Color[10000];
for (int i = 0; i < pixels.length; i++) {
    pixels[i] = Color.getWhite();
}
image.savePixels(image.getBounds(), pixels);
```

- `Color[] pixels`: هذه مصفوفة من كائنات اللون. هنا، نقوم بملئها ببيكسلات بيضاء.  
- `image.savePixels(image.getBounds(), pixels)`: هذه الطريقة تحفظ بيانات البكسل إلى الصورة. إنها تُحدّث الصورة بالألوان التي حددناها.

### الخطوة 8: مراقبة الذاكرة المؤقتة المخصصة بعد إنشاء الصورة
بعد إنشاء الصورة، من الممارسات الجيدة التحقق مرة أخرى من عدد البايتات المخصصة للذاكرة المؤقتة.
```java
long diskBytes = Cache.getAllocatedDiskBytesCount();
long memoryBytes = Cache.getAllocatedMemoryBytesCount();
```

- `long diskBytes`: يلتقط التخصيص الحالي على القرص بعد إنشاء الصورة.  
- `long memoryBytes`: يلتقط التخصيص الحالي في الذاكرة.  
هذه الخطوة ستساعدك على تحديد مقدار الذاكرة المؤقتة المستهلكة بعد عملياتك.

### الخطوة 9: التحقق من التخلص السليم
أخيرًا، من الضروري التأكد من أن جميع كائنات Aspose.PSD تم التخلص منها بشكل صحيح لتجنب تسرب الذاكرة.
```java
l1 = Cache.getAllocatedDiskBytesCount();
l2 = Cache.getAllocatedMemoryBytesCount();
```

- `l1` و `l2`: هذه المتغيرات ستساعدك على التحقق من التخصيص النهائي. إذا لم تكن صفرًا، فهذا يدل على أن بعض الكائنات لم يتم التخلص منها بشكل صحيح.

## المشكلات الشائعة والحلول
- **مجلد الذاكرة المؤقتة لم يُنشأ** – تحقق من أن التطبيق لديه أذونات كتابة للمسار الذي مررته إلى `Cache.setCacheFolder`.  
- **أخطاء نفاد الذاكرة** – تأكد مرة أخرى من تطبيق `Cache.setCacheType(CacheType.CacheOnDiskOnly)` قبل تحميل ملفات PSD الكبيرة.  
- **حجم الذاكرة المؤقتة غير المتوقع** – استخدم طرق `Cache.getAllocated*BytesCount()` بعد كل عملية رئيسية لتتبع النمو.

## الأسئلة المتكررة

**س: ما هو Aspose.PSD؟**  
ج: Aspose.PSD هي مكتبة لمطوري .NET و Java لإنشاء ومعالجة وتحويل ملفات Photoshop (PSD) برمجيًا.

**س: كيف يمكنني التحقق من حجم الذاكرة المؤقتة المخصصة؟**  
ج: استخدم طرق مثل `Cache.getAllocatedDiskBytesCount()` و `Cache.getAllocatedMemoryBytesCount()` لمراقبة الاستخدام الحالي للذاكرة المؤقتة.

**س: هل يمكنني تعيين دليل مخصص للذاكرة المؤقتة؟**  
ج: نعم، يمكنك تحديد دليل مختلف باستخدام `Cache.setCacheFolder("Your Directory Path")`.

**س: هل Aspose.PSD مجاني للاستخدام؟**  
ج: Aspose.PSD مكتبة مدفوعة، لكن يمكنك البدء بنسخة تجريبية مجانية متوفرة على [website](https://releases.aspose.com/).

**س: ماذا يحدث إذا لم أقم بالتخلص من الكائنات؟**  
ج: عدم التخلص من الكائنات قد يؤدي إلى تسرب الذاكرة، مما يجعل تطبيقك يستخدم موارد أكثر من اللازم.

## الخلاصة
التحكم في إعادة تخصيص الذاكرة المؤقتة أثناء قيامك بـ **create PSD image java** تطبيقات يمكن أن يحدث فرقًا كبيرًا في الأداء. باتباع الخطوات أعلاه، ستدير الذاكرة المؤقتة بفعالية، وتقلل استهلاك الذاكرة، وتولد ملفات PSD عالية الجودة باستخدام Aspose.PSD for Java. طبّق هذه التقنيات، وستعمل مشاريعك بسلاسة أكبر وتتحمل التوسع بشكل أفضل.

---

**آخر تحديث:** 2026-03-13  
**تم الاختبار مع:** Aspose.PSD for Java (latest release)  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}