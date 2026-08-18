---
date: 2026-03-18
description: تعلم كيفية تحويل ملفات PSD إلى PNG مع تغيير عمق اللون للـ PNG باستخدام
  Aspose.PSD للغة Java – دليل خطوة بخطوة مع أمثلة شفرة.
linktitle: Specify PNG Bit Depth in Aspose.PSD for Java
second_title: Aspose.PSD Java API
title: كيفية تحويل PSD إلى PNG بعمق بت محدد باستخدام Aspose.PSD للـ Java
url: /ar/java/optimizing-png-files/specify-png-bit-depth/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# تحويل PSD إلى PNG بعمق بت محدد باستخدام Aspose.PSD للـ Java

## المقدمة
إذا كنت بحاجة إلى **convert psd to png** والتحكم في عمق البت الدقيق للـ PNG، فأنت في المكان المناسب. في هذا الدرس سنستعرض كيفية تغيير عمق البت للـ PNG أثناء حفظ ملف PSD كصورة PNG باستخدام Aspose.PSD للـ Java. سواءً كنت تبني أداة معالجة دفعات، أو خدمة ويب، أو أداة سطح مكتب، فإن القدرة على **save png with options** مثل نوع اللون الرمادي وعمق البت المخصص تمنحك تحكمًا دقيقًا في جودة الصورة وحجم الملف.

## إجابات سريعة
- **Can I change the PNG bit depth?** نعم – استخدم `PngOptions.setBitDepth()` لتحديد 1 أو 2 أو 4 أو 8 أو 16 بت.  
- **Which color types are supported?** Grayscale، TrueColor، Indexed، وغيرها عبر `PngColorType`.  
- **Do I need a license for Aspose.PSD?** النسخة التجريبية المجانية تكفي للتطوير؛ تحتاج إلى ترخيص تجاري للإنتاج.  
- **What Java version is required?** Java 8+ (المكتبة متوافقة مع إصدارات JDK الأحدث).  
- **Is the code runnable as‑is?** نعم – فقط استبدل مسار العنصر النائب بمجلدك الخاص.

## ما هو “convert psd to png” بعمق بت مخصص؟
تحويل ملف Photoshop PSD إلى صورة PNG هو مهمة شائعة عندما تحتاج إلى تنسيق صديق للويب. إضافة القدرة على **adjust png quality** عن طريق ضبط عمق البت يتيح لك موازنة الدقة البصرية مع حجم الملف، وهو مفيد بشكل خاص للصور المصغرة، الأيقونات، أو عندما تكون سعة النطاق محدودة.

## لماذا نستخدم Aspose.PSD للـ Java؟
توفر Aspose.PSD للـ Java واجهة برمجة تطبيقات عالية المستوى تُبسط تعقيد تنسيق PSD. تتيح لك **create grayscale png**، **save png with options**، والتعامل مع ملفات تعريف الألوان دون الحاجة إلى معالجة البايتات منخفضة المستوى. المكتبة مُدارة بالكامل، متعددة المنصات، وتُحدَّث بانتظام.

## المتطلبات المسبقة
قبل أن نغوص في الكود، تأكد من وجود ما يلي:

1. **Java Development Kit (JDK)** – حمّله من [Oracle’s website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).  
2. **Aspose.PSD for Java** – احصل على أحدث ملف JAR من [this link](https://releases.aspose.com/psd/java/).  
3. **Basic Java knowledge** – يجب أن تكون مرتاحًا مع الفئات، الطرق، ومعالجة الاستثناءات.  
4. **An IDE** مثل IntelliJ IDEA أو Eclipse (اختياري لكن يُنصح به).  
5. **A sample PSD file** – ضعها في مجلد ستشير إليه في الكود.

هل لديك كل شيء؟ رائع – لنستورد الحزم الضرورية.

## استيراد الحزم
الآن بعد أن غطينا المتطلبات المسبقة، حان الوقت لإعداد بيئتنا عن طريق استيراد الحزم ذات الصلة في تطبيق Java الخاص بنا. افتح بيئة التطوير وأضف عبارات الاستيراد التالية في أعلى ملف Java الخاص بك:

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PngOptions;
```

تستورد هذه العبارات الفئات التي سنستخدمها طوال الدرس، مما يتيح لنا تحميل ملفات PSD وحفظها كصور PNG بعمق البت المحدد.

## الخطوة 1: إعداد دليل المستندات الخاص بك
قبل الخوض في معالجة الصور، لنحدد دليلًا حيث سيتم تخزين صورنا. هذا يشبه إنشاء مجلد لأدواتك الفنية قبل بدء مشروع حرفي.

```java
String dataDir = "Your Document Directory";
```

## الخطوة 2: تحميل صورة PSD
الخطوة التالية هي تحميل ملف صورة PSD الذي تريد تحويله. فكر في ذلك كفتح لوحة رسم ستقوم بأداء جميع أعمالك عليها.

```java
PsdImage psdImage = (PsdImage)Image.load(dataDir + "sample.psd");
```

هنا نستخدم طريقة `Image.load()` لقراءة ملف PSD التجريبي وتحويله إلى `PsdImage` للوصول إلى الخصائص الخاصة بـ PSD.

## الخطوة 3: إنشاء خيارات PNG
بعد أن فتحنا اللوحة، نحتاج إلى مجموعة من الخيارات لكيفية حفظ الصورة. هذا يشبه اختيار ألوانك وأنماط الفرشاة قبل البدء في الرسم.

```java
PngOptions options = new PngOptions();
```

في هذه الخطوة، نقوم بتهيئة كائن من `PngOptions`، والذي يسمح لنا بتحديد المعلمات لإخراج PNG.

## الخطوة 4: تحديد نوع اللون المطلوب
الآن نقرر أي نوع من الألوان نريد في صورة PNG النهائية. هل تريد لوحة ألوان زاهية أم نمطًا أحادي اللون؟ دعنا نتخذ هذا القرار!

```java
options.setColorType(PngColorType.Grayscale);
```

في هذا المثال، نحدد نوع اللون إلى grayscale. يمكنك أيضًا اختيار `PngColorType.TrueColor` إذا أردت صورة ملونة بالكامل. هذه هي الخطوة التي **create grayscale png** فيها.

## الخطوة 5: تحديد عمق البت
الآن لنحدد عمق البت. هذا يشبه إخبار الطابعة بمدى دقة طباعة الصورة – كلما زاد عدد البتات، زادت التفاصيل!

```java
options.setBitDepth((byte)1);
```

هنا نضبط عمق البت إلى **1 bit**، وهو مناسب للصور الرمادية البسيطة. يمكنك تغيير القيمة إلى 2 أو 4 أو 8 أو 16 حسب متطلبات الجودة الخاصة بك – مثال كلاسيكي على كيفية **change png bit depth**.

## الخطوة 6: حفظ صورة PNG
أخيرًا، حان وقت حفظ تحفتك! هذه الخطوة تُنهي مشروعنا حيث ننقل عملنا من لوحة التحرير إلى جدار المعرض.

```java
psdImage.save(dataDir + "SpecifyBitDepth_out.png", options);
```

باستخدام طريقة `save()` الخاصة بـ `PsdImage`، نحفظ الملف المحول مع تطبيق الخيارات التي حددناها. Voilà! تم حفظ صورتنا الآن بعمق البت المخصص.

## المشكلات الشائعة والحلول
- **`NullPointerException` عند تحميل الـ PSD** – تحقق مرة أخرى من أن `dataDir` يشير إلى المجلد الصحيح وأن `sample.psd` موجود.  
- **عمق بت غير مدعوم** – تدعم Aspose.PSD القيم 1، 2، 4، 8، و16 بت للـ PNG. استخدام أي قيمة أخرى سيسبب استثناء `IllegalArgumentException`.  
- **عدم توافق نوع اللون** – إذا حددت عمق بت غير متوافق مع `PngColorType` المختار، ستقوم المكتبة تلقائيًا بضبط الإعداد إلى أقرب قيمة مدعومة.

## الأسئلة المتكررة

**س: ما هو Aspose.PSD للـ Java؟**  
ج: Aspose.PSD للـ Java هي مكتبة للعمل مع ملفات PSD في تطبيقات Java، تتيح لك تعديل الصور وتحويلها.

**س: كيف يمكنني تحديد أعماق بت مختلفة؟**  
ج: يمكنك ضبط عمق البت باستخدام الطريقة `options.setBitDepth((byte)n)`، مع استبدال `n` بالعمق المطلوب.

**س: هل يمكنني استخدام Aspose.PSD مجانًا؟**  
ج: نعم، يمكنك تجربة المكتبة بنسخة تجريبية مجانية يمكنك العثور عليها [here](https://releases.aspose.com/).

**س: من أين يمكنني الحصول على ترخيص دعم لـ Aspose؟**  
ج: للحصول على ترخيص مؤقت، يمكنك التقديم [here](https://purchase.aspose.com/temporary-license/).

**س: ما نوع الصور التي يمكنني تحويلها؟**  
ج: تتعامل Aspose.PSD أساسًا مع ملفات PSD، لكنها تدعم التحويل إلى صيغ متعددة مثل PNG، JPEG، وTIFF.

## الخاتمة
لقد تعلمت الآن كيفية **convert psd to png** مع التحكم في عمق البت للـ PNG باستخدام Aspose.PSD للـ Java. من خلال تعديل `PngOptions`، يمكنك **adjust png quality**، إنشاء **grayscale png**، وضبط حجم الملف لأي سيناريو. جرّب أنواع ألوان وعمق بت مختلفة لتجد التوازن المثالي لتطبيقك.

---

**Last Updated:** 2026-03-18  
**Tested With:** Aspose.PSD for Java 24.11 (latest at time of writing)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}