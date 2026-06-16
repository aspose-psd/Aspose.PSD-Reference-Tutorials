---
date: 2026-03-07
description: تعلم كيفية إنشاء علامة مائية للصورة في ملفات PSD باستخدام Aspose.PSD
  للغة Java – دليل سريع لمعالجة صور PSD وحماية رسوماتك.
linktitle: How to Create Image Watermark in PSD Files with Aspose.PSD for Java
second_title: Aspose.PSD Java API
title: كيفية إنشاء علامة مائية للصور في ملفات PSD باستخدام Aspose.PSD للـ Java
url: /ar/java/modifying-converting-psd-images/add-watermark-psd-files/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# إضافة علامة مائية إلى ملفات PSD باستخدام Aspose.PSD للـ Java

## مقدمة
العلامات المائية طريقة دقيقة ولكن فعّالة لحماية صورك وإظهار الملكية. في هذا الدرس، ستتعلم كيفية **إنشاء علامة مائية صورة** في ملفات PSD باستخدام Aspose.PSD للـ Java. سواء كنت مصورًا يعرض معرض أعماله أو مصممًا يقدم أحدث مشاريعه، فإن إضافة علامة مائية قد تكون ضرورية للحفاظ على هوية العلامة التجارية. لذا، احضر فنجان القهوة، استرخِ، ولنبدأ!

## إجابات سريعة
- **ما هو الهدف الأساسي؟** إنشاء علامة مائية صورة في ملف PSD برمجيًا.  
- **ما المكتبة المستخدمة؟** Aspose.PSD للـ Java.  
- **كم يستغرق التنفيذ؟** تقريبًا 10‑15 دقيقة لعلامة مائية أساسية.  
- **ما المتطلبات الأساسية؟** Java JDK، مكتبة Aspose.PSD، وملف PSD مصدر.  
- **هل يمكن تصدير النتيجة كـ PNG؟** نعم – استخدم طريقة `save` مع `PngOptions`.

## ما هو **إنشاء علامة مائية صورة**؟
إنشاء علامة مائية صورة يعني إضافة نص أو رسومات شبه شفافة إلى ملف صورة برمجيًا بحيث يتم دمج معلومات الملكية مباشرةً في المحتوى البصري.

## لماذا نستخدم Aspose.PSD للـ Java لمعالجة صور psd؟
توفر Aspose.PSD مجموعة غنية من الـ APIs لـ **معالجة صور psd**، مما يتيح لك تعديل الطبقات، تطبيق التأثيرات، وتصدير الصورة النهائية دون الحاجة إلى Photoshop. تدعم التصيير عالي الدقة، عمليات الدفعة، وتعمل على جميع أنظمة التشغيل الرئيسية.

## المتطلبات المسبقة
قبل الغوص في الكود، تأكد من أن لديك ما يلي:

1. **مجموعة تطوير جافا (JDK)** – أي نسخة حديثة (8 أو أعلى).  
2. **مكتبة Aspose.PSD للـ Java** – حمّلها من [موقع Aspose](https://releases.aspose.com/psd/java/).  
3. **بيئة تطوير متكاملة (IDE)** – Eclipse، IntelliJ IDEA، أو أي محرر تفضله.  
4. **ملف PSD** – ملف تجريبي اسمه `layers.psd` موجود في دليل العمل الخاص بك.  
5. **معرفة أساسية بجافا** – الإلمام بالصفوف، الكائنات، وملفات الإدخال/الإخراج.

## استيراد الحزم
الآن بعد أن أعددت كل شيء، لنستورد الحزم الضرورية. الاستيراد في جافا يتيح لك جلب الصفوف والدوال من مكتبات مختلفة، مما يجعل الكود أكثر كفاءة. إليك ما ستحتاجه:

```java
import com.aspose.psd.Color;
import com.aspose.psd.Font;
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;
import com.aspose.psd.RectangleF;
import com.aspose.psd.StringAlignment;
import com.aspose.psd.StringFormat;
import com.aspose.psd.brushes.SolidBrush;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PngOptions;
```

## كيفية **إنشاء علامة مائية صورة** – دليل خطوة بخطوة

### الخطوة 1: إعداد الدليل الخاص بك
أولًا، نحتاج إلى تحديد المسار حيث يقع ملف PSD الخاص بك. هذا أمر حاسم لأن جافا تحتاج إلى معرفة مكان العثور على ملفاتك.

```java
String dataDir = "Your Document Directory";
```

استبدل `Your Document Directory` بالمجلد الفعلي الذي يحتوي على `layers.psd`.

### الخطوة 2: تحميل ملف PSD
بعد ذلك، سنقوم بتحميل ملف PSD وتحويله إلى كائن `PsdImage`. هذه الخطوة تحول الملف إلى صيغة يمكننا تعديلها.

```java
PsdImage psdImage = (PsdImage) Image.load(dataDir + "layers.psd");
```

فكر في ذلك كفتح كتاب لتبدأ بالكتابة على صفحاته.

### الخطوة 3: إنشاء كائن Graphics
بعد تحميل ملف PSD، نحتاج إلى إنشاء كائن `Graphics`. يتيح لنا هذا تنفيذ عمليات الرسم — كأنك تلتقط فرشاة رسم لكانفاسك.

```java
Graphics graphics = new Graphics(psdImage);
```

### الخطوة 4: تعريف الخط للعلامة المائية
حان الوقت لتحديد مظهر العلامة المائية. سنستخدم Arial بحجم خط 20. يمكنك تغيير اسم الخط أو حجمه ليتناسب مع نمط علامتك التجارية.

```java
Font font = new Font("Arial", 20.0f);
```

### الخطوة 5: إنشاء فرشاة صلبة للعلامة المائية
الفرشاة الصلبة تعطي العلامة المائية لونها وشفافيتها. سنضبط قيمة ألفا إلى 50 (من 255) للحصول على رمادي شبه شفاف.

```java
SolidBrush brush = new SolidBrush(Color.fromArgb(50, 128, 128, 128));
```

هنا، `Color.fromArgb(50, 128, 128, 128)` ينشئ لونًا رماديًا بنسبة شفافية 50% — مثالي لتوقيع خفيف.

### الخطوة 6: ضبط محاذاة النص للعلامة المائية
لضمان ظهور العلامة المائية في وسط الصورة، سنقوم بتكوين خيارات محاذاة النص.

```java
StringFormat sf = new StringFormat();
sf.setAlignment(StringAlignment.Center);
sf.setLineAlignment(StringAlignment.Center);
```

### الخطوة 7: رسم العلامة المائية باستخدام **java graphics drawstring**
الآن نصل إلى الجزء المثير. بعد تجهيز سياق الرسم، سنرسم نص العلامة المائية على الصورة باستخدام `java graphics drawstring`.

```java
graphics.drawString("Some watermark text", font, brush, new RectangleF(0, 0, psdImage.getWidth(), psdImage.getHeight()), sf);
```

استبدل `"Some watermark text"` بالنص الفعلي الذي تريد ظهوره على ملف PSD.

### الخطوة 8: **حفظ PSD كـ PNG** – **export psd png**
بعد وضع العلامة المائية، سنقوم **بحفظ psd png** (أي تصدير PSD إلى PNG) حتى يمكن عرض النتيجة في أي متصفح أو عارض صور.

```java
psdImage.save(dataDir + "AddWatermark_output.png", new PngOptions());
```

تنفيذ هذا السطر ينشئ ملف PNG جديد يحتوي على علامتك المائية.

## المشكلات الشائعة والحلول
- **العلامة المائية غير مرئية؟** تحقق من قيمة ألفا في `Color.fromArgb()`؛ قيمة أقل تجعل العلامة أكثر شفافية.  
- **الأبعاد غير صحيحة؟** تأكد من استخدام `psdImage.getWidth()` و `psdImage.getHeight()` للمستطيل بحيث يتناسب النص مع حجم الصورة.  
- **استثناءات الترخيص؟** رخصة تقييم مؤقتة تكفي للاختبار، لكن الرخصة الكاملة مطلوبة للاستخدام الإنتاجي.

## الأسئلة المتكررة

**س: هل يمكن تخصيص نص العلامة المائية؟**  
ج: بالتأكيد! فقط استبدل السلسلة في طريقة `drawString` بالنص الذي ترغب به.

**س: ماذا لو أردت خطًا مختلفًا؟**  
ج: غيّر إنشاء الـ `Font` إلى أي خط مثبت، مثل `new Font("Times New Roman", 24.0f)`.

**س: هل هناك طريقة لضبط الشفافية؟**  
ج: نعم — عدّل المعامل الأول في `Color.fromArgb(alpha, r, g, b)`. القيم الأقل للـ `alpha` تزيد الشفافية.

**س: هل يمكنني استخدام صيغ صور أخرى غير PNG؟**  
ج: بالطبع. استبدل `new PngOptions()` بـ `new JpegOptions()` أو `new BmpOptions()` لتقوم **بحفظ psd png** بصيغة مختلفة.

**س: أين يمكنني العثور على مزيد من المساعدة؟**  
ج: للاستفسارات التفصيلية، زر [منتديات Aspose](https://forum.aspose.com/c/psd/34) أو راجع [الوثائق](https://reference.aspose.com/psd/java/).

## الخاتمة
لقد تعلمت الآن كيفية **إنشاء علامة مائية صورة** في ملف PSD باستخدام Aspose.PSD للـ Java. هذه التقنية لا تحمي محتواك فحسب، بل تعزز حضور علامتك التجارية عبر جميع الأصول البصرية. جرّب خطوطًا، ألوانًا، ومستويات شفافية مختلفة لتتناسب مع أسلوبك، وتذكر أنه يمكنك **حفظ psd png** أو **export psd png** إلى أي صيغة تحتاجها.

---

**آخر تحديث:** 2026-03-07  
**تم الاختبار مع:** Aspose.PSD للـ Java 24.11  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}