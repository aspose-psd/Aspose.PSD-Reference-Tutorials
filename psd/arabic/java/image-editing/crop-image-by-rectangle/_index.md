---
date: 2026-01-01
description: استكشف كيفية قص الصورة باستخدام Aspose.PSD للـ Java. اتبع دليلنا خطوة
  بخطوة لتحميل ملف PSD، وقص مستطيل الصورة، وتحويل PSD إلى JPEG.
linktitle: Crop Image by Rectangle
second_title: Aspose.PSD Java API
title: 'قص الصورة جافا: قص الصورة بواسطة مستطيل باستخدام Aspose.PSD'
url: /ar/java/image-editing/crop-image-by-rectangle/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# قص الصورة في جافا: قص الصورة بواسطة مستطيل باستخدام Aspose.PSD

## المقدمة

تعد معالجة الرسومات جزءًا روتينيًا من **معالجة الصور في جافا**، وتوفر لك Aspose.PSD for Java واجهة برمجة تطبيقات نظيفة وعالية الأداء للعمل مع ملفات PSD. في هذا البرنامج التعليمي ستتعلم **كيفية قص الصورة** باستخدام مستطيل، تحميل ملف PSD، وأخيرًا تحويل النتيجة إلى JPEG—كل ذلك ببضع أسطر من كود جافا.

## إجابات سريعة
- **ماذا يعني “crop image java”؟** يشير إلى تقليم صورة إلى مستطيل محدد باستخدام كود جافا.  
- **أي مكتبة تتولى العملية؟** Aspose.PSD for Java توفر الفئات اللازمة.  
- **هل أحتاج إلى ترخيص للاختبار؟** يتوفر إصدار تجريبي مجاني؛ الترخيص مطلوب للإنتاج.  
- **هل يمكنني تحويل ملف PSD المقصوص إلى JPEG؟** نعم—استخدم `JpegOptions` عند الحفظ.  
- **كم يستغرق تنفيذ العملية؟** عادةً أقل من 10 دقائق لسيناريو أساسي.

## ما هو قص صورة بمستطيل في جافا؟

يعني قص صورة بمستطيل اختيار منطقة معينة (محددة بـ X, Y, العرض، والارتفاع) وتجاهل كل ما هو خارج تلك المنطقة. هذه العملية شائعة عندما تحتاج إلى التركيز على جزء معين من مستند PSD أكبر.

## لماذا نستخدم Aspose.PSD لهذه المهمة؟

- **بدون تبعيات خارجية** – يعمل مع جافا النقية.  
- **يدعم PSD، PNG، JPEG، والعديد من الصيغ الأخرى** – يمكنك **تحويل PSD إلى JPEG** فورًا.  
- **عروض عالية الدقة** – يحتفظ بمعلومات الطبقات وملفات تعريف الألوان أثناء القص.  

## المتطلبات المسبقة

- تثبيت مجموعة تطوير جافا (JDK).  
- مكتبة Aspose.PSD for Java – حمّلها من الـ [الموقع](https://releases.aspose.com/psd/java/).  

## استيراد الحزم

تأكد من تضمين الحزم اللازمة في مشروع جافا الخاص بك للاستفادة من إمكانيات Aspose.PSD for Java. أضف عبارات الاستيراد التالية في بداية ملف جافا الخاص بك:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;
import com.aspose.psd.Rectangle;

import com.aspose.psd.imageoptions.JpegOptions;
```

الآن، لنقسم العملية إلى عدة خطوات لتوجيهك خلال قص صورة بمستطيل باستخدام Aspose.PSD for Java.

## الخطوة 1: إعداد دليل المستندات الخاص بك

```java
String dataDir = "Your Document Directory";
```

استبدل `"Your Document Directory"` بالمسار الفعلي حيث يوجد ملف PSD الخاص بك.

## الخطوة 2: تحديد ملفات المصدر والوجهة

```java
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "CroppingByRectangle_out.jpg";
```

عرّف المسارات لملف PSD المصدر وملف JPEG الوجهة.

## الخطوة 3: تحميل الصورة وتخزينها مؤقتًا

```java
RasterImage rasterImage = (RasterImage)Image.load(sourceFile);

if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

هنا نقوم **بتحميل ملف PSD** إلى كائن `RasterImage` ونخزن بياناته مؤقتًا لتحسين الأداء.

## الخطوة 4: إنشاء وتعريف مستطيل القص

```java
Rectangle rectangle = new Rectangle(20, 20, 20, 20);
```

أنشئ كائنًا من فئة `Rectangle` بالحجم المطلوب للقص. تمثل المعلمات **X**, **Y**, **العرض**, و**الارتفاع** على التوالي.

## الخطوة 5: قص الصورة وحفظها

```java
rasterImage.crop(rectangle);
rasterImage.save(destName, new JpegOptions());
```

نفّذ عملية القص باستخدام المستطيل المحدد و**تحويل PSD إلى JPEG** عن طريق حفظ النتيجة باستخدام `JpegOptions`.

كرر هذه الخطوات حسب الحاجة، مع تعديل المعلمات وفقًا لمتطلباتك الخاصة.

## المشكلات الشائعة والنصائح

- **المستطيل خارج حدود الصورة** – تأكد من أن إحداثيات المستطيل داخل أبعاد الصورة المصدر.  
- **استهلاك الذاكرة** – استدعِ `rasterImage.dispose()` بعد الانتهاء لتحرير الموارد الأصلية.  
- **التحكم في الجودة** – يمكنك ضبط `JpegOptions.setQuality(int)` للتحكم في مستوى ضغط JPEG الناتج.

## الخلاصة

في هذا البرنامج التعليمي استعرضنا عملية **قص الصورة في جافا** بمستطيل باستخدام Aspose.PSD for Java. باتباع هذه الخطوات يمكنك دمج قدرات قوية لمعالجة الصور—تحميل ملف PSD، قص منطقة محددة، وتحويل النتيجة إلى JPEG—في أي تطبيق جافا.

## الأسئلة المتكررة

### س1: هل يمكنني استخدام Aspose.PSD for Java مع أطر عمل جافا أخرى؟

ج1: نعم، يمكن دمج Aspose.PSD for Java مع أطر عمل جافا متعددة، مما يوفر مرونة في مشاريع التطوير الخاصة بك.

### س2: هل هناك نسخة تجريبية مجانية متاحة لـ Aspose.PSD for Java؟

ج2: نعم، يمكنك الوصول إلى النسخة التجريبية المجانية [هنا](https://releases.aspose.com/).

### س3: أين يمكنني العثور على دعم إضافي أو مساعدة؟

ج3: زر [منتدى Aspose.PSD](https://forum.aspose.com/c/psd/34) للحصول على دعم المجتمع والنقاشات.

### س4: كيف أحصل على ترخيص مؤقت لـ Aspose.PSD for Java؟

ج4: يمكنك الحصول على ترخيص مؤقت [هنا](https://purchase.aspose.com/temporary-license/).

### س5: ما هي صيغ الصور المدعومة للقص في Aspose.PSD for Java؟

ج5: تدعم Aspose.PSD for Java صيغ صور متعددة، بما في ذلك PSD، PNG، JPEG، وغيرها.

---

**آخر تحديث:** 2026-01-01  
**تم الاختبار مع:** Aspose.PSD for Java 24.12  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}