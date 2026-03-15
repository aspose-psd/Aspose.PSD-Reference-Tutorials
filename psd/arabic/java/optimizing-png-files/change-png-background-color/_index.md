---
date: 2026-03-15
description: تعلم كيفية تحويل ملفات PSD إلى PNG وتعيين لون خلفية PNG باستخدام Aspose.PSD
  للـ Java. يتضمن دليلًا خطوة بخطوة لمعالجة البكسل في Java.
linktitle: Convert PSD to PNG & Change Background Color – Aspose.PSD Java
second_title: Aspose.PSD Java API
title: تحويل PSD إلى PNG وتغيير لون الخلفية – Aspose.PSD Java
url: /ar/java/optimizing-png-files/change-png-background-color/
weight: 11
---

 as is.

Proceed.

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# تحويل PSD إلى PNG وتغيير لون الخلفية – Aspose.PSD Java

## المقدمة
إذا كنت بحاجة إلى **تحويل PSD إلى PNG** مع تخصيص الخلفية، فأنت في المكان الصحيح. في تطوير الويب والتطبيقات الحديثة، يمكن أن يحدث PNG نظيف باللون الخلفي المناسب فرقًا كبيرًا في تناسق واجهة المستخدم وجاذبيتها البصرية. في هذا البرنامج التعليمي سنستعرض العملية بالكامل باستخدام Aspose.PSD للـ Java — تحميل ملف PSD، تحويله إلى PNG، ثم استخدام **معالجة بكسل الصورة في Java** لاستبدال البكسلات الشفافة بلون تختاره. في النهاية ستتمكن من تغيير لون خلفية PNG ببضع أسطر من الشيفرة.

## إجابات سريعة
- **ماذا يعني “تحويل PSD إلى PNG”؟** يحول مستند الفوتوشوب إلى صورة PNG محمولة مع الحفاظ على الطبقات والشفافية.  
- **أي مكتبة تتولى عملية التحويل؟** Aspose.PSD للـ Java توفر واجهة برمجة تطبيقات بسيطة لتحميل ملفات PSD وحفظها كـ PNG.  
- **هل يمكنني تغيير لون الخلفية أثناء التحويل؟** نعم — عن طريق تعديل بكسلات ARGB32 يمكنك استبدال البكسلات الشفافة بأي لون.  
- **ما المتطلبات المسبقة؟** Java JDK، بيئة تطوير متكاملة (IDE)، ومكتبة Aspose.PSD للـ Java.  
- **كم يستغرق تنفيذ العملية؟** حوالي 10‑15 دقيقة لكتابة سكريبت أساسي.

## ما هو “تحويل PSD إلى PNG”؟
تحويل ملف PSD (مستند فوتوشوب) إلى PNG ينتج تنسيق صورة خالٍ من الفقدان ومناسب للويب يدعم الشفافية. هذا مفيد بشكل خاص عندما تحتاج إلى تضمين رسومات في مواقع الويب، التطبيقات المحمولة، أو أي منصة تفضل تنسيق PNG.

## لماذا نضبط لون خلفية PNG؟
قد يظهر PNG بخلفية شفافة بشكل غير متناسق على صفحات داكنة أو فاتحة. من خلال **ضبط لون خلفية PNG**، تضمن أن الصورة تندمج بسلاسة مع عناصر واجهة المستخدم المحيطة، مما يحسن الانسجام البصري وتجربة المستخدم.

