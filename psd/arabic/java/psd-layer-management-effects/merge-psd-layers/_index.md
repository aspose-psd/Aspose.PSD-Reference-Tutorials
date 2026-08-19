---
date: 2026-04-05
description: تعلم كيفية تصدير ملفات PSD إلى PNG ودمج طبقات PSD باستخدام Aspose.PSD
  للغة Java. يتضمن تحويل PSD إلى JPEG، ضبط جودة JPEG، ونصائح تحويل PSD إلى TIFF.
keywords:
- export psd to png
- convert psd to jpeg
- how to merge psd
- set jpeg quality
- psd to tiff conversion
linktitle: تصدير PSD إلى PNG ودمج الطبقات باستخدام Aspose.PSD للـ Java
second_title: Aspose.PSD Java API
title: تصدير PSD إلى PNG ودمج الطبقات باستخدام Aspose.PSD للـ Java
url: /ar/java/psd-layer-management-effects/merge-psd-layers/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# تصدير PSD إلى PNG ودمج الطبقات باستخدام Aspose.PSD للـ Java

## مقدمة

هل تساءلت يومًا كيف يحقق المصممون الجرافيكيون تلك الصور المعقدة والمتعددة الطبقات في Photoshop؟ السر غالبًا يكمن في **تصدير PSD إلى PNG** ودمج الطبقات بذكاء. إذا كنت تعمل مع ملفات PSD في Java، فإن إتقان هذه التقنيات يمكن أن يساعدك على إنشاء صور مركبة، تقليل حجم الملف، وتحضير الأصول للنشر على الويب أو الأجهزة المحمولة. في هذا الدرس سنستعرض **كيفية دمج طبقات PSD** باستخدام Aspose.PSD للـ Java، وسنظهر لك أيضًا كيفية تصدير النتيجة إلى PNG (أو JPEG/TIFF عند الحاجة). في النهاية، ستتمكن من أتمتة إدارة الطبقات وتدفقات التصدير مباشرة من تطبيق Java الخاص بك.

## إجابات سريعة
- **ما المكتبة التي تتعامل مع ملفات PSD في Java؟** Aspose.PSD for Java.  
- **هل يمكنني تصدير PSD إلى PNG؟** نعم – فقط قم بتعيين خيارات الصورة المناسبة.  
- **كيف يمكنني دمج طبقات متعددة؟** قم بتحميل PSD، تعديل مجموعة `Layer`، ثم احفظ.  
- **ماذا لو أردت التحكم في جودة JPEG؟** استخدم `JpegOptions` واضبط الجودة (0‑100).  
- **هل يتطلب Photoshop؟** لا، Aspose.PSD يعمل بشكل مستقل عن برامج Adobe.

## ما هو تصدير PSD إلى PNG؟
يعني تصدير PSD إلى PNG تحويل مستند Photoshop (PSD) إلى ملف Portable Network Graphics (PNG) مع إمكانية تسطيح أو دمج الطبقات اختياريًا. يحافظ PNG على الشفافية وهو مدعوم على نطاق واسع في الويب، مما يجعله تنسيقًا شائعًا لأصول واجهة المستخدم.

## لماذا دمج طبقات PSD برمجياً؟
- **الأتمتة:** معالجة مئات الملفات دفعيًا دون نقرات يدوية.  
- **الأداء:** دمج الطبقات يقلل من زمن العرض في التطبيقات اللاحقة.  
- **حجم الملف:** تسطيح الطبقات غير الضرورية يمكن أن يقلص الصورة النهائية.  
- **الاتساق:** يضمن نفس ترتيب الطبقات والدمج عبر عمليات البناء.

## المتطلبات المسبقة

