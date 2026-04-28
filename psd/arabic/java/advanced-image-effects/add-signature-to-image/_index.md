---
date: 2026-04-28
description: تعلم كيفية إضافة توقيع إلى الصورة عن طريق رسم صورة على القماش باستخدام
  Aspose.PSD للـ Java. يوضح هذا الدرس لمعالجة الصور في Java كيفية حفظ الصورة بصيغة
  PNG وتراكب الرسومات.
keywords:
- add signature to image
- draw image on canvas
- save image as png
- java image processing
- add watermark java
linktitle: إضافة توقيع إلى صورة
second_title: Aspose.PSD Java API
title: إضافة توقيع إلى الصورة – رسم الصورة على القماش باستخدام Aspose.PSD للـ Java
url: /ar/java/advanced-image-effects/add-signature-to-image/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# إضافة توقيع إلى الصورة – رسم صورة على القماش باستخدام Aspose.PSD للـ Java

## مقدمة

إضافة توقيع يدوي أو رقمي **add signature to image** هو طلب شائع للعقود والفواتير أو أي مستند يحتاج إلى إثبات الأصالة. في هذا البرنامج التعليمي سترى كيف يتيح لك Aspose.PSD للـ Java **draw image on canvas** ويعامل التوقيع كطبقة تغطية أخرى. سنستعرض تحميل الصورة الأساسية، تحميل ملف التوقيع، تهيئة سياق الرسومات، رسم التغطية، وأخيرًا **save image as PNG**. في النهاية ستحصل على نمط قابل لإعادة الاستخدام لأي سيناريو **java image processing**، سواء كان توقيعًا أو علامة مائية أو شعارًا.

## إجابات سريعة
- **What does “draw image on canvas” mean?** إنه يشير إلى عرض صورة واحدة على أخرى باستخدام فئة `Graphics`.  
- **How to add a signature in Java?** حمّل ملف التوقيع كـ `Image` واستخدم `Graphics.drawImage`.  
- **Which Aspose.PSD version is required?** أي إصدار حديث 24.x؛ الكود يعمل مع أحدث مكتبة.  
- **Can I overlay multiple images?** نعم—كرر استدعاء `drawImage` بمصادر مختلفة.  
- **Do I need a license?** الإصدار التجريبي يعمل للتطوير؛ يلزم الحصول على ترخيص تجاري للإنتاج.

## ما هو “Draw Image on Canvas”؟
في مصطلحات Aspose.PSD، يعني رسم صورة على القماش طلاء كائن `Image` واحد على آخر باستخدام سياق `Graphics`. هذه العملية هي العمود الفقري لتقنيات **overlay images java** مثل إضافة العلامات المائية أو الشعارات أو التوقيعات.

## لماذا تستخدم Aspose.PSD لتغطية توقيع؟
- **Full PSD support** – يعمل مع الطبقات والأقنعة والشفافية.  
- **No native OS dependencies** – جافا نقي، مثالي لمعالجة الخادم.  
- **High‑performance rendering** – مُحسّن للملفات الكبيرة والتركيبات المعقدة.  

## المتطلبات المسبقة
- Java Development Kit (JDK) 8 أو أعلى.  
- إضافة ملف JAR الخاص بـ Aspose.PSD للـ Java إلى مسار الفئة (classpath) في مشروعك.  
- ملفان صورة: صورة أساسية (مثال: `layers.psd`) ورسمة توقيع (`sample.psd`).  

## استيراد الحزم

```java
import com.aspose.psd.Graphics;
import static com.aspose.psd.GraphicsUnit.Point;
import com.aspose.psd.Image;
import com.aspose.psd.Point;

import com.aspose.psd.imageoptions.PngOptions;
```

## الخطوة 1: تحميل الصور الأساسية والثانوية

```java
//ExStart:LoadImages
String dataDir = "Your Document Directory";

// Load the primary image (the canvas)
Image canvas = Image.load(dataDir + "layers.psd");

// Load the secondary image containing the signature graphics
Image signature = Image.load(dataDir + "sample.psd");
//ExEnd:LoadImages
```

> **Pro tip:** احرص على أن تكون الصورتان بنفس وضع اللون (RGB) لتجنب تغيرات اللون غير المتوقعة عند الرسم.

## الخطوة 2: تهيئة الرسومات (initialize graphics java)

```java
//ExStart:InitializeGraphics
Graphics graphics = new Graphics(canvas);
//ExEnd:InitializeGraphics
```

كائن `Graphics` يعمل كفرشاة تتيح لك **draw image on canvas**. تهيئته مع الـ `Image` الأساسي يربط جميع أوامر الرسم اللاحقة بهذا القماش.