## المتطلبات المسبقة
- **Java Development Kit (JDK)** – حمّله من [موقع Oracle](https://www.oracle.com/java/technologies/javase-downloads.html).  
- **بيئة تطوير متكاملة (IDE)** – IntelliJ IDEA، Eclipse، أو NetBeans تعمل بشكل جيد.  
- **مكتبة Aspose.PSD للـ Java** – احصل على أحدث نسخة من [رابط التحميل](https://releases.aspose.com/psd/java/).  
- **ملف PSD تجريبي** – احرص على وجود ملف PSD جاهز لاختبار التحويل وتغيير الخلفية.

## استيراد الحزم
لبدء العمل، استورد الفئات الأساسية من Aspose.PSD إلى مشروع Java الخاص بك:

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
```

تمنحك هذه الاستيرادات إمكانية تحميل الصور، التعامل مع البكسلات، واستخدام أدوات الألوان.

## دليل خطوة بخطوة

### الخطوة 1: تحديد مسار المستند
عرّف المجلد الذي يحتوي على ملف PSD المصدر ومكان حفظ ملف PNG الناتج.

```java
String dataDir = "Your Document Directory";
```

### الخطوة 2: تحميل صورة PSD
استخدم API الخاص بـ Aspose لتحميل ملف PSD إلى الذاكرة.

```java
PsdImage psdImage = (PsdImage) Image.load(dataDir + "sample.psd");
```

### الخطوة 3: تحويل PSD إلى PNG
أنشئ كائن `PsdImage` جديد سيعمل كحاوية للـ PNG.

```java
PsdImage pngImage = new PsdImage(psdImage);
```

### الخطوة 4: تحميل بكسلات ARGB32
احصل على بيانات البكسل لتتمكن من تعديل الألوان الفردية.

```java
int[] pixels = pngImage.loadArgb32Pixels(pngImage.getBounds());
```

### الخطوة 5: تحديد اللون الشفاف واللون البديل
حدد اللون الشفاف (عادةً ARGB 0) واختر لون الخلفية الجديد. هنا نستخدم الأصفر كمثال.

```java
int transparent = pngImage.getTransparentColor().toArgb();
int replacementColor = Color.getYellow().toArgb();
```

### الخطوة 6: المرور على البكسلات وتغيير الألوان
استبدل كل بكسل شفاف بلون الخلفية المختار.

```java
for (int i = 0; i < pixels.length; i++) {
    if (pixels[i] == transparent) {
        pixels[i] = replacementColor;
    }
}
```

### الخطوة 7: حفظ البكسلات المعدلة إلى الصورة
اكتب مصفوفة البكسل المحدثة مرة أخرى إلى صورة PNG.

```java
pngImage.saveArgb32Pixels(pngImage.getBounds(), pixels);
```

### الخطوة 8: حفظ الصورة الناتجة
أخيرًا، احفظ ملف PNG الجديد مع الخلفية المعدلة.

```java
pngImage.save(dataDir + "ChangeBackground_out.png");
```

## كيفية ضبط لون خلفية PNG في Java
توضح الشيفرة أعلاه طريقة **تغيير خلفية PNG** ببساطة عبر تعديل بيانات البكسل مباشرة. يمكنك استبدال `Color.getYellow()` بأي لون آخر مثل `Color.getRed()` أو `Color.fromArgb(255, 0, 128, 255)` لتتناسب مع لوحة تصميمك.

## المشكلات الشائعة والحلول
| المشكلة | السبب | الحل |
|-------|-------|-----|
| لا يزال PNG الناتج يظهر شفافيًا | لم يتم تطبيق لون الاستبدال بشكل صحيح | تأكد من أن المتغيّر `transparent` يطابق قيمة ARGB الشفافة الفعلية؛ استخدم `pngImage.getTransparentColor()` كما هو موضح. |
| الصورة مشوهة | تم استخدام حدود غير صحيحة عند تحميل/حفظ البكسلات | احرص على تمرير `pngImage.getBounds()` بشكل متسق لكل من `loadArgb32Pixels` و `saveArgb32Pixels`. |
| بطء الأداء مع ملفات كبيرة | حلقة تمر على ملايين البكسلات في خيط واحد | فكر في معالجة البكسلات باستخدام تدفقات متوازية (`IntStream.range(0, pixels.length).parallel()`) للصور الكبيرة. |

## الأسئلة المتكررة

**س: هل يمكنني استخدام Aspose.PSD بلغات برمجة أخرى؟**  
ج: نعم! رغم أن هذا الدليل يركز على Java، فإن Aspose.PSD متوفر أيضًا لـ .NET ومنصات أخرى.

**س: كيف أتعامل مع الأخطاء أثناء معالجة الصور؟**  
ج: غلف منطق التحويل داخل كتل `try‑catch` لالتقاط `IOException`، `InvalidOperationException`، أو الاستثناءات الخاصة بـ Aspose.

**س: هل هناك نسخة تجريبية مجانية من Aspose.PSD؟**  
ج: بالتأكيد! يمكنك تنزيل نسخة تجريبية مجانية من [هنا](https://releases.aspose.com/).

**س: ما هي صيغ الصور التي يمكنني تحويل ملفات PSD إليها؟**  
ج: يدعم Aspose.PSD صيغ PNG، JPEG، BMP، TIFF، GIF، والعديد غيرها.

**س: كيف يمكنني الحصول على الدعم إذا واجهت مشاكل؟**  
ج: يمكنك التواصل مع [منتدى دعم Aspose](https://forum.aspose.com/c/psd/34) للحصول على مساعدة من المجتمع ومهندسي Aspose.

---

**آخر تحديث:** 2026-03-15  
**تم الاختبار مع:** Aspose.PSD للـ Java 24.12 (أحدث نسخة وقت كتابة هذا الدليل)  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}