1. **مكتبة Aspose.PSD للـ Java** – قم بالتنزيل من [رابط تنزيل Aspose.PSD للـ Java](https://releases.aspose.com/psd/java/).  
2. **بيئة تطوير Java** – IntelliJ IDEA، Eclipse، أو أي IDE تفضله.  
3. **ملف PSD تجريبي** – ملف يحتوي على طبقات متعددة (مثال: `layers.psd`).  
4. **معرفة أساسية بـ Java** – يجب أن تكون مرتاحًا مع الفئات والطرق.  
5. **رخصة Aspose مؤقتة (اختياري)** – للملفات الكبيرة أو لإزالة قيود التجربة، احصل على [رخصة مؤقتة](https://purchase.aspose.com/temporary-license/).

## استيراد الحزم

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.JpegOptions;
```

## دليل خطوة بخطوة

### الخطوة 1: تحميل ملف PSD

```java
String dataDir = "Your Document Directory";
PsdImage psdImage = (PsdImage)Image.load(dataDir + "layers.psd");
```

> يقوم هذا بتحميل `layers.psd` إلى كائن `PsdImage`، مما يمنحك وصولًا كاملًا إلى طبقاته.

### الخطوة 2: فحص الطبقات (كيفية دمج PSD)

```java
Layer[] layers = psdImage.getLayers();
System.out.println("Total layers: " + layers.length);

for (Layer layer : layers) {
    System.out.println("Layer name: " + layer.getName());
}
```

> مراجعة أسماء الطبقات تساعدك على اتخاذ قرار أيها تسطيح أو الاحتفاظ بها منفصلة.

### الخطوة 3: ضبط خيارات الصورة (ضبط جودة JPEG)

```java
JpegOptions jpgOptions = new JpegOptions();
jpgOptions.setQuality(80); // Set the quality of the JPEG image (0-100)
```

> إذا كنت تفضل PNG أو TIFF، يمكنك استبدال `JpegOptions` بـ `PngOptions` أو `TiffOptions` – هنا يتم تكوين **تحويل PSD إلى TIFF**.

### الخطوة 4: حفظ الصورة المدمجة (تصدير PSD إلى PNG)

```java
psdImage.save(dataDir + "MergePSDlayers_output.png", jpgOptions);
```

> طريقة `save` تكتب النتيجة المدمجة إلى `MergePSDlayers_output.png`.  
> *نصيحة:* لتصدير إلى PNG، استبدل `jpgOptions` بـ `PngOptions`؛ يبقى باقي الكود كما هو.

## المشكلات الشائعة والحلول

- **استثناء ملف غير موجود:** تحقق من أن `dataDir` ينتهي بفاصل مسار (`/` أو `\\`) وأن `layers.psd` موجود.  
- **ألوان غير متوقعة بعد الدمج:** تأكد من توافق أوضاع دمج الطبقات؛ يمكنك تعديلها عبر `layer.setBlendMode(...)`.  
- **ملف إخراج كبير:** خفّض جودة JPEG أو استخدم مستويات ضغط PNG لتقليل الحجم.

## الأسئلة المتكررة

**س: هل من الممكن حفظ الصورة المدمجة بصيغ أخرى غير JPEG؟**  
ج: بالتأكيد! Aspose.PSD يدعم PNG، BMP، TIFF، وأكثر. فقط استخدم فئة الخيارات المقابلة (`PngOptions`، `BmpOptions`، `TiffOptions`).

**س: كيف يمكنني ضبط جودة الصورة لصيغ إخراج مختلفة؟**  
ج: كل فئة خيارات تعرض إعدادات الجودة/الضغط الخاصة بها. بالنسبة لـ JPEG، استخدم `setQuality(int)`. بالنسبة لـ PNG، يمكنك التحكم في `CompressionLevel`.

**س: هل أحتاج إلى تثبيت Photoshop لاستخدام Aspose.PSD للـ Java؟**  
ج: لا. Aspose.PSD يعمل بشكل مستقل عن Adobe Photoshop، لذا يمكنك تشغيله على أي خادم أو بيئة CI.

**س: ماذا يحدث إذا لم أضبط خيارات الصورة قبل الحفظ؟**  
ج: المكتبة تطبق الإعدادات الافتراضية (مثلاً جودة JPEG 75). تحديد الخيارات يمنحك التحكم في النتيجة النهائية.

**س: هل يمكنني تحويل PSD مباشرة إلى TIFF في خطوة واحدة؟**  
ج: نعم – أنشئ كائن `TiffOptions` واستدعِ `psdImage.save("output.tiff", tiffOptions);`.

---

**آخر تحديث:** 2026-04-05  
**تم الاختبار مع:** Aspose.PSD للـ Java 24.12 (الأحدث وقت الكتابة)  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}