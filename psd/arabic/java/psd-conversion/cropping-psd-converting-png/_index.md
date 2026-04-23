---
date: 2026-03-21
description: تعلم كيفية تحويل ملفات PSD إلى PNG وقص ملفات PSD باستخدام Aspose.PSD
  للغة Java. يوضح هذا الدليل معالجة الصور خطوة بخطوة في تطبيقات Java.
linktitle: Cropping PSD when Converting to PNG
second_title: Aspose.PSD Java API
title: كيفية تحويل PSD إلى PNG مع القص باستخدام Aspose.PSD للـ Java
url: /ar/java/psd-conversion/cropping-psd-converting-png/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# كيفية تحويل psd إلى png مع القص باستخدام Aspose.PSD للـ Java

## المقدمة
في عالم تطوير Java الديناميكي، إتقان معالجة الصور الفعّالة أمر حاسم. في هذا البرنامج التعليمي ستتعلم **كيفية تحويل psd إلى png** وقص الصورة في سير عمل واحد باستخدام مكتبة Aspose.PSD للـ Java القوية. بنهاية هذا الدليل خطوة‑بخطوة، ستكون قادرًا على إضافة قص دقيق لتصديرات PNG الخاصة بك وجعل تطبيقات Java تتعامل مع موارد PSD بثقة.

## إجابات سريعة
- **ماذا يفعل الكود؟** يقوم بتحميل PSD، يقطع مستطيلًا، ويحفظه كـ PNG.  
- **ما المكتبة المطلوبة؟** Aspose.PSD للـ Java (أحدث إصدار).  
- **هل أحتاج إلى ترخيص؟** نعم، يلزم ترخيص تجاري للاستخدام في الإنتاج.  
- **هل يمكنني تحديد أي منطقة قص؟** بالتأكيد – يمكنك ضبط قيم X و Y والعرض والارتفاع التي تحتاجها.  
- **هل هذه الطريقة سريعة للملفات الكبيرة؟** نعم، Aspose.PSD مُحسّنة للمعالجة عالية الأداء.

## ما هو تحويل psd إلى png؟
تحويل PSD إلى PNG يعني أخذ مستند Photoshop متعدد الطبقات وتحويله إلى صورة PNG غير مضغوطة. هذا التنسيق مثالي لتسليم الويب، المصغرات، أو أي سيناريو تحتاج فيه إلى صورة نقطية دون الطبقات الأصلية.

## لماذا قص PSD قبل تحويله إلى PNG؟
القص يتيح لك استخراج الجزء فقط من التصميم الذي تحتاجه، مما يقلل حجم الملف ويركّز على المحتوى البصري ذي الصلة. يكون ذلك مفيدًا بشكل خاص لإنشاء المصغرات، أصول واجهة المستخدم، أو إعداد الصور لتصاميم متجاوبة.

## المتطلبات المسبقة
قبل الغوص في البرنامج التعليمي، تأكد من توفر المتطلبات التالية:
- معرفة أساسية ببرمجة Java.  
- مجموعة تطوير Java (JDK) مثبتة على نظامك.  
- مكتبة Aspose.PSD للـ Java تم تحميلها وإضافتها إلى مشروعك.  
- ملف PSD تجريبي للاختبار.

## استيراد الحزم
في مشروع Java الخاص بك، تأكد من استيراد الحزم اللازمة لاستخدام وظائف Aspose.PSD:
```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;
import com.aspose.psd.Rectangle;
import com.aspose.psd.imageoptions.PngOptions;
```

## الخطوة 1: إعداد مشروعك
ابدأ بإنشاء مشروع Java وإضافة مكتبة Aspose.PSD للـ Java إلى مسار الفئة (classpath) الخاص بمشروعك. سيمنحك ذلك الوصول إلى جميع فئات معالجة الصور التي ستحتاجها.

