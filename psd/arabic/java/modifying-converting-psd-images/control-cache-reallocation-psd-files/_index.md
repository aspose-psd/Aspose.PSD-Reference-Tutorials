---
title: التحكم في إعادة تخصيص ذاكرة التخزين المؤقت في ملفات PSD
linktitle: التحكم في إعادة تخصيص ذاكرة التخزين المؤقت في ملفات PSD
second_title: Aspose.PSD جافا API
description: إدارة إعادة تخصيص ذاكرة التخزين المؤقت في ملفات PSD باستخدام Aspose.PSD لـ Java. تعرف على كيفية تحسين الذاكرة ومعالجة الملفات بكفاءة - وهي مثالية للمطورين.
weight: 22
url: /ar/java/modifying-converting-psd-images/control-cache-reallocation-psd-files/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# التحكم في إعادة تخصيص ذاكرة التخزين المؤقت في ملفات PSD

## مقدمة
عند العمل مع الصور وملفات Photoshop برمجيًا، تعد الكفاءة عاملاً رئيسيًا. يوفر Aspose.PSD for Java ميزات قوية لإدارة ملفات PSD ومعالجتها بسلاسة. أحد الجوانب الأساسية لتحسين الأداء هو التحكم في إعادة تخصيص ذاكرة التخزين المؤقت. تساعد إدارة ذاكرة التخزين المؤقت في الحفاظ على التوازن بين استخدام الذاكرة والقرص، مما يضمن تشغيل التطبيق الخاص بك بسلاسة، دون حدوث أعطال أو تباطؤ غير متوقع. 
## المتطلبات الأساسية
قبل أن ننتقل إلى الجزء الخاص بالبرمجة، هناك بعض الأشياء التي تحتاج إلى التأكد منها حتى يسير كل شيء بسلاسة:
1. Java Development Kit (JDK): تأكد من تثبيت JDK على جهازك. يمكنك تنزيله من[موقع أوراكل](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).
2. Aspose.PSD لـ Java: أنت بحاجة إلى تنزيل مكتبة Aspose.PSD. يمكنك العثور على أحدث إصدار[هنا](https://releases.aspose.com/psd/java/).
3. إعداد IDE: ستسهل عليك بيئة التطوير المتكاملة (IDE) مثل IntelliJ IDEA أو Eclipse إدارة التعليمات البرمجية الخاصة بك.
4. الفهم الأساسي لـ Java: الإلمام ببرمجة Java سيساعدك على فهم المفاهيم ومقتطفات التعليمات البرمجية بشكل أفضل.
5.  ترخيص Aspose (اختياري): إذا كنت ترغب في إزالة العلامات المائية والحصول على الوظائف الكاملة، ففكر في شراء ترخيص[هنا](https://purchase.aspose.com/buy) أو تجربة النسخة التجريبية المجانية[هنا](https://releases.aspose.com/).
## حزم الاستيراد
قبل أن نبدأ في كتابة الكود، دعونا نتأكد من أننا قمنا باستيراد الحزم اللازمة. فيما يلي قائمة مختصرة بما يجب تضمينه في بداية ملف Java الخاص بك:
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
## الخطوة 1: إعداد دليل البيانات الخاص بك
أول الأشياء أولاً، ستحتاج إلى إعداد دليل حيث تريد تخزين ملفات ذاكرة التخزين المؤقت الخاصة بك. يعد هذا ضروريًا لإدارة ذاكرة التخزين المؤقت بشكل فعال.
```java
String dataDir = "Your Document Directory";
Cache.setCacheFolder(dataDir);
```

- String dataDir: تحديد الدليل لذاكرة التخزين المؤقت للمستندات الخاصة بك.
- Cache.setCacheFolder(dataDir): تقوم هذه الطريقة بتعيين مجلد ذاكرة التخزين المؤقت إلى الدليل المحدد. سيتم الآن تخزين أي ذاكرة تخزين مؤقت تم إنشاؤها بواسطة Aspose هنا بدلاً من الدليل المؤقت الافتراضي.
## الخطوة 2: تكوين ذاكرة التخزين المؤقت على القرص
بعد ذلك، سنحدد أننا نريد تخزين ذاكرة التخزين المؤقت الخاصة بنا على القرص فقط. يعد هذا مفيدًا بشكل خاص إذا كان تطبيقك يستخدم ملفات كبيرة وتريد التأكد من بقاء الذاكرة خالية.
```java
Cache.setCacheType(CacheType.CacheOnDiskOnly);
```

- Cache.setCacheType(CacheType.CacheOnDiskOnly): يضمن هذا الخيار عدم الاحتفاظ بذاكرة التخزين المؤقت في الذاكرة، وهو أمر مفيد للتعامل مع ملفات PSD الكبيرة دون استهلاك الكثير من ذاكرة الوصول العشوائي.
## الخطوة 3: تحديد الحد الأقصى لحجم القرص وذاكرة التخزين المؤقت
الآن، دعونا نقيد أحجام ذاكرة التخزين المؤقت لدينا. يعد هذا أمرًا بالغ الأهمية لأن ذاكرة التخزين المؤقت غير المحدودة يمكن أن تؤدي إلى مشكلات في الأداء.
```java
Cache.setMaxDiskSpaceForCache(1073741824); // 1 جيجا بايت
Cache.setMaxMemoryForCache(1073741824); // 1 جيجا بايت
```

- Cache.setMaxDiskSpaceForCache(1073741824): يؤدي هذا إلى تعيين حد 1 جيجابايت لذاكرة التخزين المؤقت على القرص. يمكنك ضبط هذا الحجم حسب احتياجاتك.
- Cache.setMaxMemoryForCache(1073741824): بالمثل، يؤدي هذا إلى تقييد ذاكرة التخزين المؤقت في الذاكرة، مما يضمن عدم استخدام التطبيق الخاص بك لذاكرة زائدة.
## الخطوة 4: إدارة استراتيجية إعادة تخصيص ذاكرة التخزين المؤقت
تعد إدارة كيفية إعادة تخصيص ذاكرة التخزين المؤقت أمرًا ضروريًا للحفاظ على الأداء. وإليك كيف يمكنك إعداده.
```java
Cache.setExactReallocateOnly(false);
```

- Cache.setExactReallocateOnly(false): عند التعيين على false، فإن هذا يسمح لـ Aspose بإدارة إعادة تخصيص ذاكرة التخزين المؤقت بشكل أكثر مرونة، مما قد يؤدي إلى أداء أفضل.
## الخطوة 5: التحقق من حجم ذاكرة التخزين المؤقت المخصصة
تتعلق هذه الخطوة بمراقبة عدد وحدات البايت المخصصة حاليًا لذاكرة التخزين المؤقت في الذاكرة أو على القرص. فلننفذ ذلك:
```java
long l1 = Cache.getAllocatedDiskBytesCount();
long l2 = Cache.getAllocatedMemoryBytesCount();
```

- long l1: يخزن عدد البايتات المخصصة على القرص.
- long l2: يخزن عدد البايتات المخصصة في الذاكرة. 
يمكنك التحقق من هذه القيم في أي وقت للتأكد من أن التطبيق الخاص بك يدير استخدام الذاكرة والقرص كما هو متوقع.
## الخطوة 6: إنشاء صورة PSD
الآن بعد أن قمنا بإعداد تكوينات ذاكرة التخزين المؤقت الخاصة بنا، فلنقم بإنشاء صورة PSD بسيطة.
```java
PsdOptions options = new PsdOptions();
Color[] color = { Color.getRed(), Color.getBlue(), Color.getBlack(), Color.getWhite() };
options.setPalette(new ColorPalette(color));
options.setSource(new StreamSource(new ByteArrayInputStream(new byte[0])));
RasterImage image = (RasterImage) Image.create(options, 100, 100);
```

- خيارات PsdOptions: يتيح لك هذا الكائن تحديد الخيارات عند إنشاء صورة Photoshop.
- لون[] اللون: مصفوفة تحتوي على الألوان التي سيتم استخدامها في لوحة الصور.
## الخطوة 7: حفظ بيانات البكسل في الصورة
الآن، دعونا نملأ صورتنا ببيانات البكسل ونحفظها.
```java
Color[] pixels = new Color[10000];
for (int i = 0; i < pixels.length; i++) {
    pixels[i] = Color.getWhite();
}
image.savePixels(image.getBounds(), pixels);
```

- لون[] البكسل: هذه مجموعة من الكائنات الملونة. نحن هنا نملأها بالبكسلات البيضاء.
- image.savePixels(image.getBounds(), Pixels): تقوم هذه الطريقة بحفظ بيانات البكسل في الصورة. يقوم بتحديث الصورة بالألوان التي حددناها.
## الخطوة 8: مراقبة ذاكرة التخزين المؤقت المخصصة بعد إنشاء الصورة
بعد إنشاء الصورة، من الممارسات الجيدة التحقق من عدد البايتات المخصصة لذاكرة التخزين المؤقت مرة أخرى.
```java
long diskBytes = Cache.getAllocatedDiskBytesCount();
long memoryBytes = Cache.getAllocatedMemoryBytesCount();
```

- وحدات بايت طويلة: تلتقط التخصيص الحالي على القرص بعد إنشاء الصورة.
- بايت الذاكرة الطويلة: يلتقط التخصيص الحالي في الذاكرة. 
ستساعدك هذه الخطوة في تحديد مقدار ذاكرة التخزين المؤقت التي يتم استهلاكها بعد عملياتك.
## الخطوة 9: التحقق من التخلص السليم
وأخيرًا، من الضروري التأكد من التخلص من كافة كائنات Aspose.PSD بشكل صحيح لتجنب تسرب الذاكرة.
```java
l1 = Cache.getAllocatedDiskBytesCount();
l2 = Cache.getAllocatedMemoryBytesCount();
```

- l1 وl2: ستساعدك هذه المتغيرات على التحقق من التخصيص النهائي. إذا لم تكن صفرًا، فهذا يشير إلى أن بعض الكائنات لم يتم التخلص منها بشكل صحيح.
## خاتمة
يمكن أن يؤدي التحكم في إعادة تخصيص ذاكرة التخزين المؤقت في Aspose.PSD لـ Java إلى إحداث فرق كبير في أداء التطبيق الخاص بك. باتباع الخطوات الموضحة أعلاه، يمكنك إدارة ذاكرة التخزين المؤقت بشكل فعال وتقليل استخدام الذاكرة وإنشاء ملفات PSD جميلة بكفاءة. احتضن هذه التقنيات، وشاهد تطبيقاتك تزدهر بأداء مثالي!
## الأسئلة الشائعة
### ما هو Aspose.PSD؟
Aspose.PSD هي مكتبة لمطوري .NET وJava لإنشاء ملفات Photoshop (PSD) ومعالجتها وتحويلها برمجيًا.
### كيف يمكنني التحقق من حجم ذاكرة التخزين المؤقت المخصصة؟
 استخدم أساليب مثل`Cache.getAllocatedDiskBytesCount()` و`Cache.getAllocatedMemoryBytesCount()` لمراقبة استخدام ذاكرة التخزين المؤقت الحالية.
### هل يمكنني تعيين دليل مخصص لذاكرة التخزين المؤقت؟
 نعم، يمكنك تحديد دليل مختلف باستخدام`Cache.setCacheFolder("Your Directory Path")`.
### هل Aspose.PSD مجاني للاستخدام؟
Aspose.PSD هي مكتبة مدفوعة الأجر، ولكن يمكنك البدء بنسخة تجريبية مجانية متاحة عليها[موقع إلكتروني](https://releases.aspose.com/).
### ماذا يحدث إذا لم أتخلص من الأشياء؟
يمكن أن يؤدي عدم التخلص من الكائنات إلى تسرب الذاكرة، مما يتسبب في استخدام التطبيق الخاص بك لموارد أكثر من اللازم.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