## الخطوة 3: إضافة توقيع إلى الصورة (how to add signature)

```java
//ExStart:AddSignatureToImage
graphics.drawImage(
    signature,
    new Point(
        canvas.getHeight() - signature.getHeight(),   // X‑coordinate (bottom)
        canvas.getWidth() - signature.getWidth()      // Y‑coordinate (right)
    )
);
canvas.save(dataDir + "AddSignatureToImage_out.png", new PngOptions());
//ExEnd:AddSignatureToImage
```

في هذا المقتطف نقوم بـ **overlay images java** عن طريق وضع التوقيع في الزاوية السفلية اليمنى. عدّل قيم `Point` إذا كنت تحتاج إلى موضع مختلف.

## المشكلات الشائعة والحلول
| العَرَض | السبب | الحل |
|---------|-------|-----|
| التوقيع يظهر مشوّهًا | اختلاف DPI بين القماش والتوقيع | استخدم `signature.resize` قبل الرسم أو تأكد من أن كلا الملفين يشاركان نفس DPI. |
| ملف الإخراج كبير جدًا | الحفظ بدون ضغط | مرّر `PngOptions` مكوّنًا مع تعيين `CompressionLevel` إلى قيمة أعلى. |
| لم يتم رسم أي شيء | Graphics لم يتم تحريره | استدعِ `graphics.dispose()` بعد الرسم (اختياري، لكنه ممارسة جيدة). |

## نصائح إضافية للاستخدام العملي
- **Multiple signatures:** استدعِ `graphics.drawImage` بشكل متكرر مع كائنات `Image` وإحداثيات مختلفة.  
- **Opacity control:** استخدم `graphics.setOpacity(float opacity)` قبل الرسم لجعل التوقيع شبه شفاف.  
- **Rotating the signature:** طبّق `graphics.rotateTransform(angle)` إذا كنت تحتاج إلى توقيع مائل.  
- **Saving to other formats:** استبدل `PngOptions` بـ `JpegOptions` أو `BmpOptions` لإخراج JPEG أو BMP، إلخ.

## الأسئلة المتكررة

### س1: هل يمكنني إضافة توقيعات متعددة إلى صورة؟
A1: نعم، يمكنك إضافة توقيعات متعددة عن طريق تكرار الخطوات مع صور توقيع مختلفة.

### س2: هل يدعم Aspose.PSD صيغ صور أخرى؟
A2: نعم، يدعم Aspose.PSD مجموعة واسعة من صيغ الصور، مما يضمن مرونة في معالجة الصور.

### س3: هل يلزم وجود ترخيص لاستخدام Aspose.PSD للـ Java؟
A3: نعم، تحتاج إلى ترخيص صالح لاستخدام Aspose.PSD. زر [Purchase Aspose.PSD](https://purchase.aspose.com/buy) للحصول على تفاصيل الترخيص.

### س4: كيف يمكنني الحصول على دعم Aspose.PSD؟
A4: زر [Aspose.PSD Forum](https://forum.aspose.com/c/psd/34) للحصول على دعم المجتمع والنقاشات.

### س5: هل يمكنني تجربة Aspose.PSD للـ Java قبل الشراء؟
A5: نعم، يمكنك الحصول على [free trial](https://releases.aspose.com/) لاستكشاف الميزات قبل الشراء.

**الأسئلة المتكررة الإضافية**

**س: كيف أغيّر شفافية التوقيع؟**  
A: استخدم `graphics.setOpacity(float opacity)` قبل استدعاء `drawImage`. القيم تتراوح من 0.0 (شفاف) إلى 1.0 (معتم).

**س: هل من الممكن تدوير التوقيع؟**  
A: نعم—طبق مصفوفة تحويل عبر `graphics.rotateTransform(angle)` قبل الرسم.

**س: هل يمكنني رسم التوقيع على JPEG بدلاً من PNG؟**  
A: بالتأكيد. استبدل `PngOptions` بـ `JpegOptions` وحدد مستوى الجودة المطلوب.

## الخلاصة

باتباع هذه الخطوات، تعلمت **how to add signature to image** عن طريق **drawing an image on canvas** باستخدام Aspose.PSD للـ Java. يمكن تمديد النمط نفسه إلى العلامات المائية أو الشعارات أو أي رسومات تغطية، مما يمنح تطبيقات Java الخاصة بك قدرات قوية في **java image processing**.

---

**آخر تحديث:** 2026-04-28  
**تم الاختبار مع:** Aspose.PSD for Java 24.11  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}