## الخطوة 2: تحميل صورة PSD
```java
String dataDir = "Your Document Directory";
String srcPath = dataDir + "sample.psd";
// Load an existing PSD image
RasterImage image = (RasterImage)Image.load(srcPath);
```
*هنا نقوم بتحميل ملف PSD المصدر إلى كائن `RasterImage`، الذي يوفر عمليات قائمة على البكسل مثل القص.*

## الخطوة 3: تعريف منطقة القص
```java
// Create an instance of Rectangle class by passing x, y, width, and height
Rectangle cropRegion = new Rectangle(0, 0, 350, 450);
```
*الكائن `Rectangle` يحدد المنطقة التي تريد الاحتفاظ بها. اضبط قيم `x` و `y` و `width` و `height` لتناسب تصميمك. هذه الخطوة تجيب مباشرة على كلمة المفتاح “define crop region”.*

## الخطوة 4: قص صورة PSD
```java
// Call the crop method of Image class and pass the Rectangle instance
image.crop(cropRegion);
```
*استدعاء `crop` يغيّر الصورة في الذاكرة، متجاهلًا كل ما هو خارج المستطيل المحدد.*

## الخطوة 5: ضبط خيارات تصدير PNG
```java
// Create an instance of PngOptions class
PngOptions pngOptions = new PngOptions();
```
*`PngOptions` يتيح لك التحكم في إعدادات PNG الخاصة مثل مستوى الضغط، نوع اللون، وأكثر.*

## الخطوة 6: حفظ الصورة المقصوصة كـ PNG
```java
// Provide output path and PngOptions to convert the PSD file to PNG and save the output
String destName = dataDir + "export.png";
image.save(destName, pngOptions);
```
*طريقة `save` تقوم بعملية **تحويل psd إلى png** مع الحفاظ على القص الذي حددته.*

## المشكلات الشائعة والنصائح
- **أبعاد المستطيل غير صحيحة:** تأكد من أن العرض والارتفاع لا يتجاوزان حجم الصورة الأصلية، وإلا سيُطلق استثناء.  
- **استخدام الذاكرة مع PSDs الكبيرة:** حرّر كائن `RasterImage` (`image.dispose()`) بعد الحفظ لتحرير الموارد الأصلية.  
- **الترخيص غير مُحدد:** إذا شغلت الكود بدون ترخيص صالح، سيظهر علامة مائية على PNG الناتج.

## الأسئلة المتكررة
### هل يمكنني قص ملفات PSD بأشكال غير منتظمة باستخدام Aspose.PSD للـ Java؟
نعم، Aspose.PSD للـ Java يسمح لك بتعريف منطقة قص مخصصة، مما يمكنك من قص الصور إلى أشكال مختلفة.

### هل Aspose.PSD للـ Java مناسب لمهام معالجة الصور على نطاق واسع؟
بالطبع! تم تصميم Aspose.PSD للتعامل مع الصور الكبيرة بكفاءة، مما يجعله مثاليًا للمشروعات التي تتطلب معالجة صور مكثفة.

### هل أحتاج إلى ترخيص لـ Aspose.PSD للـ Java؟
نعم، يلزم وجود ترخيص صالح للاستخدام التجاري. يمكنك الحصول عليه من [Aspose Purchase](https://purchase.aspose.com/buy).

### كيف يمكنني طلب المساعدة أو الإبلاغ عن مشكلات مع Aspose.PSD للـ Java؟
قم بزيارة [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) لطلب المساعدة، مشاركة تجاربك، والإبلاغ عن أي مشكلات تواجهها.

### هل يمكنني تجربة Aspose.PSD للـ Java قبل الشراء؟
بالتأكيد! استكشف ميزات المكتبة من خلال تجربة مجانية متاحة [here](https://releases.aspose.com/).

---

**آخر تحديث:** 2026-03-21  
**تم الاختبار مع:** Aspose.PSD للـ Java 24.12 (أحدث إصدار وقت الكتابة)  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}