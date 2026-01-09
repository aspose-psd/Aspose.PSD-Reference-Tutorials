---
date: 2026-01-09
description: تعلم كيفية تحويل ملفات PSD إلى PNG وقص ملفات PSD في Java باستخدام Aspose.PSD.
  تعديل الصور بدقة أصبح سهلًا.
linktitle: Crop PSD File
second_title: Aspose.PSD Java API
title: تحويل PSD إلى PNG والقص باستخدام Aspose.PSD للـ Java
url: /ar/java/image-processing/crop-psd-file/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# تحويل PSD إلى PNG وقص ملف PSD باستخدام Aspose.PSD للغة Java

## المقدمة

إذا كنت بحاجة إلى **تحويل PSD إلى PNG** مع قص الصورة إلى المنطقة الدقيقة التي تهمك، فإن Aspose.PSD للغة Java يوفر طريقة برمجية نظيفة للقيام بذلك. في هذا الدرس سنستعرض العملية بالكامل — من إعداد المشروع إلى حفظ كل من ملف PSD المقصوص وتصدير PNG — حتى تتمكن من دمج معالجة الصور الدقيقة في أي تطبيق Java.

## إجابات سريعة
- **هل يمكن لـ Aspose.PSD تحويل PSD إلى PNG؟** نعم، يدعم التحويل المباشر مع الحفاظ على كامل تفاصيل الطبقات.  
- **هل أحتاج إلى ترخيص للقص؟** النسخة التجريبية المجانية تكفي للتطوير؛ الترخيص مطلوب للإنتاج.  
- **ما نسخة Java المطلوبة؟** يوصى بـ Java 8 أو أعلى.  
- **هل سيحافظ PNG على الشفافية؟** نعم، باستخدام `PngColorType.TruecolorWithAlpha`.  
- **هل العملية سريعة للملفات الكبيرة؟** Aspose.PSD مُحسّن للأداء على ملفات PSD عالية الدقة.

## ما هو “تحويل PSD إلى PNG” ولماذا نقصه؟

تحويل مستند Photoshop (PSD) إلى PNG خطوة شائعة عندما تحتاج إلى صورة جاهزة للويب أو نسخة خفيفة من التصميم. يتيح لك القص استخراج الجزء الذي تحتاجه فقط من اللوحة، مما يقلل حجم الملف ويركّز على المحتوى ذي الصلة. الجمع بين العمليتين في سير عمل واحد يوفر الوقت ويحافظ على بساطة قاعدة الشيفرة.

## المتطلبات المسبقة

قبل أن نبدأ، تأكد من وجود ما يلي:

- **بيئة تطوير Java** – JDK 8+ مثبتة ومُعدّة.  
- **Aspose.PSD للغة Java** – حمّل المكتبة وأضفها إلى مشروعك. يمكنك العثور على المكتبة ووثائقها [هنا](https://reference.aspose.com/psd/java/).  
- **ملف PSD تجريبي** – ملف PSD موجود داخل دليل مشروعك تريد قصه وتحويله.

## استيراد الحزم

في مشروع Java الخاص بك، ابدأ باستيراد الحزم اللازمة للاستفادة من وظائف Aspose.PSD. أضف عبارات الاستيراد التالية:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;
import com.aspose.psd.Rectangle;

import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.imageoptions.PsdOptions;
import com.aspose.psd.xmp.types.complex.colorant.ColorType;
```

## الخطوة 1: تعيين دليل المستندات

```java
String dataDir = "Your Document Directory";
```

استبدل `"Your Document Directory"` بالمسار الفعلي حيث يقع ملف PSD الخاص بك.

## الخطوة 2: تحميل ملف PSD

```java
String sourceFileName = dataDir + "1.psd";
RasterImage image = (RasterImage)Image.load(sourceFileName);
```

حمّل ملف PSD الذي تريد قصه إلى كائن `RasterImage`.

## الخطوة 3: تعريف منطقة القص

```java
image.crop(new Rectangle(10, 30, 100, 100));
```

حدد المنطقة التي تريد قصها باستخدام فئة `Rectangle`، مع توفير قيم **x** و **y** و **العرض** و **الارتفاع**.

## الخطوة 4: حفظ PSD المقصوص

```java
String exportPathPsd = dataDir + "CropTest.psd";
image.save(exportPathPsd, new PsdOptions());
```

احفظ الصورة المقصوصة مرة أخرى بصيغة PSD باستخدام المسار المحدد.

## الخطوة 5: حفظ الصورة المقصوصة كـ PNG

```java
String exportPathPng = dataDir + "CropTest.png";
PngOptions options = new PngOptions();
options.setColorType(PngColorType.TruecolorWithAlpha);
image.save(exportPathPng, options);
```

بالإضافة إلى ذلك، صدّر الصورة المقصوصة كملف PNG مع الحفاظ على الشفافية.

## لماذا نستخدم Aspose.PSD للغة Java لقص ملفات PSD؟

- **دقة كاملة للـ PSD** – جميع الطبقات والأقنعة والتأثيرات تبقى سليمة أثناء التحويل.  
- **لا حاجة إلى Photoshop الأصلي** – يعمل بالكامل على الخادم.  
- **أداء عالي** – مُحسّن للملفات الكبيرة ومعالجة الدُفعات.  
- **واجهة برمجة تطبيقات بسيطة** – بضع أسطر من الشيفرة تحقق القص والتحويل.

## المشكلات الشائعة والحلول

| المشكلة | الحل |
|-------|----------|
| **الملف غير موجود** | تحقق من أن `dataDir` ينتهي بفاصل مسار (`/` أو `\\`). |
| **فقدان الخلفية الشفافة** | تأكد من ضبط `PngOptions.setColorType(PngColorType.TruecolorWithAlpha)`. |
| **نفاد الذاكرة للـ PSD الضخمة** | عالج الصورة على أجزاء أو زد حجم heap في JVM (`-Xmx`). |
| **استثناء الترخيص** | طبّق ترخيص Aspose قبل تحميل الصورة (`License license = new License(); license.setLicense("Aspose.PSD.lic");`). |

## الأسئلة المتكررة

**س: هل يمكنني استخدام Aspose.PSD للغة Java لقص الصور بصيغ أخرى؟**  
ج: بينما يركّز الأساس على PSD، تدعم المكتبة أيضًا PNG و JPEG و BMP وغيرها من الصيغ النقطية.

**س: هل Aspose.PSD مناسب لمعالجة الصور على نطاق واسع؟**  
ج: نعم، تم تحسينه للأداء ويمكنه التعامل مع عمليات الدُفعات بكفاءة.

**س: هل هناك اعتبارات ترخيص للاستخدام في الإنتاج؟**  
ج: نعم، راجع صفحة [شراء Aspose.PSD للغة Java](https://purchase.aspose.com/buy) للحصول على التفاصيل.

**س: أين يمكنني الحصول على دعم المجتمع؟**  
ج: زر منتدى [Aspose.PSD للغة Java](https://forum.aspose.com/c/psd/34) للحصول على مساعدة من مطورين آخرين.

**س: هل يمكنني تجربة المكتبة قبل الشراء؟**  
ج: بالتأكيد — حمّل نسخة تجريبية مجانية [هنا](https://releases.aspose.com/).

## الخاتمة

الآن لديك حل كامل من البداية إلى النهاية **لتحويل PSD إلى PNG** مع قص الصورة إلى المنطقة الدقيقة التي تحتاجها. دمج هذه المقاطع في مشاريع Java الخاصة بك لأتمتة معالجة الصور بأسلوب Photoshop دون الحاجة إلى Photoshop نفسه.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**آخر تحديث:** 2026-01-09  
**تم الاختبار مع:** Aspose.PSD 24.11 للغة Java  
**المؤلف:** Aspose  

---