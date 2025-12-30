---
date: 2025-12-30
description: تعلم كيفية إنشاء ملف PSD باستخدام Java من خلال دمج صورتين باستخدام Aspose.PSD.
  اتبع دليلنا خطوة بخطوة لدمج الصور في ملف PSD بسرعة.
linktitle: Combine Images
second_title: Aspose.PSD Java API
title: كيفية إنشاء ملف PSD في جافا – دمج الصور باستخدام Aspose.PSD
url: /ar/java/image-editing/combine-images/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# إنشاء ملف PSD في Java – دمج الصور باستخدام Aspose.PSD

## المقدمة

## إجابات سريعة
- **ما هي المكتبة الأفضل لدمج الصور في PSD؟** Aspose.PSD for Java.
- **كم من الوقت تستغرق العملية؟** حوالي 10‑15 دقيقة للدمج الأساسي.
- **هل أحتاج إلى ترخيص؟** إصدار تجريبي مجاني يكفي للاختبار؛ يلزم ترخيص تجاري للإنتاج.
- **هل يمكنني إضافة أكثر من صورتين؟** نعم – كرّر استدعاءات `drawImage` لكل طبقة إضافية.
- **ما نسخة Java المدعومة؟** Java 8 وما بعدها.

## المتطلبات المسبقة

قبل البدء، تأكد من وجود ما يلي:

1. **Aspose.PSD Library** – قم بتنزيلها من [هنا](https://releases.aspose.com/psd/java/).  
2. **Java Development Kit (JDK)** – يُنصح باستخدام Java 8+.  
3. **Document Directory** – مجلد على جهازك حيث تُخزن الصور المصدر وملف PSD الناتج.

## استيراد الحزم

ابدأ باستيراد فئات Aspose.PSD المطلوبة إلى مشروعك:

```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;

import com.aspose.psd.imageoptions.PsdOptions;
import com.aspose.psd.sources.FileCreateSource;
```

## دليل خطوة بخطوة

### الخطوة 1: إنشاء خيارات PSD (تحضير الملف)

نقوم أولاً ب إنشاء كائن `PsdOptions` الذي سيحمل إعدادات الإخراج.

```java
PsdOptions imageOptions = new PsdOptions();
```

### الخطوة 2: تعيين FileCreateSource (تحديد مكان حفظ ملف PSD)

قم بتعيين `FileCreateSource` إلى الخيارات، مع الإشارة إلى ملف النتيجة المطلوب.

```java
imageOptions.setSource(new FileCreateSource(dataDir + "Two_images_result_out.psd", false));
```

### الخطوة 3: إنشاء كائن Image (تهيئة حجم اللوحة)

أنشئ كائن `Image` باستخدام الخيارات وحدد لوحة بحجم 600 × 600 بكسل.

```java
Image image = Image.create(imageOptions, 600, 600);
```

### الخطوة 4: تهيئة Graphics ورسم الصورة الأولى

يتيح لنا كائن `Graphics` الرسم على اللوحة. نقوم بمسح الخلفية إلى اللون الأبيض ونرسم الصورة المصدر الأولى على النصف الأيسر.

```java
Graphics graphics = new Graphics(image);
graphics.clear(Color.getWhite());
graphics.drawImage(Image.load(dataDir + "example1.psd"), 0, 0, 300, 600);
```

### الخطوة 5: رسم الصورة الثانية (إكمال الدمج)

الآن نضع الصورة الثانية على النصف الأيمن من نفس اللوحة.

```java
graphics.drawImage(Image.load(dataDir + "example2.psd"), 300, 0, 300, 600);
```

### الخطوة 6: حفظ ملف PSD الناتج

أخيرًا، احفظ اللوحة المدمجة على القرص.

```java
image.save();
```

تهانينا! لقد نجحت في **دمج الصور في PSD** وإنشاء ملف PSD في Java.

## لماذا دمج الصور باستخدام Aspose.PSD؟

- **Layer‑aware** – كل استدعاء `drawImage` يضيف طبقة منفصلة يمكنك تعديلها لاحقًا.  
- **Format flexibility** – يدعم PSD و PNG و JPEG و BMP والمزيد.  
- **No native dependencies** – جافا صافية، يعمل على أي نظام تشغيل يدعم JDK.

## المشكلات الشائعة والحلول

| المشكلة | السبب | الحل |
|--------|-------|------|
| `File not found` error عند تحميل الصور المصدر | مسار `dataDir` غير صحيح | تحقق من أن `dataDir` يشير إلى المجلد الذي يحتوي على `example1.psd` و `example2.psd`. |
| ملف PSD الناتج فارغ | `graphics.clear` تم استدعاؤه بعد الرسم | تأكد من تنفيذ `graphics.clear(Color.getWhite())` **قبل** أي استدعاءات `drawImage`. |
| استثناء الترخيص أثناء التشغيل | ترخيص Aspose.PSD مفقود أو منتهي الصلاحية | قم بتطبيق ترخيص صالح باستخدام `License license = new License(); license.setLicense("Aspose.PSD.lic");` قبل أي استدعاء API. |

## الأسئلة المتكررة

### س1: هل Aspose.PSD متوافق مع جميع صيغ الصور؟

ج1: يركز Aspose.PSD أساسًا على صيغة ملفات PSD. ومع ذلك، يدعم صيغًا أخرى متعددة للإدخال والإخراج.

### س2: هل يمكنني إجراء تعديلات إضافية على الصورة المدمجة؟

ج2: بالتأكيد! بعد دمج الصور، يمكنك تعديل ملف PSD الناتج باستخدام ميزات Aspose.PSD الواسعة.

### س3: هل هناك متطلبات ترخيص لاستخدام Aspose.PSD؟

ج3: نعم، يلزم وجود ترخيص صالح للاستخدام التجاري. احصل عليه من [هنا](https://purchase.aspose.com/buy).

### س4: هل يتوفر نسخة تجريبية مجانية لـ Aspose.PSD؟

ج4: نعم، يمكنك استكشاف Aspose.PSD من خلال نسخة تجريبية مجانية [هنا](https://releases.aspose.com/).

### س5: أين يمكنني العثور على دعم للاستفسارات المتعلقة بـ Aspose.PSD؟

ج5: زر [منتدى Aspose.PSD](https://forum.aspose.com/c/psd/34) للحصول على دعم المجتمع والنقاشات.

---

**آخر تحديث:** 2025-12-30  
**تم الاختبار مع:** Aspose.PSD 24.11 for Java  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}