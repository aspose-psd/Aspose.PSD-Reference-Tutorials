---
date: 2026-03-26
description: تعلم كيفية استيراد صور PSD إلى طبقات باستخدام Aspose.PSD للغة Java. يوضح
  هذا الدليل خطوة بخطوة كيفية إضافة صورة، وتعيين إحداثيات الطبقة، وتعبئة لون طبقة
  PSD.
linktitle: How to Import PSD Images to Layers using Aspose.PSD Java
second_title: Aspose.PSD Java API
title: كيفية استيراد صور PSD إلى الطبقات باستخدام Aspose.PSD Java
url: /ar/java/psd-image-modification-conversion/import-images-psd-layers/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# كيفية استيراد صور PSD إلى طبقات باستخدام Aspose.PSD Java

## مقدمة
عندما يتعلق الأمر بالعمل مع ملفات PSD، فإن معرفة **how to import psd** برمجياً يمكن أن توفر لك ساعات من العمل اليدوي. سواء كنت مصممًا جرافيكيًا، أو مطورًا يبني أداة أتمتة تصميم، أو مجرد شخص يرغب في إضفاء حيوية على عرض تقديمي، فإن إتقان التعامل مع الطبقات يفتح أمامك عالماً من الإمكانيات الإبداعية. في هذا الدرس، ستتعلم **how to import psd** صورًا إلى الطبقات باستخدام Aspose.PSD for Java، خطوة بخطوة، مع الكثير من النصائح العملية على طول الطريق. احصل على فنجان قهوة، ولنبدأ!

## إجابات سريعة
- **ما الذي يغطيه هذا الدرس؟** استيراد صورة إلى طبقة PSD باستخدام Aspose.PSD for Java.  
- **ما نسخة المكتبة المطلوبة؟** أي إصدار حديث من Aspose.PSD for Java (الـ API متوافق مع الإصدارات السابقة).  
- **هل أحتاج إلى ترخيص؟** النسخة التجريبية المجانية تكفي للتطوير؛ يلزم ترخيص تجاري للإنتاج.  
- **كم من الوقت تستغرق العملية؟** حوالي 10‑15 دقيقة للاستيراد الأساسي.  
- **هل يمكنني تغيير حجم الصورة أو موقعها؟** نعم – يمكنك ضبط إحداثيات الطبقة وتعبئة الألوان حسب الحاجة.

## ما هو “how to import psd”؟
استيراد PSD يعني تحميل مستند Photoshop برمجياً، تعديل طبقاته (مثلاً، إضافة صورة)، ثم حفظ الملف المحدث. هذا النهج مثالي للمعالجة الدفعية، توليد الرسومات تلقائيًا، أو دمج موارد التصميم في تطبيقات أكبر.

## لماذا نستخدم Aspose.PSD for Java؟
يوفر Aspose.PSD واجهة برمجة تطبيقات مُدارة بالكامل وخالية من الترخيص تُجرد تنسيق ملف PSD المعقد. ستحصل على:
- وصول مباشر إلى الطبقات، الأقنعة، وبيانات القنوات.  
- لا حاجة إلى Photoshop أو مكتبات أصلية من طرف ثالث.  
- دعم كامل لملفات تعريف الألوان، أوضاع الدمج، والضغط.  

## المتطلبات المسبقة
قبل أن نبدأ بالأمور الممتعة، دعنا نتأكد من أنك جاهز! إليك ما تحتاجه:

- Java Development Kit (JDK): تأكد من تثبيت JDK على جهازك. يمكنك تنزيل أحدث نسخة من [موقع Oracle](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).  
- Aspose.PSD for Java: تحتاج إلى مكتبة Aspose.PSD. يمكنك تنزيلها من [رابط الإصدار](https://releases.aspose.com/psd/java/). هذه المكتبة أساسية لأنها توفر جميع الوظائف اللازمة للتعامل مع ملفات PSD.  
- IDE: بيئة تطوير متكاملة جيدة (مثل IntelliJ IDEA أو Eclipse) ستسهل كتابة الكود وتصحيح الأخطاء.  
- معرفة أساسية بـ Java: الإلمام بالمفاهيم الأساسية للـ Java سيساعدك على المتابعة بسهولة.  

مع استيفاء هذه المتطلبات، أنت جاهز لبدء رحلتك مع PSD!

## كيفية استيراد صور PSD إلى الطبقات
فيما يلي دليل واضح مرقم يشرح **how to add image** إلى طبقة PSD، **set layer coordinates**، و **fill psd layer color**.

### الخطوة 1: استيراد الحزم المطلوبة
أولاً، نستورد فئات Aspose.PSD التي سنحتاجها. هذا يهيئ الأساس لبقية الكود.

```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;
import com.aspose.psd.Point;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
```

### الخطوة 2: تحديد دليل المستند
حدد موقع ملف PSD المصدر ومكان حفظ النتيجة.

```java
String dataDir = "Your Document Directory";
```

استبدل `"Your Document Directory"` بالمسار الفعلي على نظام ملفاتك حيث توجد ملفات PSD.

### الخطوة 3: تحميل ملف PSD الخاص بك
افتح ملف PSD حتى نتمكن من العمل على طبقاته.

```java
PsdImage image = (PsdImage) Image.load(dataDir + "sample.psd");
```

تأكد من أن `"sample.psd"` يطابق اسم الملف الذي تريد تحريره.

### الخطوة 4: استخراج الطبقة المستهدفة
اختر الطبقة التي ستستقبل الصورة الجديدة. هنا نستخدم الطبقة الثانية (الفهرس 1).

```java
Layer layer = image.getLayers()[1];
```

إذا كنت بحاجة إلى طبقة مختلفة، فقط غير الفهرس.

### الخطوة 5: إنشاء صورة جديدة للاستيراد
الآن سنقوم **add image psd layer** بإنشاء `PsdImage` جديد سنرسم عليه.

```java
PsdImage drawImage = new PsdImage(200, 200);
```

يمكنك تعديل العرض والارتفاع لتتناسب مع صورتك المصدر.

### الخطوة 6: تعبئة سطح الصورة (تعيين لون الطبقة)
دعنا **fill psd layer color** بخلفية صفراء زاهية. هذا يوضح كيفية تعيين لون صلب قبل الرسم.

```java
Graphics g = new Graphics(drawImage);
g.clear(Color.getYellow());
```

لا تتردد في استبدال `Color.getYellow()` بأي `Color` أخرى تفضلها.

### الخطوة 7: رسم الصورة على الطبقة (تعيين إحداثيات الطبقة)
هذا هو جوهر **how to add image** – نضع الصورة التي تم إنشاؤها حديثًا على الطبقة المختارة عند إحداثيات محددة.

```java
layer.drawImage(new Point(10, 10), drawImage);
```

استدعاء `Point(10, 10)` **sets layer coordinates** (X = 10, Y = 10). غيّر هذه القيم لتحديد موقع الصورة بدقة حيث تحتاجها.

### الخطوة 8: حفظ ملف PSD المحدث
أخيرًا، احفظ التغييرات إلى القرص.

```java
image.save(dataDir + "ImportImageToPSDLayer_out.psd");
```

امنح ملف الإخراج اسمًا ذا معنى؛ المثال يضيف `_out` للحفاظ على الأصل دون تعديل.

## المشكلات الشائعة والحلول
- **الصورة تظهر فارغة** – تأكد من استدعاء `Graphics.clear()` قبل الرسم؛ وإلا قد تكون اللوحة شفافة.  
- **تم تعديل الطبقة الخاطئة** – تذكر أن فهارس الطبقات تبدأ من 0. تحقق مرة أخرى من الفهرس الذي تستخدمه في `getLayers()`.  
- **ملف تعريف لون غير مدعوم** – Aspose.PSD يتعامل مع معظم الملفات، ولكن إذا لاحظت تغيرات في الألوان، حاول تحويل الصورة المصدر إلى sRGB قبل الاستيراد.  

## الأسئلة المتكررة

**س: ما هو Aspose.PSD for Java؟**  
ج: Aspose.PSD for Java هي مكتبة تمكّن المطورين من العمل مع ملفات PSD، مما يسمح بالتلاعب بالطبقات، الصور، وغيرها من الميزات برمجياً.

**س: هل يمكنني استخدام Aspose.PSD في لغات برمجة أخرى؟**  
ج: نعم! لدى Aspose مكتبات لمختلف لغات البرمجة، بما في ذلك .NET و C++ و Python.

**س: هل هناك نسخة مجانية من Aspose.PSD for Java؟**  
ج: نعم، توفر Aspose [نسخة تجريبية مجانية](https://releases.aspose.com/) يمكنك تنزيلها والبدء في التجربة.

**س: ماذا أفعل إذا واجهت مشاكل؟**  
ج: يمكنك زيارة [منتدى دعم Aspose](https://forum.aspose.com/c/psd/34) للحصول على مساعدة من المجتمع وخبراء Aspose.

**س: كيف أشتري ترخيصًا لـ Aspose.PSD for Java؟**  
ج: يمكنك شراء الترخيص بزيارة [صفحة شراء Aspose](https://purchase.aspose.com/buy).

---

**آخر تحديث:** 2026-03-26  
**تم الاختبار مع:** Aspose.PSD for Java (أحدث إصدار)  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}